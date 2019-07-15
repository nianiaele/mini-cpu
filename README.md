# mini-cpu
A mini 8-bits cpu on logisim. Built from scratch.

## Support instructions
- 8 bits instructions
- first 4 bits are opcode
- last 4 bits are the operand's address in memeory

| instruction | opcode | operation |
|:----:| :----: | :----: |
| LDA | 0000 | load data into adder A |
| ADD | 0001 | add |
| SUB | 0010 | sub |
| OUT | 1110 | write data to displayers |
| HLT | 1111 | halt |


## CPU architecture and data flow

![CPU architecture and data flow](https://github.com/nianiaele/mini-cpu/blob/master/img/1563224132(1).png?raw=true)

### 1 bit adder
![1 bit adder](https://github.com/nianiaele/mini-cpu/blob/master/img/1bitadder.png?raw=true)

### 1 bit ALU
![1 bit ALU](https://github.com/nianiaele/mini-cpu/blob/master/img/1bitalu.png?raw=true)


### 8 bits ALU
![1 bit adder](https://github.com/nianiaele/mini-cpu/blob/master/img/8bit%20ALU.png?raw=true)

### MAR (Memory Address Register)
![MAR](https://github.com/nianiaele/mini-cpu/blob/master/img/MAR.png?raw=true)

### GPR (General Perpose Register)
![GPR](https://github.com/nianiaele/mini-cpu/blob/master/img/GRP.png?raw=true)

### PC (Program Counter)
![PC](https://github.com/nianiaele/mini-cpu/blob/master/img/pc.png?raw=true)

### IR (Instruction Register)
![IR](https://github.com/nianiaele/mini-cpu/blob/master/img/instruction%20register(IR).png?raw=true)

### Hardwired Control Unit
![Hardwired Control Unit](https://github.com/nianiaele/mini-cpu/blob/master/img/hardwired%20control%20unit.png?raw=true)

### 8 Bits CPU
![Hardwired Control Unit](https://github.com/nianiaele/mini-cpu/blob/master/img/8bit%20ALU.png?raw=true)

## Run
- Write the binary code of the target program in memory. Start from address 0.
- Write the data into the coresponding address in memory
- Start giving CPU clock ticks. CPU will halt until it run the HLT

### Example program
Compute 16+20+24-28+32

#### instruction
| instruction | binary code | memory address |
|:----:| :----: | :----: |
| LDA R9 | 0000 1001 | 0000 (R0) |
| ADD RA | 0001 1010 | 0001 (R1) |
| ADD RB | 0001 1011 | 0010 (R2) |
| ADD RC | 0001 1100 | 0011 (R3) |
| SUB RD | 0010 1101 | 0100 (R4) |
| OUT | 1110 **** | 0101 (R5) |
| HLT | 1111 **** | 0110 (R6) |

#### data

| data(Decimal) | data(Binary) | memory address |
|:----:| :----: | :----: |
| 16 | 0001 0000 | 1001 (R9) |
| 20 | 0001 0100 | 1010 (RA) |
| 24 | 0001 1000 | 1011 (RB) |
| 28 | 0001 1100 | 1100 (RC) |
| 32 | 0010 0000 | 1101 (RD) |





