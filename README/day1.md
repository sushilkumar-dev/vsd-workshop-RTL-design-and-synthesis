# Day 1 - Introduction to Verilog RTL design and Synthesis

## 1.1 - Introduction to open-source simulator iverilog 

==> Introduction to iverilog, design Test Bench

#### Q1. What is simulator in verilog design ?
* RTL design is checked for adherence to the spec by simulating the design </br>
* Simulator is the tool used for simulating the design </br>
* iverilog is the tool used for this course </br>

#### Q2. What is design ?
* Design is the actual Verilog code or set of Verilog codes which has the intended functionality to meet with the required specifications 


#### Q3. What is TestBench ?
* TestBench is the setup to apply stimulus (test_vectors) to the design to check its functionality 


#### Q4. How simulator works ?
* Simulator looks for the changes on the input signals
* upon change to the input the output is evaluated
* if no change to the input, no change to the output!
* Simulator is looking for change in the values of input!

***

➤ The Below diagram represents the testbench generates input signals and applies them to the design, which produces corresponding outputs. These outputs are observed and verified, while the testbench itself has no external inputs or outputs.

<img width="471" height="298" alt="Screenshot from 2026-03-18 22-10-57" src="https://github.com/user-attachments/assets/c6151a45-8fa3-4187-b79c-68a1654fb1d8" /> </br> </br>



➤ The Below diagram represents the synthesized netlist and testbench are simulated using Icarus Verilog (iverilog) to generate a VCD waveform file. This VCD file is then viewed in GTKWave to verify that the synthesized design behaves correctly.

<img width="471" height="298" alt="Screenshot from 2026-03-18 22-12-31" src="https://github.com/user-attachments/assets/fade8d97-5d77-4b71-8255-851cb213926f" /></br> </br></br> </br>

***

## 1.2 - Labs using iverilog and GTKwave 

https://github.com/user-attachments/assets/ecf63020-c9f7-4971-9609-99f19b01198e

***
</br>

➤ Explaination of verilog code which we took for example in above tutorial video. </br></br></br>

<img width="471" height="298" alt="Screenshot from 2026-03-22 10-09-34" src="https://github.com/user-attachments/assets/98a8f399-607f-481d-ae9c-306afc44b0be" /> </br>

* The good_mux.v implements a 2:1 multiplexer where the output y selects between inputs i0 and i1 based on the select signal sel using combinational logic.</br></br>

<img width="471" height="498" alt="Screenshot from 2026-03-22 10-10-02" src="https://github.com/user-attachments/assets/b0424003-2c53-403e-8b03-d58baf744108" /></br>

* The tb_good_mux.v is a testbench that generates input stimulus, toggles signals over time, and produces a VCD waveform file to verify the functionality of the multiplexer.


***
## 1.3 - Introduction to yosys and logic synthesis.

➤ yosys is a Synthesizer </br>
* Tool used for converting the RTL to netlist </br>
* Yosys is the synthesizer used in this course </br>

</br>

<img width="471" height="298" alt="Screenshot from 2026-03-22 10-24-16" src="https://github.com/user-attachments/assets/d3b0b0ff-b44b-4f87-a43a-6cb2d7c72111" />

Yosys reads the Verilog design using `read_verilog` and the standard cell library using `read_liberty` to understand available hardware components.
It then synthesizes the design and generates a gate-level netlist using `write_verilog` based on the given library. </br></br>



<img width="471" height="298" alt="Screenshot from 2026-03-22 10-30-17" src="https://github.com/user-attachments/assets/384b940b-b0b1-4fae-85aa-364a1035fe64" />

The synthesized netlist and testbench are simulated using Icarus Verilog (iverilog) to generate a VCD waveform file.
This waveform is viewed in GTKWave to verify that the synthesized design matches the expected behavior. </br></br>

***

### Introduction to logic synthesis

 #### RTL design </br>
* is a Behavioral representation of the required specification 


<img width="471" height="298" alt="Screenshot from 2026-03-22 11-42-42" src="https://github.com/user-attachments/assets/635024e5-d16f-4f71-8408-8e0425175e12" />

In above image we have RTL code and we want hardware circuit with that code, then we need to map it. then the synthesis comes, the below image shows how code is converted into circuit which we call as netlist. if we want to convert code into netlist we have some popular libraries. </br>

<img width="471" height="298" alt="Screenshot from 2026-03-22 11-47-00" src="https://github.com/user-attachments/assets/2c4d53b2-82a1-40b3-9e51-10f7ae2986e0" /> </br> </br>

#### What is .lib </br>
 .lib </br>
- Collection of logical modules.
- includes basic logic gates like and, or, not etc...
- different flavors of same gates.
  
 #### Faster cells v/s Slower cells </br> 

* Faster cells are standard cells designed for high speed, giving quicker output transitions but usually consuming more power and area. </br>

* Slower cells are optimized for lower power and smaller area, but they take more time to produce outputs compared to faster cells. </br> </br>

* Faster cells have lower delay and produce outputs quickly.</br>
* Slower cells have higher delay and take more time. </br>
* Faster cells consume more power.</br>
* Slower cells consume less power.</br>
* Faster cells usually occupy more area, while slower cells are smaller.</br>

***

<img width="471" height="298" alt="Screenshot from 2026-03-22 19-24-36" src="https://github.com/user-attachments/assets/fb3df068-83e7-41b1-bc8d-b1a754c60eea" />

* The RTL code describes a multiplexer (using `assign`) and a flip-flop (using `always` block with clock and reset). During synthesis, this RTL is converted into a gate-level circuit using standard cells from the .lib and generated as a netlist.

















