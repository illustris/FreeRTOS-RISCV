# FreeRTOS port to RISC-V privileged spec 1.9.1

This is based on https://github.com/illustris/FreeRTOS-RISCV with minor fixes and improvements.

The fixes allow this code to run nicely in a Rocket RISC-V processor with a hardware configuration string and a local interrupt controller (Clint) using preemption.

Tested in Spike and Verilator with several builds including single-task, multi-task and typical demo test including queues, semaphores, mutexes and about a dozen concurrent tasks.
