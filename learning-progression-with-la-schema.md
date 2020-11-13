# CPE 1040 - Fall 2020

This is learning progression 004 for the Fall 2020 installment of the course CPE 1040: Introduction to Computer Engineering at MSU Denver.

## Composition resources
1. [Transistors](https://docs.google.com/document/d/1KpK2u7tlg9IpjeqpNTxizabOwoFxsuq-k4WMEPzzcE4/edit) narrative on Google Docs.  
2. [Old requirements](@rchive/old-requirements.md).  
3. Logic levels, etc. from [LP006](https://github.com/ivogeorg/ce-learning-progression-006-flip-flops/blob/master/learning-progression.md).  
4. Logic gates from transistors from [LP007](https://github.com/ivogeorg/ce-learning-progression-007-logic-gates/blob/master/learning-progression-with-la-schema.md).  

Table of Contents
=================

* [CPE 1040 \- Fall 2020](#cpe-1040---fall-2020)
  * [Composition resources](#composition-resources)
  * [Learning Progression 005: Transistors](#learning-progression-005-transistors)
  * [Lab kit](#lab-kit)
    * [Parts for progression](#parts-for-progression)
  * [Steps](#steps)
    * [Step 1: Transistors](#step-1-transistors)
      * [1\. Study](#1-study)
      * [2\. Apply](#2-apply)
      * [3\. Present](#3-present)
    * [Step 2: BJT circuits](#step-2-bjt-circuits)
      * [1\. Study](#1-study-1)
      * [2\. Apply](#2-apply-1)
      * [3\. Present](#3-present-1)
    * [Step 3: Soil sensor](#step-3-soil-sensor)
      * [1\. Study](#1-study-2)
      * [2\. Apply](#2-apply-2)
      * [3\. Present](#3-present-2)
    * [Step 4: Manual calibration of soil sensor](#step-4-manual-calibration-of-soil-sensor)
      * [1\. Study](#1-study-3)
      * [2\. Apply](#2-apply-3)
      * [3\. Present](#3-present-3)
    * [Step 5: Automatic calibration of soil sensor](#step-5-automatic-calibration-of-soil-sensor)
      * [1\. Study](#1-study-4)
      * [2\. Apply](#2-apply-4)
      * [3\. Present](#3-present-4)
    * [Step 6: Sensor reading](#step-6-sensor-reading)
      * [1\. Study](#1-study-5)
      * [2\. Apply](#2-apply-5)
      * [3\. Present](#3-present-5)
    * [Step 7: Logic gates out of transistors](#step-7-logic-gates-out-of-transistors)
      * [1\. Study](#1-study-6)
      * [2\. Apply](#2-apply-6)
      * [3\. Present](#3-present-6)
    * [Step 8: Half adder and full adder](#step-8-half-adder-and-full-adder)
      * [1\. Study](#1-study-7)
      * [2\. Apply](#2-apply-7)
      * [3\. Present](#3-present-7)
    * [Step 9: Simulated logic gates](#step-9-simulated-logic-gates)
      * [1\. Study](#1-study-8)
      * [2\. Apply](#2-apply-8)
      * [3\. Present](#3-present-8)
    * [Step 10: Simulated adder](#step-10-simulated-adder)
      * [1\. Study](#1-study-9)
      * [2\. Apply](#2-apply-9)
      * [3\. Present](#3-present-9)
    * [Step 11: Simulated ALU bit slice](#step-11-simulated-alu-bit-slice)
      * [1\. Study](#1-study-10)
      * [2\. Apply](#2-apply-10)
      * [3\. Present](#3-present-10)
    * [Step 12: Simulated 4\-bit ALU](#step-12-simulated-4-bit-alu)
      * [1\. Study](#1-study-11)
      * [2\. Apply](#2-apply-11)
      * [3\. Present](#3-present-11)


## Learning Progression 005: Transistors
[[toc](#table-of-contents)]  

This progression introduces transistors, the single most important electronic device in the history and present state of computing. The transistor is a 3-terminal semiconductor device which acts like an electronic switch, allowing the design of both processing and memory devices. Modern processors and memories each contain millions of transistors, packed into ever smaller areas of silicon. The progression shows how logic gates are created out of combinations of transistors. It also shows how a single transistor can server as a moisture sensor when cleverly connected. Last but not least, it continues the micro:bit I/O theme.

## Lab kit
[[toc](#table-of-contents)]  

The lab kit is described in detail in a [separate page](lab-kit.md). Please, make sure you read the care and safety instructions embedded for most of the kit components.    

### Parts for progression  
[[toc](#table-of-contents)]  

1. Breadboard.  
2. Breadboard power supply with wall plug.  
3. micro:bit breakout board (connector).  
4. 330 Ohm resistors.  
5. 10 kOhm resistors.  
6. 2N3904 (NPN) transistors.  
7. 2N3906 (PNP) transistors.  
8. LEDs.  
9. Wires.  

## Steps
[[toc](#table-of-contents)]

### Step 1: Transistors  
[[toc](#table-of-contents)]

#### 1. Study
[[toc](#table-of-contents)]

- semiconductors & doping  
- electronic switches  
- BJTs are current amplifiers  
- FETs no base current  

#### 2. Apply
[[toc](#table-of-contents)]

**TODO: Discovery and thought experiments**

1. `[<lernact-disc>]`  

#### 3. Present
[[toc](#table-of-contents)]


### Step 2: BJT circuits
[[toc](#table-of-contents)]

#### 1. Study
[[toc](#table-of-contents)]

(Apply: Pick NPN or PNP).  

#### 2. Apply
[[toc](#table-of-contents)]

**TODO: Build NPN. PNP for opt. CircuitJS opt.**

#### 3. Present
[[toc](#table-of-contents)]


### Step 3: Soil sensor  
[[toc](#table-of-contents)]

#### 1. Study
[[toc](#table-of-contents)]

- transistor-based sensor  
- H<sub>2</sub>O resistance  
- simulate  
- basic operation
- micro:bit analog I/O  

#### 2. Apply
[[toc](#table-of-contents)]

#### 3. Present
[[toc](#table-of-contents)]


### Step 4: Manual calibration of soil sensor  
[[toc](#table-of-contents)]

#### 1. Study
[[toc](#table-of-contents)]

#### 2. Apply
[[toc](#table-of-contents)]

#### 3. Present
[[toc](#table-of-contents)]


### Step 5: Automatic calibration of soil sensor
[[toc](#table-of-contents)]

#### 1. Study
[[toc](#table-of-contents)]

#### 2. Apply
[[toc](#table-of-contents)]

#### 3. Present
[[toc](#table-of-contents)]


### Step 6: Sensor reading  
[[toc](#table-of-contents)]

#### 1. Study
[[toc](#table-of-contents)]

- 5 external LEDs of different colors  
- 2 external LEDs, one w/ 4 levels of brightness based on PWM duty cycle  

#### 2. Apply
[[toc](#table-of-contents)]

#### 3. Present
[[toc](#table-of-contents)]

### Step 7: Logic gates out of transistors  
[[toc](#table-of-contents)]

#### 1. Study
[[toc](#table-of-contents)]

- [Logic Lab](https://makecode.microbit.org/courses/logic-lab)  

#### 2. Apply
[[toc](#table-of-contents)]

#### 3. Present
[[toc](#table-of-contents)]

### Step 8: Half adder and full adder

#### 1. Study
[[toc](#table-of-contents)]

Half-adder and full adder out of gates (on "paper").

#### 2. Apply
[[toc](#table-of-contents)]

**TODO: Full adder**

#### 3. Present
[[toc](#table-of-contents)]

### Step 9: Simulated logic gates

#### 1. Study

- booleans for bits!

#### 2. Apply

#### 3. Present


### Step 10: Simulated adder

#### 1. Study

- connecting simulated gates

#### 2. Apply

#### 3. Present


### Step 11: Simulated ALU bit slice

#### 1. Study

<img src="images/alu-bit-slice.png" width="300" />

- all functions of an ALU
- carry  
- shift  

#### 2. Apply

#### 3. Present

### Step 12: Simulated 4-bit ALU

#### 1. Study

- multiplexor

#### 2. Apply

**TODO: 4 alu slices; enter a, enter b, select function, get result on external leds**

#### 3. Present

