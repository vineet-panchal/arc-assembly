## Run The Assembly Programs

1. Download arctools
2. Open ARCToolsv.2.0.2.jar through the terminal

```bash
  java -jar ARCToolsv2.O.2.jar
```
3. Load the bin file of the program you want to run
4. Run the program

## Introduction To ARC Assembly

Assembly is a low-level language that translates programmed instructions to machine code. 

SPARC - Scalable Processor Architecture a Reduced Instruction Set Computing (RISC) ISA

Instruction Set Architecture (ISA) - a collection of instructions that a processor can excute.

ARC is a type of the many Assembly languages and its instruction set architecture is a subset of the SPARC ISA.

## ARC Registers

There are 32 registers that ARC works with to store and load from memory

Registers are named by their number: 0-31

#### The Registers
%r0  %r1  %r2  %r3  %r4  %r5  %r6  %r7
%r8  %r9  %r10 %r11 %r12 %r13 %r14 %r15
%r16 %r17 %r18 %r19 %r20 %r21 %r22 %r23
%r24 %r25 %r26 %r27 %r28 %r29 %r30 %r31

#### Special Registers
- %PC - Program Counter (PC)
- %PSR - Program Status Register (PSR)
- %r0 - Always 0
- %r14 - Stack Pointer
- %r15 - Link Pointer

#### PSR Register
Holds flags (bits) that indicate the status or condition of the instruction that is currently being executed.

There are 4 flags in ARC:
- Z - zero
- N - negative
- C - carry-out
- V - overflow

## ARC Instruction Set
Instructions in ARC fall under 4 categories:
- Memory instructions
- Logical instructions
- Arithmetic instructions
- Control Transfer instructions

### Memory Instructions
ld - load a register from memory (reading from memory)
st - store a register into memory (writing to memory)

load and store instructions only store data movement of data between registers and memory. 

### Logical Instructions

sethi - load the 22 most significant bits of a register
andcc - bitwise logical AND & check for condition codes or flags
orcc - bitwise logical OR & check for condition codes or flags
orncc - butwise logical NOR & check for condition codes or flags
srl - shift right (logical)

## Arithmetic Instructions

addcc - add & check for condition codes or flags
subcc - subtract & check for condition codes or flags
sra - shift right

## Control Transfer Instructions

call - call a subroutine/method/function
jmpl - jump and link (return from a subroutine call)
be - branch if zero
bneg - branch if negative
bcs - branch on carry
bvs - branch on overflow
ba - branch always (unconditionally)
bpos - branch on positive
bvc - branch on no overflow
bnc - branch on not zero
bcc - branch on carry clear
