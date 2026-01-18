# Information on Flags and Options
## Key
| Symbol | Interpretation                  |
|--------|---------------------------------|
| rd     | Destination Register            |
| rs1    | Source Register 1               |
| rs2    | Source Register 2               |
| imm    | Immediate Value                 |
| shamt  | Shift Amount                    |
| PC     | Program Counter                 |
| pre    | Predecessor Ordering            |
| succ   | Successor Ordering              |

Brackets after symbols [a:b] refer to a bit range, inclusive of both a and b. This amounts to
b - a + 1 bits in total. For example, imm[11:0] refers to a 11 - 0 + 1 = 12-bit immediate value.
## Supported RISC-V Instructions
From *The RISC-V Instruction Set Manual Volume I*, unpriveleged architecture, version 20250508 ratified.
### RV32I Base Integer Instructions (x1 - x31; x0 / zero register)
#### Integer Register-Immediate Instructions
| Instruction | Description     | Format             | Supported |
|-------------|-----------------|--------------------|-----------|
| ADDI        | Add Immediate   | rd, rs1, imm[11:0] | :x: |
| ANDI        | AND Immediate   | rd, rs1, imm[11:0] | :x: |
| ORI         | OR Immediate    | rd, rs1, imm[11:0] | :x: |
| XORI        | XOR Immediate   | rd, rs1, imm[11:0] | :x: |
| SLTI        | Set Less Than Immediate | rd, rs1, imm[11:0] | :x: |
| SLTIU       | Set Less Than Immediate Unsigned | rd, rs1, imm[11:0] | :x: |
| SLLI        | Shift Left Logical Immediate | rd, rs1, shamt[4:0] | :x: |
| SRLI        | Shift Right Logical Immediate | rd, rs1, shamt[4:0] | :x: |
| SRAI        | Shift Right Arithmetic Immediate | rd, rs1, shamt[4:0] | :x: |
| LUI         | Load Upper Immediate | rd, imm[19:0] | :x: |
| AUIPC       | Add Upper Immediate to PC | rd, imm[19:0] | :x: |
#### Integer Register-Register Instructions
| Instruction | Description     | Format             | Supported |
|-------------|-----------------|--------------------|-----------|
| ADD         | Add             | rd, rs1, rs2       | :x: |
| SUB         | Subtract        | rd, rs1, rs2       | :x: |
| AND         | AND             | rd, rs1, rs2       | :x: |
| OR          | OR              | rd, rs1, rs2       | :x: |
| XOR         | XOR             | rd, rs1, rs2       | :x: |
| SLT         | Set Less Than   | rd, rs1, rs2       | :x: |
| SLTU        | Set Less Than Unsigned | rd, rs1, rs2 | :x: |
| SLL         | Shift Left Logical | rd, rs1, rs2    | :x: |
| SRL         | Shift Right Logical | rd, rs1, rs2    | :x: |
| SRA         | Shift Right Arithmetic | rd, rs1, rs2   | :x: |
#### Control Transfer Instructions
| Instruction | Description     | Format             | Supported |
|-------------|-----------------|--------------------|-----------|
| JAL         | Jump and Link   | rd, imm[20:1]     | :x: |
| JALR        | Jump and Link Register | rd, rs1, imm[11:0] | :x: |
| BEQ         | Branch if Equal | rs1, rs2, imm[12:1] | :x: |
| BNE         | Branch if Not Equal | rs1, rs2, imm[12:1] | :x: |
| BLT         | Branch if Less Than | rs1, rs2, imm[12:1] | :x: |
| BLTU        | Branch if Less Than Unsigned | rs1, rs2, imm[12:1] | :x: |
| BGE         | Branch if Greater Than or Equal | rs1, rs2, imm[12:1] | :x: |
| BGEU        | Branch if Greater Than or Equal Unsigned | rs1, rs2, imm[12:1] | :x: |
#### Load and Store Instructions
| Instruction | Description     | Format             | Supported |
|-------------|-----------------|--------------------|-----------|
| LB          | Load Byte       | rd, imm(rs1) | :x: |
| LH          | Load Halfword   | rd, imm(rs1) | :x: |
| LW          | Load Word       | rd, imm(rs1) | :x: |
| LBU         | Load Byte Unsigned | rd, imm(rs1) | :x: |
| LHU         | Load Halfword Unsigned | rd, imm(rs1) | :x: |
| SB          | Store Byte      | rs2, imm(rs1) | :x: |
| SH          | Store Halfword  | rs2, imm(rs1) | :x: |
| SW          | Store Word      | rs2, imm(rs1) | :x: |
#### Miscellaneous Instructions (Probably will not be supported)
| Instruction | Description     | Format             | Supported |
|-------------|-----------------|--------------------|-----------|
| FENCE       | Memory Fence    | pre, succ         | :x: |
| ECALL       | Environment Call  |                 | :x: |
| EBREAK      | Environment Break |                 | :x: |
### RV32F Base Floating-Point Instructions
### RV64I Base Integer Instructions
### RV64F Base Floating-Point Instructions