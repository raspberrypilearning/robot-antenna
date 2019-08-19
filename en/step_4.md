## Make the antenna flash with code

Now you have an antenna that lights up, let's write a program to tell the LED when to turn on and off.

--- task ---

Shut your Raspberry Pi down and remove the power cable.

![Shut down](images/shut-down.png)

--- /task ---

--- task ---

Move the jumper wire that is connected to the resistor from the **3V3** pin to the pin which is labelled **17** in the diagram below:

![Pin 17](images/finished-circuit.png)

**Pin 17** is different to **3V3**: you can program it to switch the power on and off.

--- /task ---

--- task ---

Power on your Raspberry Pi and wait for it to boot.

--- /task ---

--- task ---

Open Scratch 2 by clicking on the menu and then **Programming**, followed by **Scratch 2**.

![Open Scratch 2](images/open-scratch.png)

--- /task ---

--- task ---

Remove the Scratch cat by right-clicking on it and choosing **delete** from the menu.

![scratch cat sprite with delete selected in the pop up menu ](images/delete-sprite.png)

--- /task ---

--- task ---

Click on the button for a new sprite and choose a robot from the **fantasy** folder, or, if you prefer, you can draw your own robot.

[[[generic-scratch-sprite-from-library]]]

--- /task ---

--- task ---

Click on **Events**. Drag the `when space key pressed`{:class="blockevents"} block into the Scripts area.

```blocks3
when [space v] key pressed
```

--- /task ---

--- task ---

Click on **Sound**, drag the `play sound`{:class="blocksound"} block into the Scripts area and connect it to the previous block.

```blocks3
when [space v] key pressed
+ play sound [ v]
```

--- /task ---

--- task ---

Add a sound for your robot. We chose the computer beeps from the **electronic** section.

[[[generic-scratch-sound-from-library]]]

--- /task ---

--- task ---

Go back to the Scripts tab. Click on the drop-down box in your `play sound`{:class="blocksound"} block and select the sound you just added.

```blocks3
when [space v] key pressed
+ play sound [computer beeps v]
```

--- /task ---

--- task ---

Test that your program is working so far by pressing the **space** key. In response, your robot should beep!

--- /task ---

--- task ---

Save your work by clicking **File**, then **Save project**, and call it `robot.sb3`.

--- /task ---

Now let's program the LED to flash.

--- task ---
Next add the *Raspberry Pi Simple Electronics* extension.

![add-extension](images/add-extension.png)
![simple-electronics](images/simple-electronics.png)
--- /task ---


--- task ---

Select **More blocks** and then drag this block to the bottom of your script:

```blocks3
turn LED (0 v) [on v] :: extension
```

This block allows you to specify a GPIO pin that your LED is wired to.

--- /task ---

--- task ---

Select `17` from the dropdown to specify pin 17, and leave the next drop-down as `on`. This block will turn your LED on.

```blocks
when [space v] key pressed
play sound [computer beeps v]
+ turn LED (0 v) [on v] :: extension
```

--- /task ---

--- task ---

Add a block to `wait 1 secs`{:class="blockcontrol"} from the control tab.

```blocks
when [space v] key pressed
play sound [computer beeps v]
turn LED (0 v) [on v] :: extension
+ wait (1) secs
```

--- /task ---

--- task ---

Now add another LED block, but this time ask it to set it to `off`.

```blocks
when [space v] key pressed
play sound [computer beeps v]
turn LED (0 v) [on v] :: extension
wait (1) secs
+ turn LED (0 v) [off v] :: extension

```

--- /task ---

--- task ---

Test your program by pressing the **space** key. You should see the LED turn on for a second and then turn off, and your robot should beep.

--- /task ---
