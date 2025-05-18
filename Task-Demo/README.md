# FreeRTOS Task Demo Steps

### 1. Create a New Project  
### 2. For this project we use `STM32L476RGT6`  
### 3. Configure SysTick to use TIM6  

![SYSTEM_CONFIG](docs/SYS_Config_Task_Demo.png)  
**Here are the settings**  

![IOC_View](docs/IOC_Config_View.png)  
**This is what the IOC will look like**

### 4. Enable FreeRTOS CMSISv2  
### 5. Add Task 1 and Task 2  

![TASK_VIEW](docs/RTOS_Task_Config_View.png)  
**Here is the page for adding the tasks**  

![TASK1_VIEW](docs/Task1_Config.png)  
![TASK2_VIEW](docs/Task2_Config.png)  

### 6. Configure the Clock  
### 7. Update `syscall.c`  

**You will need to manually paste these lines under the includes:**  
![Update1_VIEW](docs/SYSCALL_Update1.png)  
![Update2_VIEW](docs/SYSCALL_Update2.png)  
**Then update the `__weak__ write` to use `TMI_SendChar();`**

### 8. Update `Task1` and `Task2` Handlers  
**these are the default task handles in <pre> main.c </pre>**
![Update2_VIEW](docs/SYSCALL_Update2.png) 
### 9. Configure Debug Settings  
### 10. Run Debug → Resume  
### 11. Watch tasks print to SWV ITM Data Console  
