# FreeRTOS Task Demo Steps 
### 1. Create a New Project 
### 2. For this project we use "STM32L476RGT6"
### 3. Configure SysTick to use TIM6    
<br> ![SYSTEM_CONFIG](docs/SYS_Config_Task_Demo.png) <br><b> Here are the settings </b><br><br><b><br> ![IOC_View](docs/IOC_Config_View.png) <br><br>This is what the IOC will look like </b><br>
### 4. Enable FreeRTOS CMSISv2
### 5. Add Task 1 and 2 
<br> ![TASK_VIEW](docs/RTOS_Task_Config_View.png) <b><br> Here is the page for adding the tasks <br></b>![TASK1_VIEW](docs/Task1_Config.png) <br> ![TASK_VIEW](docs/Task2_Config.png)
### 6. Configure the clock
### 7. Update syscall.c
<br> You will need to manually paste these lines under the includes ![Update1_VIEW](docs/SYSCALL_Update1.png) <br> and update the __weak__ write to use TMI_Handle();  ![Update2_VIEW](docs/SYSCALL_Update2.png)
### 8. Update Task1 and Task2 Handlers
### 9. Configure Debug Settings
### 10. Run Debug -> Resume
### 11. Watch tasks print to SWV ITM Data Console
