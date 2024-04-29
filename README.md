# Addressing-modes
# Addressing-modes
Addressing modes:
The term addressing modes refers to the way in which the operand of an instruction is specified. The addressing mode specifies a rule for interpreting or modifying the address field of the instruction before the operand is actually executed.
RISC-type addressing modes:
• Immediate
• Register
• Absolute
• Register indirect
• Index
• Base with index
Here are the assembler syntax and addressing function of the addressing modes.
![addressing](https://github.com/MNivetha1/Addressing-modes/assets/168455467/f97072e8-2f62-4644-b440-d9a4f33fb0f9)

Immediate addressing mode:
        Immediate addressing mode allows instructions to operate directly on constant values or immediate data.
In this mode, the operand is encoded directly within the instruction itself, rather than being fetched from a memory location.
Example:
consider the RISC instruction:
ADDI R1, R2, #10
In this instruction, ADDI is the opcode for addition with immediate mode. R1 and R2 are registers, and #10 is the immediate value.
This instruction adds the value of register R2 to the immediate value 10 and stores the result in register R1.

Register Addressing mode:
          Register addressing mode involves specifying operands by referencing registers rather than memory locations.
Instructions in this mode operate directly on the contents of registers.

Example:
Consider the RISC instruction:
ADD R1, R2, R3
In this instruction, ADD is the opcode for addition with register addressing mode. R1, R2, and R3 are registers.
This instruction adds the contents of registers R2 and R3 and stores the result in register R1.

Absolute Addressing mode:
         The Absolute addressing mode involves specifying the exact memory address of an operand directly within the instruction itself.
This Absolute addressing mode simplifies instruction execution by directly specifying the memory address in the instruction itself, making it efficient for accessing specific data at known memory locations.
Example:
Consider an instruction
LOAD R1, 0x1234
where,
LOAD is the opcode for loading data into a register.
R1 is the destination register.
0x1234 is the memory address from where the data needs to be loaded.

Register indirect addressing mode:
         Register indirect addressing mode involves accessing memory indirectly through a register's value. Instead of directly specifying a memory address, the instruction refers to a register that holds the memory address where the operand is located.
Register indirect addressing mode allows for more flexible memory access and is often used for accessing data structures like arrays or linked lists.
Example:
Consider the RISC instruction:
LW R1, 0(R2)
In this instruction, LW is the opcode for "load word" with register indirect addressing mode.
R1 is the destination register where the word will be loaded.
0(R2) means that the operand is located at the memory address contained in register R2, offset by 0.

Index addressing mode:
        Index addressing mode involves accessing memory by adding an offset to a base register's value. It allows for efficient access to array elements or data structures where elements are stored at fixed offsets from a base address.
Example:
Consider an instruction
LW R1, 100(R2)
In this instruction, LW is the opcode for "load word" with index addressing mode.
R1 is the destination register where the word will be loaded.
100(R2) means that the operand is located at the memory address obtained by adding an offset of 100 to the value stored in register R2.

Base with index addressing mode:
          Base with index addressing mode involves accessing memory by adding an offset to the sum of a base register's value and an index register's value. This mode allows for flexible memory access by combining a base address with an index value.
Example:
consider the RISC instruction:
LW R1, 12(R2+R3)
In this instruction, LW is the opcode for "load word" with base with index addressing mode.
12(R2+R3) means that we want to access the field at an offset of 12 bytes from the sum of the base address stored in register R2 and the index value stored in register R3.
