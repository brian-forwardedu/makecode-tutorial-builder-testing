
# Beating Heart

## @showdialog

Welcome to the Beating Heart tutorial!

You will program your micro:bit to show a pulsing heart animation on its LED display.

## Step 1 - Add a forever loop

The heart will beat over and over, so you need a block that runs forever.

Find the ``||basic:forever||`` block. It should already be on your workspace. If not, drag one out from the ``||basic:Basic||`` drawer.

## Step 2 - Show a large heart

Inside the ``||basic:forever||`` block, add a ``||basic:show icon||`` block from the ``||basic:Basic||`` drawer.

Click the icon dropdown and choose the **Heart** icon.

```blocks
basic.forever(function () {
    basic.showIcon(IconNames.Heart)
})
```

## Step 3 - Pause before the next frame

After the large heart, add a ``||basic:pause (ms) 100||`` block from the ``||basic:Basic||`` drawer.

Change the value to **200** milliseconds. This gives the large heart a moment to show on screen.

```blocks
basic.forever(function () {
    basic.showIcon(IconNames.Heart)
    basic.pause(200)
})
```

## Step 4 - Show a small heart

Add another ``||basic:show icon||`` block below the pause.

This time, choose the **Small Heart** icon from the dropdown.

```blocks
basic.forever(function () {
    basic.showIcon(IconNames.Heart)
    basic.pause(200)
    basic.showIcon(IconNames.SmallHeart)
})
```

## Step 5 - Pause again

Add one more ``||basic:pause (ms) 100||`` block at the bottom, inside the ``||basic:forever||`` block.

Change the value to **200** milliseconds. This controls how long the small heart shows before the loop starts again.

```blocks
basic.forever(function () {
    basic.showIcon(IconNames.Heart)
    basic.pause(200)
    basic.showIcon(IconNames.SmallHeart)
    basic.pause(200)
})
```

## Step 6 - Test in the simulator

Look at the micro:bit simulator on the left side of the screen.

You should see the heart growing and shrinking, like a real heartbeat. Great work!

## Step 7 - Download to your micro:bit

Connect your micro:bit to your computer with a USB cable.

Click the **Download** button and follow the steps to send your program to the micro:bit.

Watch the LED display pulse with a beating heart!

## @showdialog

Congratulations! You built a beating heart animation on your micro:bit.

Try changing the pause times to make the heart beat faster or slower.
