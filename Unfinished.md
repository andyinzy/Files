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