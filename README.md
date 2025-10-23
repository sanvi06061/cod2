Interrupt Handling Simulation (C++)
Overview

Simulates interrupt handling for three I/O devices — Keyboard (High), Mouse (Medium), and Printer (Low) — using C++ threads (pthread) 
and priority-based scheduling. Supports masking to enable/disable device interrupts during runtime.

Features

Random interrupt generation

Priority-based handling: Keyboard → Mouse → Printer

Mask/unmask interrupts at runtime

Clear ISR output

Controls
| Key | Action               |
| --- | -------------------- |
| `k` | Toggle Keyboard mask |
| `m` | Toggle Mouse mask    |
| `p` | Toggle Printer mask  |
| `q` | Quit simulation      |


Compilation & Run
g++ interrupt_simulation.cpp -o interrupt_simulation -lpthread
./interrupt_simulation

Example Output
Keyboard Interrupt Triggered → Handling ISR → Completed
Mouse Interrupt Triggered → Handling ISR → Completed
Printer Interrupt Ignored (Masked)
