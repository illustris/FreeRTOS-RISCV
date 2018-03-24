# FreeRTOS for RISC-V

This is a port of FreeRTOS to RISC-V
## Contributors
The original port to priv spec 1.7 was contributed by [Technolution](https://interactive.freertos.org/hc/en-us/community/posts/210030246-32-bit-and-64-bit-RISC-V-using-GCC)

Update to priv spec 1.9: [illustris](https://github.com/illustris)

Update to priv spec 1.9.1: [Abhinaya Agrawal](https://bitbucket.org/casl/freertos-riscv-v191/src)

Bug fixes: [Julio Gago](https://github.com/julio-gago-metempsy)

Update to priv spec 1.10: [sherrbc1](https://github.com/sherrbc1)

## Build

You can edit `main()` in [main.c](Demo/riscv-spike/main.c) to add your FreeRTOS task definitions and set up the scheduler.

To build FreeRTOS,

```bash
cd Demo/riscv-spike
export RISCV=/opt/riscv # your riscv tools path here
make
```

## Run
```bash
spike riscv-spike.elf
```

## Tested environments

Tested on a Rocket RISC-V processor with local interrupt controller (Clint) using preemption.

Tested in Spike and Verilator with several builds including single-task, multi-task and typical demo test including queues, semaphores, mutexes and about a dozen concurrent tasks.
