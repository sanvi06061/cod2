Interrupt Handling Simulation in C++

This repository contains C++ programs that simulate interrupt handling for three I/O devices: Keyboard, Mouse, and Printer.
The simulation shows how devices are prioritized, masked, and operate asynchronously using pthread.

Features

Device Priority

Keyboard, High

Mouse, Medium

Printer, Low

Masking

Enable or disable device interrupts while the program is running.

The system ignores interrupts if they are masked.

Asynchronous Interrupt Generation

Each device generates interrupts at random, simulating real-time behavior.

Clear Output

Displays when an interrupt is triggered, handled, or ignored.

Programs

Keyboard Interrupt Simulation

File: keyboard.cpp

High-priority interrupt

Mouse Interrupt Simulation

File: mouse.cpp

Medium-priority interrupt

Printer Interrupt Simulation

File: printer.cpp

Low-priority interrupt

Output Example
Keyboard Interrupt Triggered, Handling ISR, Completed
Mouse Interrupt Ignored, Masked
Printer Interrupt Triggered, Handling ISR, Completed
Keyboard Mask Disabled
Mouse Mask Enabled

Requirements

C++ compiler that supports C++11 or higher

POSIX threads (pthread)

Compilation and Execution
# Compile keyboard simulation
g++ keyboard.cpp -lpthread -o keyboard
./keyboard

# Compile mouse simulation
g++ mouse.cpp -lpthread -o mouse
./mouse

# Compile printer simulation
g++ printer.cpp -lpthread -o printer
./printer

How It Works

Each device operates in its own thread, generating interrupts at random.

The program handles interrupts by checking the mask.

High-priority devices receive attention first if multiple interrupts happen at the same time.

The mask status can change automatically during execution to simulate control at runtime.
