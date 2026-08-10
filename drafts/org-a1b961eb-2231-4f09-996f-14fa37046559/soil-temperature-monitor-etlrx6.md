# Soil Temperature Monitor


```package
all-fwd-blocks=github:forward-education/pxt-all-fwd-blocks#v2.0.1
```


## @showdialog

Welcome to the Soil Temperature Monitor!

In this tutorial, you will use the temperature sensor from the Coding for Good Kit to read soil temperature and display a warning when the temperature is too high or too low.

## Step 1

First, open the ``||basic:Basic||`` drawer and find the ``||basic:on start||`` block. It should already be in your workspace.

We will use it to show a message when the program begins.

## Step 2

Find the ``||basic:show string " "||`` block inside the ``||basic:Basic||`` drawer. Place it inside ``||basic:on start||``.

Change the text to say **"Soil Temp"**.

```blocks
basic.showString("Soil Temp")
```

## Step 3

Now open the ``||basic:Basic||`` drawer and drag a ``||basic:forever||`` block into the workspace. This block will keep checking the temperature over and over.

## Step 4

Open the ``||logic:Logic||`` drawer and find the ``||logic:if true then / else||`` block. Place it inside the ``||basic:forever||`` block.

```blocks
basic.forever(function () {
    if (true) {
    } else {
    }
})
```

## Step 5

Now we need to check the temperature. Open the ``||fwdSensors:fwdSensors||`` drawer and find the ``||fwdSensors:temperature1 temperature (°C)||`` value block.

Open the ``||logic:Logic||`` drawer and find a ``||logic:0 < 0||`` comparison block. Place it in the **if** slot.

Put the ``||fwdSensors:temperature1 temperature (°C)||`` block on the left side. Change the operator to **>** and set the right side to **30**.

This checks if the soil is too hot (above 30°C).

```blocks
basic.forever(function () {
    if (fwdSensors.temperature1.temperature() > 30) {
    } else {
    }
})
```

## Step 6

If the soil is too hot, we want to show a warning. Open the ``||basic:Basic||`` drawer and find ``||basic:show icon||``. Place it inside the **if** section. Choose the **Skull** icon as a danger warning.

```blocks
basic.forever(function () {
    if (fwdSensors.temperature1.temperature() > 30) {
        basic.showIcon(IconNames.Skull)
    } else {
    }
})
```

## Step 7

Now add an **else if** check for temperatures that are too cold. Click the **+** button on the ``||logic:if||`` block to add an **else if** section.

Add another ``||fwdSensors:temperature1 temperature (°C)||`` comparison block. Set it to check if the temperature is **< 10** (too cold).

```blocks
basic.forever(function () {
    if (fwdSensors.temperature1.temperature() > 30) {
        basic.showIcon(IconNames.Skull)
    } else if (fwdSensors.temperature1.temperature() < 10) {
    } else {
    }
})
```

## Step 8

If the soil is too cold, show a different warning. Open the ``||basic:Basic||`` drawer and add a ``||basic:show icon||`` block in the **else if** section. Choose the **Sad** icon.

```blocks
basic.forever(function () {
    if (fwdSensors.temperature1.temperature() > 30) {
        basic.showIcon(IconNames.Skull)
    } else if (fwdSensors.temperature1.temperature() < 10) {
        basic.showIcon(IconNames.Sad)
    } else {
    }
})
```

## Step 9

When the temperature is just right, show the reading on the screen. Open the ``||basic:Basic||`` drawer and find ``||basic:show number 0||``. Place it in the **else** section.

Open the ``||fwdSensors:fwdSensors||`` drawer and drag ``||fwdSensors:temperature1 temperature (°C)||`` into the number slot.

```blocks
basic.forever(function () {
    if (fwdSensors.temperature1.temperature() > 30) {
        basic.showIcon(IconNames.Skull)
    } else if (fwdSensors.temperature1.temperature() < 10) {
        basic.showIcon(IconNames.Sad)
    } else {
        basic.showNumber(fwdSensors.temperature1.temperature())
    }
})
```

## Step 10

Open the ``||basic:Basic||`` drawer and add a ``||basic:pause (ms) 100||`` block at the bottom of the ``||basic:forever||`` block, after the if statement. Change the value to **1000** ms so the display updates every second.

```blocks
basic.forever(function () {
    if (fwdSensors.temperature1.temperature() > 30) {
        basic.showIcon(IconNames.Skull)
    } else if (fwdSensors.temperature1.temperature() < 10) {
        basic.showIcon(IconNames.Sad)
    } else {
        basic.showNumber(fwdSensors.temperature1.temperature())
    }
    basic.pause(1000)
})
```

## Step 11

Look at the simulator on the left. Try moving the temperature slider for the temperature sensor up and down. Watch the display change between the temperature number and warning icons.

When you are happy with how it works, click **Download** to send the program to your micro:bit. Then plug in your temperature sensor and push the probe into the soil!

## @showdialog

Great work! You have built a soil temperature monitor.

Your micro:bit now shows the soil temperature when conditions are normal, a sad face when the soil is too cold (below 10°C), and a skull when the soil is too hot (above 30°C). Try adjusting the temperature thresholds to suit the plants you are monitoring!
