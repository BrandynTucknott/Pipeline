## Immutable Design Choices
* Input Assembly File
    * RISC-V
    * .txt
* Stages must include at a minimum:
    * Instruction Fetch (IF)
    * Instruction Decode (ID)
    * Execute (EX)
    * Memory Access (MEM)
    * Write Back (WB)


## Customizable Design Choices
* Pipeline Stages
    * Number of stages
    * Stage names
    * Substages/stage groupings?
* Compiler Options (LLVM)
    * how good of a compiler?
    * what settings are available
* Clock cycle time (hardware)
* Branch prediction strategy (hardware)
* Hazard detection + resolution strategies (compiler/hardware)
* Cache configurations (future work)
    * levels
    * sizes
    * associativity
    * block size
    * replacement policies
* Number of registers int/float(hardware)
    * 32 vs 64 bit

## Program Functionality
* Simulate pipeline or compute?
* compute CPI/IPC and execution time
* store parameters in *.ini* file for easy modification
    * read from *.ini* file to set operating conditions




## What to do now?
* Set up *.ini* file for parameters
* set up read for assmebly instruction file (.txt file?)
* record down RV32I + RV32F instructions
* implement basic 5-stage pipeline
