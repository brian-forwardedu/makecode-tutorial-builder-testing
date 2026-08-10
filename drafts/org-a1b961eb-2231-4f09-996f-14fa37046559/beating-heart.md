# Beating Heart

## @showdialog

Welcome! In this tutorial, you will program your micro:bit to show a beating heart on its LED display. This is a great project to wear with your CHARGE for micro:bit.

## Step 1

Find the ``||basic: forever||`` block. It is already in your workspace. Code inside this block runs over and over again.

## Step 2

Open the ``||basic: Basic||`` drawer and find the ``||basic: show icon||`` block. Drag it inside the ``||basic: forever||`` block.

```blocks
basic.forever(function () {
    basic.showIcon(IconNames.Heart)
})
```

## Step 3

Make sure the icon is set to the heart shape. Click the icon picture on the block and choose the filled heart.

## Step 4

Now add a short pause so the heart stays on screen for a moment. Open the ``||basic: Basic||`` drawer and drag a ``||basic: pause (ms) 100||`` block below the ``||basic: show icon||`` block. Change the value to **300**.

```blocks
basic.forever(function () {
    basic.showIcon(IconNames.Heart)
    basic.pause(300)
})
```

## Step 5

Add a second ``||basic: show icon||`` block below the pause. This time, choose the small heart icon so the heart appears to beat.

```blocks
basic.forever(function () {
    basic.showIcon(IconNames.Heart)
    basic.pause(300)
    basic.showIcon(IconNames.SmallHeart)
})
```

## Step 6

Add another ``||basic: pause (ms) 100||`` block below the small heart. Change the value to **300**. This creates a rhythm for the heartbeat.

```blocks
basic.forever(function () {
    basic.showIcon(IconNames.Heart)
    basic.pause(300)
    basic.showIcon(IconNames.SmallHeart)
    basic.pause(300)
})
```

## Step 7

Look at the simulator on the left side of the screen. You should see the heart growing and shrinking in a steady beat. Try changing the pause values to make the heart beat faster or slower.

## Step 8

When you are happy with your beating heart, connect your micro:bit to your computer and click the **Download** button to send the program to your micro:bit. Then attach it to your CHARGE for micro:bit and wear it!

## @showdialog

Great work! You have built a beating heart wearable with your micro:bit and CHARGE for micro:bit. Try changing the icons or pause times to make it your own.
