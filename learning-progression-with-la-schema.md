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
    * [Step 10: Full adder emulation](#step-10-full-adder-emulation)
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
**questions from the Google doc**  

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

- [guide](https://learn.sparkfun.com/tutorials/soil-moisture-sensor-hookup-guide) (note, it's for a different board)   
- schematic  

- transistor-based sensor  
- H<sub>2</sub>O resistance  
- simulate  
- basic operation
- micro:bit analog I/O  

#### 2. Apply
[[toc](#table-of-contents)]

**TODO: complete the guide**  
**TODO: simulate in CircuitJS  (with a gate resistor slider)**    

#### 3. Present
[[toc](#table-of-contents)]


### Step 4: Manual calibration of soil sensor  
[[toc](#table-of-contents)]

#### 1. Study
[[toc](#table-of-contents)]

#### 2. Apply
[[toc](#table-of-contents)]

**TODO: Manual calibration (with `map`) and bars**  

#### 3. Present
[[toc](#table-of-contents)]


### Step 5: Automatic calibration of soil sensor
[[toc](#table-of-contents)]

#### 1. Study
[[toc](#table-of-contents)]

#### 2. Apply
[[toc](#table-of-contents)]

**TODO: Program for user-assisted auto calibration before operation**

#### 3. Present
[[toc](#table-of-contents)]


### Step 6: Sensor reading  
[[toc](#table-of-contents)]

#### 1. Study
[[toc](#table-of-contents)]


#### 2. Apply
[[toc](#table-of-contents)]

**TODO: 5 external LEDs of different colors**  
**TODO: 2 external LEDs, one w/ 4 levels of brightness based on PWM duty cycle**  


#### 3. Present
[[toc](#table-of-contents)]

### Step 7: Logic gates out of transistors  
[[toc](#table-of-contents)]

#### 1. Study
[[toc](#table-of-contents)]

- [Logic Lab](https://makecode.microbit.org/courses/logic-lab)  

#### 2. Apply
[[toc](#table-of-contents)]

**TODO: On paper, build and measure.**
**TODO: On breadboard, XOR with NPN and resistors.**
**TODO: On CiruictJS, a 6-NPN-transistor design of an XOR.**

#### 3. Present
[[toc](#table-of-contents)]

### Step 8: Half adder and full adder

#### 1. Study
[[toc](#table-of-contents)]

Show the process for the half-adder, all steps and whatever theory is necessary.  

#### 2. Apply
[[toc](#table-of-contents)]

**TODO: Full adder**
**TODO: Half subtractor**
**TODO: Full subtractor**

#### 3. Present
[[toc](#table-of-contents)]

### Step 9: Simulated logic gates

#### 1. Study

- booleans for bits!
- Boolean algebra!  
- simulating connections    
- `logic` function  

#### 2. Apply

**TODO: Build all gates**  
**TODO: Build XOR**  
**TODO: (Challenge) Build OR out of AND and OR**  
**TODO: (Challenge) Build gates out of NANDs**  

#### 3. Present


### Step 10: Full adder emulation

#### 1. Study

- bits and pieces of the program  

#### 2. Apply

**TODO: Full-adder emulation program**

#### 3. Present


### Step 11: ALU bit slice

#### 1. Study

<img src="images/alu-bit-slice.png" width="300" />

- all functions of an ALU  
- multiplexor/selector/decoder  
- carry  
- shift  

#### 2. Apply

1. `[<lernact-prac>]`Trace and highlight the active lines for the NOT function in the bit-slice diagram.  

2. `[<lernact-prac>]`Put 4 bit slices next to each other and connect them to form a 4-bit ALU. Answer the following questions:
   1. How many control lines do you have in total, and what are they? (Make sure they are properly connected in your diagram.)  
   2. How many data lines do you have in total, and what are they? (Make sure they are properly connected in your diagram.)  

3. `[<lernact-prac>]`**[Optional challenge, max 7 extra step points]** ALUs usually include comparison functions as well. They might or might not be performed inside the slices. Read this [post](https://www.electronics-tutorials.ws/combination/comb_8.html) on building a digital comparator. Modify the ALU bit-slice design from the diagram by removing the XOR function and substituting a LESS function instead.  

4. `[<lernact-prac>]`**[Optional challenge, max 3 extra step points]** The same as 11.2.3 without adding any gates, so that, with the removal of the XOR gate, the new bit slice has _one gate less_.  

#### 3. Present

In the [Lab Notebook](README.md) and [images](images) directory:

1. Show your work for 11.2.1 in well-formatted Markdown, including whatever images, tables, or other graphical elements you find necessary.  
2. Answer question 11.2.2.1.  
3. Answer question 11.2.2.2.  
1. Show your work for 11.2.2 in well-formatted Markdown, including whatever images, tables, or other graphical elements you find necessary.  
1. Show your work for 11.2.3 in well-formatted Markdown, including whatever images, tables, or other graphical elements you find necessary.  
1. Show your work for 11.2.4 in well-formatted Markdown, including whatever images, tables, or other graphical elements you find necessary.  


### Step 12: Emulated 4-bit ALU

#### 1. Study

- multiplexor

#### 2. Apply

1. `[<lernact-prac>]`Implement an emulator of a full adder for 4-bit unsigned integers. Requirements:
   1. Use the emulated full-adder bit slice from a previous step as a unit.  
   2. Build 5 external LED circuits to show the result, including overflow. Consider the leftmost LED bit position as an `[<cept>]`_overlfow flag_.    
   3. Pick operand `a` on the micro:bit screen.  
   4. Pick operand `b` on the micro:bit screen.  
   5. Show the result on the external LEDs.  

2. `[<lernact-prac>]`**[Optional challenge, max 5 extra step points]** Implement an emulator of a full adder for 4-bit 2s-complement signed integers. Apart from an extension of the full-adder slice, the requirements are the same as in 12.2.1. _Hint: Consider preprocessing the operands before doing the final addition._  

3. `[<lernact-prac>]`**[Optional challenge, max 10 extra step points]** Implement an emulated ALU bit slice, based on simulated logic gates, with the following functions, and the necessary control lines:
   1. Logical AND.  
   2. Logical OR.  
   3. Logical NOT.  
   4. Logical XOR.  
   5. 2s-complement binary addition.  
   6. Left shift by 1 bit at a time.  
   7. Right shift by 1 bit at a time.  
   8. **[Additional challenge, max 3 extra step points]** An 8-th function of your choice (e.g. NAND).    
   
4. `[<lernact-prac>]`**[Optional challenge, max 10 extra step points]** Implement an emulator of a 4-bit ALU using the bit slice from the previous exercise as a unit. The rest of the requirements are the same as in 12.2.1.  

#### 3. Present

In the [programs](programs) directory:

1. Add your program from 12.2.1 with filename `microbit-program-12-2-1.js`.  
2. Add your program from 12.2.2 with filename `microbit-program-12-2-2.js`.  
3. Add your program from 12.2.3 with filename `microbit-program-12-2-3.js`.  
4. Add your program from 12.2.4 with filename `microbit-program-12-2-4.js`.  

In the [Lab Notebook](README.md):

1. Link to the program from 12.2.1.  
2. Link to a demo video of the operation of the program from 12.2.1.  
3. Link to the program from 12.2.2.  
4. Link to a demo video of the operation of the program from 12.2.2.  
5. Link to the program from 12.2.3.  
6. Link to a demo video of the operation of the program from 12.2.3.  
7. Link to the program from 12.2.4.  
8. Link to a demo video of the operation of the program from 12.2.4.  
