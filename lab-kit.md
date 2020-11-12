# Lab kit

A take-home lab kit for CPE 1040, LP004-005. It was assembled by SparkFun. The contents and descriptions of the various components can be found on [SparkFun's special page for MSUD](https://www.sparkfun.com/msu_denver).  

Table of Contents
=================

* [Lab kit](#lab-kit)
  * [1\. Breadboard](#1-breadboard)
    * [Guide](#guide)
    * [Care](#care)
  * [2\. Multimeter](#2-multimeter)
    * [Guide](#guide-1)
    * [Care](#care-1)
  * [3\. Wires](#3-wires)
  * [4\. Resistors](#4-resistors)
  * [5\. Semiconductors](#5-semiconductors)
    * [Guide](#guide-2)
      * [Diodes](#diodes)
      * [Light\-emitting diodes (LEDs)](#light-emitting-diodes-leds)
      * [Transistors](#transistors)
      * [Soil sensor](#soil-sensor)
    * [Care](#care-2)

## 1. Breadboard
[[toc](#table-of-contents)]  

A breadboard is a plate with through-holes and [internal electrical connections](http://wiring.org.co/learning/tutorials/breadboard/) for use with hands-on circuit building and prototyping. This is the white plastic block shown in the picture below. Also in the picture, there are a [power supply](https://www.sparkfun.com/products/13032) (with a [wall adapter](https://www.sparkfun.com/products/15314) and a [microbit connector](https://www.sparkfun.com/products/13989).

<img src="images/01-breadboard.jpg" width="600" />  

The power supply is connected to one end of the breadboard along the short side. The microbit connector is connected to the middle of the long side of the breadboard, along the A column (when looking at the side opposite to the one where the power supply is installed). Take a look at the next pictures:

<img src="images/02-breadboard-assembled.jpg" width="400" />  | <img src="images/15-power-supply-rails.jpg" width="400" /> | <img src="images/14-mb-breakout-col-a.jpg" width="400" />
--- | --- | ---


### Guide
[[toc](#table-of-contents)]  

SparkFun, who assembled the lab kit for us, has very thorough guides:
1. For [using a breadboard](https://learn.sparkfun.com/tutorials/how-to-use-a-breadboard/all), including the power supply. Pay special attention to how the breadboard rows and columns are connected. This is something you have to get used to.    
2. For [hooking up the micro:bit to the breadboard](https://learn.sparkfun.com/tutorials/microbit-breakout-board-hookup-guide).  

### Care
[[toc](#table-of-contents)]  

Pay attention to these care directions:
1. Take a look at this [image from the SparkFun guide](https://cdn.sparkfun.com/r/600-600/assets/2/f/9/d/a/513a1dfbce395fe524000001.JPG) for the correct connection of the power supply. The [header pins](https://www.mouser.com/images/samtec/images/samtec_mtms_SPL.jpg), of which it has 2 groups of 4 on both sides, have to be inserted into the rails of the breadboard, in the first two rows on one end, with the VCC label on the side of the red rail line and the GND on the side of the blue rail line.  
2. To make the power supply more stable, you can use a piece of hard putty underneath it.  

   <img src="images/12-uhu-tac.jpg" width="200"/> | <img src="images/16-power-supply-pad.jpg" width="200"/> 
   --- | ---

3. The power supply has two tiny switches, one for ON-OFF and one for 3.3V-5V. _Handle the switches very gently._ When the power supply is on, a red LED is lit up. It is brighter for 5V than for 3.3V. We will use 3.3V for our projects.  
4. The micro:bit works at 3.3V, but we won't be powering it from the power supply, but through the USB cable or battery. _Do not plug the micro:bit connector into one of the rails!_  
5. Pushing in the micro:bit connector takes quite a bit of force. _Use a hard flat surface (e.g. scissors) to push straight down, to avoid mangling the header pins._  

<img src="images/13-mb-breakout-scissors.jpg" width="200"/>  

## 2. Multimeter
[[toc](#table-of-contents)]  

The [multimeter](https://www.sparkfun.com/products/12966) is a device that can measure electrical quantities, namely voltage (in Volts), current (in Amperes), resistance (in Ohms), as well as continuity of a circuit.  
| | |
|---|---|
| <img src="images/03-multimeter-backside.jpg" width="300"/> | You need to open the flap on the back to connect the 9V PP3 battery |
| <img src="images/04-multimeter-battery-in.jpg" width="300"/> | There is only one way you can connect the battery leads to the wire connector |
| <img src="images/05-multimeter-front-probes.jpg" width="300"/> | Multimeter needs probes to measure the right circuit quantity |
| <img src="images/06-multimeter-front-needle-probes.jpg" width="300"/> | Needle tipped probles can reach inside a breadboard hole |

### Guide
[[toc](#table-of-contents)]  

The sparkfun [multimeter tutorial](https://learn.sparkfun.com/tutorials/how-to-use-a-multimeter) is comprehensive and covers a lot of topics. _Consider this required reading._  

### Care
[[toc](#table-of-contents)]  

Follow these directions for safety and tool care:
1. Always connect the black probe to the middle hole, named COM, which stands for common.  
2. For this course, connect the red probe to the right-hand hole. You will not need to use the left-hand hole, as we are not going to generate such a large current (10 Amperes).  
3. The dial on the face of the multimeter chooses the function. Mind the following two points:
   1. Never select a current measument function (A) to measure voltage. Never select a voltage measurement function (V) to measure current.  
   2. Always select a function with a rating larger than you expect your quantity to be. For example, to measure voltages around 3.3V, set the dial to 20V:
   
      |   |   |
      |---|---|
      <img src="images/18-measuring-3v3.jpg" width="200"/>  | <img src="images/17-multimeter-closeup.jpg" width="200"/>  

4. The needle-tipped probes are extremely sharp. _Always replace the caps when you are leaving them unattended and/or not using them._  
5. Keep your multimiter dial in the OFF position when not in use to conserve the battery.  

## 3. Wires
[[toc](#table-of-contents)]  

Wires are used to connect elecrical circuits. Not much to say about them.  

<img src="images/07-wires.jpg" width="400"/>

Red wires are conventionally used to connect to the voltage source of the circuit (Vcc) or generally a higher voltage; black wires are used to connect to zero voltage, usually called ground (GND), or generally a lower voltage. Note that the multimeter follows this convention, and you should always connect its black probe to ground or lowest voltage.  

## 4. Resistors
[[toc](#table-of-contents)]  

Resistors are passive circuit elements, which oppose the flow of current. Ohm's Law involves a nice interdependence between the three most important electric circuit quantities, namely volgage (V), current (I), and resistance (R): <img src="https://render.githubusercontent.com/render/math?math=V = IR">.  

<img src="images/08-resistors.jpg" width="400"/>   

The units of resistance are Ohm's (because of Ohm's Law), usually indicated by the greek letter omega (<img src="https://render.githubusercontent.com/render/math?math=\Omega">). The kit contains two different resistor types:  <img src="https://render.githubusercontent.com/render/math?math=10 K\Omega"> (large resistance), and <img src="https://render.githubusercontent.com/render/math?math=330 \Omega"> (small resistance).  

Resistors for breadboards have color bands on their body, which can be used to read off their resistance, tolerance, and rating. Take a look at the [color chart](https://www.mouser.com/technical-resources/conversion-calculators/resistor-color-code-calculator). Of course, you can always use the multimeter in resistance mode (<img src="https://render.githubusercontent.com/render/math?math=\Omega">) and connect the resistor between the two probes to measure its resistance.   

## 5. Semiconductors
[[toc](#table-of-contents)]  

Semiconductors are active circuit elements, meaning that they perform certian functions on the signals in the circuit. They are highly engineered devices made from silicon, gallium, boron, phosphorus, arsenic, and some metals to make systematic use of electromagnetic and electromechanical properties of solic matter on the border of the quantum world.

| <img src="images/08-resistors.jpg" width="400"/> | <img src="images/11-LEDs.jpg" width="400"/> | <img src="images/09-soil-sensor.jpg" width="400"/> |
|---|---|---|

We have two different classes of devices: diodes, and transistors.  

### Guide
[[toc](#table-of-contents)]  

#### Diodes
[[toc](#table-of-contents)]  

Diodes look in their packaging like resistors, but they perform a non-linear function, namely they conduct current in one direction (without resisting it significantly) and do not allow it to flow in the other (until a breakdown voltage threshold is passed). Contrary to resistors, diodes are directional.  

#### Light-emitting diodes (LEDs)
[[toc](#table-of-contents)]  

LEDs are light-emitting diodes. When hooked to a circuit in the conducting orientation, they emit light.  

#### Transistors
[[toc](#table-of-contents)]  

Transistors are the most important fundamental hardware unit of computation. It is a 3-terminal device where one of the terminals controls the current that will flow between the other two. In this sense, transistors are electronic switches. Computers are made out of millions of transistors, which underlie both processors and memories.  

#### Soil sensor
[[toc](#table-of-contents)]  

The soil sensor is essentially a transistor, hooked up in such a way that the strength of the signal that sends to the computer (the micro:bit in our case) depends on the resistance (or, conversely, the conductance) between the two prongs, which are inserted in soil or directly in water.  

### Care
[[toc](#table-of-contents)]  

Semiconductor devices have to be connected according to their documentation, with proper voltages applied to the right terminals. Otherwise, they may be damaged irreversibly. Follow these directions to keep them intact:
1. Hook up LEDs with the longer leg toward Vcc and shorter leg toward GND. This is the conducting direction.  
2. Never hook up an LED directly between Vcc and GND. There should be always a 330 Ohm current-limiting resistor in series with the LED.  
3. The particular type of transistors that we have in the kit are bipolar-junction transistors (BJTs). They are current amplifiers, come in two flabors (NPN and PNP), and have 3 terminals called base (B), emitter (E), and collector (C). Follow the instructions in their documentation to identify which is which and connect them properly and safely.  
4. Never connect the base (B) of a transistor to a voltage without a current-limiting resistor. The base current for BJTs should be very small, so a 10 KOhm resistor in series is standard for the base.  
5. Here are the datasheets:
   1. NPN transistor: [2N3904](https://www.sparkfun.com/datasheets/Components/2N3904.pdf).  
   2. PNP transistor: [2N3906](https://www.sparkfun.com/datasheets/Components/2N3906.pdf).  
   3. Diode: [1N4148](https://www.diodes.com/assets/Datasheets/ds12019.pdf).  
   4. LED: [info sheet](https://cdn.sparkfun.com/datasheets/Components/LED/SFE-03-0010-LEDInsertCards-RainbowPack-03-Outlines.pdf).  
6. Do not dip more than the prongs of the soil sensor in water.  


