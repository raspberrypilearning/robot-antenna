## Make the antenna flash with code

Now you have an antenna that lights up, let's write a program to tell the LED when to turn on and off.

+  Shut your Raspberry Pi down and remove the power cable.

+ Move the jumper wire that is connected to the resistor from the **3V3** pin to the pin which is labelled **17** in the diagram below:

![Pin 17](images/finished-circuit.png)

**Pin 17** is different to **3V3**: you can program it to switch the power on and off.

+ Power on your Raspberry Pi and wait for it to boot.

+ Open Scratch 2 by clicking on the menu and then **Programming**, followed by **Scratch 2**.

![Open Scratch 2](images/open-scratch2.png)

+ Right-click on the Scratch cat and choose **delete** from the menu.

- Click on the button for a new sprite and choose a robot from the **fantasy** folder, or, if you prefer, you can draw your own robot.

[[[generic-scratch-sprite-from-library]]]

- Click on **Events**. Drag the `when space key pressed`{:class="blockevents"} block into the Scripts area.

+ Click on **Sound**, drag the `play sound`{:class="blocksound"} block into the Scripts area and connect it to the previous block.

```blocks
when [space v] key pressed
play sound [ v]
```

+ Add a sound for your robot. We chose the computer beeps from the **electronic** section.

[[[generic-scratch-sound-from-library]]]

-  Go back to the Scripts tab. Click on the drop-down box in your `play sound`{:class="blocksound"} block and select the sound you just added.

- Test that your program is working so far by pressing the **space** key. In response, your robot should beep!

- Save your work by clicking **File**, then **Save project**, and call it `robot.sb2`.

Now let's program the LED to flash.

+ Enable the Pi GPIO extension. This will give you some extra blocks for programming the LED.

[[[rpi-scratch-add-pi-gpio]]]

+ Select **More blocks** and then drag this block to the bottom of your script:

```blocks
set gpio () to [output high v] :: extension
```

This block allows you to specify a GPIO pin, and whether it is on `[output high]` or off `[output low]`.

+ Type `17` into the circle to specify pin 17, and leave the drop-down on `high`. This block will turn your LED on.

+ Add a `wait 1 secs`{:class="blockcontrol"} block.

+ Now add another `set gpio` block, but this time ask it to set GPIO pin 17 to `low`.

--- hints ---
--- hint ---
Here is how your code should look:

```blocks
when [space v] key pressed
play sound [computer beeps v]
set gpio (17) to [output high v] :: extension
wait (1) secs
set gpio (17) to [output low v] :: extension
```
--- /hint ---
--- /hints ---


- Test your program by pressing the **space** key. You should see the LED turn on for a second and then turn off, and your robot should beep.
