## Connect your antenna

Now let's connect the antenna to the Raspberry Pi to make a **circuit**.

Make sure your Raspberry Pi is switched off.

--- task ---

Turn your Raspberry Pi so that it is facing the same way as the one in the diagram below:

![The GPIO pins](images/gpio.png)

--- /task ---

Look at the pins which are sticking out of the top right of your Raspberry Pi. These pins let the Raspberry Pi communicate with the outside world.

--- task ---

Take the jumper wire that is connected to the resistor and plug it onto the pin labelled **3V3** on the diagram. This pin provides power to the LED, so it's rather like connecting the LED to the positive side of a battery.

--- /task ---

--- task ---

Take the jumper wire that is connected to the short leg of the LED and plug it onto the pin labelled **GND** on the diagram. This pin provides grounding to the LED, like connecting it to the negative side of a battery would do.

--- /task ---

When you have plugged in both wires, you have a circuit.

--- task ---

Power on your Raspberry Pi, and your LED should switch on. If it is not, make sure that you have plugged the jumper wires into the correct pins by checking the diagram above.

--- /task ---

--- collapse ---
---
title: Why does the LED shine?
---
When the circuit is plugged into the Raspberry Pi pins, electricity can flow through it. This flow is called the current. The LED only lights up when electric current flows from the long leg to the short leg.

The resistor reduces the amount of electric current passing through the circuit. This protects the LED from breaking, as a high current would make the light shine more brightly and then stop working.

--- /collapse ---
