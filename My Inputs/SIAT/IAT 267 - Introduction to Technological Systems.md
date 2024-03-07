---
created: 2023-12-31
status: 🔴
tags:
  - input
  - siat
links: "[[My Inputs]]"
professor: 
semester: Spring 2022
---
## Summary
### Context
- 
### Main Takeaways
- arduino is surprisingly easy and fun
### Questions/Connections/Thoughts
- 
## Notes

**

IAT 267 FINAL EXAM MASTER REVIEW

  

TECHNOLOGICAL SYSTEMS

  

Technological Systems: systems that use technology, we focus on computer-based 

Electronics: electrical circuits used to convey info for electronics

  

1. Embedded System: the processor is hidden in microcontroller

1. Microprocessor: a CPU on a single integrated circuit
    
2. Sensors:  detects physical event and converts to electrical signal
    
3. Actuator: output device to create a response 
    

  

2. Computer System: 

Purpose: turn data into information

Data: raw fact

Information: summarized data to use in decision-making

Hardware: physical components 

Software: electronic instructions

Operations: 

1. Input
    
2. Processing (data to information)
    
3. Storage (temporary: RAM, permanent: harddrive)
    
4. Output (actuators)
    
5. Communication (send and receive data)
    

  

General Principles of Computer Systems:

1. Universal Computing Device: all computers can compute the same given enough time and memory
    

Turing Machine: mathematical model of device to perform any computation

-write/read symbols on infinite tape

-state transitions based on current symbol

Turing Thesis: every computation can be done by a Turing machine

Universal Turing Machine: Turing machine that can implement all Turing machines

Input: data plus description of computation (other Turing Machine)

-programmable

-instructions part of input data

-the computers we know emulate this

2. Transformation Between Layers:
    

1. Problem
    

-natural language

-ambiguous, imprecise

2. Algorithm
    

-well-defined step-by-step procedure to produce specific result

3. Programming 
    

-express algorithm using computer language

4. Instruction Set Architecture (ISA) 
    

-specifies set of instructions computer can perform (data type, addressing mode)

5. Microarchitecture
    

-detailed organization of processor implementation

-different implementations of single ISA

6. Circuits
    

-combine basic operations to realize microarchitecture

7. Devices 
    

-properties of materials

-manufacturability 

  

Key Concepts:

1. Iterative Design
    

-imagine, design, build, get it to work

-process of design requires many iterations

2. Trade Offs
    

-solving one problem can create other problems

Space/Time: compress image to reduce transmission time/cost

-what are you sacrificing to improve other aspects?

-each solution has benefits and drawbacks

3. Real-World Constraints
    

-many interacting parts with their own issues (physical/processing constraints)

4. Feedback
    

Negative: if perturbed moves back to equilibrium state at bottom of hill (thermostat)

Positive: if perturbed moves away from equilibrium state at top of hill (explosion)

5. Controlling Complexity
    

Abstraction: ‘black box’ programmable devices that can be used without completely understanding what’s going on inside 

Modularity: composing systems of reusable mix-and-match parts

-breaking down problem into smaller pieces that can be used to solve many problems

  

BASIC ELECTRICITY CONCEPTS

  

1. Voltage: Volts (V)
    

-relative level of electrical energy between any 2 circuit points

-voltage source adds energy to current

2. Current: Amperes/Amps (A)
    

-rate of flow of charge through any point in circuit

3. Resistance: Ohms (Ω)
    

-amount that component resists flow of current 

Insulator: high resistance

Semiconductor: medium resistance

Conductor: low resistance

4. Electrical Power: Watts (W) = Volts (V) + Amps (A)
    

-combination of current and voltage

Ohm’s Law: less resistance = more current

Voltage (V) = Current (I) * Resistance (R)

V = A * O

V = I * R

  

Direct Current (DC): current on one wire, ground on other, constant voltage between

-supply is always higher voltage

-good for electronics

Alternating Current (AC): alternates voltage on two wires

-good for long-distance commercial electrical power transport

  

ELECTRICAL CIRCUIT

  

Characteristics: 

1. closed loop
    
2. contains a source of electrical energy (battery)
    
3. contains a load
    
4. flow of electricity 
    

-from positive to negative charge

-path of least resistance

-all electrical energy must be used (or components overheat to use extra energy)

5. described by schematic 
    

  

Types:

-multiple events are necessary to be series or parallel

  

1. Serial Circuit: components connected end-to-end
    

-electrons flow through one after the other

Resistance = R1 + R2 + R3

Voltage = V1 + V2 + V3

Current = I1 = I2 = I3

  

2. Parallel Circuit: components connected side-by-side
    

-current through all components at once

Resistance = (1/R1 + 1/R2 + 1/R3)^-1

Voltage = V1 = V2 = V3

Current = I1 + I2 + I3

  

Short Circuit: circuit with no load, wires melt because current keeps increasing

  

ELECTRICAL COMPONENTS

  

1. Diodes: permit flow of electricity in one direction and block in other direction
    

Anode: positive end

Cathode: negative end

2. Light-Emitting Diode (LED): diode that emits light when current flows through at correct voltage 
    

-so little resistance they require a 330 resistor to prevent short circuit

Longer prong: Anode/voltage (+)

Shorter prong: Cathode/ground (-)

3. Switches: control flow of current through junction in circuit
    
4. Resistors: limit current flow in circuit
    
5. Potentiometer: resistor that can change resistance
    

Outer leads: fixed value resistor (VCC and ground)

Center lead: connects to wiper, slides along fixed resistor (read by microcontroller)

6. Solderless Breadboard: circuit board for prototyping
    

  

INTERACTION WITH COMPUTERS

  

-think computing, not computer

-computer can take on any form we need to solve issue

Computing as Medium:

1. can store sounds and images
    

Random Access Media: non-sequential parts of computer memory can be called up as if next to each other

Linear Media: tape, film

2. reduce barriers of time and space
    

-networking

3. create more complex relationships between sensed and caused events
    

-lowering blinds when sunny, turn on light when person enters room

  

Elements of Interaction: 

Interaction: conversation between physical and virtual world

Transduction: conversion of one form of energy into another, enables interaction

Physical World: many forms of energy (mechanical, light, pressure)

Computer System: electrical energy only

1. Digital Transducer: limited number of states (usually 2), “whether or not”
    
2. Discrete Transducer: like digital but many states 
    
3. Analog Transducer: continuous range of states, “how much?” (stronger, faster, brighter)
    

  

1. Input: Listening
    

Transducers: 

Sensors: converts physical phenomena into an electrical signal

-switches, levers, sliders

-takes less energy than output

2. Processing: Thinking
    

-requires a computer and programming to read input, make decision and activate

output

3. Output: Speaking/Acting
    

Transducers: Actuators: converts electrical signal into physical phenomena

-motor, buzzer

-creates light, sound, movements

  

Types of Inputs/Outputs:

1. Type of Reading
    

1. Analog: output is continuous
    

-requires analog to digital conversion for computer interface

-often output is variable resistance to control voltage

2. Digital: output is digital signal (0 or 1)
    

-most work with a threshold 

2. Electrical Properties
    

1. Passive: produce signal only when subjected to sensed quantity
    

-no external power needed

2. Active: always sending out signal to sense quantity  
    -needs external power
    

3. Event Ordering: how input/output flows over time
    

1. Serial: events happening one after another
    
2. Parallel: events happening simultaneously
    

  

In Practice: Project Stages:

1. Decide what happens from user’s POV
    
2. Decide what changes as user takes action (output)
    
3. Focus on what not how
    
4. Break into stages of input, processing and output
    
5. Identify outputs as analog or digital
    
6. Begin search for transducers
    

  

TOOLS OF INTERACTION

  

1. Transducers
    
2. Microcontroller
    
3. Circuit
    
4. Programming
    
5. Serial Communication
    

  

SENSORS:

1. analog
    
2. digital
    
3. passive
    
4. active
    

  

Sensor Output:

1. resistance change
    
2. voltage change
    
3. capacitance change
    
4. current change
    

  

Voltage Divider and Analog Sensors:

-analog sensors work like variable resistor

-resistance directly influenced by condition it measures

Voltage Divider Circuit: used to turn changing resistance of sensor into proportional change of voltage that can be better understood by ICs/microcontrollers 

Voltage Divider Principle: Vout = R2/(R1 + R2) * Vin

  
  

Analog Sensors used in Class:

  

1. Rotation Sensor (variable resistor):
    

-rotates 300º

Type: resistive 3-pin

fully clockwise: minimum resistance

fully counterclockwise: maximum resistance (10kΩ)

  

2. Slider (variable resistor):
    

Type: resistive 3-pin

one side: 0

other side: max resistance (10kΩ)

  

3. Temperature Sensor:
    

-measures ambient temperature from -40ºC to 125ºC

-outputs voltage directly proportional to temperature (temp increase = voltage increase)

-not that accurate

Formula: temperature in ºC = (sensorValue - 200) / 4

  

4. Touch Sensor:
    

touched: 0 resistance

not touched: max resistance

-will work through ¼ inch of glass

  

5. Force Sensor:
    

no force: max resistance

more force: less resistance, value/voltage increases

-not designed for constant force over time

  

6. Light Sensor:
    

Type: resistive 2-pin

no light: 500kΩ resistance

10 lux: 10kΩ - 5kΩ resistance

-resistance is in voltage divider with 7.5kΩ resistor

  

Underlying Physical Principles:

  

1. Piezoelectric Sensors:
    

Piezoelectric Effect: energy converted between mechanical and electrical forms

-discovered in 1880s by Curie brothers

-can measure force, flexure, acceleration, heat, acoustic vibrations

-transducers can be electric to mechanical (speaker) or mechanical to electric (microphone)

How it Works: Crystals have a permanent electrical polarization

1. cells of crystal have dipole oriented and aligned
    
2. this excess surface charge attracts charge from atmosphere, canceling charge and making crystal electrically neutral. 
    
3. when pressure is applied, cells deform which disrupts orientation, making charge no longer canceled
    
4. excess surface charge = voltage
    
5. must be able to measure crystal surface charge for this to be useful
    

  

2. Force Sensing Resistors
    

-composed of 2 parts:

1. Resistive material applied to a film
    
2. Set of digitizing contacts applied to another film
    

How it works: resistive material makes an electrical path between 2 sets of conductors on another film. More force applied = better connection = increased conductivity 

Conductivity:  reciprocal of resistance (1/R)

Methods to Sense Force:

Force (F): vector quantity (magnitude and direction)

1. Acceleration: measure acceleration of known mass on which unknown force operates
    
2. Gravity-Balance: compare unknown force with action of gravitational force on known mass
    
3. Pressure-Sensing: convert force to fluid pressure measured using pressure transducer
    

  

3. Temperature Sensors:
    

1. Thermal Resistors: change resistance with temperature change
    

1. Resistance Temperature Device (RTDs): based on tendency of naturally occurring materials to change physical dimensions with temperature change
    

-change physical dimensions with temperature change

2. Thermistor: made from human-made semiconductor substance
    

-negative temperature coefficient (resistance decreases as temperature increases)

2. Thermocouple: most popular temperature sensors
    

-cheap but limited accuracy (~1ºC)

Seebeck Effect: junction between 2 metals creates voltage which is a function of temperature

  

4. Light Sensing:
    

Light: form of electromagnetic radiation

1. Quantum Detectors: convert incoming radiation into electron in semiconductor device, process resulting current with electronic circuitry
    

-most popular

-best performance for detection of optical radiation

-photon is absorbed and electron is liberated in the structure with energy of the photon

2. Thermal Detectors: absorb energy and measure change in temperature with thermometer
    

-limited by availability of sensitive and small heat capacity thermometers

  

Quality Parameters of Sensor System:

  

1. Transfer Function: functional relationship between physical input signal and electrical output signal 
    

-sensor calibrated using known inputs/outputs

-expensive, individually calibrated sensors use certified calibration curve

2. Sensitivity: relationship between changes in physical input signal and electrical output signal
    

-ratio of small change in electrical signal to small change in physical signal

slope = sensitivity, S = y/x or S = do/di

3. Accuracy: difference in measured value and actual value
    

-defined as percentage of actual value

4. Precision: ability of instrument to reproduce certain readings within given deviation
    
5. Repeatability: ability to reproduce output the same when same input is given under same environmental conditions
    
6. Range & Span: limits between which inputs/outputs can vary.
    

Span: maximum value - minimum value of input

7. Stability (drift): ability to give the same output when constant input is measured over a period of time
    

Drift: expressed as percentage of full range output

8. Hysteresis: different output for increasing and decreasing value of input (with magnetized sensors)
    

  

SENSING TOUCH:

  

Haptics: study and implementation of interaction techniques involving touch

  

1. Force-Sensitive Resistor: converts mechanical force into electrical resistance
    

-small, flat

2. Flex Sensor: vary resistance based on amount bent (up to 180º)
    

-10kΩ to 40kΩ resistance

-used in VR gloves

3. Pressure Sensors: measure pressure exerted by gas or fluid 
    

-most common in hydraulic or pneumatic applications

4. Capacitance Sensor: (most popular) can sense lightest touch using electric charge stored in body
    

-small electrical charge in human body disrupts internal capacitance value so the reading changes

-can detect touch or almost touch

-no moving parts, can be hidden within material 

-works with anything that carries a static charge

5. Heat Sensor: measure touch with increase in heat using thermal sensor
    

  

SERVO MOTORS:

  

-actuator for producing precise movement

-can be positioned 0-180º

-3 wire PWM (only works on PWM pins) 

-5V interface

-easy, precise, controllable, repeatable movement

How it works: PWM, voltage pulse only goes in long enough to move to desired angle

How to code:

1. Pulse: write pulse to motor of desired length in microseconds (us)
    
2. Angle: value between 0 and 180º
    

Arduino Servo Library: allows control of servos

#include <Servo.h>

Servo servo;

servo.attach(pin number);

servo.write(angle value);

servo.read(); returns servo angle value

  
  

ARDUINO![](https://lh7-us.googleusercontent.com/dJAB4c8dbpDgEAMO8DP3EF3IZhcEFzR2xMwRi2u53M0RPaTgrfAxiEgP4QKPPJ0WeSfw5MqJixYWAbMG4O4FMejhRJ5BEZCvfnuOeSpxzNbs65mU3DTPVg3wSU_G-kAp3JsndvktwFKBQP5YvDZKbA)

  

1. Arduino Controller: the hardware (circuit board with programmable chip)
    

Microcontroller: small inexpensive computing device

-for sensing input and controlling output devices

-Arduino microcontroller is the brain of the system you build

2. Arduino Working Environment: simple open-source IDE built in Java
    
3. Language and Compiler: create code for microcontroller
    

  

Arduino IDE (Wiring/Micro C):

Keywords: reserved words

Sketches: Arduino programs

-reads program from top down

1. Initialization: declare variables outside of setup() and loop()
    
2. Setup(): runs once
    
3. Loop(): runs repeatedly
    
4. Functions: add custom functions for greater control/complexity
    

  

Flow Control: 

1. connect Arduino to computer with USB
    
2. select board under ‘tools’
    
3. edit code
    
4. compile
    
5. upload to board
    

  

Comments:

// single line comment

/* */ multiline comment

-title and description header on all programs 

-explain what each method does

  

Constants:

HIGH/LOW: define voltage level for digital pins

HIGH: 5V

LOW: 0V

INPUT/OUTPUT: setting dual purpose pins to preferred setting

INPUT: receiving signal

OUTPUT: sending signal

LED_BUILTIN: for control of built in LED 

  

Methods:

  

pinMode(pinNumber, INPUT/OUTPUT): declare if pin is input or output

pinMode(pinNumber, INPUT-PULLUP): activates a built-in pullup resistor of 20KΩ

  

delay(milliseconds): wait for number of milliseconds before continuing to execute

-1000 milliseconds = 1 second

  

millis(): returns number of milliseconds since program started running

-useful if need to keep track of time

  

|   |   |
|---|---|
|Reading Input|pinMode(pin, INPUT)|
|digitalRead(pinNumber)<br><br>-reads state of digital pin in input mode<br><br>-simple on (5V) or off (0V)|analogRead(pinNumber)<br><br>-reads value of analog pin, returns range 0-1023 (voltage being passed into pin)<br><br>-0 = 0V, 1023 = 5V<br><br>-only send analog signals in 0-5V range, otherwise issues will arise|
|Sending Output|pinMode(pin, OUTPUT)|
|digitalWrite(pinNumber, HIGH/LOW)<br><br>-turn pin on or off|analogWrite(pinNumber, value 0-255)<br><br>-only works on pin 3, 5, 6, 9, 10, 11 (with ~ symbol)<br><br>-writes analog value to output pin between 0 (0V) -255 (5V)|

  

Arduino Inputs and Outputs:

  

|   |   |
|---|---|
|Digital Pins (input or output)|Analog Pins (input only)|
|Input: on/off switch<br><br>Pin: can input or output<br><br>  <br><br>0 = 0V<br><br>1 = 5V<br><br>HIGH = 5V<br><br>LOW = 0V<br><br>  <br><br>transducers: switch<br><br>  <br><br>Output: fan, radio, light, motor, can be directly connected (LED)<br><br>-Arduino interrupts power to device|Input: range of values<br><br>Pin: only input (no voltage from pin)<br><br>  <br><br>0 = 0V<br><br>1023 = 5V<br><br>  <br><br>transducers: variable resistor, light/force/flex sensor, thermistor<br><br>-variable resistors have high resistance so use 10kΩ resistors with them<br><br>  <br><br>-Arduino has built-in analog to digital converter (ADC) measures range of voltage and converts voltage value to 10-bit digital value<br><br>-use voltage divider setup (Arduino can only read voltage)<br><br>  <br><br>Pulse Width Modulation (PMW): turns on/off so fast it creates less voltage<br><br>-digital to analog converter takes duty cycle between 0 and 255<br><br>Duty Cycle: how much (%) of pulse is high (5V), how much is low (0V)|

  
  

SERIAL COMMUNICATION

  

-computer communicating with microprocessor

-digital pulses back and forth at agreed upon rate, 1 bit at a time (0s and 1s), 

Serial: one after the other

  

Digital Pin 0 (TX) and 1 (RX): leave empty if doing serial communication

-lights for TX and RX light up when serial communication is happening

Limits: needs to use USB cable, can only send 1 bit at a time 

1. 0/TX: transmitter (from Arduino)
    
2. 1/RX: receiver (to Arduino)
    

  

Protocols: parameters the two devices agree on in order to send information

1. Physical Connection: connection of microcontroller to computer
    

-port selection

2. Timing: bits per second
    

-data doesn’t make any sense if not set to same number

-set baud rate/bit rate: Serial.begin(9600);

-typically 8 bits grouped together into a byte, one byte per millisecond

Asynchronous: each device has own clock

3. Electrical Connection: voltage level of electrical pulses
    

5V = 1 bit

0V = 0 bit

4. Package Size: how big of data you are sending/how to group the bits
    

-grouping at 8 bits (Byte) is default option

-can send numbers 0-255 and characters

  

Data Measurement:

  

Bit: 0 or 1

Byte: 8 bits

Kilobyte: 1024 bits

Megabyte: 1024 kilobytes

Gigabyte: 1024 megabyte

  

Debugging Serial Communication:

-difficult because could be at computer, circuit or microprocessor level

-look at TX/RX LEDS, print to serial port

  

Arduino Serial Library:

Serial.begin(9600): set bit rate in setup()

Serial.read(): reads incoming serial data, returns int of first byte of incoming serial data available (as ASCII character) (or -1 if no data available)

-receives data, reads it from computer, received as bytes

Serial.parseInt(): transfers ASCII character to int, slightly slower than read()

Serial.available(): gets number of bytes available for reading by port (already arrived and stored in serial buffer)

Serial.end(): disables serial communication

Serial.peek(): returns next Byte (character) of data without removing it from buffer

Serial.print(): prints data to port as human readable text (converted to string)

Serial.println(): prints with /n character appended to end (converted to string)

Serial.write(): send Byte/regular integer to computer

Serial.write(data, length): useful for large amounts of data 

  

SerialEvent(): callback function called after loop when there is serial data in buffer

  

PROCESSING: simplified Java for visually-oriented applications

  

1. Processing Development Environment
    
2. Collection of Functions
    

-basic functions are core programming interface (API)

-libraries with advanced features

3. Language Syntax
    

-Java for babies

4. Online Community
    

  

setup()

framerate(fps)

size(w, h)

draw()

point(x, y)

line(x1, y1, x2, y2)

triangle(x1, y1, x2, y2, x3, y3)

rect(x, y, w, h)

rectMode(CORNER, CENTER)

ellipse(x, y, w, h)

ellipseMode(CENTER, CORNER)

  

print(): print to console

println(): prints to console with /n appended on end

delay(milliseconds)

noLoop(): stop calling draw()

loop(): call draw again

  

color: additive RGBA model

background(r, g, b)

stroke(r, g, b)

strokeWeight(w)

noStroke()

fill(r, g, b)

noFill()

  

callbacks:

setup(), draw()

mousePressed, mouseClicked, mouseReleased, mouseDragged

keyPressed, keyReleased

  

Data Types:

int: -2M - 2M

float: decimal point

  

char: one character

-characters stored as numbers, see encoding in ASCII chart

-can do arithmetic on characters using ASCII value

val = val - ‘0’: converts from char to number

  

byte: -128 - 127

boolean: true or false

String: “enclosed in quotes”

  

Processing and Serial Communication: one program per serial port at a time (can’t print to serial port and run with Processing)

  

Processing Serial Library: manually import, enables microcontroller connection

1. import Processing serial library
    

import processing.serial.*;

2. create port object
    

Serial myPort;

3. initialize port object
    

myPort = new Serial(this, “name”, 9600);

4. read/write data
    

while(myPort.available() > 0){

myPort.read();

myPort.write()}

  

Data Flow:

|   |   |
|---|---|
|Processing to Arduino|Arduino to Processing|
|-mouse/keyboard interactions<br><br>-code to control outputs|-sensor data|

  

Serial Communication:

  

1. Arduino to Processing:
    

|   |   |
|---|---|
|Arduino|Processing|
|void setup(){<br><br>Serial.begin(9600);<br><br>}<br><br>  <br><br>void loop(){<br><br>Serial.println(analogRead(A0));<br><br>delay(10);<br><br>}|void serialEvent(Serial myPort){<br><br>String incoming = myPort.readStringUntil(‘\n’);<br><br>  <br><br>if (incoming != null){<br><br>incoming = trim(incoming);<br><br>float in = float(incoming);<br><br>in = map(in, 0, 1023, 0, height);<br><br>}}<br><br>}|

  

2. Processing to Arduino:
    

|   |   |
|---|---|
|Processing|Arduino|
|import processing.serial.*;<br><br>Serial myPort;<br><br>  <br><br>void setup(){<br><br>myPort = new Serial(this, “name”, 9600);<br><br>}<br><br>  <br><br>void draw(){<br><br>myPort.write();<br><br>}|int incoming;<br><br>  <br><br>void setup(){<br><br>Serial.begin(9600);<br><br>}<br><br>  <br><br>void loop(){<br><br>if (Serial.available() > 0){<br><br>incoming = Serial.read();<br><br>}<br><br>}|

  

Data From Multiple Sensors: group in different packets

|   |   |
|---|---|
|Arduino|Processing|
|pin A0 = 255 <br><br>Serial.print(“a”);<br><br>Serial.print(A0);<br><br>Serial.print(“a”);<br><br>Serial.println();  //denotes end of one sensor data<br><br>pin A1 = 60<br><br>Serial.print(“b”);<br><br>Serial.print(A1);<br><br>Serial.print(“b”);<br><br>Serial.println();<br><br>  <br><br>Serial.print(“&”); //denotes end of package<br><br>  <br><br>delay(100);  //wait 100 ms until next reading (allows time for processing)|Variable to hold values received from serial port:<br><br>byte[] inBuffer = new byte[15]; //size of the serial buffer to allow for end of data characters and all chars (see arduino code)<br><br>  <br><br>Use splitTokens() method to look for certain characters in string of values<br><br> port.readBytesUntil('&', inBuffer);  <br><br>//read in all package data until '&' is encountered (end of package)<br><br>  <br><br>if (inBuffer != null) {<br><br>      String myString = new String(inBuffer);<br><br>//convert data to a string so we can use splitTokens()<br><br>String[] p = splitTokens(myString, "&");  //p is all sensor data (with a's and b's) ('&' is eliminated)<br><br>p = [“a255a\nb60b\n”]<br><br>String[] light_sensor = splitTokens(p[0], "a");  //get light sensor reading <br><br>light_sensor = [“\n”, “255”, “b60b\n”]<br><br>  <br><br>valP_light= int(light_sensor[1]); //add to reading array<br><br>(valP_light = 255)<br><br>  <br><br> String[] slider_sensor=splitTokens(p[0], "b");  <br><br>//get slider sensor reading<br><br>  <br><br>valP_slider=int (slider_sensor[1]);<br><br>//add to reading array|

  

PRESENCE AND MOVEMENT

  

-how to detect objects in space

  

Movement: sensor determined by how much we have to know about motion

1. position
    
2. orientation
    
3. velocity
    
4. absolute/relative position
    
5. identity (discern between objects)
    

  

1. Ranging/Distance Sensors: sense distance of body from sensor and movement in front of sensor
    

-do not operate uniformly at all distances, have zones where most sensitive (view cone)

-can only detect distance not position in 2D space 

Trilateration: using 3 sensors to obtain exact position

Range: ~9ft

Constraints: apply constraints to environment to minimize technological complexity (limit people, entrances/exits)

Operating Principle:

1. send out reference signal (light, magnet, sound)
    
2. measure amount of energy that reflects off target, compare to original signal (or how much time sound takes to bounce back)
    
3. difference converted into electrical signal read by microcontroller
    

  

2. Detecting Presence: can use distance sensor for this
    

-binary output (present or not)

1. Switches:
    

1. foot switch on floor (inefficient, must be robust)
    
2. photoelectric (light beam hits target sensor, when beam broken switch activated)
    
3. magnetic (magnetic object detected, activates switch)
    

3.  Motion Detector: (most common) respond to change in infrared light
    

1. Active: sends out signal, reflects back from object, measure intensity
    
2. Passive: human temperature emits some infrared light, detect intensity to determine motion
    

  

3. Determining Position: where a person is in space
    

-position/motion information means we can determine velocity and speed

1. Digital Sensors: (multiple floor switches)
    
2. Infrared Sensors: (send out infrared beam, read reflection of beam off target)
    

Range: 1.5” - 56”

-3 wires (digital use needs close proximity, analog use measures closeness between 0-1023 (higher = closer))

3. Ultrasonic Sensors: send ping of sound, measure time to come back
    

Range: ~6ft - 34ft

-can still run with infrared interference (sun)

  

4. Rotation:
    

1. Potentiometer: impractical, can’t move 360 degrees
    
2. Accelerometer: measures change in speed of movement (acc)
    

-typically 2-3 axes of measurement based on gravity

3. Video Tracking: can capture position, rotation, distance
    

Computer Vision Techniques: extract info about scene from video

Difficulty: light/shadow change, use infrared light in dark

Factors to Consider:

-strong, even light, high contrast

-infrared light (attach infrared light source to target)

Method: 

1. computer reads camera’s images
    
2. image stored in 2D array of pixels
    
3. each pixel has brightness, colour
    
4. compare characteristics of pixels (assuming objects are unique)
    
5. continuously detect color of pixel in center of object
    
6. find color match in next frame, object is there
    

In Processing:

1. import vid library
    
2. write code to read camera (each time new frame available video library generates a captureEvent)
    
3. add method to capture pixel colour at mouse click point 
    
4. add new global variables for x, y (position)
    
5. add mouseReleased() method at end of sketch
    
6. add code at end of draw to draw the tracking ellipse
    
7. scan all pixels in image, check RGB components
    
8. add findColor() method that takes target colour as parameter and returns pixel matching the colour as return value
    

  

5. Identity: discern specific object
    

Challenge: more than one object to track/identify

-many sensors do not support multiple targets (infrared, ultrasonic)

1. Presence: is it near me?
    
2. Address: where is it?
    
3. Identification: what is it?
    

  

Humans: look, feel, smell, taste, sound of objects

Computers:

1. optical recognition
    

-video colour tracking

-shape recognition

-barcodes

2. RFID
    

  

Methods:

  

1. Computer Vision: detects colour, shape
    

By color: simple computationally

By shape: more complex as geometry has to be known from every angle

pro: adjustable distance to object

con: complex, line of sight

  

2. Barcodes: pattern of lines to encode alphanumeric string
    

-computer scans image, interprets light and dark bands as 0 or 1

1D barcode: lines

2D barcode/Quick Response Code (QR): square, contains hyperlink

con: needs to see object, limited by camera quality

  

3. Radio Frequency Identification (RFID): reader sends short-range radio signal picked up by RFID tag, tag transmits back short string of data
    

pro: tags do not need to be visible

1. Passive: tag has integrated circuit with radio transceiver and small amount of nonvolatile memory
    

-powered by current from reader’s signal

-energy is just enough to power tag to transmit data once

2. Active: tag has own power supply and radio transceiver
    

-transmits signal in response to messages received from reader

pro: longer range

con: more expensive

  

NETWORKING

  

DATA EXCHANGE:

  

User/Application:

User: gets feedback and output from application

1. understand what application is doing
    
2. understand how user actions are interpreted
    
3. understand how to get application to do what user wants
    

Application: gets input from user on what to do

  

Machine/Application:

1. Context (continuous/non-continuous, synchronous/asynchronous, peer-to-peer, client-server)
    
2. Means of communication (how?)
    
3. Machines used (between what devices?)
    
4. Amount of data being exchanged
    

  

Why networking?

-remote data

-remote access

-remote control

Benefits:

1. enables applications to work remotely
    
2. gather data from internet
    
3. network multiple devices and machines
    

  

1. Simplest Network: one-to-one connection between two objects
    

Rules/Layers of Agreement:

1. Physical: 
    

-connections of physical inputs/outputs

-how many connections between the two devices

Arduino: receives data on digital pin 0 (RX), sends it out on digital pin 1 (TX)

2. Electrical: 
    

-what voltage levels are sent to represent bits of data

Arduino: 0V and 5V to represent bits

3. Logical: 
    

-what do changes in voltage mean?

Arduino: 5V signal is 1, 0V signal is 0

4. Data: 
    

-timing of bits

-how many bits make up a data (packaging)

Arduino: data send 9600 bits per second, each package contains 8 bits

5. Application: 
    

-how are groups of bits arranged into messages (the part the user interacts with)

Arduino: one byte sent from PC to Arduino and processed

  

2.  More Complex Network: The Internet: need network map to keep track of multiple things connected
    

1. Directly Connected Network: every device is connected to every other device
    

pro: still path if one connection is broken

con: redundant connection is not cost/effort effective

2. Star Network: all devices are connected through one central device
    

pro: less redundancy

con: if center goes down all go down, if connection severed no backup

3. Ring Network: each device is connected to 2 others
    

pro: backup connection is one is severed

con: inefficient

  

NETWORKING PROTOCOLS:

  

Addressing: application on one machine sends message to other machine’s application, needs an address to identify receiving application

  

To Identify Receiving Application We Need:

1. name/address of host machine
    
2. identity of receiving process on host (on Internet applications the destination is specified by IP address)
    

  

1. Hardware Address: based on physical hardware
    

-only changes if hardware changes

-00:11:24:9b:f3:70

  

2. IP Address: based on network connected to
    

-changed when connected to a different network 

IPV4: 4 numbers from 0-255 (192. 168.1.20)

IPV6: more numbers, used in case we run out one day

  

Ports: computer has single physical connection to network

-all data desired for particular computer arrives through this connection

-computer identified by 32-bit IP address

-ports identified by 16-bit address

  

Data Sending and the Internet:

  

Packets: the data being sent over the Internet broken into smaller pieces for easier sending

-can see this work through ping command

Ping Command: tests whether Internet host is reachable, measures round-trip time to host to see how ‘far away’ host is

  

Getting an HTML file:

-application running on local computer connected to Internet through wireless router

1. app sends data to router
    
2. router sends message to network provider
    
3. message is routed to correct network provider for the server you want to make a request from
    
4. the server will receive request for the file
    

![](https://lh7-us.googleusercontent.com/32q2AH2F0wa8l5IbF840Vfvfq7F95Bv3GGDvKMjIa4RdMxPVdcBSf5CdcW9sCwznUSfpgCWPgAFnte_DC6CsW_uINiaD8eSTreqrRuOpZ6dZl2trAFouKa7RDgAnSjksYhgTnyWYL_NrJtjH0OonGg)

  
  

Network Communication in Processing: Network Library

-application can communicate with other Processing applications

-can download data from Internet

-can send data to be stored or processed remotely

  

1. Client Class: used to create client object that connects to server to exchange data
    

-sends the request, waits for/receives replies

-connects to small number of servers at one time

-interacts directly with end-users using GUI

Client client = new Client(this, “server name”, port number)

available()

read()

readChar()

readBytes()

readBytesUntil()

readString()

readStringUntil()

write()

clear()

stop()

ip()

  

2. Server Class: used to create server objects that can send and receive data to and from any client connected to it
    

-receives client requests, processes and serves replies (passive)

-accepts connection from many clients

-does not interact directly with end users

Server server = new Server(this, port number)

write()

available()

stop()

disconnect()

  

Structure of Network Application:

1. User Interface: what the user sees and interacts with 
    
2. Application Logic: what data action to take based on user interaction
    
3. Application-Level Protocol: how data communicates with server
    

  

Network Layering:

1. Application (HTTP)
    
2. Transport: responsible for getting packets to destination, 2 protocols 
    

1. Transmission Control Protocol (TCP): reliable!
    

-connection-oriented service (handshaking before beginning data transfer)

-reliable data transfer, same order, all info is sent

-both ways messages are sent

-congestion and flow control systems regulating transmission

2. User Datagram Protocol (UDP): fast!
    

-lightweight transport protocol with minimalist service model

-connectionless, no handshaking before communication

-unreliable, no guarantee/confirmation of arrival, order may change

-no flow/congestion control, info can flow at any rate

-good for real-time applications (fast) like streaming

3. Network (IP address)
    
4. Link (device)
    

  
  
  
  
  
  
**