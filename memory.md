## How to run examples
```C++
cd /esp/esp-idf/tools/unit-test-app
idf.py -T driver flahs monitor
```
## RAM of ESP32
ESP32 RAM:  
- DRAM: Data RAM
- IRAM: Instruction RAM, 32-bit aligned
- 

Add a PSRAM

PSRAM--Pseudo static random access memory，伪静态随机存储器；

## malloc
```C++
void *malloc(size_t size);
```
> 说明：**malloc 向系统申请分配指定size个字节(Byte)的内存空间,并返回一个指向它的指针。**返回类型是** void* 类型**。**void* **表示未确定类型的指针。C,C++规定，**void* 类型**可以强制转换为任何其它类型的指针。具体内容如下：

malloc returns a void pointer to the allocated space, or NULL if there is insufficient memory available. To return a pointer to a type other than void, use a type cast on the return value. The storage space pointed to by the return value is guaranteed to be suitably aligned for storage of any type of object. If size is 0, malloc allocates a zero-length item in the heap and returns a valid pointer to that item. Always check the return from malloc, even if the amount of memory requested is small.

```C++
#include <stdio.h>
#include <string.h>
#include <stdlib.h>

int main(){
	char *str;
    /*initial memory allocate*/
    str = (char *)malloc(15);
    strcpy(str,"runoob");
    printf("String　= %s, Address = %u\n", str, str);
    /*re-allocate the memory*/
}

```
TODO: diff between realloc, malloc, calloc