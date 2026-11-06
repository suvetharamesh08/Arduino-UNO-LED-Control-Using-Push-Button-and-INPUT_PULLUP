# 💡 Arduino Push Button Controlled LED System

### Interactive LED Control Using Arduino UNO and Push Button

---

## 📌 Project Overview

The **Arduino Push Button Controlled LED System** is a beginner-friendly embedded systems project that demonstrates digital input and output interfacing using Arduino UNO.

In this project, a push button is used to control an LED. When the button is pressed, the LED turns ON, and when the button is released, the LED turns OFF.

The system uses the Arduino's internal pull-up resistor through the `INPUT_PULLUP` mode, eliminating the need for an external pull-up resistor.

This project provides practical knowledge of digital signal reading, conditional statements, and basic hardware interfacing.

## 🎯 Project Objectives

- To understand digital input and output operations.
- To interface a push button with Arduino UNO.
- To control an LED based on button input.
- To understand the `INPUT_PULLUP` configuration.
- To implement conditional logic using `if-else` statements.

## 🛠️ Hardware Requirements

| S.No | Component | Quantity |
|---|---|---|
| 1 | Arduino UNO | 1 |
| 2 | LED | 1 |
| 3 | Push Button | 1 |
| 4 | 220Ω Resistor | 1 |
| 5 | Breadboard | 1 |
| 6 | Jumper Wires | As Required |
| 7 | USB Cable | 1 |

## 💻 Software Requirements

- Arduino IDE
- Arduino C/C++ Programming
- Arduino UNO Board Support Package

## 🔌 Pin Configuration

| Component | Arduino Pin |
|---|---|
| LED | Digital Pin 5 |
| Push Button | Digital Pin 6 |

**Note:** The push button is connected between digital pin 6 and GND because the program uses `INPUT_PULLUP`.

## ⚙️ Working Principle

The project works based on the input received from the push button.

1. **Button Pressed:** When the push button is pressed, the input becomes LOW, and the LED turns ON.
2. **Button Released:** When the button is released, the input becomes HIGH, and the LED turns OFF.
3. **Continuous Monitoring:** Arduino continuously reads the button state and controls the LED accordingly.

The `INPUT_PULLUP` mode internally enables a pull-up resistor, keeping the input HIGH when the button is not pressed.

## 💻 Arduino Source Code

```cpp
int led = 5;
int button = 6;

void setup() {
  pinMode(led, OUTPUT);
  pinMode(button, INPUT_PULLUP);
}

void loop() {
  int buttonState = digitalRead(button);

  if (buttonState == LOW) {
    digitalWrite(led, HIGH);
  } else {
    digitalWrite(led, LOW);
  }
}
```

## 📸 Project Output

The output demonstrates the LED responding to the push button.

<!-- Add your project output image below -->

![Arduino Push Button Controlled LED System](button-led-output.jpg)

## 📂 Repository Structure

```text
Arduino-Push-Button-LED-Control/
│
├── README.md
├── Push_Button_LED.ino
└── button-led-output.jpg
```

## 🧠 Concepts Learned

- Digital Input and Output Interfacing
- Push Button Interfacing
- LED Control Using Arduino
- INPUT_PULLUP Configuration
- `digitalRead()` Function
- `digitalWrite()` Function
- Conditional Statements (`if-else`)
- Basic Embedded Systems Programming

## 🚀 Applications

- Push-button-operated lighting systems.
- Electronic switching circuits.
- Home automation systems.
- Control panels and user interfaces.
- Basic embedded system applications.
## 📸 Project Output

![Arduino Push Button Controlled LED System](<BUTTON LED.jpeg>)

⭐ **If you find this project useful, don't forget to star the repository!**

*Exploring Embedded Systems Through Practical Electronics Projects.*
