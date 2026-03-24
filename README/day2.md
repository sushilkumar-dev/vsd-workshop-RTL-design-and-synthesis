# day2 - Timing libs, hierarchical vs flat synthesis and efficient flop coding styles

## 2.1 Introducton to timing .lib

The file `sky130_fd_sc_hd__tt_025C_1v80.lib` is a standard cell library used during synthesis to provide timing, power, and area information of available hardware cells.

It helps the synthesis tool map RTL code into real gates (like AND, OR, MUX, flip-flops) under typical conditions (tt), 25°C temperature, and 1.8V supply.

