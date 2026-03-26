# day2 - Timing libs, hierarchical vs flat synthesis and efficient flop coding styles

## 2.1 Introducton to timing .lib

The file `sky130_fd_sc_hd__tt_025C_1v80.lib` is a standard cell library used during synthesis to provide timing, power, and area information of available hardware cells.

It helps the synthesis tool map RTL code into real gates (like AND, OR, MUX, flip-flops) under typical conditions (tt), 25°C temperature, and 1.8V supply.

## 2.2 Hier synthesis and flat synthesis

* Hierarchical synthesis is a method where each module is synthesized separately while preserving the design hierarchy, making it easier to manage and debug large designs.

* Flat synthesis combines all modules into a single level by removing hierarchy, allowing better optimization but making the design harder to analyze and debug.

## Why Flops and Flop coding styles 

* Flip-flops (flops) are used to store data and synchronize signals with a clock, making them essential for designing sequential circuits.

* Example code:


