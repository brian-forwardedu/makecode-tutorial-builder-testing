
# Automatic Night Light


```package
all-fwd-blocks=github:forward-education/pxt-all-fwd-blocks#v2.0.1
```


## @showdialog

Welcome! In this tutorial you will build an automatic night light.

The solar sensor will measure how bright the room is. When it gets dark, the LED ring will turn on automatically.

## Step 1

We want our program to keep checking the light level over and over. Find the ``||basic: forever||`` block. It should already be in your workspace.

## Step 2

Inside ``||basic: forever||``, add an ``||logic: if true then||`` block from the ``||logic: Logic||`` drawer. This will let us check whether it is dark.

```blocks
basic.forever(function () {
    if (true) {
    }
})
```

## Step 3

Now we need a condition. Find ``||fwdSensors: solar1 light level % is under 20||`` from the ``||fwdSensors: Sensors||`` drawer and place it in the ``||logic: if||`` slot, replacing the word ``true``.

This means the light ring will only turn on when the light level drops below 20 percent.

```blocks
basic.forever(function () {
    if (fwdSensors.solar1.isPastThreshold(20, fwdEnums.OverUnder.Under)) {
    }
})
```

## Step 4

Inside the ``||logic: if||`` block, add ``||fwdLights: set ledRing1 all pixels color||`` from the ``||fwdLights: Lights||`` drawer. This block sets the color of every pixel on the LED ring at once.

```blocks
basic.forever(function () {
    if (fwdSensors.solar1.isPastThreshold(20, fwdEnums.OverUnder.Under)) {
        fwdLights.ledRing1.setAllPixelsColor(0xffffff)
    }
})
```

## Step 5

Click the color circle on the ``||fwdLights: set ledRing1 all pixels color||`` block and choose white. White light works best for a night light.

## Step 6

Now we need to turn the light off when the room is bright. Click the plus icon on the ``||logic: if||`` block to add an ``||logic: else||`` section.

```blocks
basic.forever(function () {
    if (fwdSensors.solar1.isPastThreshold(20, fwdEnums.OverUnder.Under)) {
        fwdLights.ledRing1.setAllPixelsColor(0xffffff)
    } else {
    }
})
```

## Step 7

Inside the ``||logic: else||`` section, add another ``||fwdLights: set ledRing1 all pixels color||`` block. This time choose black (no color) to turn the ring off.

```blocks
basic.forever(function () {
    if (fwdSensors.solar1.isPastThreshold(20, fwdEnums.OverUnder.Under)) {
        fwdLights.ledRing1.setAllPixelsColor(0xffffff)
    } else {
        fwdLights.ledRing1.setAllPixelsColor(0x000000)
    }
})
```

## Step 8

Add a ``||basic: pause (ms) 100||`` block from the ``||basic: Basic||`` drawer at the very bottom of the ``||basic: forever||`` block, after the ``||logic: if / else||``. Change the value to **500**.

This short pause keeps the program from checking too quickly and saves power.

```blocks
basic.forever(function () {
    if (fwdSensors.solar1.isPastThreshold(20, fwdEnums.OverUnder.Under)) {
        fwdLights.ledRing1.setAllPixelsColor(0xffffff)
    } else {
        fwdLights.ledRing1.setAllPixelsColor(0x000000)
    }
    basic.pause(500)
})
```

## Step 9

Test your program in the simulator. Slide the solar sensor value down below 20 percent. The LED ring should light up white. Slide it back up and the ring should turn off.

## Step 10

When you are happy with how it works, click **Download** to send the program to your micro:bit. Connect your solar sensor and LED ring, then try covering the solar sensor with your hand to trigger the night light.

## @showdialog

Great work! Your automatic night light is complete.

The solar sensor watches the light level, and the LED ring switches on the moment the room gets dark. Try changing the threshold number to make your night light more or less sensitive.
