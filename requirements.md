# CPE 1040 - Spring 2020

## Assignment 5: Transistors


### 2. Requirements

#### Week 12 - micro:bit I/O

2. Soil sensor:
   1. Keeping at least one analog output pin, open a digital input pin and hook it up to a TTL input button on the workstation. Light the external LED when you detect a 1 on the input button (that is, the button is _pressed_). _Note: Do you need an external or internal [pullup resistor](https://www.google.com/search?q=pullup+pulldown+resistor&oq=pullup+pull)?_ Commit the JavaScript file to your assignment repository, calling it `digital-in.js`. Build the circuit and take a short video of its operation. Do a short writeup in [README.md](README.md) and include a link to the video.
   2. Hook up the soil moisture sensor. There are three wires coming out: VCC, GND, and SIG. Pick a GPIO pin, configure it as digital output, and wire VCC to it. Pick a GPIO pin, configure it as analog in, and wire SIG to it. GND whould be wired to ground on the micro:bit.
   3. Write a program that:
      1. Reads the sensor input in a loop with pauses to get the reading.
		2. It only powers the sensor when it takes a reading, by writing a 1 and then a 0 to the digital output pin. **Do not hook up the VCC on the sensor to a constant 3.3V or leave the digital pin to 1 when you are not taking a reading. This degrades the sensor quickly! **
		3. Maps the range of input values of the sensor (you need to measure them yourself) to the range 0-4. Use the [`map`](https://makecode.microbit.org/reference/pins/map) function. This is called _calibration_ of the sensor. For the minimum value, take a reading with a dry sensor not touching anything; for the maximum value, take a reading with the sensor prongs dipped in shallow water. **Do not immerse the whole sensor in water!**
		4. When it takes a sensor reading, it lights up as many rows of the LED matrix as correspond to the rescaled magnitude of the reading.
   4. Commit the JavaScript file to your assignment repository, calling it `manual-calibration.js`. Build the circuit and take a short video of its operation. Do a short writeup in [README.md](README.md) and include a link to the video.
   5. Write a program that does the calibration programmatically:
      1. When the program starts, it prompts the user to take three readings of the low and three readings of the high values of the range. It starts by showing the South icon image to prompt the user to take a low value, and records it. Then, it shows the North icon image to prompt the user to take a high value, and records it. It repeats this two more times, for a total of 3 readings for each.
      2. It takes the average of the low values and sets the range minimum to that value. It does the same for the range maximum.
      3. It performs the mapping, exits the calibration subprogram, scrolls "Calibration success" once, and starts normal operation described in the previous task.
   6. Commit the JavaScript file to your assignment repository, calling it `auto-calibration.js`. Build the circuit and take a short video of its operation. Do a short writeup in [README.md](README.md) and include a link to the video.
3. Tag:
   1. When done with Week 12, including the videos and writeups in [README.md](README.md), tag the repository with the tag "FP-Week-12".
   2. If you need to change anything before you start Week 13, when you are done with the new commits, tag again, using the tag "FP-Week-12-1".
   

## Resources

### micro:bit 

1. micro:bit [lessons](https://makecode.microbit.org/lessons).
2. micro:bit [ideas](https://microbit.org/ideas/).
3. A list of some more [advanced projects](https://www.itpro.co.uk/desktop-hardware/26289/13-top-bbc-micro-bit-projects).
4. The assembled micro:bit resources at the [awesome micro:bit list](https://github.com/carlosperate/awesome-microbit).
5. micro:bit [reference](https://makecode.microbit.org/reference), and specifically the [pins](https://makecode.microbit.org/reference/pins) section.
6. The technical documentation for the micro:bit [GPIO edge connector](https://tech.microbit.org/hardware/edgeconnector/) and [pins](https://makecode.microbit.org/device/pins).
7. SparkFun [micro:bit breadboard bridge hookup guide](https://learn.sparkfun.com/tutorials/microbit-breakout-board-hookup-guide) (contains micro:bit GPIO pin function [table](https://learn.sparkfun.com/tutorials/microbit-breakout-board-hookup-guide#hardware-overview)).

### Sensors

1. SparkFun soil moisture sensor [hookup guide](https://learn.sparkfun.com/tutorials/soil-moisture-sensor-hookup-guide). _Note: For Arduino._

### Oscilloscopes

1. Oscilloscopes made easy [Part 1](https://www.youtube.com/watch?v=uU3FhH7_MWo), [Part 2](https://www.youtube.com/watch?v=5VyotIVwRiA).
2. Oscilloscope tutorials [SparkFun](https://www.youtube.com/watch?v=u4zyptPLlJI), [Martin Lorton](https://www.youtube.com/watch?v=CzY2abWCVTY).
3. Rigol 1000 Series oscilloscopes [documentation](https://www.rigolna.com/products/digital-oscilloscopes/1000z/).

### I2C

1. SparkFun I2C [tutorial](https://learn.sparkfun.com/tutorials/i2c).
2. Typescript I2C [support](https://makecode.microbit.org/reference/pins).
3. I2C [bus](https://www.i2c-bus.org/).
4. Wikipedia article on [I2C](https://en.wikipedia.org/wiki/I%C2%B2C).
5. Micro:bit I2C [addresses](https://tech.microbit.org/hardware/i2c/).
6. Micro:bit runtime/DAL support for [I2C:](https://lancaster-university.github.io/microbit-docs/ubit/i2c/).
7. Article on [connecting I2C devices]( https://smalldevices.com.au/blogs/resources/connecting-i2c-devices-to-the-bbc-micro-bit) to the micro:bit.
8. Micro:bit [software stack](https://mattwarren.org/2017/11/28/Exploring-the-BBC-microbit-Software-Stack/).
9. Micro:bit [IoT](https://www.iot-programmer.com/index.php/books/26-micro-bit-iot-in-c).
10. MicroPython support for [I2C](https://microbit-micropython.readthedocs.io/en/latest/i2c.html).

### Github

1. Github Tutorial for Beginners ([webpage](https://product.hubspot.com/blog/git-and-github-tutorial-for-beginners)).
2. Github Basics for Mac and Windows ([video](https://www.youtube.com/watch?v=0fKg7e37bQE)).
3. git & Github Crash Course for Beginners ([video](https://www.youtube.com/watch?v=SWYqp7iY_Tc)).
4. Introduction to Github for Beginners ([video](https://www.youtube.com/watch?v=fQLK8Ib_SKk)).
5. About `git` ([webpage](https://git-scm.com/about)).
6. `git` [documentation](https://git-scm.com/doc) (webpage, book, videos, reference manual).
7. [Github markdown cheat sheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet).

### JavaScript

1. Technically, the language which is used side-by-side with Blocks in the Makecode environment is a subset of [TypeScript](https://makecode.com/language), which itself is a superset of JavaScript (technically, [ECMAScript](https://www.ecma-international.org/ecma-262/10.0/index.html#Title)), with some JS features not implemented in Makecode.
2. The limited [JavaScript mini-tutorial](https://makecode.microbit.org/javascript) in Makecode. Make sure you read it but that can't be your only reference.
3. Official [TypeScript documentation]():
   1. TypeScript in 5 min [tutorial](https://www.typescriptlang.org/docs/handbook/typescript-in-5-minutes.html). _**Highly recommended!** You will need to [download](https://www.typescriptlang.org/index.html#download-links) and install an integrated development envinronment (IDE). The two that I recommend are Visual Studio Code from Microsoft and WebStorm from JetBrains._
   2. The full documentation and reference is under _Handbook_. Bear in mind that you are drinking from the hose. Don't be surprised if not everything is presented in a strictly incremental manner.
   3. The Microsoft TypeScript page on [Github](https://github.com/microsoft/TypeScript), including the [TypeScript language sepecification](https://github.com/microsoft/TypeScript/blob/master/doc/spec.md).
4. In-browser TypeScript [playground](https://www.typescriptlang.org/play/index.html). Note that micro:bit specific code will not run, but you can still play. _Start making the distinction between a generic multi-purpose programming language (TypeScript) and functionality (packages, libraries, objects, etc.) that is specific to a particular device (micro:bit), though written in the same programming language._
5. A pretty good and very palatable JS tutorial with in-browser coding, by [Codecademy](https://www.codecademy.com/learn/introduction-to-javascript).
6. Extensive and detailed [JS tutorial](https://javascript.info/), with some advanced material thrown in. _**I like this one!**_
7. The most authoritative JS resource on the Web, including tutorials and reference, by [Mozilla](https://developer.mozilla.org/en-US/docs/Web/JavaScript).
8. micro:bit [reference](https://makecode.microbit.org/reference/), especially [GPIO pins](https://makecode.microbit.org/reference/pins).
