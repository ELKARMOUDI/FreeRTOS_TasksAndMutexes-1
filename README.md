# FreeRTOS Threads and Mutex using STM32F411-NUCLEO /Part-1 

![FreeRTOS](https://img.shields.io/badge/FreeRTOS-v10.4.3-green)
![STM32](https://img.shields.io/badge/STM32F4-HSI_84MHz-blue)

<img src="https://github.com/user-attachments/assets/fc4dc86e-1b26-42c3-af91-a1fabc61b27a" width="700" alt="DEC36A30-19E8-494C-B521-14DC6DD952CE_4_5005_c">


## Features
- 🧵 **Three FreeRTOS Threads** with execution profiling
- 🔒 **Mutex-protected UART** (USART2 @ 115200 baud)
- 📊 **Task Profilers** counting execution cycles
- 💡 **GPIO Control** (PA5 LED, PC13 button input)
- ⏱️ **84MHz System Clock** via HSI/PLL

## Hardware Setup
| Component | Pin | Function |
|-----------|-----|----------|
| LED | PA5 | Output |
| Button | PC13 | Input |
| UART2 | PA2/PA3 | Debug console |

## Code Architecture
```c
// Main components:
osThreadId defaultTaskHandle, Thread1Handle, Thread2Handle;
osMutexId uart_mutexHandle;

void StartDefaultTask() { /* Profiler++ */ }
void Thread1Func() { /* Profiler++ */ }
void Thread2Func() { /* Profiler++ */ }
