# RS485-Communication-module-

# RS485 Master-Slave Communication

## Overview

This project demonstrates Master-Slave communication using the RS485 protocol with Arduino. The RS485 standard is widely used for robust serial communication over long distances. The Master device sends data to the Slave device, and the Slave device responds accordingly.

The Master device reads an analog value from a sensor and transmits it to the Slave device. The Slave device, in turn, controls an LED based on the received data. This communication is bidirectional, allowing the Master and Slave to exchange information seamlessly.

## Hardware Requirements

For this project, you will need the following components:

### Master:
- Arduino board (e.g., Arduino Uno)
- RS485 Module (MAX485 or equivalent)
- Analog sensor (e.g., Potentiometer or LM35 Temperature Sensor)
- OLED Display (SSD1306 or similar) - Optional for displaying Master data
- Jumper wires

### Slave:
- Arduino board (e.g., Arduino Uno)
- RS485 Module (MAX485 or equivalent)
- LED (with a current-limiting resistor)
- Jumper wires

## Wiring Diagram

Please refer to the provided wiring diagrams for connecting the components:

### Master:
![Master Wiring Diagram](master_wiring_diagram.png)

### Slave:
![Slave Wiring Diagram](slave_wiring_diagram.png)

## Installation

To set up the Master and Slave devices:

1. Connect the components as per the wiring diagrams.
2. Upload the `Master_RS485_Communication.ino` code to the Master Arduino board.
3. Upload the `Slave_RS485_Communication.ino` code to the Slave Arduino board.

## How it Works

1. Upon powering up, the Master initializes the RS485 communication, the analog sensor, and the OLED display (if used).

2. The Master continuously reads the analog value from the sensor and sends it to the Slave device via RS485.

3. The Slave device receives the data and converts it into a PWM duty cycle value suitable for controlling the LED.

4. The Slave sets the PWM output to control the LED brightness based on the received data.

5. If an OLED display is connected to the Master, it will show the current data being sent to the Slave.

## Troubleshooting

If you encounter any issues:

- Check the wiring connections carefully, ensuring all connections are secure and accurate.
- Verify that the correct libraries are installed in your Arduino IDE (e.g., Adafruit_GFX and Adafruit_SSD1306 for Master).

## License

This project is licensed under the [MIT License](LICENSE).

---

