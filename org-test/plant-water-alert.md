
# Plant Water Alert


```package
all-fwd-blocks=github:forward-education/pxt-all-fwd-blocks#v2.0.1
```


## @showdialog

Welcome! In this tutorial, you will use a moisture sensor to check if a plant needs water.
When the soil is too dry, the micro:bit will show a warning so you know it is time to water your plant.

## Step 1 - Set up a forever loop

Find the ``||basic: forever||`` block. It should already be on your workspace.
Your code will go inside this block so it keeps checking the soil again and again.

## Step 2 - Read the moisture sensor

Inside the ``||basic: forever||`` block, add an ``||logic: if then else||`` block from the ``||logic: Logic||`` drawer.

```blocks
basic.forever(function () {
    if (true) {
    } else {
    }
})
```

## Step 3 - Add the moisture condition

Click the ``||fwdSensors: fwdSensors||`` drawer and find the ``||fwdSensors: moisture level||`` block.
Place it into the left side of a ``||logic: less than ( < )||`` comparison block, then set the right side to **25**.
Put this whole comparison into the **if** condition.

This means: "if the soil moisture is below 25, the soil is too dry."

```blocks
basic.forever(function () {
    if (fwdSensors.moisture1.moistureLevel() < 25) {
    } else {
    }
})
```

## Step 4 - Show a warning when dry

Inside the **if** section, add a ``||basic: show icon||`` block from the ``||basic: Basic||`` drawer.
Choose the **Sad** face icon to warn that the plant needs water.

```blocks
basic.forever(function () {
    if (fwdSensors.moisture1.moistureLevel() < 25) {
        basic.showIcon(IconNames.Sad)
    } else {
    }
})
```

## Step 5 - Show all is well when moist

Inside the **else** section, add another ``||basic: show icon||`` block.
Choose the **Happy** face icon to show the plant has enough water.

```blocks
basic.forever(function () {
    if (fwdSensors.moisture1.moistureLevel() < 25) {
        basic.showIcon(IconNames.Sad)
    } else {
        basic.showIcon(IconNames.Happy)
    }
})
```

## Step 6 - Add a pause

After the ``||logic: if then else||`` block, add a ``||basic: pause (ms) 100||`` block from the ``||basic: Basic||`` drawer.
Change the value to **1000** so the micro:bit checks the moisture once every second.

```blocks
basic.forever(function () {
    if (fwdSensors.moisture1.moistureLevel() < 25) {
        basic.showIcon(IconNames.Sad)
    } else {
        basic.showIcon(IconNames.Happy)
    }
    basic.pause(1000)
})
```

## Step 7 - Test in the simulator

Look at the simulator on the left side of the screen.
Try moving the moisture slider up and down to see the happy and sad faces change.
Does the sad face appear when the moisture is low?

## Step 8 - Download to your micro:bit

Connect your micro:bit and your Climate Action Kit moisture sensor.
Click the **Download** button to send your program to the micro:bit.
Push the sensor into some soil and watch the display to see if your plant needs water!

## @showdialog

Great work! You built a plant watering alert using a moisture sensor.
Your micro:bit will now keep watch over your plant and let you know when it is thirsty.
