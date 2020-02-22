# CPE 1040 - Spring 2020

## Assignment 5: Transistors

Author: Ivo Georgiev, PhD  
Last updated: 2020-02-22  
Code: 98ffb5e9c5964e27028001933faec10caa0e4709  

This is assignment 5 for the Spring 2020 installment of the CPE 1040 - Intro to Computer Engineering course at MSU Denver.

### Overview

This assignment introduces transistors and electrical circuits that employ them. _Refer to the [requirements](requirements.md) for this assignment. Filling out the [README](README.md) for this repository is part of the assignment. Refer to the [criteria](criteria.md) for submitted assignments!_

#### Requirements

1. **(TODO)** pnp/npn transistor circuits with LEDs and switches at the base

2. Soil sensor **(TODO): Divide into two, namely, manual calibration and auto-calibration.**:
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

1. [micro:bit lessons](https://makecode.microbit.org/lessons).

2. [micro:bit ideas](https://microbit.org/ideas/).

3. A list of some more [advanced projects](https://www.itpro.co.uk/desktop-hardware/26289/13-top-bbc-micro-bit-projects).

4. The [projects](https://github.com/carlosperate/awesome-microbit#%EF%B8%8F-projects) at the [awesome micro:bit list](https://github.com/carlosperate/awesome-microbit).

5. micro:bit [technical documentation](https://tech.microbit.org/).

### Transistors
**(TODO)**
1. pnp datasheet
2. npn datasheet
3. circuit video

### Sensors

1. SparkFun soil moisture sensor [hookup guide](https://learn.sparkfun.com/tutorials/soil-moisture-sensor-hookup-guide). _Note: For Arduino._

### Github

1. Github Tutorial for Beginners ([webpage](https://product.hubspot.com/blog/git-and-github-tutorial-for-beginners)).

2. Github Basics for Mac and Windows ([video](https://www.youtube.com/watch?v=0fKg7e37bQE)).

3. git & Github Crash Course for Beginners ([video](https://www.youtube.com/watch?v=SWYqp7iY_Tc)).

4. Introduction to Github for Beginners ([video](https://www.youtube.com/watch?v=fQLK8Ib_SKk)).

5. About `git` ([webpage](https://git-scm.com/about)).

6. `git` [documentation](https://git-scm.com/doc) (webpage, book, videos, reference manual).

7. [Github markdown cheat sheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet).

### JavaScript

1. Technically, the language which is used side-by-side with Blocks in the Makecode ronment is a subset of [TypeScript](https://makecode.com/language), which itself is a superset of JavaScript (technically, [ECMAScript](https://www.ecma-international.org/ecma-262/10.0/index.html#Title)), with some JS features not implemented in Makecode.

2. The limited [JavaScript mini-tutorial](https://makecode.microbit.org/javascript) in Makecode.

3. Official [TypeScript documentation](https://www.typescriptlang.org/docs/home.html):
   1. TypeScript in 5 min [tutorial](https://www.typescriptlang.org/docs/handbook/typescript-in-5-minutes.html). _Note: You will need to [download](https://www.typescriptlang.org/index.html#download-links) and install an integrated development environment (IDE). The two that I recommend are Visual Studio Code from Microsoft and WebStorm from JetBrains._
   2. The full documentation and reference is under _Handbook_. Bear in mind that you are drinking from the hose. Don't be surprised if not everything is presented in a strictly incremental manner.
   
4. In-browser TypeScript [playground](https://www.typescriptlang.org/play/index.html). Note that micro:bit specific code will not run, but you can still play. _Start making the distinction between a generic multi-purpose programming language (TypeScript) and functionality (packages, libraries, objects, etc.) that is specific to a particular device (micro:bit), though written in the same programming language._

5. A pretty good and very palatable JS tutorial with in-browser coding, by [Codecademy](https://www.codecademy.com/learn/introduction-to-javascript).

6. Extensive and detailed [JS tutorial](https://javascript.info/), with some advanced material thrown in. **I like this one!**

7. The most authoritative JS resource on the Web, including tutorials and reference, by [Mozilla](https://developer.mozilla.org/en-US/docs/Web/JavaScript).

