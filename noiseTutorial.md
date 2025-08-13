# My DeskFan Tutorial
# Flash-a-rama

## It's time to code! @showdialog

Let's get real bright. We're going to make all the lights flash on your board!

![Flash lights](https://static.wixstatic.com/media/9e10e9_f4c35f4407bf4fb4963fa98f174f1aa4~mv2.jpg/v1/fill/w_1074,h_500,fp_0.50_0.50,q_85,enc_auto/9e10e9_f4c35f4407bf4fb4963fa98f174f1aa4~mv2.jpg)

## Build the circuit as shown @showdialog

Let's get real bright. We're going to make all the lights flash on your board!

![Flash lights](https://static.wixstatic.com/media/9e10e9_f4c35f4407bf4fb4963fa98f174f1aa4~mv2.jpg/v1/fill/w_1074,h_500,fp_0.50_0.50,q_85,enc_auto/9e10e9_f4c35f4407bf4fb4963fa98f174f1aa4~mv2.jpg)


## Step 1
Add a ``||logic:if true then||`` block. 

## Step 2
Drag the ``||basic:show leds||`` block into the ``||basic:forever||`` block. 

## Step 3 - Show the temperature

Get a ``||input:temperature||`` block and place it in the value slot of ``||basic:show number||``.

```blocks
basic.forever(function() {
    basic.showNumber(input.temperature())
    basic.showString("Hello")
    basic.showIcon(IconNames.Chessboard)
    basic.pause(100)
    radio.sendMessage(0)

})
```

## Step 4

```blocks
basic.forever(function() {
    strip.show()

})
```
```package
neopixel=github:microsoft/pxt-neopixel

```
<script src="https://makecode.com/gh-pages-embed.js"></script><script>makeCodeRender("{{ site.makecode.home_url }}", "{{ site.github.owner_name }}/{{ site.github.repository_name }}");</script>

