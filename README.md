# FreeRTOS Threads and Mutex using STM32F411-NUCLEO /Part-1 

![FreeRTOS](https://img.shields.io/badge/FreeRTOS-v10.4.3-green)
![STM32](https://img.shields.io/badge/STM32F4-HSI_84MHz-blue)


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
