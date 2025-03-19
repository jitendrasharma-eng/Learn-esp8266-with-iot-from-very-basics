# Learn-esp8266-with-iot-from-very-basics
This repository contains 8 hands-on experiments to help beginners learn esp8266 with iot and hardware interfacing step by step. Each experiment includes circuit diagrams, code, and explanations.

Experiment 1: Blinking LED with ESP8266 (NodeMCU)
Components:
ESP8266 (NodeMCU)
LED (any color)
220Ω resistor
The blinking LED experiment is the "Hello World" of embedded systems. It demonstrates how to control an LED using an ESP8266 (NodeMCU) board.  ESP8266 uses GPIO pins, such as D5.

How It Works:
The setup() function configures D5 as an output pin. The loop() function turns the LED ON for 1 second and then OFF for 1 second, repeating indefinitely.

How to Run This Experiment:
1️⃣ Connect the LED to D5 of ESP8266 (with a 220Ω resistor in series).
2️⃣ Upload the provided code to the ESP8266 NodeMCU board.
3️⃣ Observe the LED blinking every 1 second.

Experiment 2: Connecting ESP8266 to Wi-Fi
Components:
ESP8266 (NodeMCU)
Wi-Fi Network (SSID & Password)
Computer with Arduino IDE
This experiment demonstrates how to connect an ESP8266 NodeMCU to a Wi-Fi network. The ESP8266 can connect to a Wi-Fi router, allowing it to communicate over the internet or a local network.

How It Works:
The setup() function initializes the serial monitor and starts the Wi-Fi connection using the given SSID ("iot") and password ("jitendra1234"). The ESP8266 keeps checking until it successfully connects to the Wi-Fi network. Once connected, it prints "NodeMCU is Connected!" along with the assigned IP address.

How to Run This Experiment:
1️⃣ Connect the ESP8266 NodeMCU to your computer via USB.
2️⃣ Open the Arduino IDE and select the correct Board (NodeMCU 1.0) and Port.
3️⃣ Replace "iot" and "jitendra1234" with your actual Wi-Fi SSID and Password.
4️⃣ Upload the provided code to the ESP8266 NodeMCU.
5️⃣ Open the Serial Monitor (9600 baud rate) to see the connection status.

Experiment 3: Controlling an LED using ESP8266 Web Server
Components:
ESP8266 (NodeMCU)
LED (any color)
220Ω resistor
Wi-Fi Network (SSID & Password)
This experiment demonstrates how to control an LED using a web server hosted on an ESP8266 NodeMCU. The ESP8266 connects to a Wi-Fi network and listens for incoming HTTP requests. When a user accesses http://<ESP_IP>/ledon, the LED turns ON. When accessing http://<ESP_IP>/ledoff, the LED turns OFF.

How It Works:
1️⃣ The ESP8266 connects to a Wi-Fi network using the provided SSID ("iot") and password ("jitendra1234").
2️⃣ It starts an HTTP server on port 80.
3️⃣ When a client (web browser) sends a request, the ESP8266 reads it and checks for "/ledon" or "/ledoff".
4️⃣ Based on the request, it turns the LED ON or OFF.
5️⃣ The server continues listening for new requests.

How to Run This Experiment:
1️⃣ Connect the LED to D5 of ESP8266 (with a 220Ω resistor in series).
2️⃣ Upload the provided code to the ESP8266 NodeMCU.
3️⃣ Open the Serial Monitor (9600 baud rate) and note the ESP8266's IP address.
4️⃣ Open a web browser and enter:

http://<ESP_IP>/ledon → LED turns ON
http://<ESP_IP>/ledoff → LED turns OFF
5️⃣ Observe the LED behavior.

Experiment 4: Controlling an LED using ESP8266 in Access Point Mode
Components:
ESP8266 (NodeMCU)
LED (any color)
220Ω resistor
Wi-Fi-enabled device (Laptop/Mobile)
This experiment demonstrates how to control an LED using a web server hosted on an ESP8266 NodeMCU. Unlike the previous experiment, this ESP8266 creates its own Wi-Fi network (Access Point mode) instead of connecting to an existing Wi-Fi network.

How It Works:
1️⃣ The ESP8266 creates a Wi-Fi hotspot (SSID: "NodeMCU", Password: "123456789").
2️⃣ A web server starts on port 80.
3️⃣ Any device can connect to the "NodeMCU" Wi-Fi and send HTTP requests to control the LED.
4️⃣ When a user accesses:

http://192.168.4.1/ledon → LED turns ON
http://192.168.4.1/ledoff → LED turns OFF
How to Run This Experiment:
1️⃣ Connect the LED to D5 of ESP8266 (with a 220Ω resistor in series).
2️⃣ Upload the provided code to the ESP8266 NodeMCU.
3️⃣ Open the Serial Monitor (9600 baud rate) and note the ESP8266's Access Point (AP) IP address (Default: 192.168.4.1).
4️⃣ On your mobile/laptop, connect to the "NodeMCU" Wi-Fi using password "123456789".
5️⃣ Open a web browser and enter:

http://192.168.4.1/ledon → LED turns ON
http://192.168.4.1/ledoff → LED turns OFF
6️⃣ Observe the LED behavior.

Experiment 5: Controlling LEDs via Web Server
Components:
✔ ESP8266 NodeMCU
✔ 2 LEDs (any color)
✔ 2 × 220Ω resistors

This experiment demonstrates how to control LEDs using an ESP8266-based web server. When you open a webpage on your browser, you can turn the LEDs ON/OFF with buttons.

How It Works
1️⃣ setup() - Initialize ESP8266 & Wi-Fi
Connects the ESP8266 to the Wi-Fi network (iot, password: jitendra1234).
Prints "NodeMCU is connected!" along with the IP address on the Serial Monitor.
Starts the web server and sets LED pins (D5, D6) as OUTPUT.
2️⃣ loop() - Handle Web Requests
When a client (browser) connects, ESP8266 reads the HTTP request.
If the request matches /led1on, /led1off, /led2on, or /led2off, it controls the LEDs accordingly.
Sends a webpage with buttons for controlling the LEDs.
How to Run This Experiment
1️⃣ Connect the LEDs to ESP8266 on pins D5 and D6 (with 220Ω resistors).
2️⃣ Upload the provided code to ESP8266 using Arduino IDE.
3️⃣ Open Serial Monitor and note the ESP8266 IP address.
4️⃣ Enter the IP address in your browser (e.g., http://192.168.1.100).
5️⃣ Click the buttons to turn LEDs ON/OFF!

Experiment 6: Sending DHT11 Sensor Data to ThingSpeak
Components:
✔ ESP8266 NodeMCU
✔ DHT11 Temperature & Humidity Sensor
✔ ThingSpeak IoT Cloud Account

This experiment demonstrates how to measure temperature and humidity using a DHT11 sensor and send the data to ThingSpeak for real-time monitoring.

How It Works
1️⃣ setup() - Connect to Wi-Fi & Initialize Sensor
The ESP8266 connects to the Wi-Fi network (iot, password: jitendra1234).
The DHT11 sensor is initialized on pin D5.
The ESP8266 connects to ThingSpeak, a cloud platform for IoT data logging.
2️⃣ loop() - Read Sensor & Send Data to ThingSpeak
Reads temperature and humidity from the DHT11 sensor.
Prints the sensor values to the Serial Monitor.
Sends temperature and humidity data to ThingSpeak using writeField().
Waits 2 seconds before the next update.
How to Run This Experiment
1️⃣ Connect the DHT11 sensor to ESP8266:

VCC → 3.3V
GND → GND
DATA → D5
2️⃣ Create a ThingSpeak account and set up a channel.
3️⃣ Replace myChannelNumber and myWriteAPIKey with your ThingSpeak details.
4️⃣ Upload the code to ESP8266 using Arduino IDE.
5️⃣ Open Serial Monitor to see real-time sensor readings.
6️⃣ Go to your ThingSpeak channel and observe the temperature & humidity graphs!

Experiment 7: Sending DHT11 Sensor Data to ThingSpeak Using HTTP Requests
Components:
✔ ESP8266 NodeMCU
✔ DHT11 Temperature & Humidity Sensor
✔ ThingSpeak IoT Cloud Account

This experiment demonstrates how to send temperature and humidity data to ThingSpeak using HTTP GET requests instead of the ThingSpeak library.

How It Works
1️⃣ setup() - Connect to Wi-Fi & Initialize Sensor
The ESP8266 connects to the Wi-Fi network (iot, password: jitendra1234).
The DHT11 sensor is initialized on pin D5.
2️⃣ loop() - Read Sensor & Send Data to ThingSpeak via HTTP
Reads temperature and humidity from the DHT11 sensor.
Prints the sensor values to the Serial Monitor.
Constructs custom HTTP URLs for temperature (field1) and humidity (field2).
Uses the ESP8266HTTPClient library to send HTTP GET requests to ThingSpeak API.
Checks and prints the HTTP response code (should be 200 for success).
Waits 2 seconds before sending the next value.
How to Run This Experiment
1️⃣ Connect the DHT11 sensor to ESP8266:

VCC → 3.3V
GND → GND
DATA → D5
2️⃣ Create a ThingSpeak account and set up a channel.
3️⃣ Replace api_key with your own ThingSpeak Write API Key.
4️⃣ Upload the code to ESP8266 using Arduino IDE.
5️⃣ Open Serial Monitor to see the data being sent.
6️⃣ Go to your ThingSpeak channel and observe the temperature & humidity graphs updating in real-time!

Experiment 8: 
Project: COVID-19 Data Display on LCD Using ESP8266
📌 Objective: Fetch COVID-19 statistics from ThingSpeak API and display them on a 16x2 I2C LCD.

🛠️ Hardware Requirements
ESP8266 NodeMCU
16x2 LCD Display (I2C)
Jumper Wires
Wi-Fi Connection
📝 Code Overview
1️⃣ setup() - Connect to Wi-Fi & Initialize LCD
Connects ESP8266 to the Wi-Fi network (iot, password: jitendra1234).
Initializes the 16x2 LCD using the I2C protocol (0x27 address).
Prints the local IP address of ESP8266 on the Serial Monitor.
2️⃣ loop() - Fetch COVID-19 Data & Display on LCD
Sends an HTTP GET request to ThingSpeak API (url1).
Receives data as a single string (data).
Uses StringSplitter library to separate values (cases, deaths, recoveries).
Cleans the extracted values by removing unwanted characters.
Displays each value (Cases, Deaths, Recoveries) one by one on the LCD with a 3-second delay.
How to Run This Project
1️⃣ Connect the I2C LCD to ESP8266:

SDA → D2
SCL → D1
VCC → 3.3V
GND → GND
2️⃣ Upload the Code to ESP8266 using Arduino IDE.
3️⃣ Monitor Serial Output for debugging.
4️⃣ Watch the data update on the LCD every 3 seconds!
