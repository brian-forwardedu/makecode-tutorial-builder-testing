# Solar Sensor Loop


```package
all-fwd-blocks=github:forward-education/pxt-all-fwd-blocks#v2.0.1
```


## @showdialog

Welcome! In this tutorial, you will use a loop to read the light level from a solar sensor over and over again. The micro:bit will show you the light level on its screen as a number.

## Step 1

Find the ``||basic: on start||`` block. It is already in your workspace. We will not use it right now, so leave it empty.

## Step 2

Open the ``||basic: Basic||`` drawer and find the ``||basic: forever||`` block. Drag it into the workspace. Code inside this block runs in a loop, over and over again.

## Step 3

Open the ``||fwdSensors: fwdSensors||`` drawer. Find the ``||fwdSensors: solar1 light level (%)  ||`` block. This block reads the current light level from the solar sensor.

## Step 4

Open the ``||basic: Basic||`` drawer and find the ``||basic: show number 0||`` block. Drag it inside the ``||basic: forever||`` block.

## Step 5

Go back to the ``||fwdSensors: fwdSensors||`` drawer and drag the ``||fwdSensors: solar1 light level (%)  ||`` block into the number slot of the ``||basic: show number||`` block. Now the micro:bit will display the solar sensor reading each time through the loop.

## Step 6

Open the ``||basic: Basic||`` drawer and find the ``||basic: pause (ms) 100||`` block. Drag it inside the ``||basic: forever||`` block, just below the ``||basic: show number||`` block. Change the pause time to **500** ms. This slows the loop down so the numbers are easier to read.

## Step 7

Look at the simulator on the left. You should see a number scrolling across the micro:bit display. Try sliding the solar sensor slider in the simulator to change the light level. Watch the number change!

## Step 8

When you are ready, click the **Download** button to send your program to the micro:bit. Hold the solar sensor up to a light source and watch the number change on the display.

## @showdialog

Great work! You used a forever loop to read the solar sensor again and again, and displayed the light level on the micro:bit. Try using an if block next to make something happen when the light gets bright or dim!
