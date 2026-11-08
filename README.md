# AXI-VIP
A configurable, reusable Universal Verification Methodology (UVM) Verification IP (VIP) environment developed in SystemVerilog to verify the AMBA AXI protocol. This VIP models an active Master and Slave architecture capable of driving, monitoring, and checking pipelined write and read burst transactions concurrently across all 5 AXI channels.

Key Features & Highlights

1) 5-Channel Architecture: Implements concurrent, semaphore-synchronized handling of Write Address (AW), Write Data (W), Write Response (B), Read Address (AR), and Read Data (R) channels.
2) Configurable VIP Topology: Easily scales to multiple master and slave agents controlled centrally through a unified environment configuration.
3) Burst Type Support: Full support for FIXED (2'b00), INCR (2'b01), and WRAP (2'b10) burst types with automated wrap-boundary calculation.
4) Transfer Sizes & Alignments: Accommodates 1-byte, 2-byte, and 4-byte transfer sizes, aligned and unaligned addressing, and enforces 4KB boundary compliance.
5) Dynamic Strobe Generation: Automatically calculates per-beat write strobes (WSTRB) based on start address, burst size, and bus width.
6) Handshake & Backpressure Modeling: Randomized VALID/READY delays test interface robustness and protocol flow control under heavy backpressure.
7) Functional Coverage & Checking: Uses analysis FIFOs for automated transaction matching alongside cross-coverage across burst lengths, sizes, and types.
