# Arduino LCD Counter with Up/Down Buttons

This project is a simple **button-controlled counter** using an **Arduino Uno** and a **16x2 I2C LCD**. The counter value is displayed on the LCD and can be incremented or decremented using two push buttons.

## 🧰 Components Used

- Arduino Uno
- 16x2 I2C LCD Display (I2C address: `0x3F`)
- 2 x Push Buttons
- Breadboard
- Jumper Wires
- USB Cable

## 🔌 Wiring Overview

### LCD to Arduino
| LCD Pin | Arduino Pin |
|---------|-------------|
| GND     | GND         |
| VCC     | 5V          |
| SDA     | A4          |
| SCL     | A5          |

### Buttons to Arduino
| Button | Arduino Pin |
|--------|-------------|
| Up     | D2          |
| Down   | D3          |

Each button is connected between its Arduino digital pin and GND. The sketch uses `INPUT_PULLUP`, so no external resistors are needed.

## 🧠 How It Works

- The LCD displays the text:
- Press the **Up** button to increase the counter.
- Press the **Down** button to decrease the counter.
- The value updates in real-time on the LCD screen.
- Serial Monitor logs button presses and count value for debugging.

## 🧾 Code Features

- Uses the `LiquidCrystal_I2C` library to control the LCD.
- Debounces button inputs with a 50ms delay.
- Uses internal pull-up resistors to simplify wiring.
- Contains separate functions for Up and Down button handling.

## 🔧 Setup Instructions

1. Wire your components as described above.
2. Install the `LiquidCrystal_I2C` library in the Arduino IDE.
3. Upload the provided sketch to your Arduino Uno.
4. Open the Serial Monitor (baud rate 9600) to see debug output.

## 🚀 Possible Enhancements

- Add EEPROM functionality to save the counter value.
- Include a reset button.
- Add long-press support for faster counting.
