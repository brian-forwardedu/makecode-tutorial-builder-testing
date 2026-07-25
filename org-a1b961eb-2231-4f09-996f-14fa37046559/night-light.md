
# Night Light

## @showdialog

Welcome! In this tutorial you will build a night light.
The micro:bit will check how bright or dark the room is and turn its LED display on when it gets dark.

## Step 1

We need to check the light level over and over again, so we will use a ``||basic:forever||`` loop.

Find the ``||basic:forever||`` block. It should already be in your workspace. If it is not there, drag one out from the ``||basic:Basic||`` drawer.

## Step 2

Now we need to make a decision. If it is dark, turn the light on. If it is bright, turn the light off.

From the ``||logic:Logic||`` drawer, drag an ``||logic:if true then / else||`` block and place it inside the ``||basic:forever||`` block.

```blocks
basic.forever(function () {
    if (true) {
    } else {
    }
})
```

## Step 3

Now we need to check the light level. The micro:bit has a built-in light sensor that returns a number from 0 (very dark) to 255 (very bright).

From the ``||logic:Logic||`` drawer, drag a ``||logic:0 < 0||`` comparison block and place it in the **true** slot of your ``||logic:if||`` block.

```blocks
basic.forever(function () {
    if (0 < 0) {
    } else {
    }
})
```

## Step 4

From the ``||input:Input||`` drawer, drag a ``||input:light level||`` block and place it on the **left** side of the ``||logic:< ||`` comparison.

Then change the number on the **right** side to **100**. This means the light will turn on when the light level drops below 100.

```blocks
basic.forever(function () {
    if (input.lightLevel() < 100) {
    } else {
    }
})
```

## Step 5

When it is dark, we want to show a bright pattern. From the ``||basic:Basic||`` drawer, drag a ``||basic:show icon||`` block into the **if** branch (the top section). Choose the **square** icon to look like a lamp shining.

```blocks
basic.forever(function () {
    if (input.lightLevel() < 100) {
        basic.showIcon(IconNames.Square)
    } else {
    }
})
```

## Step 6

When the room is bright, we want to turn the display off. From the ``||basic:Basic||`` drawer, drag a ``||basic:clear screen||`` block into the **else** branch (the bottom section).

```blocks
basic.forever(function () {
    if (input.lightLevel() < 100) {
        basic.showIcon(IconNames.Square)
    } else {
        basic.clearScreen()
    }
})
```

## Step 7

Time to test! Look at the simulator on the left. Find the **light level** slider under the micro:bit and drag it left to make it dark. The LEDs should light up. Drag it right to make it bright and the LEDs should turn off.

## Step 8

Download your program to the micro:bit. Click the **Download** button at the bottom of the screen and follow the instructions to copy the file to your micro:bit.

Try covering the front of the micro:bit with your hand to make it dark. Your night light should turn on!

## @showdialog

Great work! You built a night light that reacts to the world around it.
Try changing the number **100** to a different value to make your night light more or less sensitive to light.
