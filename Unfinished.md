RTOS
==
系统的核心就是任务管理，FreeRTOS 也不例外
多任务处理功能
任务的创建、删除、挂起和恢复等操作
```c++
// Perform an action every 10 ticks.
void vTaskFunction( void * pvParameters )
{
TickType_t xLastWakeTime;
const TickType_t xFrequency = 10;

    // Initialise the xLastWakeTime variable with the current time.
    xLastWakeTime = xTaskGetTickCount ();
    for( ;; )
    {
        // Wait for the next cycle.
        vTaskDelayUntil( &xLastWakeTime, xFrequency );

        // Perform action here.
    }
}
```
## 多任务系统
单片机系统一般在main 函数里面用while(1)做一个大循环来完成所有的处理.单任务系统

任务创建、删除、返回值
--
<center>**创建**</center>
```c++
	BaseType_t xTaskCreate(
			TaskFunction_t pvTaskCode,
			const char * const pcName,
			unsigned short usStackDepth,
			void *pvParameters,
			UBaseType_t uxPriority,
			TaskHandle_t * pvCreatedTask
                          );
```

- pvTaskCode:指针，指向任务函数的入口。任务永远不会返回（位于死循环内）。该参数类型TaskFunction_t定义在文件projdefs.h中，定义为：
> typedefvoid (*TaskFunction_t)( void * )。
- pcName：任务描述。主要用于调试。字符串的最大长度由宏configMAX_TASK_NAME_LEN指定，该宏位于FreeRTOSConfig.h文件中。
- usStackDepth：指定任务堆栈大小，能够支持的堆栈变量数量，而不是字节数。比如，在16位宽度的堆栈下，usStackDepth定义为100，则实际使用200字节堆栈存储空间。堆栈的宽度乘以深度必须不超过size_t类型所能表示的最大值。比如，size_t为16位，则可以表示的最大值是65535。
- pvParameters：指针，当任务创建时，作为一个参数传递给任务。
- uxPriority：任务的优先级。具有MPU支持的系统，可以通过置位优先级参数的portPRIVILEGE_BIT位，随意的在特权（系统）模式下创建任务。比如，创建一个优先级为2的特权任务，参数uxPriority可以设置为( 2 | portPRIVILEGE_BIT )。
- pvCreatedTask：用于回传一个句柄（ID），创建任务后可以使用这个句柄引用任务。

------

<center>** 返回值  **  </center>
如果任务成功创建并加入就绪列表函数返回pdPASS，否则函数返回错误码。
errCOULD_NOT_ALLOCATE_REQUIRED_MEMORY： 任务创建失败，堆内存不足。具体参见projdefs.h。  

<center>**删除**</center>
 > voidvTaskDelete( TaskHandle_t xTask );

从RTOS内核管理器中删除一个任务。任务删除后将会从就绪、阻塞、暂停和事件列表中移除。在文件FreeRTOSConfig.h中，必须定义宏INCLUDE_vTaskDelete 为1，本函数才有效。

注：被删除的任务，其在任务创建时由内核分配的存储空间，会由空闲任务释放。如果有应用程序调用xTaskDelete()，必须保证空闲任务获取一定的微控制器处理时间。任务代码自己分配的内存是不会自动释放的，因此删除任务前，应该将这些内存释放。

------
<center>**用法**</center>

```C++
/* 创建任务. */
void vTaskCode( void * pvParameters )
{
    for( ;; )
    {
       /* 任务代码放在这里 */
    }
}
/* 创建任务函数 */
void vOtherFunction( void )
{
    static unsigned char ucParameterToPass;
    xTaskHandlexHandle;
    
     /* 创建任务，存储句柄。注：传递的参数ucParameterToPass必须和任务具有相同的生存周期，
        因此这里定义为静态变量。如果它只是一个自动变量，可能不会有太长的生存周期，因为
                中断和高优先级任务可能会用到它。 */
     xTaskCreate( vTaskCode, "NAME", STACK_SIZE,&ucParameterToPass, tskIDLE_PRIORITY, &xHandle );
     
     /* 使用句柄删除任务. */
    if( xHandle !=NULL )
    {
        vTaskDelete( xHandle );
    }
}
```

___

任务控制API
 > void vTaskDelay( portTickTypexTicksToDelay )

 - 调用vTaskDelay()函数后，任务会进入阻塞状态，持续时间由vTaskDelay()函数的参数xTicksToDelay指定，单位是系统节拍时钟周期。常量portTICK_RATE_MS 用来辅助计算真实时间，此值是系统节拍时钟中断的周期，单位是毫秒。在文件FreeRTOSConfig.h中，宏INCLUDE_vTaskDelay 必须设置成1，此函数才能有效。

 - vTaskDelay()指定的延时时间是从调用vTaskDelay()后开始计算的相对时间。比如vTaskDelay(100)，那么从调用vTaskDelay()后，任务进入阻塞状态，经过100个系统时钟节拍周期，任务解除阻塞。因此，vTaskDelay()并不适用与周期性执行任务的场合。此外，其它任务和中断活动，会影响到vTaskDelay()的调用（比如调用前高优先级任务抢占了当前任务），因此会影响任务下一次执行的时间。API函数vTaskDelayUntil()可用于固定频率的延时，它用来延时一个绝对时间。
