<h1 align="center" > <strong> LED </strong> </h1>



<p>This project covers the basics of how to connect and blink an LED using an Arduino board.</p>

![Final Project](https://github.com/BracleyPremed/LED-/blob/main/RD.png)
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

```
</br>


<h3>Key Points About the Code</h3>

```cpp
pinMode(pin, OUTPUT); //Initializes the pin as an output.
```

```cpp
digitalWrite(pin, HIGH); // Turns the LED ON by sending 5V to the anode.
```

```cpp
digitalWrite(pin, LOW); // Turns the LED OFF (0V).
```

```cpp
delay(milliseconds); //(Optional) Use to control ON/OFF timing.
                    //Example: delay(500); waits 500 milliseconds.
```

<h4> Note </h4>
<p>Always use a current-limiting resistor in series with an LED. </p>




<p><strong>Sam Cherilus </strong></p>


