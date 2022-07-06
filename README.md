## Python and the Pi Pico Blue Board

<table align="right">
<tr><td><img alt="Fun!" src="http://www.makikiweb.com/Pi/Art/blue_board_rainbow_300.jpg" align="right" height="200" width="220">
<p>
<center><b>Python on the Pi Pico</b></center>
</td>
</tr></table>

#### by Craig Miller

Learning Python can be fun. Learning Python on the Raspberry Pi Pico where lights flash, change colour and appear to flow back and forth is even more **fun**

VicPiMakers has teamed up with Q-Rangers to create a Raspberry Pi Pico blue board for learning Python. With this board, you will be able to control a string of multicoloured **NeoPixels** from Python. The NeoPixels are pre-wired, and no soldering or jumpers are required.

In addition to the Pi Pico and the NeoPixels, the board also has a project board, where using jumpers, simple circuits can be created and controlled via Python. Circuits using Light Emitting Diodes (LEDs) and light sensors can be used to not only create games, but also show how you can write programs that interact with the real world.

### Circuit Python

The Pi Pico is loaded with [Circuit Python](https://learn.adafruit.com/welcome-to-circuitpython), a flavour of micro-Python to run on embedded devices like the Pi Pico created by **AdaFruit**.
 
#### Controlling NeoPixels from Python

Circuit Python includes libraries which make programming the NeoPixels a breeze, hiding the hardware complexity. By importing the `neopixel` library, it is a simple 3 line program to light the NeoPixels *red*

```
# Update this to match the number of NeoPixel LEDs connected to your board.
num_pixels = 5

pixels = neopixel.NeoPixel(board.GP0, num_pixels)
pixels.brightness = 0.25

while True:
    pixels.fill((255, 0, 0))
```

There are many examples of using Python on NeoPixels on the [AdaFruit website](https://learn.adafruit.com/getting-started-with-raspberry-pi-pico-circuitpython/neopixel-leds)


#### Controlling the World from Python

The Pi Pico board has a built-in LED which can be controlled from Python. Blinking a LED from software control may not be all that exciting, but combining it with a button, means you can now create a game. AdaFruit has an [example of controlling the built-in, and controlling it with a button](https://learn.adafruit.com/getting-started-with-raspberry-pi-pico-circuitpython/blinky-and-a-button) (aka a switch).

The game [React](https://github.com/cvmiller/react), written in Python, tests your reaction time, by flashing the LED, and measures the time it takes to press the button.

### The Blue Board Hardware

The Blue Board has the following components:

* Raspberry Pi Pico
* 5 NeoPixels 
* Project board with 2 General Purpose Input/Output (GPIO) pre-wired

![Blue Board](http://www.makikiweb.com/Pi/Art/pi_pico_neopixels_800_2.jpg "Blue Board")


#### Pi Pico

The [Raspberry Pi Pico](https://www.raspberrypi.com/documentation/microcontrollers/raspberry-pi-pico.html) is the newest of the Raspberry Pi family, and departs from the larger Pi's in that it **does not run linux**. Instead, it is targeted at the embedded or Internet of Things (IoT) market. But that doesn't mean there isn't some power, it comes with:

* a Dual-core ARM processor
* 2 MB of onboard flash storage
* 264kBytes of RAM

#### NeoPixels

[NeoPixels](https://learn.adafruit.com/adafruit-neopixel-uberguide) are addressable, multi-colour capable LEDs. One can create strings of tens of NeoPixels individually controlling each, creating banners, light runners, even games. The blue board comes with five (5) pre-wired NeoPixels.

#### Project Board

The Project board is pre-wired to two (2) GPIO pins on the Pi Pico to allow one to create simple circuits, such as buttons for input, or LEDs for output, all controlled via Python.

To create your own projects, the following parts are also supplied:

* An LED that emits white light.  The negative terminal is marked with a black line on the side of the LED
* A 100 ohm current limiting resistor to prevent burning out the LED
* A momentary switch button
* A light sensitive resistor
* A 10k ohm resistor for making a voltage divider for the analog inputs
Some hookup wire


A logical wiring diagram of the blue board with the project board attach looks like this:

![Blue Board](http://www.makikiweb.com/Pi/Art/pi_pico_fritz_board_v2_800.jpg "Project Board")

Shown for clarity, each row of five pin sockets in the wireless breadboard are connected:

![Back of Project Board](http://www.makikiweb.com/Pi/Art/pi_pico_project_board_back_300.jpg)

### Getting Circuit Python

Circuit Python is an interpreter which must be downloaded to the Pi Pico. It should already be on the Pico, appearing as **CIRCUITPY** in Windows File Explorer when the Pico is plugged into the computer USB. However should you need to load it, the Pi Foundation has an [excellent tutorial](https://www.raspberrypi.com/documentation/microcontrollers/micropython.html) on downloading and installing MicroPython to the Pi Pico. 

That said, Circuit Python a "fork" of MicroPython has better support for NeoPixels. It is therefore recommended to use **Circuit Pyhon UF2** file. As of this writing, the latest stable release is 7.3.1. You can [download the UF2 Circuit Python](https://circuitpython.org/board/raspberry_pi_pico/) file here.

Additional [Python Libraries](https://circuitpython.org/libraries) for Circuit Python can be downloaded and copied to the **lib** directory on the blue board.

Circuit Python has been pre-installed on the blue board.

### Using the Thonny IDE to program Python on the Pi Pico

There is a good Integrated Development Environment (IDE), called **Thonny** which runs on Window, Mac, or even a Linux-based Raspberry Pi (e.g. the Pi3 or Pi4).
 
![Thonny](https://thonny.org/img/screenshot.png)

#### Installing Thonny

It is easy to [install Thonny](https://microcontrollerslab.com/getting-started-raspberry-pi-pico-thonny-ide/#Thonny_IDE_Installation_Steps) by following this [guide](https://microcontrollerslab.com/getting-started-raspberry-pi-pico-thonny-ide/#Thonny_IDE_Installation_Steps).

#### Running your first Python Program

Once **Thonny** is installed on your Desktop computer, follow this [Guide for running your first Python program](https://microcontrollerslab.com/getting-started-raspberry-pi-pico-thonny-ide/#Test_Thonny_IDE_Installation_with_LED_Blinking_Example), which blinks the on-board LED. 

Be sure to select **CircuitPython** as the interpreter in Thonny. The default program name is **code.py** rather than MicroPython's *main.py*.




### Learning Python

Python is the world's most popular computer programming language. There are hundreds of thousands of programs written in Python. The **Blue Board** will get you started on learning Python, and making computers do what you want, rather than bring limited to what a program does.





---
<small>

<br>

29 June 2022<br>
Updated 5 July 2022<br>
Draft 5 - updated with Circuit Python library info<br>
Draft 6 - placed on git hub (and revision control)

</small>

