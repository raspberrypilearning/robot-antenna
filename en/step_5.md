## Make the antenna flash with code

Now you have an antenna that lights up, let's write a program to tell the LED when to turn on and off.

+  Shut your Raspberry Pi down and remove the power cable.

+ Move the jumper wire that is connected to the resistor from the 3V3 pin to GPIO pin 17 which is labelled in the diagram below:

![Pin 17](images/finished-circuit.png)

GPIO pin 17 is special as you can program it to switch the power on and off.

+ Power on your Raspberry Pi and wait for it to boot.

+ Open Scratch 2 by clicking on **Menu** and **Programming**, followed by **Scratch 2**.

![Open Scratch 2](images/open-scratch2.png)

+ Enable the Pi GPIO extension

[[[rpi-scratch-add-pi-gpio]]]

+ Right-click on the Scratch cat and choose **delete** from the menu.

- Click on the button for a new sprite and choose a robot from the **fantasy** folder, or if you prefer you could draw your own robot.

[[[generic-scratch-sprite-from-library]]]


- Click on **Events**. Drag the `when space key pressed` block onto the scripts area.

+ Click on **Sound** and drag the `play sound` block onto the scripts area and connect it to the previous block.

![When space](images/when-space.png)

+ Add a sound for your robot. We chose the computer beeps from the **electronic** section.

[[[generic-scratch-sound-from-library]]]

-  Go back to the scripts area. Click on the drop down box next to play sound and select the sound you just imported.

- Test that your program so far is working by pressing space key. Your robot should beep!

- Save your work by clicking **File** then **Save project** and call it `robot.sb2`.

Now let's make ...

- Drag a `wait 1 second` block onto the scripts area and connect it to the broadcast block.

- Test your program by clicking on the robot sprite. You should see the LED shine and stay on.

- Drag another `broadcast` block onto your scripts area and connect it to the wait 1 second block. Click on the drop down menu on the broadcast block and select **new**.

    In the message name box type `gpio17off` This will switch off the LED.

- Now add another `wait 1 second` block to the script.

- Test your program again by clicking on the robot sprite. You should see the LED turn on for one second and turn off for one second.

    ![](images/pin17-on-off.png "Turn pin 17 off")
