# riscv-register-implementation


Overview  ---
This project presents the design and simulation of a 16-bit register file based on RISC-V architecture principles. Implemented using Logisim, the design employs decoder-based write selection and multiplexer-based read operations to store and access processor data.



Implementation---

Write Operation (Decoder-Based)

1. A 4-bit write address is applied to the decoder.  
2. The 4-to-16 decoder activates exactly one output line.  
3. The selected output is ANDed with the RegWrite signal.  
4. On the rising edge of the clock, the selected register stores the input data.

Register Storage

1. The register file consists of 16 registers, each 16 bits wide.  
2. Registers are implemented using D flip-flops.  All registers share a common clock.


Read Operation (Multiplexer-Based)

1. Read addresses are given to the multiplexer select lines.  
2. The multiplexers select the corresponding register outputs.  The selected register values appear at the read outputs.



Expected output---

The decoder selects the required register for writing, and the selected register stores the 16-bit data on the clock edge.  
The stored values are read correctly through the multiplexers according to the given read addresses.  
Two registers can be accessed at the same time, matching the dual-read behavior of a RISC-V register file.

note:
method to access  -- 
Download the zip file and extract the .circ file
once its open in logisim , double click on the reg16 file under dev0, you can find this near the input blocks on the left hand side of the software.
