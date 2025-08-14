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
    radio-broadcast.sendMessage(0)
    datalogger.setColumnTitles("temperature", "acceleration", "light")
    sendMessage(0)
    radio.sendMessage(0)

})
```

## Step 4

```blocks
basic.forever(function() {
    neopixel.show()


})
```

## Step 5

```blocks
let strip = neopixel.create(DigitalPin.P0, 24, NeoPixelMode.RGB_RGB)
while (true) {
    let x = input.acceleration(Dimension.X) / 2;
    let y = input.acceleration(Dimension.Y) / 2;
    let z = input.acceleration(Dimension.Z) / 2;
    strip.shift(1);
    strip.setPixelColor(0, neopixel.rgb(x, y, -z));
    neopixel.strip.show();
    basic.pause(100);
}
```

## Step 1

Instructions for step 1 of activity 1 here...

```blocks
let strip2 = neopixel.create(DigitalPin.P0, 24, NeoPixelMode.RGB)
```

## Step 2

Instructions for step 2 of activity 1 here...


```package
neopixel=github:microsoft/pxt-neopixel#v0.6.12
```

<script src="https://makecode.com/gh-pages-embed.js"></script><script>makeCodeRender("{{ site.makecode.home_url }}", "{{ site.github.owner_name }}/{{ site.github.repository_name }}");</script>
