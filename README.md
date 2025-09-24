# Projects

This project focuses on building a simple computer that implements a **Reduced Instruction Set Computer (RISC)**.  
The ARMv7 architecture that I studied previously is also a RISC instruction set architecture (ISA).  
Here, I designed and implemented my own RISC processor — much simpler than ARMv7 — but enough to give me a strong grasp of how computers actually work.  

---

## Register File Design

RISC processors use a hardware structure known as a **register file**, which is essentially a collection of registers multiplexed together.  

- **Reads**: In my design, register reads are **combinational**. This means that after sending a read request, the value is available immediately after a small combinational delay.  
- **Writes**: Register writes are **sequential**, happening only on the rising clock edge.  
- **Modern CPUs**: In high-performance processors, reads are often pipelined to achieve higher clock frequencies. Since this is my first attempt at building a RISC CPU, I kept the read path combinational — leaving pipelined reads as a clear area for improvement.  

**Register File Schematic:**  

<img width="753" height="401" alt="image" src="https://github.com/user-attachments/assets/80537faa-48ce-4501-8d2b-95ad558568bd" />  

---

## Instruction Set

The “Simple RISC Machine” executes programs written with a very small set of instructions.  
While it is minimal compared to commercial ISAs, this project helped me understand instruction execution at the hardware level.  

---

## Current Status

I’m continuing to refine the CPU and experimenting with making it run as fast as possible.  

---

## Key Learnings

- Trade-offs between combinational and sequential logic  
- Timing and critical path considerations in register file design  
- Exposure to pipelining concepts as an area for improvement  
