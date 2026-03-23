# FreeRTOS Task Demo Steps

### 1. Create a New Project  
### 2. Use Target MCU: `STM32L476RGT6`  
> Configure NEWLIB_REENTRANT
![newlib](docs/NEWLIB_REENT_Config.png)

### 3. Configure SysTick to Use TIM6  

![SYSTEM_CONFIG](docs/SYS_Config_Task_Demo.png)  
**TIM6 selected for SysTick configuration**

![IOC_View](docs/IOC_Config_View.png)  
**IOC Configuration Overview**

### 4. Enable FreeRTOS CMSISv2  
### 5. Add Task 1 and Task 2  

![TASK_VIEW](docs/RTOS_Task_Config_View.png)  
**RTOS Task Configuration Window**

![TASK1_VIEW](docs/Task1_Config.png)  
![TASK2_VIEW](docs/Task2_Config.png)  
**Task 1 and Task 2 Configuration**

### 6. Configure the Clock Tree  
### 7. Update `syscall.c`  

**Paste these lines under the includes section:**  
![Update1_VIEW](docs/SYSCALL_Update1.png)  
![Update2_VIEW](docs/SYSCALL_Update2.png)  

**Then update the `__weak__ write()` function to use `TMI_SendChar();`**

### 8. Update Task Handlers in `main.c`  

**Default task handle definitions:**  
![default_VIEW](docs/DEFAULT_Task_Handles.png)

**Updated task handle configuration:**  
![configured_VIEW](docs/CONFIG_Task_Handles.png)  

>  Make sure `Task1Handle` and `Task2Handle` are updated in your `main.c`.

### 9. Configure Debug Settings (SWV Enabled)  
![debug_CONFIG](docs/DEBUGGER_CONFIG.png)

### 10. Run Debug → Click "Resume"  
![debug_run](docs/Debug_Symbol.png)

> Configure the trace
![config_trace](docs/CONFIG_TRACE.png)

> Be sure to use ITM Stimulus port 0
![use_zero](docs/USE_ZERO.png)

### 11. Observe Output in SWV ITM Data Console 
