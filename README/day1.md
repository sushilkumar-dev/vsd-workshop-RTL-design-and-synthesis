# Day 1 - Introduction to Verilog RTL design and Synthesis

## 1.1 - Introduction to open-source simulator iverilog 

==> Introduction to iverilog, design Test Bench

#### Q1. What is simulator in verilog design ?
• RTL design is checked for adherence to the spec by simulating the design </br>
• Simulator is the tool used for simulating the design </br>
      • iverilog is the tool used for this course </br>

#### Q2. What is design ?
• Design is the actual Verilog code or set of Verilog codes which has the intended functionality to meet with the required specifications 


#### Q3. What is TestBench ?
• TestBench is the setup to apply stimulus (test_vectors) to the design to check its functionality 


#### Q4. How simulator works ?
• Simulator looks for the changes on the input signals
•upon change to the input the output is evaluated
    •if no change to the input, no change to the output!
• Simulator is looking for change in the values of input!

***

➤ The Below diagram represents the testbench generates input signals and applies them to the design, which produces corresponding outputs. These outputs are observed and verified, while the testbench itself has no external inputs or outputs.

<img width="471" height="298" alt="Screenshot from 2026-03-18 22-10-57" src="https://github.com/user-attachments/assets/c6151a45-8fa3-4187-b79c-68a1654fb1d8" /> </br> </br>



➤ The Below diagram represents the synthesized netlist and testbench are simulated using Icarus Verilog (iverilog) to generate a VCD waveform file. This VCD file is then viewed in GTKWave to verify that the synthesized design behaves correctly.

<img width="471" height="298" alt="Screenshot from 2026-03-18 22-12-31" src="https://github.com/user-attachments/assets/fade8d97-5d77-4b71-8255-851cb213926f" /></br> </br></br> </br>

***

## 1.2 - Labs using iverilog and GTKwave 




