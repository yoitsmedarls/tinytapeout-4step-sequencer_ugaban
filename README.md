![](../../workflows/gds/badge.svg) ![](../../workflows/docs/badge.svg) ![](../../workflows/wokwi_test/badge.svg) ![](../../workflows/fpga/badge.svg)

# 2-Channel 4-Step Hardware Sequencer

Designed by John Daryl Ugaban for the TinyTapeout IC Design Bootcamp.

## Description

This project is a hardware-based 4-step digital sequencer designed within the Wokwi editor. Built entirely using standard combinational and sequential logic gates, the circuit allows a user to program two separate 4-step sequences using 8 input switches. These sequences are then played back via two output channels synced to a master clock.

## How it Works

* **Playhead:** A 2-bit synchronous counter (built with D Flip-Flops, a NOT gate, and an XOR gate) tracks the current step (0 to 3). It increments on every clock pulse.
* **Data Selection:** Two sets of 4-to-1 multiplexer trees use the counter's 2-bit output to route the state of the input switches to the final output pins.

## How to Test

1. Program the desired sequence for **Channel 1** using input switches 1 to 4 (`IN0` - `IN3`).
2. Program the desired sequence for **Channel 2** using input switches 5 to 8 (`IN4` - `IN7`).
3. Pulse the clock input to advance the sequencer one step at a time.
4. Observe the active HIGH output states on `OUT0` (Channel 1) and `OUT1` (Channel 2).

## I/O Mapping

### Inputs
* **IN0 - IN3:** Step 1 to Step 4 programming for Channel 1.
* **IN4 - IN7:** Step 1 to Step 4 programming for Channel 2.
* **CLK:** Master clock input to advance the sequence.

### Outputs
* **OUT0:** Channel 1 output.
* **OUT1:** Channel 2 output.
* **OUT2 - OUT7:** Unused.

---

## What is Tiny Tapeout?

Tiny Tapeout is an educational project that aims to make it easier and cheaper than ever to get your digital and analog designs manufactured on a real chip.

To learn more and get started, visit [tinytapeout.com](https://tinytapeout.com).

## Resources

- [FAQ](https://tinytapeout.com/faq/)
- [Digital design lessons](https://tinytapeout.com/digital_design/)
- [Learn how semiconductors work](https://tinytapeout.com/siliwiz/)
- [Join the community](https://tinytapeout.com/discord)
- [Build your design locally](https://www.tinytapeout.com/guides/local-hardening/)
