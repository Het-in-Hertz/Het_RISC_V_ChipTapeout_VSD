# Documentation
## Table of Content:
1. Acknowledgement 
2. Abstract
3. Tool Setup
   - 3.1 Oracle Virtual Machine
   - 3.2 Tools inside machine
4. Lecture Summary of Getting started with Digital VLSI SOC Design and Planning

 

## 1.Acknowledgments

I sincerely thank the entire VSD team for their unwavering support, expert guidance, and providing such an exceptional learning platform throughout this RISC-V Reference SoC Tapeout Program. Their dedication to fostering hands-on experience and advancing semiconductor education has been invaluable to my growth as an engineer.

I would also like to express my gratitude to all other involved professionals and institutions who made this program possible, including but not limited to IIT Gandhinagar, Prof. Rajat Moona, Mr.Sameer Patel, Efabless, and Mr. Muhammed Kasim. Their contributions and collaboration have greatly enriched this learning journey.

## 2.Abstract
This repository contains comprehensive installation guidelines for open-source VLSI and EDA toolchains, tailored for academic and project-based workflows. The documented process includes step-by-step instructions to install key tools such as Yosys, Iverilog, GTKWave on Ubuntu 20.04 with a recommended hardware setup (6GB RAM, 50GB storage, 4 vCPUs), ensuring consistency and reliability for new users. Detailed system checks, version requirements, and configuration scripts are supplied to streamline both individual and group development environments in semiconductor and hardware design projects. Usage of oracle virtual machine is advocated in case of Windows and the steps for same are also demonstrated.

This repo is designed for educational purposes and is being submitted as part of a tool setup and system verification exercise, with all tool snapshots and configuration documentation included for transparency and reproducibility.

This also includes a summary of the lecture:Getting started with Digital VLSI SOC Design and Planning.

## 3.Tool Setup setup
### 3.1 Virtual Box
Go to: https://www.virtualbox.org/wiki/Downloads

<img width="1916" height="869" alt="image" src="https://github.com/user-attachments/assets/2366824b-a72c-4d3c-ad7c-6017dd5ca5c0" />

Click on windows host and download the file:

<img width="362" height="81" alt="image" src="https://github.com/user-attachments/assets/f8fb4cdf-3b9f-4ba4-972f-fc9f26a36d85" />

Download Ubuntu iso from Ubuntu Website

<img width="1753" height="614" alt="image" src="https://github.com/user-attachments/assets/5d6363df-36dc-4f3d-81aa-87f6ca3fbf96" />

Plug it in while creating virtual machine 



And run the Virtual Machine

###3.2 Tools Setup
Open terminal.

#### Yosys:
'''bash
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

#### Iverilog:
Steps to install iverilog
sudo apt-get update
sudo apt-get install iverilog

#### Gtkwave
Steps to install gtkwave
sudo apt-get update
sudo apt install gtkwave

## 4.Lecture Summary
Custom Processor Design Workflow
Below is the description of the end-to-end workflow for designing a custom processor chip, from validating your application to silicon fabrication and board bring-up.

### Workflow Steps
1. Application Validation
Compile the target application with GCC and verify the output.
Ensure the application behaves as expected before proceeding.

2. Specification Modeling in C
Model the processor’s specifications in a C environment.
Test the application on this model and confirm outputs match expectations.
Freeze the specifications once verified.

3. RTL (HDL) Implementation
Implement processor specs in Verilog as a “soft copy” of the hardware.
Simulate the Verilog and C models to confirm matching outputs.

4. Modular RTL Structure
Divide Verilog into processor core and separate peripheral/IP blocks.
Ensure processor and macro blocks are synthesizable.
Analog IPs need to functionally simulate as needed.

5. GPIO Integration & I/O Testing
Integrate GPIO logic and validate at the I/O level.

7. Physical (Transistor-Level) Design
Convert RTL to a transistor-level netlist.
Generate a GDSII file with metal and layer info for fabrication.

8. Tapeout and Fabrication
Conduct final checks and submit GDSII for manufacturing (tapeout/tapein).
Obtain fabricated silicon (chipset).

9. Board Bring-Up & Validation
Mount the chip on a custom board.
Run the validated application on the board, matching all previously measured outputs.

10. Target Applications
Designed for 100–130 MHz operation—ideal as an Arduino replacement or controller in low-frequency devices (TVs, ACs, etc).









