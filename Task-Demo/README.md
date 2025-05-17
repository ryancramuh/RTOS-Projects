# FreeRTOS Task Demo Steps 
1. Create a New Project 
2. For this project we use "STM32L476RGT6"
3. Configure SysTick to use TIM6    <br> ![SYSTEM_CONFIG](docs/SYS_Config_Task_Demo.png) <br><b> Here are the settings </b><br><br><b><br> ![IOC_View](docs/IOC_Config_View.png) <br>This is what the IOC will look like </b>
4. Enable FreeRTOS CMSISv2
5. Add Task 1 and 2 <br> ![TASK_VIEW](docs/RTOS_Task_Config_View.png) <b><br> Here is the page for adding the tasks <br> 
6. Configure the clock
7. Update syscall.c
8. Update Task1 and Task2 Handlers
9. Configure Debug Settings
10. Run Debug -> Resume
11. Watch tasks print to SWV ITM Data Console
