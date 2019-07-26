## LEARNING LIST
**heap **  
TODO:
https://blog.csdn.net/qq_29343201/article/details/59614863  
https://www.hrwhisper.me/c-dynamic-memory-allocation-and-the-data-struct-of-malloc-and-heap-overflow-attack/

**stack**

**Printf(%d,%s,%u,%i,%f)**

**diff between stack,heap,static in C language**  
TODO:  
https://www.jianshu.com/p/3a87e581473a  
**multitask dev in C**  
**menuconfig**


------



------
## 2019 07 26 Schedule

```sequence
ADC-->>ADC:thread 1
DAC->DAC:thread 2
```


- [ ] Creat two thread which run the ADC&DAC individually.
- [ ] Read FreeRTOS docs below:
- task creation
- task control
- task utilities
- kernel control
- queues
- queue sets
> They could be found in https://freertos.org/a00125.html

------
## 2019 07 25 Schedule

```sequence
ADC->DAC:get value 
```

- [x] ADC get the value from from DAC, unlock the
> component config->driver configurations->ADC configuration
- [x] Read docs about FREERTOS
- [ ] Try to creat two thread which run the ADC&DAC individually.

```sequence
ADC-->>ADC:thread 1
DAC->DAC:thread 2
```