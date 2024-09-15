# RFID Attendance System using ESP32

**Author: Sunny Allana**  
**GitHub: [Sunny Allana](https://github.com/sunnyallana/)** <br/>
**LinkedIn: [Sunny Allana](https://www.linkedin.com/in/sunnyallana/)** <br/>
**Instagram: [Sunny Allana](https://www.instagram.com/imsunnyallana/)**

![IMG_20230506_014157_397](https://github.com/user-attachments/assets/5ba428c0-32d2-4a40-8ff7-e6fb1cb87621)

This project implements an RFID attendance system using an ESP32 microcontroller, an RFID reader (MFRC522), and an OLED display. The system reads RFID card IDs and sends them to a server using HTTP requests for attendance tracking and logging.

## Table of Contents

- [Introduction](#introduction)
- [Requirements](#requirements)
- [Hardware Setup](#hardware-setup)
- [Software Setup](#software-setup)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

## Introduction

The RFID attendance system utilizes an ESP32 microcontroller to interact with RFID cards and a server for data storage and processing. When a user scans their RFID card, the system reads the unique card ID, sends it to the server over Wi-Fi, and receives a response indicating successful or failed attendance.

The OLED display provides user feedback during the scanning process, displaying messages such as "Hello, User!" and "Kindly scan your card."

## Requirements

To use this project, you will need the following components:

- ESP32 microcontroller board
- MFRC522 RFID reader module
- OLED display (SSD1306) with I2C interface
- Wi-Fi network connection
- RFID cards or tags

## Hardware Setup

1. Connect the MFRC522 RFID reader module to the ESP32 board using SPI communication. Make sure to connect the SDA and SCK pins of the OLED display to the corresponding pins on the ESP32 (as specified in the code).

2. Power up the ESP32 and OLED display using a suitable power supply.

3. Ensure that the ESP32 board has access to a Wi-Fi network for communication with the server.

## Software Setup

1. Install the Arduino IDE (Integrated Development Environment) on your computer.

2. Install the required libraries in the Arduino IDE:
   - MFRC522 library for RFID functionality.
   - Adafruit_SSD1306 library for OLED display control.
   - WiFi library for Wi-Fi connectivity.
   - HTTPClient library for making HTTP requests.

3. Open the `RFID_Attendance.ino` file in the Arduino IDE.

4. Modify the following variables in the code to match your Wi-Fi credentials and server configuration:
   - `ssid`: Your Wi-Fi network SSID.
   - `password`: Your Wi-Fi network password.
   - `device_token`: Your device token for server authentication.
   - `URL`: The URL or IP address of the server where attendance data will be sent.

5. Upload the code to your ESP32 board.

## Usage

1. Power up the ESP32 board and the RFID reader.

2. The OLED display will show "Hello, User!" and "Kindly scan your card" in a loop.

3. Present an RFID card to the RFID reader. The system will read the card ID and send it to the server.

4. The server will respond with a message indicating successful or failed attendance, which will be displayed on the OLED screen.

5. If there are any issues with Wi-Fi connectivity, the system will attempt to reconnect automatically.

## Contributing

Contributions to this project are welcome! If you find any bugs or have suggestions for improvements, please open an issue or submit a pull request.

## License

This project is licensed under the [MIT License](LICENSE). Feel free to use, modify, and distribute the code as per the terms of the license.
