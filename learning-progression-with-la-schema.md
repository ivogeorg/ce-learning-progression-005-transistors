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
10. Multimeter with needle-tipped probes.  

## Steps
[[toc](#table-of-contents)]

### Step 1: Transistors  
[[toc](#table-of-contents)]

#### 1. Study
[[toc](#table-of-contents)]

_Note: Watching the videos referenced at the begging of sections is the best way to understand this material. In some cases, there may be multiple videos that cover the same material, to give you extra depth. The text below briefly covers the main points, without going into detail._

##### Semiconductors

`[<lernact-see>]`Video of [semiconductor operation](https://www.youtube.com/watch?v=33vbFFFn04k) by [Ben Eater](https://eater.net/).    

`[<lernact-rd>]``[<cept>]`_Semiconductors_ are materials which occupy a middle ground between metals (conductors) and dielectrics, in terms of their `[<cept>]`_conductivity_ of electrical current.
 
Semiconductors are usually pure `[<cept>]`_chemical elements_ (like silicon, Si) which have been `[<cept>]`_doped_, that is, to which a small amount of another element has been added, to create a cumulative excess of free electrons (e.g. phosphorus, P), thus charging the material negative (`[<cept>]`_n-doping_), or a cumulative dearth of free electrons (e.g. boron, B), thus charging the material positive (`[<cept>]`_p-doping_).
 
When p-doped and n-doped regions are created next to each other, interesting electrical behavior occurs, mostly to do with the properties of the resulting  `[<cept>]`_depletion region_ at the `[<cept>]`_p-n junction_.  

Semiconductor `[<cept>]`_fabrication_ is a complex process. This [booklet](https://www.halbleiter.org/en/) is an accessible first look at the different steps.  

##### The diode

`[<lernact-see>]`Video of [bipolar diode operation](https://www.youtube.com/watch?v=-SSkjWuUri4).  

`[<lernact-rd>]`Diodes are elements which conduct current in only one direction. The simplest diodes are just PN junctions. The N side is called a `[<cept>]`_cathode_, while the P side is called the `[<cept>]`_anode_. When positive voltage is applied from cathode to anode, that is  + NP -, the excess electrons in the cathode region are attracted to the positive voltage terminal, drawing away from the center region of the diode. Similarly, the excess of holes (that is, the dearth of electrons) are attracted to the negative terminal, also drawing away from the center region. As a result, the depletion region, which is the center area where excess electrons recombine with excess holes to make the region electrically neutral, grows and prevents the flow of current through the diode. When voltage is applied in the opposite direction, that is - NP +, the depletion region shrinks or disappears completely, and current can flow.

##### The transistor

`[<lernact-see>]`Video of [transistor operation](https://www.youtube.com/watch?v=DXvAlwMAxiA) by [Ben Eater](https://eater.net/).  
`[<lernact-see>]`Video of [transistor operation](https://www.youtube.com/watch?v=7ukDKVHnac4).  
`[<lernact-see>]`Video of [NPN and PNP transistor operation](https://www.youtube.com/watch?v=R0Uy4EL4xWs).  

`[<lernact-rd>]`Transistors:
1. Are active circuit elements.   
2. Have 3 terminals.  
3. Use either current or voltage to control a larger current.   
4. Act as switches.  

We will exclusively focus on the so-called `[<cept>]`_bipolar-junction transistors (BJTs)_, which are either a thin N-doped region sandwiched between two thicker P-doped regions (PNP transistor), or a thin P-doped region sandwiched between two thicker N-doped regions (NPN transistor). The middle region is called the `[<cept>]`_base (B)_ and is the one which controls the current between the two outer regions, the `[<cept>]`_emitter (E)_ and the `[<cept>]`_collector (C)_. When the voltage difference between the base and emitter becomes 0.7 V, base current starts to flow, as a result of which a much larger collector current starts to flow also. Thus, BJTs are current amplifiers. 

For the NPN transistor, V<sub>BE</sub> = + 0.7 V and the base current flows out of the base. For the PNP transistor, V<sub>BE</sub> = - 0.7 V (or V<sub>EB</sub> = + 0.7 V) and the base current flows into the base.

##### Field-effect transistors

`[<lernact-see>]`Video of [MOSFET operation](https://www.youtube.com/watch?v=stM8dgcY1CA).  

`[<lernact-rd>]`As opposed to BJTs, `[<cept>]`_field-effect transistors (FETs)_ do not have base current. Instead, they employ variable voltage applied to the `[<cept>]`_gate_ terminal (analagous to the base in BJTs) to shrink or expand the conducting region between the other two terminals, the `[<cept>]`_source_ (analogous to the emitter in BJTs) and the `[<cept>]`_drain_ (analogous to the collector in BJTs).

##### A note on current direction

`[<lernact-rd>]`The convention is that `[<cept>]`_positive current_ flows in the direction opposite the flow of the electron charges. It is good practice to check whether a material refers to `[<cept>]`_conventional current_ or not.  

#### 2. Apply
[[toc](#table-of-contents)]

1. `[<lernact-texp>]`If you connect two bipolar junction diodes in series, either in PN-NP or NP-PN configuration, and connect a wire between them to act as the base, can you make a PNP or NPN transistor? Why or why not?  
2. `[<lernact-disc>]`BJT transistors use their base current to control the main circuit current, whereas FET transistors only use voltage and have no base current. Which of the two types would you think more likely to be the choice for the production of integrated circuits (like processors and memory sticks), where transistors are packed very densely and close to each other?  
3. `[<lernact-disc>]`**[Optional challenge, max 10 extra step points]** **TODO** SRAM cell and SRAM operation...  
4. `[<lernact-disc>]`**[Optional challenge, max 10 extra step points]** Processors and memory are the fundamental devices of computing. There is a constant urge to pack more and more transistors closer and closer together to get larger capacities in smaller packages. How are transistor density and the `[<cept>]`_dark silicon_ problem related?  

#### 3. Present
[[toc](#table-of-contents)]

In the [Lab Notebook](README.md):

1. Answer the questions in 1.2.1. Show your work in well-formatted Markdown, including whatever images, tables, or other graphical elements you find necessary.  
2. Answer the question in 1.2.2. Show your work in well-formatted Markdown, including whatever images, tables, or other graphical elements you find necessary.  
1. Answer the questions in 1.2.3. Show your work in well-formatted Markdown, including whatever images, tables, or other graphical elements you find necessary.  
1. Answer the questions in 1.2.4. Show your work in well-formatted Markdown, including whatever images, tables, or other graphical elements you find necessary.  


### Step 2: BJT circuits
[[toc](#table-of-contents)]

#### 1. Study
[[toc](#table-of-contents)]

`[<lernact-see>]`Video of [NPN and PNP Transistors as `[<cept>]`_common-emitter switches_](https://www.youtube.com/watch?v=kNVaIqmKUoI)

`[<lernact-rd>]`Our kit has 4 NPN and 4 PNP transistors, also LEDs and resistors. We'll use a single NPN transistor, and LED, a 330 Ohm resistor, and a 10 kOhm resistor to build our first transistor circuit. It will use a micro:bit output pin, digital or analog, to drive the circuit. In particular:
1. The transistor base will be connected _through a large resistor of 10 kOhms_ to the micro:bit pin. The resistor makes sure that the `[<cept>]`_base current_ is very low. Larger current will damage the transistor.  
2. The NPN transistor is a `[<cept>]`_current amplifier_, meaning that a small base current allows a much larger collector current to flow.  
3. The LED is connected _through a small resistor of 330 Ohms_ to the 3.3V power pin of the micro:bit and the collector of the NPN transistor. The resistor again limits the size of the current that flows through the LED, protecting it from damage. This part of the circuit is usually known as the `[<cept>]`_load circuit_, in the sense that this is what the transistor is turning on and off.  
4. Both the base current and the collector current flow into the emitter. So there are two closed loops of our circuit:  
   1. The base loop is 3.3V -- switch (via pin on/off) -- 10 kOhm resistor -- transistor base -- transistor emitter -- ground (GND pin of the micro:bit).  
   2. The collector loop is 3.3V -- 330 Ohm resistor -- transistor collector -- transistor emitter -- ground (GND pin of the micro:bit).  

Take a look at the following sketch:

<img src="images/npn-led-microbit.png" width="600" />

Note the following:
1. The micro:bit image in the sketch is without the connector, which has the pins in order.  
2. The pins used a 3.3V, GND, and P11.  
3. It matters how the LED and transistor are connected:  
   1. For the LED, always connect the longer leg toward power (3.3V) and the shorter toward ground (GND).  
   2. For the NPN transistor, read the [2N3904 datasheet](https://www.sparkfun.com/datasheets/Components/2N3904.pdf) to identify the base, collector, and emitter pins. The curved semi-cylindrical package makes this easy.    
4. The circuit operation can be seen in [this short video](https://msudenver.yuja.com/V/Video?v=2191285&node=8088986&a=1353912353&autoplay=1).  

#### 2. Apply
[[toc](#table-of-contents)]

1. `[<lernact-prac>]`Build the NPN circuit from the sketch and videos. Run P11 as `digitalWritePin`. Measure the following, in to different states: 
   1. With P11 **on** (that is, outputing logical 1 or approximately 3.3V):  
      1. The voltage between the 330 Ohm resistor and the LED. Calculate the voltage drop V<sub>R330</sub> across the resistor.  
      2. The voltage between the LED and the transistor collector. This is V<sub>C</sub>. Calculate the voltage drop V<sub>LED</sub> across the LED. Does it match the specification in the LED package in the lab kit?  
      3. The collector current I<sub>C</sub> flowing through the load circuit. Calculate the resistance of the LED.  
      4. The voltage between the 10 kOhm resistor and the transistor base. This is V<sub>B</sub>. Calculate:
         1. The voltage drop V<sub>R10K</sub> across the resistor.  
         2. The voltage V<sub>CB</sub> between the collector and base.  
         3. The voltage V<sub>CE</sub> between the collector and emitter.  
         4. The voltage V<sub>BE</sub> between the base and emitter. Is it what you expected from your knowledge of BJTs?        
      5. The base current I<sub>B</sub> flowing across the base resistor. Calculate the current amplification factor I<sub>C</sub>/I<sub>B</sub>.  
      6. The emitter current I<sub>E</sub> flowing through the common segment of the two closed loops of the circuit. Does _common emitter_ ring a bell? What is the relationship of the three currents I<sub>C</sub>, I<sub>B</sub>, I<sub>E</sub>? Is is what you expected from your knowledge of BJTs?  
   2. With P11 **off** (that is, outputing logical 0 or approximately 0.0V): 
      1. V<sub>C</sub>.  
      2. V<sub>B</sub>.  
      1. V<sub>E</sub>. Calculate V<sub>BE</sub>. Is it what you expected from your knowledge of BJTs?    

2. `[<lernact-prac>]`In the same circuit, run P11 as an `analogWritePin` with levels in the whole range [0, 1023]. Identify at what output level P11 turns on the LED (that is, the LED is visibly shining). For this level, what is the actual voltage at the pin?  

3. `[<lernact-prac>]`Where else can the load circuit be connected in the circuit without significantly changing the overall behavior?  

4. `[<lernact-prac>]`**[Optional challenge, max 7 extra step points]** Build the PNP circuit from the first video and perform the corresponding measurements as in 2.1.1. Refer to the [2N3906 datasheet](https://www.sparkfun.com/datasheets/Components/2N3906.pdf) for the terminal identification.    

5. `[<lernact-prac>]`**[Optional challenge, max 7 extra step points]** Build and simulate the circuit from 2.2.1 in the [CircuitJS simulator](http://lushprojects.com/circuitjs/circuitjs.html). Use a switch in place of the micro:bit pin.      

#### 3. Present
[[toc](#table-of-contents)]

In the [programs](programs) directory:

1. Add your program from 2.2.1 with filename `microbit-program-2-2-1.js`.  
2. Add your program from 2.2.2 with filename `microbit-program-2-2-2.js`.  
3. Add your program from 2.2.4 with filename `microbit-program-2-2-4.js`.  

In the [Lab Notebook](README.md):

1. Show all your measurements from 2.1.1.  
2. Link to the program from 2.2.1.  
3. Link to a demo video of the operation of the program from 2.2.1.  
4. Show all your measurements from 2.1.2.  
5. Link to the program from 2.2.2.  
6. Link to a demo video of the operation of the program from 2.2.2.  
7. Show your work from 2.2.3.  
8. Link to the program from 2.2.4.  
9. Link to a demo video of the operation of the program from 2.2.4.  
10. Show all your measurements from 2.1.4.  
11. Record a video of the circuit from 2.2.5 operating in the simulator with V<sub>B</sub> and V<sub>C<sub> shown in scopes and switch open and closed.  
 

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
- videos of gates from (FET) transistors  

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
