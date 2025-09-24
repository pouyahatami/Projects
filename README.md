#Simple RISC-V Processor

This project focuses on building a simple computer that implements a **Reduced Instruction Set Computer (RISC)**.  
Here, I designed and implemented my own RISC processor while much simpler than ARMv7, it gave me a strong grasp of how computers actually work.  

---

## Register File Design

RISC processors use a hardware structure known as a **register file**, which is essentially a collection of registers multiplexed together.  

- **Reads**: In my design, register reads are **combinational**. This means that after sending a read request, the value is available immediately after a small combinational delay.  
- **Writes**: Register writes are **sequential**, happening only on the rising clock edge.  
- **Modern CPUs**: In high-performance processors, reads are often pipelined to achieve higher clock frequencies. Since this is my first attempt at building a RISC CPU, I kept the read path combinational — leaving pipelined reads as a clear area for improvement.  

**Register File Schematic:**  

<img width="753" height="401" alt="image" src="https://github.com/user-attachments/assets/80537faa-48ce-4501-8d2b-95ad558568bd" />  

---

