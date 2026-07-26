# Loop Explorer

## @showdialog

Welcome to Loop Explorer! In this tutorial, you will learn how a loop repeats actions for you. Instead of writing the same code over and over, a loop does the hard work. Let's build it together!

## Step 1

A ``||basic:forever||`` block runs the code inside it over and over, forever. You will already see one in the workspace. We will not use it for this tutorial, so go ahead and delete it by dragging it to the trash.

## Step 2

Find the ``||loops:repeat 4 times||`` block inside the **Loops** drawer. Drag it into the empty workspace. This block will run the code inside it a set number of times.

## Step 3

Change the number in ``||loops:repeat 4 times||`` from **4** to **5**. Your loop will now repeat five times.

## Step 4

Open the **Basic** drawer and find the ``||basic:show number 0||`` block. Place it inside the ``||loops:repeat 5 times||`` block.

## Step 5

Open the **Basic** drawer again and find the ``||basic:pause (ms) 100||`` block. Place it inside the loop, just below the ``||basic:show number 0||`` block. Change the pause to **500** ms. This gives you time to see each number.

## Step 6

Now we need a number that changes each time the loop runs. Open the **Loops** drawer and find the ``||loops:for index from 0 to 4||`` block. Replace your ``||loops:repeat 5 times||`` block with this one. Move the two blocks inside it to stay inside the new loop.

## Step 7

Find the ``||loops:index||`` value block inside the **Loops** drawer. Place it into the ``||basic:show number 0||`` block, replacing the **0**. Now the screen will show the current loop count each time!

## Step 8

Look at the simulator on the left. Press the play button if it is not already running. You should see the numbers 0, 1, 2, 3, and 4 appear on the micro:bit display one at a time. The loop is doing all the work!

## Step 9

Try changing the **4** in ``||loops:for index from 0 to 4||`` to a larger number, like **9**. Watch the simulator count all the way up to your new number. You changed the loop without rewriting every step!

## Step 10

When you are happy with your loop, click the **Download** button to send your program to a real micro:bit and watch it count on the actual device.

## @showdialog

Great work! You have learned how a loop repeats actions for you automatically. Instead of writing ten show number blocks, one loop does it all. Keep experimenting with loops in your next project!
