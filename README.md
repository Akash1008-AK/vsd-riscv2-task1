# vsd-riscv2-task1
task 1 18.04.2026-20.04.2026

Task-1: Environment Setup

Step 1: Codespace Setup
1.Forked the repository
2.Created a GitHub Codespace
3.Environment built successfully

Step 2: Verify Toolchain
Ran the following commands:
riscv64-unknown-elf-gcc --version
spike
iverilog -V

output displayed :
how to addRISC-V GCC version displayed
Spike simulator working
Icarus Verilog version displayed


Step 3: Run RISC-V Program

ran the given sample program in using the terminal 1st then loaded the remote linux environment usint the given readme file and executed the sample program at the evvironment 

then changed the n value to 24 and executed the same program again in the remote terminal and got the output 

commands used for the location and execution 

cd samples
riscv64-unknown-elf-gcc -o sum1ton.o sum1ton.c
spike pk sum1ton.o

output got :
Sum from 1 to 9 is 45

Sum from 1 to 24 is 300

Questions given 

1. Where is the RISC-V program located?
The RISC-V program is located in the samples directory of the repository, such as sum1ton.c.

2. How is the program compiled and loaded into memory?
The program is compiled using the RISC-V cross-compiler riscv64-unknown-elf-gcc, which converts the code into an executable.
 It is then executed using the Spike simulator (spike pk), which loads it into simulated memory.

3. How does the RISC-V core access memory and memory-mapped IO?
The RISC-V core accesses memory using addresses. Memory and IO devices are accessed using memory-mapped IO, where specific addresses correspond to hardware components.

4. Where would a new FPGA IP block logically integrate in this system?
A new FPGA IP block would be integrated as a memory-mapped peripheral, allowing the processor to interact with it using address-based communication.



