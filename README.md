# Pipeline
This repository was intended as a way for me to learn about pipelines in the context of
computer architecture. The current intended use is to be able to feed the program a text file
containing the instructions (RISC-V, maybe x86 in the future) to be exected, along with some parameters (such as clock cycle
time, cycles per instruction, pipeline forwarding, limited user-defined forwarding, etc). 
This program will then compute the total number of cycles to execute the code and
total execution time. It may also include more stats such as CPI/IPC, total number of stalls,
and a cycle-by-cycle breakdown of what is happening in the pipeline.

As I learn more about computer architecture and pipelines, I intend to expand this program
to include more features. May also include the ability for a user defined pipeline, but this
would be in the far future if at all.

## Current Status
Currently, I am contemplating how to best structure the program, including how to ensure
ease of expandability in the future.

## Put usage instructions here

## Put stuff about language and compiler versions here
