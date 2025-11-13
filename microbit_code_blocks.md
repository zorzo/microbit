```javascript
basic.forever(function () { 
    pins.digitalWritePin(DigitalPin.P0, 0) 
    pins.digitalWritePin(DigitalPin.P1, 1) 
    basic.pause(500) 
    pins.digitalWritePin(DigitalPin.P0, 1) 
    pins.digitalWritePin(DigitalPin.P1, 0) 
    basic.pause(500) 
```

```javascript
pins.setPull(DigitalPin.P2, PinPullMode.PullUp) 
basic.forever(function () { 
    if (pins.digitalReadPin(DigitalPin.P2) == 0) { 
        pins.digitalWritePin(DigitalPin.P0, 0) 
        pins.digitalWritePin(DigitalPin.P1, 1) 
        basic.pause(500) 
        pins.digitalWritePin(DigitalPin.P0, 1) 
        pins.digitalWritePin(DigitalPin.P1, 0) 
        basic.pause(500) 
    } 
```

```javascript
basic.forever(function () { 
    led.plotBarGraph( 
    pins.analogReadPin(AnalogPin.P0), 
    1023 
    ) 
```

```javascript
let svetlo = 0 
let kalibracia = 0 
```

```javascript
basic.forever(function (){     
```

```javascript
     basic.showIcon(IconNames.Heart)    } else {            
     basic.showIcon(IconNames.Square)     
```

```javascript
basic.forever(function () { 
    music.ringTone(262) 
    basic.pause(100) 
    music.ringTone(330) 
    basic.pause(100) 
    music.ringTone(392) 
    basic.pause(100) 
    music.ringTone(330) 
    basic.pause(100) 
```

```javascript
input.onButtonPressed(Button.A, function () { 
    pins.digitalWritePin(DigitalPin.P0, 1) 
    pins.digitalWritePin(DigitalPin.P1, 0) 
    pins.digitalWritePin(DigitalPin.P2, 0) 
```

```javascript
input.onButtonPressed(Button.B, function () { 
    pins.digitalWritePin(DigitalPin.P0, 0) 
    pins.digitalWritePin(DigitalPin.P1, 1) 
    pins.digitalWritePin(DigitalPin.P2, 0) 
```

```javascript
input.onButtonPressed(Button.AB, function () { 
    pins.digitalWritePin(DigitalPin.P0, 0) 
    pins.digitalWritePin(DigitalPin.P1, 0) 
    pins.digitalWritePin(DigitalPin.P2, 1) 
```

```javascript
basic.forever(function () { 
```

```javascript
pins.setEvents(DigitalPin.P0, PinEventType.Edge) 
pins.setPull(DigitalPin.P0, PinPullMode.PullUp) 
 
control.onEvent(EventBusSource.MICROBIT_ID_IO_P0, 
```

```javascript
    pins.digitalWritePin(DigitalPin.P2, 1) 
```

```javascript
control.onEvent(EventBusSource.MICROBIT_ID_IO_P0, 
```

```javascript
    pins.digitalWritePin(DigitalPin.P2, 0) 
```

```javascript
led.enable(false) 
basic.forever(() => { 
    pins.digitalWritePin(DigitalPin.P3, 1)  
    pins.digitalWritePin(DigitalPin.P4, 1)  
    pins.digitalWritePin(DigitalPin.P6, 1)  
    pins.digitalWritePin(DigitalPin.P7, 1)  
    basic.pause(2000)  
    pins.digitalWritePin(DigitalPin.P3, 0)  
    pins.digitalWritePin(DigitalPin.P4, 0)  
    pins.digitalWritePin(DigitalPin.P6, 0)  
    pins.digitalWritePin(DigitalPin.P7, 0)  
    basic.pause(5000) 
```

```javascript
led.enable(false)  
basic.forever(() => { 
    pins.digitalWritePin(DigitalPin.P3, 1)  
    pins.digitalWritePin(DigitalPin.P7, 0)  
    basic.pause(1000)  
    pins.digitalWritePin(DigitalPin.P4, 1)  
    pins.digitalWritePin(DigitalPin.P3, 0)  
    basic.pause(1000)  
    pins.digitalWritePin(DigitalPin.P6, 1)  
    pins.digitalWritePin(DigitalPin.P4, 0)  
    basic.pause(1000)  
    pins.digitalWritePin(DigitalPin.P7, 1)  
    pins.digitalWritePin(DigitalPin.P6, 0)  
    basic.pause(1000) 
```

```javascript
pins.digitalWritePin(DigitalPin.P0, 1) 
basic.forever(function () { 
    pins.digitalWritePin(DigitalPin.P0, 0) 
    basic.pause(1000) 
    pins.digitalWritePin(DigitalPin.P0, 1) 
    basic.pause(1000) 
```

```javascript
input.onButtonPressed(Button.A, function () { 
    pins.servoWritePin(AnalogPin.P0, 0) 
```

```javascript
input.onButtonPressed(Button.B, function () { 
    pins.servoWritePin(AnalogPin.P0, 180) 
```

```javascript
input.onButtonPressed(Button.AB, function () { 
    pins.servoWritePin(AnalogPin.P0, 90) 
```

```javascript
grove.onGesture(GroveGesture.Right, function () { 
    basic.showString("R") 
```

```javascript
grove.onGesture(GroveGesture.Left, function () { 
    basic.showString("L") 
```

```javascript
grove.onGesture(GroveGesture.Forward, function () { 
    basic.showArrow(ArrowNames.North) 
```

```javascript
grove.onGesture(GroveGesture.Backward, function () { 
    basic.showArrow(ArrowNames.South) 
```

```javascript
basic.forever(function () { 
    if (grove.measureInCentimeters(DigitalPin.P0) >= 10) { 
        basic.showIcon(IconNames.Yes) 
    } else { 
        basic.showIcon(IconNames.No) 
    } 
    basic.pause(100) 
```

```javascript
basic.forever(function () { 
    music.playTone(grove.measureInCentimeters(DigitalPin.P1) * 10, 
music.beat(BeatFraction.Whole)) 
```

```javascript
let A = 0 
let disp: grove.TM1637 = null 
input.onGesture(Gesture.Shake, function () { 
    A += 1 
    disp.show(A) 
    basic.pause(100) 
```

```javascript
let disp: grove.TM1637 = null 
```

```javascript
basic.forever(function () { 
    disp.show(grove.measureInCentimeters(DigitalPin.P0)) 
    basic.pause(100) 
```

```javascript
let pasik: neopixel.Strip = null 
let uhol = 0 
```

```javascript
basic.forever(function () { 
    pasik.showRainbow(1, 360) 
    pasik.rotate(pins.analogReadPin(AnalogPin.P0)) 
    pasik.show() 
    basic.pause(100) 
```

```javascript
let svetlo = 0 
basic.forever(function () { 
    svetlo = pins.analogReadPin(AnalogPin.P1) 
    if (svetlo >= 100) { 
        pins.digitalWritePin(DigitalPin.P2, 1) 
        music.playTone(262, music.beat(BeatFraction.Whole)) 
        basic.pause(100) 
        pins.digitalWritePin(DigitalPin.P2, 0) 
        basic.pause(100) 
    } else { 
        pins.digitalWritePin(DigitalPin.P0, 0) 
        pins.digitalWritePin(DigitalPin.P2, 0) 
    } 
    basic.pause(100) 
```

```javascript
basic.forever(function () { 
    if (grove.measureInCentimeters(DigitalPin.P1) < 5) { 
        for (let i = 0; i < 20; i++) { 
            pins.digitalWritePin(DigitalPin.P2, 1) 
            music.playTone(262, music.beat(BeatFraction.Whole)) 
            basic.pause(100) 
            pins.digitalWritePin(DigitalPin.P2, 0) 
            basic.pause(100) 
        } 
    } 
    basic.pause(100) 
```

```javascript
let noise = 0 
let light = 0 
led.enable(false) 
basic.forever(function () { 
    light = smarthome.ReadLightIntensity(AnalogPin.P1) 
    if (light < 50) { 
        noise = smarthome.ReadNoise(AnalogPin.P2) 
        if (noise > 70) { 
            neopixel.create(DigitalPin.P3, 1, 
```

```javascript
            basic.pause(10000) 
            neopixel.create(DigitalPin.P3, 1, 
```

```javascript
        } 
    } 
```

```javascript
let teplota = 0 
```

```javascript
basic.forever(function () { 
    teplota = smarthome.ReadTemperature(TMP36Type.TMP36_temperature_C, 
```

```javascript
    OLED.clear() 
    OLED.showStringNoNewLine("Teplota:") 
    OLED.showNumberNoNewLine(teplota) 
    if (teplota > 30) { 
        music.beginMelody(music.builtInMelody(Melodies.BaDing), MelodyOptions.Once) 
        pins.digitalWritePin(DigitalPin.P2, 1) 
        basic.pause(5000) 
        pins.digitalWritePin(DigitalPin.P2, 0) 
        basic.pause(500) 
    } else { 
        pins.digitalWritePin(DigitalPin.P2, 0) 
    } 
```

```javascript
pins.setPull(DigitalPin.P2, PinPullMode.PullUp) 
pins.servoWritePin(AnalogPin.P7, 180) 
let okno = -1 
basic.forever(function () { 
    if (pins.digitalReadPin(DigitalPin.P2) == 0) { 
        okno = okno * -1 
        if (okno == 1) { 
            neopixel.create(DigitalPin.P1, 1, NeoPixelMode.RGB).range(0, 
```

```javascript
            pins.servoWritePin(AnalogPin.P7, 0) 
            basic.pause(2000) 
        } else { 
            pins.servoWritePin(AnalogPin.P7, 180) 
            basic.pause(2000) 
            neopixel.create(DigitalPin.P1, 1, NeoPixelMode.RGB).range(0, 
```

```javascript
        } 
    } 
```

```javascript
basic.forever(function () { 
    if (pins.analogReadPin(AnalogPin.P1) > 500) { 
        music.beginMelody(music.builtInMelody(Melodies.BaDing), MelodyOptions.Once) 
        pins.digitalWritePin(DigitalPin.P2, 1) 
        basic.pause(10000) 
    } else { 
        pins.digitalWritePin(DigitalPin.P2, 0) 
        basic.pause(10000) 
    } 
```

```python
    a, b = 0, 1 
    while a < n: 
        print(a, end=' ') 
        a, b = b, a+b 
    print() 
```

```python
from microbit import * 
```

```python
from microbit import * 
```

```python
    for y in range(0, 5): 
        display.set_pixel(x,y,9) 
```

```python
from microbit import * 
```

```python
from microbit import * 
```

```python
from microbit import * 
```

```python
from microbit import * 
```

```python
from microbit import * 
```

```python
            "39093:"  
            "30903:"  
            "39093:"  
            "33333") 
```

```python
from microbit import * 
```

```python
              "30003:"  
              "30903:"  
              "30003:"  
              "33333") 
```

```python
              "30093:"  
              "30003:"  
              "39003:"  
              "33333") 
```

```python
              "39003:"  
              "30903:"  
              "30093:"  
              "33333") 
```

```python
              "39093:"  
              "30003:"  
              "39093:"  
              "33333") 
```

```python
              "39093:"  
              "30903:"  
              "39093:"  
              "33333") 
```

```python
              "39093:"  
              "39093:"  
              "39093:"  
              "33333") 
```

```python
from microbit import * 
```

```python
    if button_a.is_pressed() and button_b.is_pressed(): 
        display.scroll("AB") 
        break 
    elif button_a.is_pressed(): 
        display.scroll("A") 
    elif button_b.is_pressed(): 
        display.scroll("B") 
```

```python
from microbit import * 
```

```python
    if button_a.was_pressed(): 
        display.scroll("A") 
    else: 
        display.scroll(Image.ASLEEP) 
    sleep(1000) 
```

```python
from microbit import * 
```

```python
    sleep(3000) 
    count = button_a.get_presses() 
    display.scroll(str(count)) 
```

```python
from microbit import * 
```

```python
    if pin0.is_touched(): 
        display.show(Image.HAPPY) 
    else: 
        display.show(Image.SAD) 
```

```python
from microbit import * 
```

```python
    if pin0.read_digital(): 
        display.show(Image.HAPPY) 
    else: 
        display.show(Image.SAD) 
```

```python
from microbit import * 
```

```python
    pin0.write_digital(1) 
    sleep(500) 
    pin0.write_digital(0) 
    sleep(500) 
```

```python
from microbit import * 
```

```python
    pin0.write_analog(1023) 
    sleep(2000) 
    pin0.write_analog(767) 
    sleep(2000) 
    pin0.write_analog(511) 
    sleep(2000) 
    pin0.write_analog(255) 
    sleep(2000) 
```

```python
from microbit import * 
```

```python
    pin0.write_analog(180) 
    sleep(1000) 
    pin0.write_analog(1) 
    sleep(1000) 
```

```python
from microbit import * 
```

```python
    for freq in range(880, 1760, 16): 
        music.pitch(freq, 6) 
    for freq in range(1760, 880, -16): 
        music.pitch(freq, 6) 
```

```python
from microbit import * 
```

```python
music.play(music.BIRTHDAY) 
```

```python
from microbit import * 
```

```python
        "E4:4", "F4:4", "G4:8", "E4:4", "F4:4", "G4:8"] 
music.play(tune) 
```

```python
from microbit import * 
```

```python
        "E:4", "F", "G:8"] 
music.play(tune) 
```

```python
from microbit import * 
```

```python
from microbit import * 
```

```python
    x = accelerometer.get_x() 
    y = accelerometer.get_y() 
    z = accelerometer.get_z() 
    print("x, y, z:", x, y, z) 
    sleep(500) 
```

```python
from microbit import * 
```

```python
    reading = accelerometer.get_x() 
    if reading > 20: 
        display.show("R") 
    elif reading < -20: 
        display.show("L") 
    else: 
        display.show("-") 
```

```python
from microbit import * 
```

```python
    gesture = accelerometer.current_gesture() 
    if gesture == "face up": 
        display.show(Image.HAPPY) 
    else: 
        display.show(Image.ANGRY) 
```

```python
from microbit import * 
```

```python
    smer = ((15 - compass.heading()) // 30) % 12 
    display.show(Image.ALL_CLOCKS[smer]) 
```

```python
from microbit import * 
```

```python
    subor.write("Lorem ipsum") 
```

```python
from microbit import * 
```

```python
    text = subor.read() 
    display.scroll(text) 
```

```python
from microbit import * 
```

```python
    subor.write("Lorem ipsum") 
```

```python
    subor.write("Lorem ipsum") 
```

```python
from microbit import * 
```

```python
    subor.write("Lorem ipsum") 
```

```python
    subor.write("Lorem ipsum") 
```

```python
from microbit import * 
```

```python
 from microbit import * 
```

```python
    subor.write("Lorem ipsum") 
```

```python
from microbit import * 
```

```python
radio.on() 
radio.config(channel=19)         
radio.config(power=7)           
```

```python
        radio.send(my_message) 
        incoming = radio.receive() 
        if incoming is not None: 
            display.show(incoming) 
            print(incoming) 
        sleep(500) 
```

```python
from microbit import * 
```

```python
radio.on() 
```

```python
    if button_a.was_pressed(): 
        # vysielanie. 
        radio.send('x')   
        # príjem. 
    incoming = radio.receive() 
    if incoming == 'x': 
        display.show(Image.HEART) 
```

```python
        sleep(500) 
        display.clear() 
        # obcas odpovedz 
        if random.randint(0, 3) == 0: 
            sleep(500) 
            radio.send('x')   
```

```python
from microbit import * 
```

```javascript
basic.forever(function () { 
    motorbit.freestyle(50, 0) 
    basic.pause(1000) 
    motorbit.freestyle(0, 50) 
    basic.pause(1000) 
```

```javascript
basic.forever(function () { 
    motorbit.forward(0) 
    basic.pause(2000) 
    motorbit.forward(25) 
    basic.pause(2000) 
    motorbit.forward(50) 
    basic.pause(2000) 
    motorbit.forward(75) 
    basic.pause(2000) 
    motorbit.forward(100) 
    basic.pause(2000) 
```

```javascript
basic.forever(function () { 
    motorbit.forward(70) 
    basic.pause(500) 
    motorbit.back(50) 
    basic.pause(500) 
    motorbit.turnleft(50) 
    basic.pause(500) 
    motorbit.turnright(50) 
    basic.pause(500) 
    motorbit.brake() 
    basic.pause(500) 
    motorbit.freestyle(-40, 30) 
    basic.pause(500) 
```

```javascript
pins.analogSetPeriod(AnalogPin.P2, 2000) 
basic.forever(function () { 
    pins.analogWritePin(AnalogPin.P2, 0) 
    basic.pause(2000) 
    pins.analogWritePin(AnalogPin.P2, 255) 
    basic.pause(2000) 
    pins.analogWritePin(AnalogPin.P2, 511) 
    basic.pause(2000) 
    pins.analogWritePin(AnalogPin.P2, 767) 
    basic.pause(2000) 
    pins.analogWritePin(AnalogPin.P2, 1023) 
    basic.pause(2000) 
```

```javascript
basic.showIcon(IconNames.Target) 
radio.setGroup(1) 
radio.sendNumber(0) 
 
input.onGesture(Gesture.Shake, function () { 
    basic.showString("x") 
    radio.sendNumber(0) 
```

```javascript
input.onButtonPressed(Button.A, function () { 
    basic.showString("<") 
    radio.sendNumber(1) 
```

```javascript
input.onButtonPressed(Button.B, function () { 
    basic.showString(">") 
    radio.sendNumber(2) 
```

```javascript
input.onButtonPressed(Button.AB, function () { 
    basic.showIcon(IconNames.Triangle) 
    radio.sendNumber(3) 
```

```javascript
basic.showIcon(IconNames.Target) 
radio.setGroup(1) 
 
radio.onReceivedNumberDeprecated(function (receivedNumber) { 
    if (receivedNumber == 0) { 
        basic.showString("x") 
        motorbit.brake() 
    } 
 
    if (receivedNumber == 1) { 
        basic.showString("<") 
        motorbit.turnright(40) 
    } 
 
    if (receivedNumber == 2) { 
        basic.showString(">") 
        motorbit.turnleft(40) 
    } 
 
    if (receivedNumber == 3) { 
        basic.showIcon(IconNames.Triangle) 
        motorbit.forward(40) 
    } 
```

```javascript
basic.showIcon(IconNames.Sword) 
radio.setGroup(1) 
basic.forever(() => { 
    radio.sendValue("x", input.acceleration(Dimension.X) / 10) 
    basic.pause(100) 
    radio.sendValue("y", input.acceleration(Dimension.Y) / 10) 
    basic.pause(100) 
```

```javascript
let xPovel = 0 
let yPovel = 0 
 
radio.onDataPacketReceived(({ receivedString: name, receivedNumber: value }) => { 
    if (name == "x") { 
        xPovel = value 
    } else { 
        if (name == "y") { 
            yPovel = value 
        } 
    } 
```

```javascript
basic.showIcon(IconNames.House) 
radio.setGroup(1) 
```

```javascript
basic.forever(() => { 
    if (xPovel > 0) { 
        motorbit.turnleft(xPovel) 
    } else { 
        motorbit.turnright(Math.abs(xPovel)) 
    } 
```

```javascript
basic.forever(() => { 
    if (xPovel > 0) { 
        motorbit.turnleft(xPovel) 
    } else { 
        motorbit.turnright(Math.abs(xPovel)) 
    } 
 
    if (yPovel > 0) { 
        motorbit.forward(yPovel) 
    } else { 
        motorbit.back(Math.abs(yPovel)) 
    } 
```

```javascript
let praveKoleso = 0 
let laveKoleso = 0 
let yPovel = 0 
let xPovel = 0 
basic.showIcon(IconNames.House) 
radio.setGroup(1) 
```

```javascript
radio.onDataPacketReceived(function ({ receivedString: name, receivedNumber: value 
```

```javascript
    if (name == "x") { 
        xPovel = value 
    } else { 
        if (name == "y") { 
            yPovel = value 
        } 
```

```javascript
    } 
```

```javascript
basic.forever(function () { 
    laveKoleso = yPovel + xPovel 
    praveKoleso = yPovel - xPovel 
    motorbit.freestyle(praveKoleso, laveKoleso) 
```

```javascript
input.onButtonPressed(Button.A, function () { 
    RingbitCar.forward() 
```

```javascript
input.onButtonPressed(Button.B, function () { 
    RingbitCar.back() 
```

```javascript
input.onButtonPressed(Button.AB, function () { 
    RingbitCar.brake() 
```

```javascript
basic.forever(function () { 
    RingbitCar.forward() 
    basic.pause(400) 
    RingbitCar.turnright() 
    basic.pause(100) 
```

```javascript
input.onButtonPressed(Button.A, function () { 
    RingbitCar.freestyle(100, 50) 
```

```javascript
input.onButtonPressed(Button.B, function () { 
    RingbitCar.brake() 
```

```javascript
let strip = neopixel.create(DigitalPin.P0, 2, NeoPixelMode.RGB) 
basic.forever(function () { 
    strip.showColor(neopixel.colors(NeoPixelColors.Red)) 
    basic.pause(100) 
    strip.showColor(neopixel.colors(NeoPixelColors.Blue)) 
    basic.pause(100) 
```

```javascript
radio.setGroup(90) 
basic.forever(function () { 
    radio.sendValue("x", Math.idiv(input.acceleration(Dimension.X), 10)) 
    basic.pause(100) 
    radio.sendValue("y", Math.idiv(input.acceleration(Dimension.Y), 10)) 
    basic.pause(100) 
```

```javascript
radio.setGroup(90) 
 
radio.onDataPacketReceived(function ({ receivedString: name, receivedNumber: value 
```

```javascript
    if (name == "x") { 
        xValue = value 
    } else { 
        if (name == "y") { 
            yValue = value 
        } 
    } 
```

```javascript
let rightwheel = 0 
let leftwheel = 0 
let yValue = 0 
let xValue = 0 
```

```javascript
basic.showIcon(IconNames.Triangle) 
```

```javascript
basic.forever(function () { 
    leftwheel = yValue + xValue 
    rightwheel = yValue - xValue 
    RingbitCar.freestyle(leftwheel, rightwheel) 
```

```javascript
basic.forever(function () { 
    if (input.lightLevel() > 40) { 
        RingbitCar.forward() 
    } else { 
        RingbitCar.turnleft() 
    } 
```

```javascript
basic.showNumber(0) 
basic.forever(function () { 
    if (RingbitCar.tracking(RingbitCar.TrackingStateType.Tracking_State_2)) { 
        basic.showNumber(2) 
        basic.pause(200) 
    } 
    if (RingbitCar.tracking(RingbitCar.TrackingStateType.Tracking_State_1)) { 
        basic.showNumber(1) 
        basic.pause(200) 
    } 
    basic.showNumber(0) 
```

```javascript
basic.forever(function () { 
    if (RingbitCar.tracking(RingbitCar.TrackingStateType.Tracking_State_2)) { 
        RingbitCar.freestyle(50, 0) 
        basic.pause(100) 
    } 
    if (RingbitCar.tracking(RingbitCar.TrackingStateType.Tracking_State_1)) { 
        RingbitCar.freestyle(0, 50) 
        basic.pause(100) 
    } 
    RingbitCar.freestyle(100, 100) 
```

```javascript
basic.forever(function () { 
    if (RingbitCar.tracking(RingbitCar.TrackingStateType.Tracking_State_1)) { 
        RingbitCar.freestyle(0, 50) 
        basic.pause(100) 
    } else { 
        RingbitCar.freestyle(50, 0) 
        basic.pause(100) 
    } 
```

```javascript
let strip = neopixel.create(DigitalPin.P0, 2, NeoPixelMode.RGB) 
basic.forever(function () { 
    strip.showColor(neopixel.colors(NeoPixelColors.Red)) 
    basic.pause(100) 
    strip.showColor(neopixel.colors(NeoPixelColors.Blue)) 
    basic.pause(100) 
```

```javascript
basic.forever(function () { 
    basic.showNumber(sonarbit.sonarbit_distance(Distance_Unit.Distance_Unit_cm, 
```

```javascript
let sonar = 0 
```

```javascript
basic.forever(function () { 
    sonar = sonarbit.sonarbit_distance(Distance_Unit.Distance_Unit_cm, 
```

```javascript
    if (sonar < 25 && sonar != 0) { 
        RingbitCar.freestyle(0, 100) 
        basic.pause(500) 
    } else { 
        RingbitCar.forward() 
    } 
```

```javascript
    btVal = pins.analogReadPin(AnalogPin.P2) 
    if (btVal < 256) { 
        btNum = 1 
    } else { 
        if (btVal < 597) { 
            btNum = 2 
        } else { 
            if (btVal < 725) { 
                btNum = 3 
            } else { 
                if (btVal < 793) { 
                    btNum = 4 
                } else { 
                    if (btVal < 836) { 
                        btNum = 5 
                    } else { 
                        if (btVal < 938) { 
                            btNum = 6 
                        } else { 
                            btNum = 0 
                        } 
                    } 
                } 
            } 
        } 
    } 
```

```javascript
let btVal = 0 
let btNum = 0 
```

```javascript
basic.forever(function () { 
    button() 
    if (btNum) { 
        basic.showNumber(btNum) 
```

```javascript
    } else { 
        if (pins.analogReadPin(AnalogPin.P0) < 400) { 
            basic.showString("-X") 
        } else { 
            if (pins.analogReadPin(AnalogPin.P0) > 600) { 
                basic.showString("X") 
            } else { 
                if (pins.analogReadPin(AnalogPin.P1) < 400) { 
                    basic.showString("-Y") 
                } else { 
                    if (pins.analogReadPin(AnalogPin.P1) > 600) { 
                        basic.showString("Y") 
                    } else { 
                        basic.clearScreen() 
                    } 
                } 
            } 
        } 
    } 
```

```javascript
    btVal = pins.analogReadPin(AnalogPin.P2) 
    if (btVal < 256) { 
        btNum = 1 
    } else { 
        if (btVal < 597) { 
            btNum = 2 
        } else { 
            if (btVal < 725) { 
                btNum = 3 
            } else { 
                if (btVal < 793) { 
                    btNum = 4 
                } else { 
                    if (btVal < 836) { 
                        btNum = 5 
                    } else { 
                        if (btVal < 938) { 
                            btNum = 6 
                        } else { 
                            btNum = 0 
                        } 
                    } 
                } 
            } 
        } 
    } 
```

```javascript
let btVal = 0 
let btNum = 0 
```

```javascript
radio.setGroup(1) 
```

```javascript
basic.forever(function () { 
    button() 
    if (btNum) { 
        radio.sendValue("b", btNum) 
    } else { 
        radio.sendValue("x", pins.analogReadPin(AnalogPin.P0)) 
        basic.pause(100) 
        radio.sendValue("y", pins.analogReadPin(AnalogPin.P1)) 
        basic.pause(100) 
    } 
```

```javascript
radio.setGroup(1) 
 
radio.onDataPacketReceived(function ({ receivedString: name, receivedNumber: value 
```

```javascript
    if (name == "x") { 
        xJoy = value 
    } else { 
        if (name == "y") { 
            yJoy = value 
        } 
    } 
 
    if (bolaKalibracia == 0) { 
        xZero = xJoy 
        yZero = yJoy 
        bolaKalibracia = 1 
    } 
```

```javascript
let rightwheel = 0 
let leftwheel = 0 
```

```javascript
let yJoy = 0 
let xJoy = 0 
 
let yValue = 0 
let xValue = 0 
```

```javascript
basic.showIcon(IconNames.Triangle) 
let xZero = 0 
let yZero = 0 
 
let bolaKalibracia = 0 
 
basic.forever(function () { 
    xValue = xJoy - xZero 
    yValue = yJoy - yZero 
    leftwheel = yValue + xValue 
    rightwheel = yValue - xValue 
    RingbitCar.freestyle(leftwheel, rightwheel) 
```

```javascript
let bolaKalibracia = 0 
```

```javascript
        xZero = xJoy 
        yZero = yJoy 
        bolaKalibracia = 1 
    } 
```

```javascript
    xValue = xJoy - xZero 
    yValue = yJoy - yZero 
```

```javascript
    leftwheel = yValue + xValue 
    rightwheel = yValue - xValue 
```

```javascript
basic.showIcon(IconNames.Heart) 
```

```javascript
input.onButtonPressed(Button.A, function () { 
    wuKong.setServoAngel(wuKong.ServoList.S0, 90) 
```

```javascript
input.onButtonPressed(Button.A, function () { 
    wuKong.setServoAngel(wuKong.ServoList.S0, 110) 
```

```javascript
input.onButtonPressed(Button.B, function () { 
    wuKong.setServoAngel(wuKong.ServoList.S0, 70) 
```

```javascript
input.onButtonPressed(Button.AB, function () { 
    wuKong.setServoAngel(wuKong.ServoList.S0, 90) 
```

```javascript
basic.showIcon(IconNames.Square) 
```

```javascript
input.onButtonPressed(Button.A, function () { 
    wuKong.setServoAngel(wuKong.ServoList.S1, 110) 
```

```javascript
input.onButtonPressed(Button.B, function () { 
    wuKong.setServoAngel(wuKong.ServoList.S1, 70) 
```

```javascript
input.onButtonPressed(Button.AB, function () { 
    wuKong.setServoAngel(wuKong.ServoList.S1, 90) 
```

```javascript
input.onButtonPressed(Button.A, function () { 
    wuKong.setServoAngel(wuKong.ServoList.S1, 180) 
```

```javascript
input.onButtonPressed(Button.B, function () { 
    wuKong.setServoAngel(wuKong.ServoList.S1, 0) 
```

```javascript
basic.showIcon(IconNames.Square) 
```

```javascript
input.onButtonPressed(Button.A, function () { 
    wuKong.setServoAngel(wuKong.ServoList.S1, 70) 
    for (let i = 0; i < 4; i++) { 
        wuKong.setServoAngel(wuKong.ServoList.S0, 70) 
        basic.pause(1000) 
        wuKong.setServoAngel(wuKong.ServoList.S0, 110) 
        basic.pause(1000) 
    } 
    wuKong.setServoAngel(wuKong.ServoList.S1, 90) 
```

```javascript
input.onButtonPressed(Button.A, function () { 
    wuKong.setAllMotor(0, -100) 
    basic.pause(1000) 
    wuKong.setAllMotor(0, -50) 
    basic.pause(1000) 
    wuKong.setAllMotor(0, 0) 
```

```javascript
    basic.pause(1000) 
    wuKong.setAllMotor(0, 50) 
    basic.pause(1000) 
    wuKong.setAllMotor(0, 100) 
```

```javascript
input.onButtonPressed(Button.B, function () { 
    wuKong.stopAllMotor() 
```

```javascript
    wuKong.setServoAngel(wuKong.ServoList.S0, 90) 
    wuKong.setServoAngel(wuKong.ServoList.S1, 90) 
    wuKong.setServoAngel(wuKong.ServoList.S2, 90) 
    wuKong.setServoAngel(wuKong.ServoList.S3, 90) 
```

```javascript
basic.pause(500) 
```

```javascript
    wuKong.setServoAngel(wuKong.ServoList.S0, 180 - lp) 
    wuKong.setServoAngel(wuKong.ServoList.S1, pp) 
    wuKong.setServoAngel(wuKong.ServoList.S2, 180 - lz) 
    wuKong.setServoAngel(wuKong.ServoList.S3, pz) 
```

```javascript
    wuKong.setServoAngel(wuKong.ServoList.S0, 90) 
    wuKong.setServoAngel(wuKong.ServoList.S1, 90) 
    wuKong.setServoAngel(wuKong.ServoList.S2, 90) 
    wuKong.setServoAngel(wuKong.ServoList.S3, 90) 
```

```javascript
basic.pause(500) 
```

```javascript
input.onButtonPressed(Button.A, function () { 
    wuKong.mecanumRun(wuKong.RunList.Front) 
    basic.pause(500) 
    wuKong.mecanumStop() 
    basic.pause(100) 
    wuKong.mecanumRun(wuKong.RunList.rear) 
    basic.pause(500) 
    wuKong.mecanumStop() 
    basic.pause(100) 
    wuKong.mecanumRun(wuKong.RunList.left) 
    basic.pause(500) 
    wuKong.mecanumStop() 
    basic.pause(100) 
    wuKong.mecanumRun(wuKong.RunList.right) 
    basic.pause(500) 
    wuKong.mecanumStop() 
```

```javascript
input.onButtonPressed(Button.A, function () { 
    wuKong.mecanumSpin(wuKong.TurnList.Left) 
    basic.pause(500) 
    wuKong.mecanumStop() 
    basic.pause(100) 
    wuKong.mecanumSpin(wuKong.TurnList.Right) 
    basic.pause(500) 
    wuKong.mecanumStop() 
```

```javascript
input.onButtonPressed(Button.A, function () { 
    wuKong.mecanumDrift(wuKong.TurnList.Left) 
    basic.pause(2000) 
    wuKong.mecanumStop() 
    basic.pause(200) 
    wuKong.mecanumDrift(wuKong.TurnList.Right) 
    basic.pause(2000) 
    wuKong.mecanumStop() 
```

```javascript
input.onButtonPressed(Button.A, function () { 
    wuKong.mecanumRun(wuKong.RunList.Front) 
    basic.pause(500) 
    wuKong.mecanumStop() 
    basic.pause(200) 
    wuKong.mecanumRun(wuKong.RunList.rear) 
    basic.pause(500) 
    wuKong.mecanumStop() 
    basic.pause(200) 
    wuKong.mecanumSpin(wuKong.TurnList.Left) 
    basic.pause(1000) 
    wuKong.mecanumStop() 
    basic.pause(200) 
    wuKong.mecanumSpin(wuKong.TurnList.Right) 
    basic.pause(1000) 
    wuKong.mecanumStop() 
    basic.pause(200) 
    wuKong.mecanumDrift(wuKong.TurnList.Left) 
    basic.pause(2000) 
    wuKong.mecanumStop() 
    basic.pause(200) 
    wuKong.mecanumDrift(wuKong.TurnList.Right) 
    basic.pause(2000) 
    wuKong.mecanumStop() 
```

```javascript
input.onButtonPressed(Button.A, function () { 
    RTC_DS1307.DateTime( 
    2019, 
    8, 
    31, 
    11, 
    31, 
    0 
    ) 
```

```javascript
basic.forever(function () { 
    basic.showNumber(RTC_DS1307.getTime(RTC_DS1307.TimeType.SECOND)) 
```

```javascript
basic.forever(function () { 
    OLED.clear() 
    OLED.writeString("Teplota ") 
    OLED.writeNum(input.temperature()) 
    OLED.writeString(" stupnov.") 
    OLED.newLine() 
    OLED.newLine() 
    OLED.writeString("Svetlo (0 - 255) ") 
    OLED.writeNum(input.lightLevel()) 
    basic.pause(2000) 
```

```javascript
basic.forever(function () { 
    ... 
    zobrazHodnoty(nTeplota, nSvetlo) 
    ... 
```

```javascript
    OLED.clear() 
    OLED.writeString("Teplota ") 
    OLED.writeNum(teplota) 
    OLED.writeString(" stupnov.") 
    OLED.newLine() 
    OLED.newLine() 
    OLED.writeString("Svetlo (0 - 255) ") 
    OLED.writeNum(0) 
```

```javascript
let nSvetlo = 0 
let nTeplota = 0 
```

```javascript
basic.forever(function () { 
    nTeplota = input.temperature() 
    nSvetlo = input.lightLevel() 
    zobrazHodnoty(nTeplota, nSvetlo) 
    basic.pause(2000) 
```

```javascript
    OLED.clear() 
    OLED.writeString("Teplota ") 
    OLED.writeNum(teplota) 
    OLED.writeString(" stupnov.") 
    OLED.newLine() 
    OLED.newLine() 
    OLED.writeString("Svetlo (0 - 255) ") 
    OLED.writeNum(svetlo) 
```

```javascript
let nSvetlo = 0 
let nTeplota = 0 
```

```javascript
basic.forever(function () { 
    nTeplota = input.temperature() 
    nSvetlo = input.lightLevel() 
    zobrazHodnoty(nTeplota, nSvetlo) 
    ESP8266_IoT.connectThingSpeak() 
    ESP8266_IoT.setdata( 
    "ZHUTMJ2523RNxxx", 
    nTeplota, 
    nSvetlo, 
    0, 
    0, 
    0, 
    0, 
    0, 
    0 
    ) 
    ESP8266_IoT.uploadData() 
    basic.pause(10000) 
```

```javascript
    OLED.clear() 
    OLED.writeString("X: ") 
    OLED.writeNum(aX) 
    OLED.newLine() 
    OLED.newLine() 
    OLED.writeString("Y: ") 
    OLED.writeNum(aY) 
    OLED.newLine() 
    OLED.newLine() 
    OLED.writeString("Z: ") 
    OLED.writeNum(aZ) 
```

```javascript
let zrychlenieZ = 0 
let zrychlenieY = 0 
let zrychlenieX = 0 
```

```javascript
basic.forever(function () { 
    zrychlenieX = input.acceleration(Dimension.X) 
    zrychlenieY = input.acceleration(Dimension.X) 
    zrychlenieZ = input.acceleration(Dimension.Z) 
    zobrazHodnoty(zrychlenieX, zrychlenieY, zrychlenieZ) 
    ESP8266_IoT.connectThingSpeak() 
    ESP8266_IoT.setdata( 
    "3APKROE8NG9MNIWX", 
    zrychlenieX, 
    zrychlenieY, 
    zrychlenieZ, 
    0, 
    0, 
    0, 
    0, 
    0 
    ) 
    ESP8266_IoT.uploadData() 
    basic.pause(1000) 
```

```javascript
    OLED.clear() 
    OLED.writeString("Svetlo (0-100): ") 
    OLED.writeNumNewLine(svetlo) 
```

```javascript
let nSvetlo = 0 
```

```javascript
basic.forever(function () { 
    nSvetlo = Environment.ReadLightIntensity(AnalogPin.P1) 
    basic.pause(1000) 
    zobrazHodnotu(nSvetlo) 
```

```javascript
    OLED.clear() 
    OLED.writeString("Svetlo (0-100): ") 
    OLED.writeNumNewLine(svetlo) 
```

```javascript
let nSvetlo = 0 
```

```javascript
basic.forever(function () { 
    nSvetlo = Environment.ReadLightIntensity(AnalogPin.P1) 
    basic.pause(2000) 
    zobrazHodnotu(nSvetlo) 
    ESP8266_IoT.connectThingSpeak() 
    ESP8266_IoT.setdata( 
    "HE2FNQQ3xxxxx", 
    nSvetlo, 
    0, 
    0, 
    0, 
    0, 
```

```javascript
    0, 
    0, 
    0 
    ) 
    ESP8266_IoT.uploadData() 
    basic.pause(5000) 
```
