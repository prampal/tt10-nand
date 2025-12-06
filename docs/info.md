<!---

This file is used to generate your project datasheet. Please fill in the information below and delete any unused
sections.

You can also include images in this folder and reference them in the markdown. Each image must be less than
512 kb in size, and the combined size of all images must be less than 1 MB.
-->

## How it works

A NAND gate implements the logical negation of an AND operation. Its symbol is an AND gate followed by a small inversion bubble, indicating the NOT action. The diagram represents the logical behavior of the NAND function.

To begin, we define the module. In Verilog, module is the keyword used to declare a design block, and NAND_2 is the identifier for this particular module. The list of signals inside the parentheses forms the port list, which specifies the module’s inputs and outputs.

Inside the module, we introduce additional internal connections as needed: wire Yd;

A wire represents a signal line that is driven by another source. Since Yd is only used internally, it does not appear in the module’s port list.

The logic is built using Verilog’s built-in primitives:
and(Yd, A, B);
not(Y, Yd);

The AND gate processes inputs A and B, producing an intermediate result in Yd. The NOT gate then inverts this value to generate the final output Y. The endmodule keyword marks the conclusion of the module.

## How to test

Simulate the design and verify that the outputs match the standard truth table for a NAND gate.

NAND Truth Table

Inputs| Outputs A | B | Y 0 0 1 0 1 1 1 0 1 1 1 0

## External hardware

List external hardware used in your project (e.g. PMOD, LED display, etc), if any

No External Hardware Used
