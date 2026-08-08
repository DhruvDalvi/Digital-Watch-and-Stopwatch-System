# Digital-Watch-and-Stopwatch-System
This project implements a Digital Watch and Stopwatch System using Verilog RTL. The design uses synchronous digital logic to implement timekeeping and stopwatch functionality, including time counters, rollover logic, and control operations. A basic SystemVerilog testbench is included to simulate the RTL design and verify its functional behavior.

# Features

* Digital timekeeping using hours, minutes, and seconds counters
* Stopwatch functionality
* Start/stop control for the stopwatch
* Reset functionality
* Clock divider / timing generation
* Automatic counter rollover
* Synchronous RTL design
* SystemVerilog-based functional testbench
* Simulation waveform-based verification

# Design

The system is implemented using:

* **Verilog** – RTL design
* **SystemVerilog** – Testbench
* **Simulation** – Used to verify counter operation, reset behavior, and stopwatch controls

# Main Functional Blocks

``` text
              ┌─────────────────────┐
Clock ────────►                     │
              │    Clock Divider    │
              │                     │
              └──────────┬──────────┘
                         │
                         ▼
              ┌─────────────────────┐
              │   Time Counters     │
              │                     │
              │ Seconds             │
              │ Minutes             │
              │ Hours               │
              └──────────┬──────────┘
                         │
                         ▼
              ┌─────────────────────┐
              │  Stopwatch Control  │
              │                     │
              │ Start / Stop / Reset│
              └──────────┬──────────┘
                         │
                         ▼
                  Time / Stopwatch
                     Outputs
```
# File Structure


Digital-Watch-Stopwatch/
│
├── rtl/
│   └── digital_watch_stopwatch.v
│
├── tb/
│   └── digital_watch_stopwatch_tb.sv
│
├── sim/
│   └── waveforms/
│
└── README.md


# Verification

A basic SystemVerilog testbench was developed to verify the RTL functionality.

The testbench checks:

* Reset operation
* Time counter progression
* Seconds-to-minutes rollover
* Minutes-to-hours rollover
* Stopwatch start operation
* Stopwatch stop operation
* Stopwatch reset operation

Simulation waveforms are used to observe the behavior of the counters and control signals.

# Simulation

The RTL can be simulated using tools such as:

* QuestaSim / ModelSim
* Vivado Simulator



# Skills Demonstrated

* Verilog RTL Design
* Synchronous Digital Design
* Counters and Clock Division
* Finite-State / Control Logic
* SystemVerilog Testbench Development
* Functional Simulation
* Waveform Debugging

# Future Improvements

* Add a proper self-checking SystemVerilog testbench
* Add assertions for counter rollover and control operations
* Add functional/code coverage
* Add a 7-segment display interface
* Implement the design on an FPGA
* Add alarm functionality
* Add lap/reset functionality to the stopwatch
