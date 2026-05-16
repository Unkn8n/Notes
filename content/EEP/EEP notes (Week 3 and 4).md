# Week 3 and 4 : Expanding Microcontroller Applications

### What is Arduino?

Arduino is an open-source electronics platform based on easy-to-use hardware and software. Arduino boards are able to read inputs and turn it into an output.

![image.png](EEP%20notes.assets/image%20(6).png)

Components of the Arduino UNO R3:

1. ATmega328P Microcontroller
2. Power IN: The power to the Arduino board can be supplied via
   - USB Connector (5V): also doubles as a serial port to communicate with the computer.
   - DC Power Jack (7-12V via AC to DC adapter or battery pack)
   - Vin/GND pins (7-12V with 9V battery)
3. Power OUT

   • for powering external components

   • 5V and 3.3V pins (board regulated)

4. Reset Button

   • to reset/restart the program.

5. On-Board Built-In LED

   • indicate that the Arduino board is

   receiving power.

   • flicker during sketch upload and serial

   communication.

6. Digital INPUT/OUTPUT pins

   • to read/write digital signal to digital

   input/output components

   • pins marked with ~ can produce Pulse

   Width Modulated (PWM) output with

   duty cycle between 0 (off) to 255 (on).

   The PWM square wave can be used to

   simulate "analogue" output (e.g., to

   control the brightness of LED or speed

   of motor).

7. Analogue INPUT pins

   • to read analogue input

   • convert voltage signal from analogue

   sensor into useful digital signal via

   analogue-to-digital converter (ADC)

   • can also function exactly like digital pins

**Types of Inputs**

1. Digital Inputs

These components send a `HIGH` or `LOW` signal. Connect them to digital pins (2–13) and use `digitalRead()` or specific libraries.

- **Push-button:** Sends a `HIGH` or `LOW` state depending on whether it is pressed.
- **Touch Sensor:** Acts like a push-button but triggers when a finger alters capacitance.
- **IR Sensor Module:** Uses an infrared beam to detect obstacles or lines, outputting binary detection states.
- **Sound Sensor Module:** Detects sounds over a set volume threshold and outputs a digital trigger.



2. Analog Inputs

These components output a variable voltage (0V to 5V). Connect them to analog pins (A0–A5) and use `analogRead()`.

- **Potentiometer:** A manual dial that alters resistance to change the input voltage level.
- **Photoresistor:** Changes electrical resistance based on light levels to measure brightness.
- **Water Level Sensor:** Uses exposed trace lines to measure electrical conductivity based on water height.



#### Week 3B - Expanding Microcontroller Applications (pt1)

### **Learning to read Photoresistor**

A photoresistor is a light-sensitive type of variable resistor, sometimes called a LDR (light-dependent resistor), that provides analogue signal depending on light intensity.



To make a circuit involving a Photoresistor, you'll need the following:

- Arduino microcontroller
- Breadboard
- Jumper Wires
- Photoresistor
- LED
- Resistors (220 Ohm and 4.7k Ohm)

or use the thinkercad model

[Circuit design Photoresistor with Arduino (Blocks) - Tinkercad](https://www.tinkercad.com/things/2Nc3pC5EE1Y-)



or use the thinkercad model [https://www.tinkercad.com/things/2Nc3pC5EE1Y-photoresistor-with-arduino-blocks](https://www.tinkercad.com/things/2Nc3pC5EE1Y-photoresistor-with-arduino-blocks)

Resistors come in different resistance values.

![image.jpeg](EEP%20notes.assets/image.jpeg)

Source: [https://www.calculator.net/resistor-calculator.html](https://www.calculator.net/resistor-calculator.html)



![image.png](EEP%20notes.assets/image%20(7).png)

Source: [https://techexplorations.com/guides/arduino/common-circuits/voltage-divider-photoresistor/](https://techexplorations.com/guides/arduino/common-circuits/voltage-divider-photoresistor/)



Do note that the Photoresistor needs to be paired with another resistor to form a voltage divider.



A LDR changes resistance depending on light:

More light → lower resistance

Less light → more resistance



An Arduino analog pin measures voltage and not resistance, so we use a voltage divider to convert resistance changes into voltage changes.

The output voltage changes on the ratio of the two resistances, which will determine the voltage at A0.

A brighter environment results in lower LDR resistance, which changes the resistance ratio and shifts the voltage at the Arduino analog pin.

In darkness, the LDR resistance increases, again changing the ratio and shifting the voltage in the opposite direction.

---

#### Why not connect only the LDR?

5V –- LDR –- A0

At first glance it seems like it should work because LDR changes resistance.

However, an Arduino analog pin does not measure resistance - it measures voltage relative to GND.

For a meaningful voltage reading, there must be a complete circuit that creates a defined voltage at the input pin.

If the LDR is connected alone:

- There is no path to GND
- No voltage divider is formed
- The input voltage becomes undefined or unstable

So the reading will not reliably reflect light changes.

A voltage divider ensures a stable and measurable voltage that reflects changes in light.

---

#### Thermometer System

After learning to read a photoresistor and mapping out it's output to control the brightness of an LED, swap out the photoresistor for a TMP36 temperature sensor and add a few more LEDs to allow the lighting up of LEDs according to the temperature.

Components required:

• Arduino microcontroller

• Breadboard

• Jumper wires

• TMP36 temperature sensor (Ensure that it isn't a NPN transistor as it looks similar)

• LED (any colour) x3

• Resistors (220 ohm) x3

or use the thinkercad model

[Circuit design Temperature Sensor LED Bar Graph (Blocks) - Tinkercad](https://www.tinkercad.com/things/gI3ld4LXcH8-temperature-sensor-led-bar-graph-blocks)

Block code for thermometer system:

![image.png](EEP%20notes.assets/image%20(8).png)

Can be found if you click on the thinkercad link



**Step 1 (Setting up and displaying temperature):**

Set a baseline: This is where the program will compare the reading with.

Sensor reading: It reads the raw data from A0 and does an offset and a multiplier* and converts the voltage to a Celsius value.

> *To find the offset and multiplier,

> Take 2 different temperatures, a Cold point and a Hot point, then record the reference and raw reading.

![image.png](EEP%20notes.assets/image%20(9).png)

> The reference is the actual temperature while raw is the recorded one.

> Gain is the multiplier.

> This is known as a Two Point Calibration, I have linked a article covering it below if you're interested.

Conversion: It converts Celsius to Fahrenheit using the standard formula of

F = C * (9/5) + 32

Output:

It prints both Celsius and Fahrenheit values to serial monitor to track the values live.

**Step 2 (Temperature logic):**

The "If" statements help to manage the lighting of the LEDs.

Since the baseline is 40,

- If the temperature is below 40, all LEDs will be set to Low (off)
- If the temperature is between 40 - 49, pin 2 will be set to High (on)
- If the temperature is between 50 - 59, pin 2 and 3 will be set to High (on)
- If the temperature is between 60-69, all pins will be set to High (on)
- If the temperature is higher than or equal to 70, all pins will be set to High (on)

**Step 3 (Looping wait time):**

The last block will be the wait block where it helps to manage the block code by ensuring that the display is updated every second and prevents the code from running too fast.



If you're looking at the C++ codes, it's about the same and quite straightforward.



Extra:

[Sensor Calibration Techniques: Offset, Gain and Linearization - Zbotic](https://zbotic.in/sensor-calibration-techniques-offset-gain-and-linearization/#offset)

#### Week 4 [HBL week]-  Expanding Microcontroller Applications (pt2)

Lowkenuinely, I think can just follow the slides cuz ain no way im explaining allat.😭



And that's it… imma sleep.