# CPE 1040 - Introduction to Computer Engineering

## Assignment: Final Project

## Part II (Week 13, Assignment #8)

### 1. Summary

This is the final project and the last required assignment. It contains lab work, source code versioning, and a writeup. The [README.md](README.md) is empty for you to fill with your project writeup. This file, [requirements.md](requirements.md) contains the requirements. There are three parts to the final project, to be done, in order, in weeks 12-14, respectively:
1. An extended version of Assignment #6, requiring some basic I/O and pin operation on the microbit.
2. Oscilloscope exercises and passing data over I2C.
3. Tutorial on creating a Makecode extension package for the soil moisture sensor.
The file [criteria.md](criteria.md) contains the criteria for passing.

### 2. Requirements

#### Week 12 - micro:bit I/O

1. LEDs:
   1. Follow the instructions in the SparkFun [micro:bit breakout board hookup guide](https://learn.sparkfun.com/tutorials/microbit-breakout-board-hookup-guide). Build the circuit, using 3 LEDs of different colors. Remember the proper orientation of the LEDs (long leg toward higher voltage). Commit the JavaScript file to your assignment repository, calling it `original-guide.js`. Build the circuit and take a short video of its operation. Do a short writeup in [README.md](README.md) and include a link to the video.
   2. Reconfigure the circuit and rewrite the program to avoid disabling the LED matrix. Choose the correct 3 pins from the [micro:bit GPIO function table](https://learn.sparkfun.com/tutorials/microbit-breakout-board-hookup-guide#hardware-overview). Add code to demonstrate that the LED matrix is enabled. Commit the JavaScript file to your assignment repository, calling it `enable-matrix.js`. Build the circuit and take a short video of its operation. Do a short writeup in [README.md](README.md) and include a link to the video.
   3. Now that you have a 5x5 LED matrix and 3 external LEDs, extend your favorite screensaver program to include the external LEDs into the changing pattern. Do something interesting. Commit the JavaScript file to your assignment repository, calling it `twenty-eight.js`. Build the circuit and take a short video of its operation. Do a short writeup in [README.md](README.md) and include a link to the video.
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
   
#### Week 13 - Oscilloscopes and serial protocols

1. Oscilloscope warmup:
   1. Watch the first 4 oscilloscope videos [referenced below](#oscilloscopes).
   2. Take a look at the Rigol 1000 Series oscilloscopes documentation site to see what resources you have in case you need mmore in-depth knowledge.
   3. The oscilloscope shows _continuous varying signals_ that it detects at the tips of its _probes_. The probe has a two wires: _signal_ (red or central probe), and _ground_ (black or outside wire). _Remember that voltage is a **relative** potential, so, unless you connect the ground, which serves as the **reference level**, you will get garbage._
   4. Connect a Rigol probe to Channel 1.
2. Visualize simple continuous signals:
   1. Visualize the following signals, using the **Auto** regime and default settings (trigger on a rising edge on CH1). For each signal, take a **video** of the setup (the source wire and connection of the oscilloscope probe) and the display of the oscilloscope, while varying one of the signal properties (wave shape, frequency, amplitude) using the controls of the source. Write up one sentence in the [README](README.md), enough to be able to insert a link to the video. Signals:
      1. Configure the **OUT** of the built-in function generator on the workstation with whatever function you want. _Remember that we used it to drive external LEDs._
      2. Fire up the standalone Rigol function generator. It is right beneath the multimeter. Connect a probe. _Notice that the function generator probes also have two wires._ Connect it properly to the oscilloscope probe. Repeat the previous task with this new source.
      3. Write a one-line micro:bit program to set an analog pin to emit PWM pulses. Which pin function will you use? Capture the signal. _PWM stands for [Pulse Width Modulation](https://en.wikipedia.org/wiki/Pulse-width_modulation) and is a method to control servo motors. PWM is based on a square wave signal where the pulses (that is, the sections where the signal is *_*high**) vary in width. The servo motor decodes the signal (essentially comparing the width of the pulse to the period of the square wave) and rotates the shaft accordingly._
      4. To repeat the task from (1), you need a loop for your program in (3). Write a loop that varies the duty cycle, up and down, between 5% and 95%, in steps of 5%. _Note: Here, you need to read on the oscilloscope what the period of the base wave is, to calculate the duty cycles. Include the period and the pulse widths for the highest and lowest duty cycle in your short writeup._
   2. Explore the _other_ servo function, using the oscilloscope. Once you figure it out, write a small program to demo the operation, and record the video. _You might or might not need to use the **Single** mode of the oscilloscope._
3. I2C warmup:
   1. Read the SparkFun [I2C tutorial](https://learn.sparkfun.com/tutorials/i2c).
   2. In a small writeup in the [README](README.md), answer the following questions:
      1. What are the disadvantages of the other two serial communication channels, UART and SPI, and how does I2C improve on them?
      2. I2C is a two-wire serial communication channel. What are the two wires, SDA and SCL?
      3. What distinguishes the _master_ and the _slaves_?
      4. How are the two types of protocol _frames_ different?
      5. What is the most appropriate _trigger_ for capturing an I2C frame on the oscilloscope?
      6. (Advanced) If the micro:bit is configured by default as a _master_, and two micro:bits, connected to each other via the SDA and SCL lines, communicate over I2C? (**Bonus** for a convincing argument, one way or another.)
4. First steps with I2C:
   1. In a loop, configure the micro:bit to write a number to some arbitrary I2C address. The address can be arbitrary. Capture an I2C frame on the oscilloscope. _Note that I2C has 2 wires, so you will need 2 probes, and set the correct trigger on the correct channel._ Use the **Single** mode on the oscillocope. Take a picture of your setup and a picture of the oscilloscope display. In the writeup, analyze what you have captured:
      1. What frame did you capture?
      2. What does the I2C write function do when there is nothing connected?
      3. Is there a difference in what you capture if you write a number to one of the internal device addresses? _(The accelerometer and magentometer (compass) are connected to the I2C bus on the micro:bit PCB. Their addresses can be found [here](https://tech.microbit.org/hardware/i2c/).)_
   2. Write a short program to read a number from the I2C devices on the micro:bit. For each device:
      1. Find the appropriate [I2C address](https://tech.microbit.org/hardware/i2c/) for the device you want to read from. What are the three numbers? Which one should you use in `function i2cReadNumber(address: number, format: NumberFormat, repeated?: boolean): number;`? (**Bonus** for a cogent argument about why there are three numbers. Hint: Write them in binary and compare!)
      2. Try signed and unsigned single bype integers.
      3. Scroll the values on the LED matrix. 
      4. What values do you read?
      5. Can you get different values by moving the micro:bit around.
5. **(Advanced, optional, and bonus)** Simple pulse-based protocol:
   1. Program one micro:bit to emit pulse-based patterns by driving a digital output pin. Use a 50% duty cycle. Start with the 11111<sub>2</sub> pattern.
   2. Program another micro:bit to detect the pattern by listening on an digital input pin. Play with the `bits.onPulsed()` and `bits.pulseDuration()` functions.
   3. Generate and capture all 5-bit patterns. _How will you deal with the patterns that start with the same value as your protocol line (that is, if your line is high by default, how will you deal with patterns that start with 1, and if you line is low by default, how will you deal with patterns that start with 0)?_ Devise a demo that shows this capability on a video. You may use the LED matrix to show the sent and received patterns, for comparison.
      
#### Week 14 - I2C sensors & Makecode packages
   
TBD, topic tentative

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
