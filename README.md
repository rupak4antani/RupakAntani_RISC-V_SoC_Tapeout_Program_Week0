# RupakAntani_RISC-V_SoC_Tapeout_Program_Week0
## Week 0 - Tool Installation

This repository aims to explain the open-source tools available for performing the RTL to GDSII flow of a chip and the steps required to install these tools as a part of the "India RISC-V SoC Tapeout Program"

## Open-Source Tools for Chip Design ##

Some of the open-source along with their purpose are mentioned below:

| Tool         | Category                 | Purpose                                                                 |
|--------------|--------------------------|-------------------------------------------------------------------------|
| Yosys        | Logic Synthesis          | Synthesizes RTL (Verilog) to gate-level netlist.                        |
| Icarus Verilog (iverilog) | Simulation               | Compiles and simulates Verilog designs.                                |
| GTKWave      | Waveform Viewer          | Displays and analyzes simulation waveforms (`.vcd` files).              |
| OpenSTA      | Static Timing Analysis   | Performs timing analysis on synthesized netlists.                       |
| Magic        | Layout Editor & DRC/LVS  | Custom IC layout editor, design rule check (DRC) & layout vs. schematic (LVS). |
| Netgen       | LVS Tool                 | Compares netlists for Layout vs. Schematic verification.                 |
| ngspice      | Circuit Simulator        | Analog/mixed-signal simulation using SPICE models.                       |
| OpenROAD     | PnR (Place & Route)      | Automatic RTL-to-GDSII digital flow (floorplanning, placement, routing). |
| TritonRoute  | Router                   | Detailed routing engine used inside OpenROAD.                            |
| KLayout      | Layout Viewer            | GDSII/OASIS viewer and editing.                                          |
| Verilator    | Simulator (Cycle-accurate)| High-speed SystemVerilog/Verilog simulation and linting.                 |
| Fossil + Git | Version Control          | Manage design files and collaboration.                                   |

