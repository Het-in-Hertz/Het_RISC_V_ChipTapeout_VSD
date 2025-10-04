# Documentation
## Table of Content:
1. Acknowledgement 
2. Abstract
3. Part1: Soc and BabySoc Theory
4. Part2: Labs
   
## 1.Acknowledgments

I sincerely thank the entire VSD team for their unwavering support, expert guidance, and providing such an exceptional learning platform throughout this RISC-V Reference SoC Tapeout Program. Their dedication to fostering hands-on experience and advancing semiconductor education has been invaluable to my growth as an engineer.

I would also like to express my gratitude to all other involved professionals and institutions who made this program possible, including but not limited to IIT Gandhinagar, Prof. Rajat Moona, Mr.Sameer Patel, Efabless, and Mr. Muhammed Kasim. Their contributions and collaboration have greatly enriched this learning journey.

# 2.Abstract

## **Part 1: Theory (Conceptual Understanding) - Abstract**

This section establishes the theoretical foundation of System-on-Chip (SoC) design principles and explores how the BabySoC serves as an educational platform. The study examines the fundamental components of SoC architecture including processor cores, memory subsystems, input/output interfaces, and specialized processing units. Through comprehensive analysis of SoC design methodologies, this section demonstrates how BabySoC, comprising RVMYTH (RISC-V processor), 8x-PLL (clock generator), and 10-bit DAC (analog interface), provides a simplified yet complete representation of modern SoC systems. The theoretical framework emphasizes the critical role of functional modelling as a prerequisite to RTL implementation, highlighting its importance in early design validation, architectural exploration, and performance analysis. This conceptual understanding serves as the foundation for practical implementation and establishes BabySoC as an effective learning vehicle for understanding complex SoC design principles in an accessible format.

## **Part 2: Labs (Hands-on Functional Modelling) - Abstract**

This practical section implements functional modelling and simulation of the VSDBabySoC using industry-standard open-source tools including Icarus Verilog (iverilog) for compilation and GTKWave for waveform analysis. The laboratory work demonstrates the complete simulation workflow from source code compilation to behavioral verification through systematic steps: repository cloning, Verilog module compilation, simulation execution, and comprehensive waveform analysis. Key simulation aspects examined include reset operation timing, clock signal generation and distribution, and inter-module dataflow between the RVMYTH core, PLL, and DAC components. The hands-on experience provides practical validation of theoretical concepts through detailed waveform analysis, documenting critical signals such as CLK (PLL-generated clock), reset (system initialization), and OUT (DAC analog output). This laboratory work bridges the gap between conceptual understanding and practical implementation, demonstrating how functional modelling serves as a crucial verification step before proceeding to RTL synthesis and physical design stages.

---

# Lab Implementation Guide for VSDBabySoC Functional Modelling

## **Prerequisites Installation**

### **Step 1: Install Required Packages**



### **What is a System-on-Chip (SoC)?**

A System-on-Chip (SoC) is an integrated circuit that combines most or all key components of a computer or electronic system onto a single microchip[13]. It represents a high level of integration that minimizes the need for separate, discrete components, thereby enhancing power efficiency and simplifying device design[13].

An SoC integrates one or more processor cores with critical peripherals, delivering lower power consumption and reduced semiconductor die area compared to traditional multi-chip architectures[13]. This comprehensive integration is conceptually similar to how a microcontroller is designed, but providing far greater computational power[13].

---

### **Components of a Typical SoC**

#### **1. Processor Cores**
- The heart of the SoC, usually containing at least one or more coprocessors[10]
- Can be microcontrollers, microprocessors, or Digital Signal Processors (DSPs)[10]
- ARM architecture is a common choice for SoC processor cores[13]

#### **2. Memory Subsystem**
- **Volatile Memory**: RAM (SRAM and DRAM)[10]
- **Non-volatile Memory**: ROM, EEPROM, and flash memory[10][13]
- Forms memory hierarchy and cache hierarchy for optimal performance[13]

#### **3. Input/Output Interfaces**
- GPIO (General Purpose Input/Output)
- Communication interfaces: USB, SPI, I2C, UART[16]
- Connectivity modules: Bluetooth, Wi-Fi, Ethernet[16]

#### **4. Specialized Processing Units**
- **GPU (Graphics Processing Unit)**: For image processing and visualization[10]
- **DSP**: For signal processing operations and data collection[10]
- **Encoder/Decoder**: For information interpretation and conversion[10]

#### **5. Peripheral Components**
- Network Interface Cards for system connectivity[10]
- Power Management Units
- Clock generation circuits (PLLs)
- ADC/DAC converters[10]

---

### **Why BabySoC is a Simplified Model for Learning SoC Concepts**

BabySoC serves as an educational platform that demonstrates fundamental SoC design principles in a simplified, manageable format[29]. Here's why it's ideal for learning:

#### **Educational Focus**
- **Manageable Complexity**: BabySoC contains only essential components, making it easier to understand the interactions between different IP blocks[29]
- **Open-Source Design**: All components are open-source and well-documented, allowing students to examine the complete design flow[29]
- **Real Implementation**: Despite being simplified, it represents a complete SoC that can be fabricated using Sky130 technology[29]

#### **Core Components of BabySoC**
1. **RVMYTH**: A RISC-V based processor core that executes instructions[29]
2. **8x-PLL**: Generates stable clock signals for the system[29]
3. **10-bit DAC**: Provides interface to communicate with analog devices[29]

#### **Learning Objectives**
- Understanding how different IP cores interact within an SoC[29]
- Learning the complete design flow from RTL to GDSII[29]
- Practicing mixed-signal design concepts with both digital and analog components[29]

---

### **The Role of Functional Modelling Before RTL and Physical Design Stages**

Functional modelling is a crucial preliminary step that occurs before detailed RTL implementation and serves several critical purposes[11][20]:

#### **Purpose and Benefits**

##### **1. Early Design Validation**
- Validates system behavior against specifications before investing in detailed RTL coding[20]
- Helps identify and correct functional mismatches early in the design cycle[9]
- Reduces risk of propagating errors to later stages[9]

##### **2. Architectural Exploration**
- Allows designers to conceptualize system behavior through algorithms and data flow[11]
- Enables exploration of different architectural approaches[11]
- Provides abstract representation for initial system verification[11]

##### **3. Performance Analysis**
- Enables early performance estimation and optimization[14]
- Helps identify potential bottlenecks in system architecture[14]
- Supports architectural co-design decisions[13]

#### **Functional Modelling in BabySoC Context**

For BabySoC, functional modelling involves[29]:
- **System-level simulation** using tools like Icarus Verilog and GTKWave
- **Component interaction verification** between RVMYTH, PLL, and DAC
- **Signal flow analysis** from clock generation through processing to analog output
- **Behavioral verification** before synthesis and physical implementation

#### **Design Flow Integration**

The functional modelling stage bridges the gap between[11][20]:
- **High-level specifications** (written in natural language or high-level models)
- **RTL implementation** (detailed hardware description in Verilog/VHDL)
- **Physical design** (gate-level netlist and layout generation)

This approach ensures that the fundamental system behavior is correct before proceeding to more resource-intensive RTL design and physical implementation phases[11][20].

---

### **Conclusion**

Understanding SoC fundamentals through BabySoC provides a solid foundation for complex system design. The simplified yet complete nature of BabySoC allows students to grasp essential concepts like component integration, signal flow, and mixed-signal design. Functional modelling serves as a critical validation step that ensures design correctness before moving to detailed RTL implementation, ultimately saving time and resources in the overall design process.

The combination of theoretical understanding and practical implementation using simulation tools like Icarus Verilog and GTKWave prepares students for real-world SoC design challenges while providing hands-on experience with industry-standard design methodologies.
