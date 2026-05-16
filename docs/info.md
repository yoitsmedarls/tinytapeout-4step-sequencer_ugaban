<!---

This file is used to generate your project datasheet. Please fill in the information below and delete any unused
sections.

You can also include images in this folder and reference them in the markdown. Each image must be less than
512 kb in size, and the combined size of all images must be less than 1 MB.
-->

## How it works

This project is a hardware-based 4-step digital sequencer. A 2-bit synchronous counter tracks the current step (0 to 3) and increments on every clock pulse. Two sets of 4-to-1 multiplexers use this counter to route the state of the input switches to the final output pins, allowing for two separate programmed sequences.

## How to test

1. Set the desired sequence for Channel 1 using input switches 1-4.
2. Set the desired sequence for Channel 2 using input switches 5-8.
3. Pulse the clock input to advance the sequencer one step at a time.
4. Observe the output states on OUT0 (Channel 1) and OUT1 (Channel 2).

## External hardware

Two LEDs connected to OUT0 and OUT1 to visualize the sequence outputs.
