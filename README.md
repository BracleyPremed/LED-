# LED 

This project covers the basics of how to connect and blink an LED using an Arduino board.
![Final Project](https://github.com/BracleyPremed/LED-/blob/main/IMG_7454.HEIC)
---

## LED Component Basics

- **Long leg**: Positive (Anode)
- **Short leg**: Negative (Cathode)

 The **short leg** (negative/cathode) should be connected to the **GND (ground)** pin on the board.

---

## How to Choose a Resistor for an LED

Use **Ohm’s Law**:

V = IR


Where:
- **V** = (Board Voltage) - (LED Forward Voltage)
  - Example: (5V board - 2V LED = 3V needed across the resistor)
- **I** = Desired current (typically 10–20 mA for LEDs)

 **Resistor value controls LED brightness**.

**Typical LED forward voltage:** 1.8V to 2.2V.

---

## Arduino Code

This is the code used to **light up two LEDs**:

```cpp
int num = 7; 
int numP = 6;

void setup() {
  pinMode(num, OUTPUT);
  pinMode(numP, OUTPUT);
}

void loop() {
  digitalWrite(num, HIGH);
  digitalWrite(numP, HIGH);
}
Key Points About the Code
pinMode(pin, OUTPUT);: Initializes the pin as an output.

digitalWrite(pin, HIGH);: Turns the LED ON by sending 5V to the anode.

digitalWrite(pin, LOW);: Turns the LED OFF (0V).

delay(milliseconds);: (Optional) Use to control ON/OFF timing.
Example: delay(500); waits 500 milliseconds.

Example Circuit Layout

Notes
Always use a current-limiting resistor in series with an LED.

Typical resistor values for 5V Arduino boards:

220Ω (brighter)

330Ω (less bright but safer)

Adjust resistor value depending on the LED brightness you desire.

Quick Reference: Resistor Calculation Example

Board Voltage	LED Voltage	Target Current	Resistor Value
5V	2V	20mA	150Ω
5V	2V	15mA	200Ω
5V	2V	10mA	300Ω
(Values calculated with R = (5V - 2V) ÷ Target Current)


---
