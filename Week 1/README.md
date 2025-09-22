# Documentation
## Table of Content:
1. Acknowledgement 
2. Abstract
3. Day 1
4. Day 2
5. Day 3
6. Day 4
7. Day 5
   
## 1.Acknowledgments

I sincerely thank the entire VSD team for their unwavering support, expert guidance, and providing such an exceptional learning platform throughout this RISC-V Reference SoC Tapeout Program. Their dedication to fostering hands-on experience and advancing semiconductor education has been invaluable to my growth as an engineer.

I would also like to express my gratitude to all other involved professionals and institutions who made this program possible, including but not limited to IIT Gandhinagar, Prof. Rajat Moona, Mr.Sameer Patel, Efabless, and Mr. Muhammed Kasim. Their contributions and collaboration have greatly enriched this learning journey.

## 2.Abstract


## 3.Day 1

### Iverilog and GTKwave

<img width="1055" height="500" alt="image" src="https://github.com/user-attachments/assets/611fe149-e9e4-4e8a-b670-8fb345b47ebc" />

RTL design is the simulation of the given specs for a hardware on a simulator;here iverilog. A file or a set of file contains the verilog code. To check if the design is obeying the required specs a stimulus is applied through testbench(test vectors) and output is observed.Every change in input re-evaluates the output.
With the help of Iverilog simulation is carried out by inputing test vectors to a design file and a .vcd file is generated. GTKwave is used to visualize the .vcd file. 

### Day 1 Lab 1(Exploring files)
Cloning a folder from github

<img width="1172" height="771" alt="image" src="https://github.com/user-attachments/assets/d40722d6-109c-45e8-a3bd-ec25eed242aa" />

inside the folder cloned from github

<img width="787" height="46" alt="image" src="https://github.com/user-attachments/assets/c1b59eb1-dd9e-4b8c-860d-aa8aeb03e966" />

inside verilog_files

<img width="1709" height="441" alt="image" src="https://github.com/user-attachments/assets/f9666ff5-5d15-4af8-9cb9-6ccb50931c90" />

inside lib

<img width="802" height="43" alt="image" src="https://github.com/user-attachments/assets/a6f15a1a-06e5-4c3a-b175-f287f7eb0b3b" />

inside my_lib

<img width="868" height="48" alt="image" src="https://github.com/user-attachments/assets/dc1f46bc-a8b0-4595-b9d0-5ee97c0fff6c" />

inside verilog_models

<img width="976" height="43" alt="image" src="https://github.com/user-attachments/assets/6bf1670b-3cdd-4ecc-bb9a-bca5ad9b3692" />

### Day 1 lab 2 (Opening designs  testbench and using verilog and gtkwave)

Each file in verilog_files has tb_file_name.v and corresponding file_name.v.

The following command invokes iverilog and simulates resulting in a a.out file
<img width="1233" height="25" alt="image" src="https://github.com/user-attachments/assets/5194c898-427d-421e-b85f-7b5215d4bcef" />

<img width="1772" height="421" alt="image" src="https://github.com/user-attachments/assets/f67a5dcc-e356-493e-8ceb-ea6dd5706a0c" />

We execute the a.out file and a .vcd file is dumped.

<img width="997" height="67" alt="image" src="https://github.com/user-attachments/assets/478beadf-e4dd-4b05-a177-ec7a9d23652b" />

Gtkwave is used to plot the information in vcd file

<img width="1124" height="145" alt="image" src="https://github.com/user-attachments/assets/20439c20-fd9b-413a-b64d-8f45d0670194" />

Following is the output of the gtk command. To get a perfect output use the zoom to fit option in gtk.

<img width="1003" height="661" alt="image" src="https://github.com/user-attachments/assets/95a7137a-6fd7-449a-b291-5c38adc170e5" />

To check what is written in file we check using gvim tb_good_mux.v -o good_mux.v to open the design of  mux and corrresponding testbench

<img width="1491" height="762" alt="image" src="https://github.com/user-attachments/assets/6c354921-b9e7-467b-97b6-6b97692eb1eb" />

 ### Yosys

<img width="1819" height="481" alt="image" src="https://github.com/user-attachments/assets/370d420f-fce7-4e2e-b021-ae3f6578e85c" />
  
 Yosys is a synthesizer that converts RTL into Netlist i.e. CMOS or interconnects level.In yosys read_verilog reads the design and read_liberty reads the library and finally a write_verilog writes out the netlist file. This netist is the representation of design in form of standard cells. To verify the synthesis(i.e no change in design after netlist conversion) we run the netlist file in Iverilog using the same testbench. Both design and netlist output must be same.

 #### Logic synthesis


 ### Day 1 Lab3(Intro to Yosys)
 First step is to invoke yosys by 
<img width="935" height="758" alt="image" src="https://github.com/user-attachments/assets/439ef466-9f90-417e-b42b-ef27778d44ca" />
<img width="724" height="736" alt="image" src="https://github.com/user-attachments/assets/c8454f0f-4b3e-4894-a8b7-a5f0126a377a" />
<img width="1897" height="271" alt="image" src="https://github.com/user-attachments/assets/de459ea8-6c2b-448e-8f67-4fccf736569b" />
<img width="1488" height="706" alt="image" src="https://github.com/user-attachments/assets/5407279f-1171-4720-95b8-3f58f4dd3f5c" />
<img width="921" height="878" alt="image" src="https://github.com/user-attachments/assets/078a3965-31e0-4290-8db5-190fcfb90634" />
<img width="1236" height="296" alt="image" src="https://github.com/user-attachments/assets/8ef932fc-e2e6-4840-9358-057e6dc325fd" />
<img width="346" height="84" alt="image" src="https://github.com/user-attachments/assets/2c37ef41-b057-455b-9d09-fd1a35bf19d0" />
<img width="503" height="317" alt="image" src="https://github.com/user-attachments/assets/fcd29c4b-9d7f-4ffa-b7db-ea927763c566" />
<img width="1129" height="47" alt="image" src="https://github.com/user-attachments/assets/47242697-e56b-4f2a-acb2-b035ea7fc3f6" />
<img width="1129" height="47" alt="image" src="https://github.com/user-attachments/assets/b407fe13-f7ce-4ef3-8416-6795710fd5b9" />
<img width="614" height="154" alt="image" src="https://github.com/user-attachments/assets/4888590e-6f79-4834-b543-2353b1604853" />
<img width="165" height="51" alt="image" src="https://github.com/user-attachments/assets/cd3cd8a7-58a6-41e5-be14-4c7f57084d1c" />











