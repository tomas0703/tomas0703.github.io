---
title: Logic Gates
---

AND Gate
Beginning on row 12 where the black arrow marks the initial current supply, current travels toward two push-buttons wired in series. When no buttons are pressed (0,0 input) or only one button is pressed (1,0 or 0,1), the series circuit remains broken, leaving current halted along the red trace and keeping the output at 0. Only when both buttons are pressed simultaneously (1,1 input) does the path complete along the green line, allowing current to pass through the pull-down resistor to energize the output rail (1).

OR Gate
Starting on row 18 at the main supply terminal indicated by the black arrow, current splits into two parallel branches, each equipped with a diode to prevent reverse current flow. With no buttons pressed (0,0 input), current cannot cross the open switches and dissipates along the neutral gray path to ground (0). Pressing either the first button (1,0), the second button (0,1), or both together (1,1) completes the circuit, directing current along the orange trace through the forward-biased diodes to power the output terminal (1).

NOT Gate (Inverter)
Beginning on row 25 at the positive supply rail marked by the black arrow, current naturally flows along the default green path directly to the output node, holding it HIGH (1) when no button is pressed (0 input). Pressing the input button (1 input) supplies base current to an NPN transistor, turning it on and creating a low-resistance short along the blue path directly to ground, which starves the output rail and drops it to LOW (0).

NAND Gate
Originating at row 31 where the black arrow designates incoming current, the path connects through a pull-up resistor straight to the output pin along the yellow trace. For inputs (0,0), (1,0), or (0,1), at least one of two series-connected transistors remains turned off, keeping the ground path blocked and maintaining a HIGH output (1). Only when both buttons are held down (1,1) do both transistors saturate, steering current down the red line to ground and pulling the output down to 0.

NOR Gate
Beginning at row 37 at the positive rail marked by the black arrow, current flows by default along the top purple path to the output terminal when both inputs are inactive (0,0 input), generating a HIGH signal (1). If either button (1,0 or 0,1) or both buttons (1,1) are pressed, the activated parallel transistors form a shortcut along the brown path to ground, draining the current and dropping the output to 0.

XNOR Gate
Starting on row 50 where the black arrow highlights the primary power line, current enters a dual-branch switching network. When neither button is pressed (0,0 input) or both buttons are pressed together (1,1 input), current flows unimpeded through the matched transistor pairs along the magenta path to drive the output HIGH (1). When only a single button is pressed (1,0 or 0,1), the cross-wired switches imbalance the network, steering current along the dark gray trace directly to ground and yielding a LOW output (0).
