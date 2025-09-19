# RupakAntani_RISC-V_SoC_Tapeout_Program_Week0
## Week 0 - Tool Installation

This repository aims to explain the open-source tools available for performing the RTL to GDSII flow of a chip and the steps required to install these tools as a part of the "India RISC-V SoC Tapeout Program"

## Open-Source Tools for Chip Design ##

Some of the open-source tools along with their purpose are mentioned below:

| Tool         | Category                 | Purpose                                                                 |
|--------------|--------------------------|-------------------------------------------------------------------------|
| Yosys        | Logic Synthesis          | Synthesizes RTL (Verilog) to gate-level netlist.                        |
| Icarus Verilog (iverilog) | Simulation               | Compiles and simulates Verilog designs.                                |
| GTKWave      | Waveform Viewer          | Displays and analyzes simulation waveforms (`.vcd` files).              |
| OpenSTA      | Static Timing Analysis   | Performs timing analysis on synthesized netlists.                       |
| Magic        | Layout Editor & DRC/LVS  | Custom IC layout editor, design rule check (DRC) & layout vs. schematic (LVS). |
| Netgen       | LVS Tool                 | Compares netlists for Layout vs. Schematic verification.                 |
| ngspice      | Circuit Simulator        | Analog/mixed-signal simulation using SPICE models.                       |
| OpenROAD     | PnR (Place & Route)      | Automatic digital flow (floorplanning, placement, routing).              |
| TritonRoute  | Router                   | Detailed routing engine used inside OpenROAD.                            |
| KLayout      | Layout Viewer            | GDSII/OASIS viewer and editing.                                          |
| Verilator    | Simulator (Cycle-accurate)| High-speed SystemVerilog/Verilog simulation and linting.                 |
| OpenLane     | RTL-to-GDSII Flow        | Complete automated digital ASIC design flow (uses Yosys, OpenROAD, Magic, etc.). |
| Fossil + Git | Version Control          | Manage design files and collaboration.                                   |

## Minimum System Requirements ##

- 6 GB RAM + 50 GB HDD
- Ubuntu 20.04+
- 4vCPU

## Steps for Installing Yosys tool ##

$ sudo apt-get update
$ git clone https://github.com/YosysHQ/yosys.git
$ cd yosys
$ sudo apt install make (If make is not installed please install it)
$ sudo apt-get install build-essential clang bison flex \
libreadline-dev gawk tcl-dev libffi-dev git \
graphviz xdot pkg-config python3 libboost-system-dev \
libboost-python-dev libboost-filesystem-dev zlib1g-dev
$ make config-gcc
$ make
$ sudo make install

## Steps for Installing Icarus Verilog tool ##

$ sudo apt-get update
$ sudo apt-get install iverilog

## Steps for Installing GTKWave tool ##

$ sudo apt-get update
$ sudo apt install gtkwave

## Steps for Installing NGSpice tool ##

First, download the zip file from https://sourceforge.net/projects/ngspice/files/ and then run the following commands:

$ tar -zxvf ngspice-37.tar.gz
$ cd ngspice-37
$ mkdir release
$ cd release
$ ../configure --with-x --with-readline=yes --disable-debug
$ make
$ sudo make install

## Steps for Installing Magic tool ##

$ sudo apt-get install m4
$ sudo apt-get install tcsh
$ sudo apt-get install csh
$ sudo apt-get install libx11-dev
$ sudo apt-get install tcl-dev tk-dev
$ sudo apt-get install libcairo2-dev
$ sudo apt-get install mesa-common-dev libglu1-mesa-dev
$ sudo apt-get install libncurses-dev
$ git clone https://github.com/RTimothyEdwards/magic
$ git magic
$ ./configure
$ make
$ make install

## Steps for Installing OpenLane tool ##

$ sudo apt-get update
$ sudo apt-get upgrade
$ sudo apt install -y build-essential python3 python3-venv python3-pip make git
$ sudo apt install apt-transport-https ca-certificates curl software-properties-common
  curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o
  /usr/share/keyrings/docker-archive-keyring.gpg
$ echo "deb [arch=amd64 signed-by=/usr/share/keyrings/docker-archive-keyring.gpg]
  https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee
  /etc/apt/sources.list.d/docker.list > /dev/null
$ sudo apt update
$ sudo apt install docker-ce docker-ce-cli containerd.io
$ sudo docker run hello-world
$ sudo groupadd docker
$ sudo usermod -aG docker $USER
$ sudo reboot
$ docker run hello-world
