---
layout: project
type: project
image: img/EmbeddedTimer/EmbeddedTimer.png
title: "Embedded Stopwatch & Countdown Timer"
date: 2025-11-23
published: true
labels:
  - Embedded Systems
  - C
  - FPGA
  - VHDL
  - ARM HPS
summary: "Designed and implemented an embedded stopwatch and countdown timer running on the DE10-Standard board, integrating ARM HPS software with FPGA hardware using memory-mapped I/O. Implemented a finite-state machine in C and custom VHDL logic for 7-segment display control."
---
This project is an **embedded stopwatch and countdown timer application** developed for the DE10-Standard (ARM HPS + FPGA) platform. The system runs directly on hardware and supports two independent modes—stopwatch (count up) and countdown timer (count down)—with full interaction through physical buttons, switches, LEDs, and HEX displays.

The application is split across software running on the ARM HPS and custom hardware logic implemented on the FPGA. The ARM side is responsible for application logic, timing, and input handling, while the FPGA handles low-level display decoding. Communication between software and hardware is achieved through **memory-mapped I/O over the Lightweight HPS–FPGA bridge**, creating a clear separation of concerns between computation and hardware control.

---

## System Architecture

### HPS (Software – C)
- Implements the complete stopwatch and countdown finite-state machines  
- Handles user input via pushbuttons (KEY[3:0]) and switches (SW[9:0])  
- Maintains timekeeping using a software timer module with millisecond accumulation  
- Writes numeric time values (HHMMSS) to FPGA registers via a Hardware Abstraction Layer (HAL)  

### FPGA (Hardware – VHDL)
- Custom `decoder_7seg.vhd` module converts 4-bit digits into 7-segment patterns  
- Offloads segment decoding from the CPU for correctness and performance  
- Drives HEX0–HEX5 displays through dedicated FPGA logic  

This architecture allowed the ARM processor to work with simple numeric values while the FPGA handled display-specific details, improving modularity and reliability.

---

## Application Logic

The system is driven by a **finite-state machine (FSM)** supporting both stopwatch and countdown modes:

- **Stopwatch:** Ready → Running → Paused → Finished  
- **Countdown:** Set Hours → Set Minutes → Set Seconds → Running → Paused → Finished  

Key behaviors:
- KEY0 always returns the system to an idle state  
- KEY2 toggles start/pause during active timing  
- Switch values provide numeric input for preset times  
- Time updates occur on a consistent 10 ms loop for responsiveness  

LEDs and HEX displays provide visual feedback, including blinking alerts when the countdown reaches zero.

---

## My Role & Contributions
This was an individual embedded systems project, and I was responsible for the full hardware–software integration.

Key contributions included:
- Designing and implementing the application logic and FSM in C  
- Writing modular peripheral drivers for buttons, switches, LEDs, and HEX displays  
- Building a Hardware Abstraction Layer to safely access memory-mapped FPGA registers  
- Implementing a software-based timer for accurate timekeeping without hardware timers  
- Writing custom VHDL (`decoder_7seg.vhd`) to perform 7-segment decoding in hardware  
- Integrating and debugging the system directly on the DE10-Standard board via embedded Linux and SSH  

---

## Key Takeaways
- Gained hands-on experience with ARM HPS–FPGA communication using memory-mapped I/O  
- Learned how to design clean abstractions between hardware, drivers, and application logic  
- Strengthened understanding of finite-state machines in real-time embedded systems  
- Developed confidence debugging embedded Linux applications running on physical hardware  
- Reinforced the importance of timing accuracy and responsiveness in user-facing embedded systems  

---

## Challenges & Solutions
- **Unreliable button presses:** Implemented edge detection with a 10 ms polling loop to avoid bounce  
- **Incorrect HEX display output:** Moved digit decoding from software to FPGA using VHDL  
- **Timing drift:** Replaced long sleep delays with millisecond accumulation for stable updates  
- **Long FPGA synthesis times:** Structured debugging to minimize rebuild cycles  

---

## Potential Enhancements
- Replace polling-based input with hardware interrupts  
- Add hardware timer support for higher timing precision  
- Extend display functionality (decimal points, >99 hour support)  
- Implement debouncing logic in hardware  

---

## Demo & Links
- **Demo Video:** [https://youtu.be/JK8QUs_x1eA](https://youtu.be/JK8QUs_x1eA)
- **GitHub Repository:** [https://github.com/elijahbrandner/EmbeddedTimer](https://github.com/elijahbrandner/EmbeddedTimer)  
