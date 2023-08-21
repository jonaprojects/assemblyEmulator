# Welcome to Emu++

## Installation

You can install Emu++ by running the following command in the terminal:

```bash
pip install assembly-emulator
```

## Usage

First, import the module:

```python
from assembly_emulator import asm8086_demo
```

The easiest way to get started is to execute the program's <code>main</code> method.

```python
asm8086_demo.main()
```

And then you should see the folowing menu:

![menu](image.png "Menu")

You can enter 'C' to continue in 'Console Mode'. In console mode, you can run each line and get an immediate feedback. Namely, after each command you execute you can view the changes in the registers, the stacks, etc.

Alternatively, you can enter 'T' to enter 'Text Editor' mode. In text editor mode, you first enter all of your code and after you are done you can see the result.

In order to move to the execution stage you can use the <code>%finish</code> special command. After that, you will see the relevant information about the execution and then you'll be able to save your program in a file of your choice.

You can also enter 'F' to upload the
assembly code from an external file.
This might actually be the most convenient approach when creating a whole assembly program.

## Supported Commands

- <code>mov</code> - assign a value to a register or a variable
- <code>add</code> - add a value to a register or a variable
- <code>sub</code> - subtract a value from a register or a variable
- <code>mul</code>
- div
- <code>xchg</code> - exchange the contents of two registers
- lea
- <code>inc</code> - increase the value of a register or a variable by 1
- <code>dec</code> - decrease the value of a register or a variable by 1
- <code>xor</code> - logical extensive or operation between two registers or variables
- <code>or</code> - logical or operation between two registers or variables
- <code>int</code> - call a certain interrupt.
- <code>cmp</code> - compare between the values of two registers or variables. if they are equal a corresponding flag will be updated.
- <code>jmp</code> - jump to a certain label in memory
- <code>je</code> - jmp if equal, depending on the result of the last cmp operation
- <code>jne</code> - jmp if not equal, depending on the result of the last cmp operation
- <code>jz</code> - jmp if zero
- <code>jnz</code> - jmp if not zero
- <code>ja</code> - jmp if above
- <code>jb</code> - jmp if below
- <code>print</code> - print the value of a certain register or variable
- input
- <code>push</code> - push a value of a register or a variable to the stack
- <code>pop</code> - remove a value from the stack
- <code>pusha</code> - push all of the values of the registers to the stack
- <code>popa</code> - remove all the values from the stack
- <code>loop</code>
- <code>proc</code> - create a procedure
- <code>endp</code> - denote the end of a procedure
- <code>call</code> - call a procedure

### Define Variables

You can create variables according to their desired size in memory using the db, dw, and dd keywords.

In theory, in assembly 8086 the 'db' keyword creates a variable that takes 1 byte in memory (8 bits), dw ('define word') allocates 2 bytes in memory (16 bits) and dd ('define double word') allocates 32 bits in memory.

For example:

```
; add an example here
```

### Special Commands

There are several special commands that allow you to override the overall flow of the program.

- <code>%finish</code> - finish writing code and move to the execution stage
- <code>%about</code> - Information about the project
- <code>%cmd</code> - View all special commands
- <code>%help</code> - View the supported features of the project.
