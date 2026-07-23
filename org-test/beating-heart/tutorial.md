
# Beating Heart

## @showdialog

Welcome to the Beating Heart tutorial!

In this project, you will program the micro:bit to display an animation that looks like a beating heart using the LED screen.

## Step 1 - Open the forever block

Look at the workspace. You will see a ``||basic: forever||`` block already on the screen.

All of the blocks for your animation will go inside this block so the heart keeps beating.

```blocks
basic.forever(function () {
})
```

## Step 2 - Show a large heart

Find the ``||basic: show icon||`` block inside the ``||basic: Basic||`` drawer.

Drag it into the ``||basic: forever||`` block.

Click the icon picture and choose the **Heart** shape.

```blocks
basic.forever(function () {
    basic.showIcon(IconNames.Heart)
})
```

## Step 3 - Add a short pause

Find the ``||basic: pause (ms) 100||`` block in the ``||basic: Basic||`` drawer.

Place it after the ``||basic: show icon||`` block.

Change the value to **200** milliseconds. This keeps the large heart on screen for a moment.

```blocks
basic.forever(function () {
    basic.showIcon(IconNames.Heart)
    basic.pause(200)
})
```

## Step 4 - Show a small heart

Find another ``||basic: show icon||`` block and place it after the pause.

Click the icon picture and choose the **Small Heart** shape.

```blocks
basic.forever(function () {
    basic.showIcon(IconNames.Heart)
    basic.pause(200)
    basic.showIcon(IconNames.SmallHeart)
})
```

## Step 5 - Add another pause

Find another ``||basic: pause (ms) 100||`` block and place it after the small heart icon.

Change the value to **200** milliseconds. This keeps the small heart on screen before the animation repeats.

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

You should see the heart growing and shrinking in a loop. That is your beating heart animation!

Try changing the pause values to make the beat faster or slower.

## Step 7 - Download to your micro:bit

Connect your micro:bit to the computer with the USB cable.

Click the **Download** button at the bottom of the screen.

Follow the steps to copy the program to your micro:bit and watch the heart beat on the real device.

## @showdialog

Great work! You have built a beating heart animation on the micro:bit.

Try changing the pause times or adding more icons to make the animation your own.
