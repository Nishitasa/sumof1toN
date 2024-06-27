VSD QUADRON INTERN

Task 1
Write a c program to count the sum of 1 to N
![Virtual box installation](https://github.com/Nishitasa/sumof1toN/assets/173664538/982957fc-32b6-4fad-bcc5-5125da4cc46e)
Installation of Virtual box 
![Installation of Ubuntu](https://github.com/Nishitasa/sumof1toN/assets/173664538/ca7f9c71-18a4-46bd-9bb9-faad0622f1a0)
open the terminal
![Terminal](https://github.com/Nishitasa/sumof1toN/assets/173664538/ee40e637-fa6a-4df2-8d64-f7587aef2a51)
![Cprogramming code for sumof1toN](https://github.com/Nishitasa/sumof1toN/assets/173664538/88f86b41-44db-4b8a-8d2c-84fe87e633d7)
Apply the code and receive the output, Sum of numbers from 1to N is:
We can apply this to any number of N values
![Screenshot from 2024-06-24 12-17-45](https://github.com/Nishitasa/sumof1toN/assets/173664538/90238b19-c366-4778-8d20-342cbcdad971)
RISCV64 output

Task 1 completed

TASK 2
My project title is Creating a Smart Elevator Controller 
![image](https://github.com/Nishitasa/sumof1toN/assets/173664538/c7da7880-ef91-4560-86f9-2bdda08b4021)

A smart elevator, refers to an elevator system that incorporates advanced technologies to enhance efficiency, safety, and user experience. These elevators utilize various sensors, algorithms, and connectivity features to improve their performance and functionality. These elevators are particularly beneficial in high-traffic buildings where efficient vertical transportation is crucial. Key features of smart elevators include:
Traffic Analysis and Optimization

Security and Access Control

Energy Efficiency
![The code applied for smart elevator controller](https://github.com/Nishitasa/sumof1toN/assets/173664538/d8c23bc2-8174-42bd-bd8c-9dd8531c290e)
Open the Terminal leafpad and apply the code .Save the file
Then give the command:

gcc file name

/.a.out
![Output](https://github.com/Nishitasa/sumof1toN/assets/173664538/e60ade6d-68bd-470e-b5f9-3862b54f0e6d)
The output is displayed 
![The project which is applied to riscv](https://github.com/Nishitasa/sumof1toN/assets/173664538/1f33ae24-b198-4a7c-9a60-381fdf1fe6dd)
Converting the C program to RISCV and complied to recieve the output

TASK 3

We have to observe the SPIKE Simulation and observe  with -O1 and -Ofast. 

With -O1 command:

The output we got from gcc should be equal to the simulation.The command riscv64-unknown-elf-gcc-O1 -mabi=lp64 -march=rv64i -o elevator.o elevator.c.Then run the code and give them the required output in C .

![Screenshot from 2024-06-27 10-30-09](https://github.com/Nishitasa/sumof1toN/assets/173664538/47295c95-9379-4e57-9bdc-513f10b4e0d5)

Therefore verification for command -O1 is done.Run them using spike simulation

Here we will debug the code from main.We use the command spike -d pk elevator.o

The initial address we see from the code is 10230 so we point them using counter.

until pc 0 10230 refers that after 10230 they debug .Type reg 0 sp
![Screenshot from 2024-06-27 10-48-11](https://github.com/Nishitasa/sumof1toN/assets/173664538/3e876312-dda3-4e3e-be4f-2d309b38c17a)
![Screenshot from 2024-06-27 10-52-01](https://github.com/Nishitasa/sumof1toN/assets/173664538/56f651e4-a9a6-45ba-9ff1-899be3960b41)

Next with -Ofast command:

This is same as above .The command riscv64-unknown-elf-gcc-O1 -mabi=lp64 -march=rv64i -o elevator.o elevator.c.Then run the code and give them the required output in C
Then use the command gcc elevator.c .Output is verified using ./a.out command

![Screenshot from 2024-06-27 10-58-02](https://github.com/Nishitasa/sumof1toN/assets/173664538/055b5c8f-2010-4e10-8f4e-e920336c83d7)

Run using spike simulation
![Screenshot from 2024-06-27 10-59-18](https://github.com/Nishitasa/sumof1toN/assets/173664538/1d329252-0daa-40f2-bb09-5a638b19ab34)
The starting address is 10230 we see the next instruction manually by clicking ENTER.
Apply spike -d pk elevator.o

To view next reg 0 a2 gives the register value at a2 operand.Click ENTER

Then various address are available
![Screenshot from 2024-06-27 10-59-43](https://github.com/Nishitasa/sumof1toN/assets/173664538/27885fef-093b-4726-9186-97fc14500e47)

To check next subtract the address with 16 so see the upcoming instruction.
![Screenshot from 2024-06-27 11-01-50](https://github.com/Nishitasa/sumof1toN/assets/173664538/9a0119bd-49d6-4a14-b4f0-ed8ab3da4fa8)

