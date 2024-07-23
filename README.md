# Vsdsquadron-mini-Internship

<details>

<summary><h3>Task 1: </h3> Using a RISC-V simulator, write a C program to count the sum of all numbers from 1 to n</summary>

## Task 1 
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

</details>

<details>

<summary><h3>Task 2:Smart Elevator controller</summary>
 
 My project title is Creating a Smart Elevator Controller</summary>
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
</details>

<details>

<summary><h3> Task 3:We have to observe the SPIKE Simulation and observe  with -O1 and -Ofast</summary>

. 

**With -O1 command**:

The output we got from gcc should be equal to the simulation.The command riscv64-unknown-elf-gcc-O1 -mabi=lp64 -march=rv64i -o elevator.o elevator.c.Then run the code and give them the required output in C .

![Screenshot from 2024-06-27 10-30-09](https://github.com/Nishitasa/sumof1toN/assets/173664538/47295c95-9379-4e57-9bdc-513f10b4e0d5)

Therefore verification for command -O1 is done.Run them using spike simulation

Here we will debug the code from main.We use the command spike -d pk elevator.o

The initial address we see from the code is 10230 so we point them using counter.

until pc 0 10230 refers that after 10230 they debug .Type reg 0 sp
![Screenshot from 2024-06-27 10-48-11](https://github.com/Nishitasa/sumof1toN/assets/173664538/3e876312-dda3-4e3e-be4f-2d309b38c17a)
![Screenshot from 2024-06-27 10-52-01](https://github.com/Nishitasa/sumof1toN/assets/173664538/56f651e4-a9a6-45ba-9ff1-899be3960b41)

**Next with -Ofast command**:

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

</details>
<details>

<summary><h3>Task 4: </h3> RISC-V instruction type (R, I, S, B, U, J)  </summary>

 
RISC-V (pronounced “risk-five”) is a new instruction set architecture (ISA) that was originally
designed to support computer architecture research and education, but which we now hope will
also become a standard free and open architecture for industry implementations.

RISC-V has been designed to support extensive customization and specialization. The base integer
ISA can be extended with one or more optional instruction-set extensions, but the base integer
instructions cannot be redefined. We divide RISC-V instruction-set extensions into standard and
non-standard extensions.

![image](https://github.com/Nishitasa/vsd-quadron-intern/assets/173664538/04f7dc87-c2d2-4aad-9280-b2c5910846db)

![image](https://github.com/Nishitasa/vsd-quadron-intern/assets/173664538/2e4042ad-8ae7-4915-aa44-42cc7fe8f864)

There are various formats :
1.R-Format
2.I-Format
3.S-Format
4.B-Format
5.U-Format
6.J-Format

**R-Format**:

This format instructions are frequently thought of as the most “simple” because they typically include operations that map closely to the capabilities that we generally associate with a computer at the lowest level. Arithmetic operations, such as adding, subtracting, and bit shifting all fall into this category.
![image](https://github.com/Nishitasa/vsd-quadron-intern/assets/173664538/2874f8e3-f0e6-4637-93af-2d2804b5ee84)

**I-Format**:

This format instructions eliminate the second register (rs2) and function (funct7) fields from the R format in favor of a large immediate value field. This format is specifically useful for supplying constants for arithmetic instructions, or loading data from a location in memory.
![image](https://github.com/Nishitasa/vsd-quadron-intern/assets/173664538/9bec60f6-5134-4e70-abc9-80d088bb1f5c)

**S-Format**:

Next up is S format instructions, which reintroduce our second register operand (rs2), but eliminate the destination register rd. An important attribute to notice is that we don’t simply change the bits used for rd to now represent rs2, we instead split our immediate value across two separate fields, allowing rs2 to be placed in the same location in S format instructions as it was in R format (and every other format that utilizes rs2). When we explore how instruction decoding works, the reasoning behind this strategy and the impact it has on complexity of the hardware design will become more apparent.
![image](https://github.com/Nishitasa/vsd-quadron-intern/assets/173664538/a7a0e366-890e-4fdb-896f-fd6af3b39e5a)

**U-Format**:

U, which we chose the lui instruction to demonstrate, but didn’t specify its actual purpose. lui refers to “load upper immediate”, and now that we have looked at a few instructions that use immediate values, we should have somewhat of an intuition for how it is used. The U format has the smallest number of fields out of all core instruction formats, only supporting opcode, rd, and a 20 bit immediate.
![image](https://github.com/Nishitasa/vsd-quadron-intern/assets/173664538/dc0ca1c9-72a3-46c6-a459-7a9f80f7403d)

B-Format:

The B-format in RISC-V is used for conditional branch instructions. The B-format is designed to encode branch instructions that compare two registers and conditionally branch to a target address. Here’s the structure of the B-format instruction:

-----------------------------------------------------------
| imm[12|10:5] | rs2 | rs1 | funct3 | imm[4:1|11] | opcode |
-----------------------------------------------------------

**J-Format**:

In the RISC-V instruction set architecture (ISA), the "J" type instruction is used for jump operations. The format for a J-type instruction is designed to support jump operations with a 20-bit immediate value that is sign-extended to 32 bits and shifted left by one bit to form the jump target address

|  imm[20]  |  imm[10:1]  |  imm[11]  |  imm[19:12]  |  rd  |  opcode  |

Lets Decode the instruction set :

**add r1,r2,r3*

This is R-Type instruction.It is used for register-register operations.The field format is

rd (5 bits): The destination register. In this case, r1 (also known as x1 in RISC-V) is represented by the binary encoding of 1 which is 00001.
funct3 (3 bits): Specifies the type of operation within the R-type class. For the add instruction, funct3 is 000.
rs1 (5 bits): The first source register. Here, r2 (also known as x2 in RISC-V) is represented by the binary encoding of 2 which is 00010.
rs2 (5 bits): The second source register. Here, r3 (also known as x3 in RISC-V) is represented by the binary encoding of 3 which is 00011.

32bit-0000000 00011 00010 000 00001 0110011

**sub r3,r1,r2*

 R-type instruction in the RISC-V ISA. R-type instructions are used for register-register operations. The R-type format includes the opcode, source registers, destination register, and function codes (funct3 and funct7).

opcode: 0110011 (for integer register-register operations)
funct3: 000 (for subtraction, as it falls under the ADD/SUB group)
funct7: 0100000 (specific to subtraction)
rd: 00011 (for register x3)
rs1: 00001 (for register x1)
rs2: 00010 (for register x2)

32bit -0100000 00010 00001 000 00011 0110011

**and r2,r1,r3*

This R-Type instruction set.

Opcode: 0110011 (for all R-type instructions)
funct3: 111 (for AND)
funct7: 0000000 (for AND)
rs1: r1
rs2: r3
rd: r2

32-bit-0000000 00011 00001 111 00010 0110011

**OR r8, r2, r5*

This is R-type instruction set.

funct7: 0000000
rs2: 00101
rs1: 00010
funct3: 110
rd: 01000
opcode: 0110011

32-bit-0000000 00101 00010 110 01000 0110011

**xor r8,r1,r4*

This is R-type instruction set

Opcode: 0110011
rd (r8): 01000
funct3: 100
rs1 (r1): 00001
rs2 (r4): 00100
funct7: 0000000

32-bit-0000000_00100_00001_100_01000_0110011

**SLT r10,r2,r4*

This is R-type instruction set
For the slt (set less than) instruction:

opcode: 0110011
funct3: 010
funct7: 0000000
Register Mappings:
r10: destination register (rd)
r2: first source register (rs1)
r4: second source register (rs2)

For the slt r10, r2, r4 instruction, we can break it down and encode it as follows:

opcode: 0110011
rd: 01010 (binary for register 10)
funct3: 010
rs1: 00010 (binary for register 2)
rs2: 00100 (binary for register 4)
funct7: 0000000

32-bit pattern-0000000 00100 00010 010 01010 0110011


**ADDI r12,r3,5*

The instruction ADDI r12, r3, 5 is an I-type instruction in the RISC-V ISA. The I-type format is used for immediate arithmetic instructions, load instructions, and some other immediate-based instructions.

Opcode: The opcode for ADDI is 0010011.
rd: The destination register r12 is 01100 in binary.
funct3: The function code for ADDI is 000.
rs1: The source register r3 is 00011 in binary.
Immediate: The immediate value 5 is 000000000101 in binary (12 bits)

32-bit pattern-0000000001010001100000110010011

**SW r3,r1,4*

The SW (Store Word) instruction in the RISC-V instruction set is an example of an S-type (Store) instruction format. The S-type instruction format is used for store operations, which store the contents of a register into memory.

For the SW r3, r1, 4 instruction:

Opcode: 0100011 (SW)
rs2: r3 (register 3)
rs1: r1 (register 1)
funct3: 010 (SW function code)
Immediate: 4 (split into imm[11:5] and imm[4:0])
Let's break this down:

Immediate value 4 in binary: 000000000100

imm[11:5] = 0000000
imm[4:0] = 00100
rs2 (r3) in binary: 00011
rs1 (r1) in binary: 00001
funct3 for SW: 010
Opcode for SW: 0100011

32-bit-pattern-0000000 00011 00001 010 00100 0100011

**SRL r16,r11,r2*

This is a R-Type instruction set.

funct7: 0000000
rs2: 00010 (r2)
rs1: 01011 (r11)
funct3: 101 (SRL)
rd: 10000 (r16)
opcode: 0110011 (SRL)

32-bit -0000000 00010 01011 101 10000 0110011

**BNE r0,r1,20*

This is a B-Type instruction set
BNE r0, r1, 20 in RISC-V is a branch instruction used for conditional branching. 

Opcode: 1100011 (BNE)
rs1: 00000 (register r0)
rs2: 00001 (register r1)
Immediate: 20 (decimal) or 0x14 (hexadecimal), which in binary is 0000000000100 (12 bits, considering sign extension).

32-bit-| 000000000010 | 00000 | 00001 | 1100011 |

**BEQ r0,r0,15*

This is a B-Type instruction set

The instruction BEQ r0, r0, 15 in RISC-V assembly corresponds to a branch equal (BEQ) operation. In RISC-V, branch instructions fall under the B-type format.

Opcode (7 bits): 1100011 (BEQ opcode)
rs1 (5 bits): 00000 (register r0)
rs2 (5 bits): 00000 (register r0)
Immediate (12 bits): 15 in binary is 000000000111

32-bit-000000000111  00000  00000   000

**LW r13,r11,2*

This is a I-Type instruction set

The instruction LW r13, r11, 2 in RISC-V assembly language is used to load a word from memory into register r13, with an offset of 2 bytes from the address stored in register r11. In RISC-V, this operation corresponds to the I-type (Immediate-type) format for load instructions. 

Opcode (7 bits): 0000011 (LW opcode)
rd (5 bits): 01101 (register r13)
rs1 (5 bits): 01011 (register r11)
Immediate (12 bits): 000000000010 (binary for 2

32-bit-000000000010  01011   010       01101  0000011

**SLL r15,r11,2*

This is a R-type instruction set.
The instruction SLL r15, r11, 2 in RISC-V assembly language performs a left logical shift on the value stored in register r11 by 2 bits and stores the result in register r15. 

Opcode (7 bits): 0110011 (SLL opcode)
rd (5 bits): 01111 (register r15)
funct3 (3 bits): 001 (for SLL)
rs1 (5 bits): 01011 (register r11)
rs2 (5 bits): 00000 (register r0, which signifies the shift amount)
funct7 (7 bits): 0000000 (for SLL)

32-bit-0000000   00000  01011   001      01111  0110011

</details>

<details>

<summary><h3>Task 5:GTK waveform </summary>

In this we need to find the output waveforms for the instructions which we learnt in Task 4.

**Steps to perform*

1.Firstly give the command :
                            
                            sudo apt-get update
                            sudo apt-get install iverilog gtkwave

2. Setup Your Project Directory
Create a directory for your project and place your Verilog files and testbench there.

                          mkdir rv
                          cd rv

3.Then from the reference copy the code of verilog and testbench and save them.

4.Give the command line 

                        touch rv_riscv32.v
                        touch rv_riscvtb.v

5.Compile these files using Icarus Verilog:

                                    iverilog -o rv_riscv32 rv_riscv32.v rv_riscvtb.v
                                    ./rv_riscv32

6.View the Waveform
Open the waveform file using GTKWave:

                                  gtkwave iiitb_rv32i.vcd
                                  
![Ubuntu commands and installation of gtkwave and iverilog](https://github.com/Nishitasa/vsd-quadron-intern/assets/173664538/73a60cb0-b6ba-4673-86a6-8c0c972c0a89)

Then it will open GTKWAVE

![Gtkwave](https://github.com/Nishitasa/vsd-quadron-intern/assets/173664538/8d494094-1fe3-4aa5-9487-3931f4563002)
![gtkwave commands](https://github.com/Nishitasa/vsd-quadron-intern/assets/173664538/9af72765-903a-4b2f-9578-af379afd2373)

![EX_mem open and waveforms with clock](https://github.com/Nishitasa/vsd-quadron-intern/assets/173664538/c7814b93-da2b-42b3-a6a7-0b535af42288)

Select the instructions from EX_MEM_IR[31:0]

**INSTRUCTION ADD r1,r2,r3*
![ADD r1, r2, r3](https://github.com/Nishitasa/vsd-quadron-intern/assets/173664538/025a0d89-3672-46f3-8ca5-3b2999deceb0)

**INSTRUCTION SUB r3, r1, r2*
![SUB r3, r1, r2](https://github.com/Nishitasa/vsd-quadron-intern/assets/173664538/54eb94d0-5277-4600-ad46-1478670e023e)

**Instruction AND r2, r1, r3*
![AND r2, r1, r3](https://github.com/Nishitasa/vsd-quadron-intern/assets/173664538/e98dd319-0e0b-4b8d-9e25-6b49353d9052)

**Instruction OR r8, r2, r5*
![OR r8, r2, r5](https://github.com/Nishitasa/vsd-quadron-intern/assets/173664538/4c68d4ae-4abe-4caa-a9ce-c7ca6238b13e)

**Instruction XOR r8, r1, r4*
![XOR r8, r1, r4](https://github.com/Nishitasa/vsd-quadron-intern/assets/173664538/625c73b4-adfe-4670-8101-a6becf03fcf7)

**Instruction SLT r10, r2, r4*
![SLT r10, r2, r4](https://github.com/Nishitasa/vsd-quadron-intern/assets/173664538/31a13ead-e52f-4bf1-9d4d-d3b6f945602b)

**Instruction ADDI r12, r3, 5*
![ADDI r12, r3, 5](https://github.com/Nishitasa/vsd-quadron-intern/assets/173664538/6d010385-20af-44cd-993b-0726fe991463)

**Instruction SW r3, r1, 4*
![SW r3, r1, 4](https://github.com/Nishitasa/vsd-quadron-intern/assets/173664538/11336ba0-d70d-46a1-b260-4b1edc7b7822)

**Instruction SRL r16, r11, r2*
![SRL r16, r11, r2](https://github.com/Nishitasa/vsd-quadron-intern/assets/173664538/21c13d83-9d1c-422c-abeb-60bf8e1aae3d)

**Instruction BNE r0, r1, 20*
![BNE r0, r1, 20](https://github.com/Nishitasa/vsd-quadron-intern/assets/173664538/bf5716ec-08c7-4805-b755-eb7b789bc826)

**Instruction SLL r15, r11, r2*
![SLL r15, r11, r2](https://github.com/Nishitasa/vsd-quadron-intern/assets/173664538/2e1aaa3c-38ac-485d-8bab-14bbfc7aec8e)

</details>

<details>

<summary><h3>Task6:PROJECT</summary>

The task is to implement Ascent control Engineer:Creating a DOOR LOCK SYSTEM using RISC-V board

## Overview:

An elevator controller is responsible for managing the operation of an elevator, including tasks such as moving the elevator car to the desired floor, opening and closing the doors, and handling user requests efficiently. Creating a smart elevator controller using a RISC-V board involves designing both the hardware and software components to ensure reliable and efficient operation.

## Components Required:

1.RISC-V Board
2.LED display 
3.Power Supply(12V or 24V)
4.Bread Board
5.Jumper Wires
6.Keypad

## Circuit connections:

1.RISC-V Board Setup:

Connect the RISC-V board to the breadboard using jumper wires.
Ensure that the board is powered using an appropriate power supply.


2.Display (7-segment LED or LCD):
Connect the display pins to the appropriate GPIO (General Purpose Input/Output) pins on the RISC-V board.



![image](https://github.com/Nishitasa/vsd-quadron-intern/assets/173664538/112745d0-e33a-4cb0-8c7d-a95eb0cb1033)

## Program Code:

               #include <debug.h>
#include <ch32v00x.h>
#include <ch32v00x_gpio.h>
#include <ch32v00x_i2c.h>
#include <string.h>

// Keypad configuration
#define ROWS 4
#define COLS 4
const uint16_t rowPins[ROWS] = {GPIO_Pin_0, GPIO_Pin_1, GPIO_Pin_2, GPIO_Pin_3}; // Adjust according to your setup
const uint16_t colPins[COLS] = {GPIO_Pin_4, GPIO_Pin_5, GPIO_Pin_6, GPIO_Pin_7}; // Adjust according to your setup

// Keypad matrix
char keypadMatrix[ROWS][COLS] = {
    {'1', '2', '3', 'A'},
    {'4', '5', '6', 'B'},
    {'7', '8', '9', 'C'},
    {'*', '0', '#', 'D'}
};

// LCD configuration
#define LCD_ADDR 0x27 // Adjust the I2C address for your LCD

// Password configuration
const char *correctPassword = "1234";
char inputPassword[10];
int inputIndex = 0;

// Function prototypes
void initGPIO(void);
void initI2C(void);
void lcdWriteCommand(uint8_t cmd);
void lcdWriteData(uint8_t data);
void lcdInit(void);
void lcdPrint(const char *str);
char readKeypad(void);
void checkPassword(void);
void Delay(uint32_t time);

int main(void) {
    // Initialize system
    SystemInit();
    initGPIO();
    initI2C();
    lcdInit();

    lcdPrint("Enter Password:");
    
    while (1) {
        char key = readKeypad();
        if (key) {
            if (key == '#') { // Enter key
                checkPassword();
                inputIndex = 0; // Clear input for next attempt
            } else if (key == '*') { // Clear key
                inputIndex = 0;
                lcdPrint("Enter Password:");
            } else {
                if (inputIndex < sizeof(inputPassword) - 1) {
                    inputPassword[inputIndex++] = key;
                    inputPassword[inputIndex] = '\0';
                    lcdPrint(inputPassword);
                }
            }
        }
        Delay(10); // Debounce delay
    }
}

void initGPIO(void) {
    GPIO_InitTypeDef GPIO_InitStructure;
    
    RCC_APB2PeriphClockCmd(RCC_APB2Periph_GPIOA, ENABLE);

    // Initialize rows as output
    GPIO_InitStructure.GPIO_Pin = GPIO_Pin_0 | GPIO_Pin_1 | GPIO_Pin_2 | GPIO_Pin_3;
    GPIO_InitStructure.GPIO_Mode = GPIO_Mode_Out_PP;
    GPIO_InitStructure.GPIO_Speed = GPIO_Speed_50MHz;
    GPIO_Init(GPIOA, &GPIO_InitStructure);

    // Initialize columns as input
    GPIO_InitStructure.GPIO_Pin = GPIO_Pin_4 | GPIO_Pin_5 | GPIO_Pin_6 | GPIO_Pin_7;
    GPIO_InitStructure.GPIO_Mode = GPIO_Mode_IPU;
    GPIO_Init(GPIOA, &GPIO_InitStructure);
}

void initI2C(void) {
    I2C_InitTypeDef I2C_InitStructure;

    RCC_APB1PeriphClockCmd(RCC_APB1Periph_I2C1, ENABLE);
    
    I2C_InitStructure.I2C_ClockSpeed = 100000; // Adjust as necessary
    I2C_InitStructure.I2C_Mode = I2C_Mode_I2C;
    I2C_InitStructure.I2C_DutyCycle = I2C_DutyCycle_2;
    I2C_InitStructure.I2C_OwnAddress1 = 0x00;
    I2C_InitStructure.I2C_AcknowledgedAddress = I2C_AcknowledgedAddress_7bit;
    I2C_Init(I2C1, &I2C_InitStructure);
    I2C_Cmd(I2C1, ENABLE);
}

void lcdWriteCommand(uint8_t cmd) {
    I2C_GenerateSTART(I2C1, ENABLE);
    while (!I2C_CheckEvent(I2C1, I2C_EVENT_MASTER_MODE_SELECT));
    I2C_Send7bitAddress(I2C1, LCD_ADDR, I2C_Direction_Transmitter);
    while (!I2C_CheckEvent(I2C1, I2C_EVENT_MASTER_TRANSMITTER_MODE_SELECTED));
    I2C_SendData(I2C1, cmd);
    while (!I2C_CheckEvent(I2C1, I2C_EVENT_MASTER_BYTE_TRANSMITTED));
    I2C_GenerateSTOP(I2C1, ENABLE);
}

void lcdWriteData(uint8_t data) {
    I2C_GenerateSTART(I2C1, ENABLE);
    while (!I2C_CheckEvent(I2C1, I2C_EVENT_MASTER_MODE_SELECT));
    I2C_Send7bitAddress(I2C1, LCD_ADDR, I2C_Direction_Transmitter);
    while (!I2C_CheckEvent(I2C1, I2C_EVENT_MASTER_TRANSMITTER_MODE_SELECTED));
    I2C_SendData(I2C1, data);
    while (!I2C_CheckEvent(I2C1, I2C_EVENT_MASTER_BYTE_TRANSMITTED));
    I2C_GenerateSTOP(I2C1, ENABLE);
}

void lcdInit(void) {
    Delay(50); // Wait for LCD to power up

    // Initialize LCD in 4-bit mode
    lcdWriteCommand(0x33); // Function set
    lcdWriteCommand(0x32); // Function set
    lcdWriteCommand(0x28); // 4-bit mode, 2 lines, 5x8 dots
    lcdWriteCommand(0x0C); // Display on, cursor off
    lcdWriteCommand(0x06); // Entry mode set
    lcdWriteCommand(0x01); // Clear display
    Delay(2); // Wait for clear command to complete
}

void lcdPrint(const char *str) {
    while (*str) {
        lcdWriteData(*str++);
    }
}

char readKeypad(void) {
    for (int row = 0; row < ROWS; row++) {
        // Set all rows to high except the current one
        GPIO_ResetBits(GPIOA, rowPins[row]); // Set current row low
        for (int col = 0; col < COLS; col++) {
            if (GPIO_ReadInputDataBit(GPIOA, colPins[col]) == RESET) { // If key is pressed
                while (GPIO_ReadInputDataBit(GPIOA, colPins[col]) == RESET); // Wait for key release
                GPIO_SetBits(GPIOA, rowPins[row]); // Set row back to high
                return keypadMatrix[row][col];
            }
        }
        GPIO_SetBits(GPIOA, rowPins[row]); // Set row back to high
    }
    return '\0'; // No key pressed
}

void checkPassword(void) {
    if (strcmp(inputPassword, correctPassword) == 0) {
        lcdPrint("Access Granted");
    } else {
        lcdPrint("Access Denied");
    }
    Delay(2000); // Show result for 2 seconds
    lcdPrint("Enter Password:");
}

void Delay(uint32_t time) {
    // Simple delay loop
    while (time--) {
        for (volatile uint32_t i = 0; i < 1000; i++);
    }
}
</details>

<details>

<summary><h3>PROJECT</summary>

 PIN connection
 ![pin Connection](https://github.com/user-attachments/assets/39d06f72-4953-45bd-9525-f166aab5cbc0)

APPLICATION VIDEO:

https://drive.google.com/file/d/1edcnWnK5Y7pqWLp8H07GEQTBxb7qI-YY/view?usp=sharing
