<h1>Learn-esp8266-with-iot-from-very-basics</h1>
<p>This repository contains 8 hands-on experiments to help beginners learn ESP8266 with IoT and hardware interfacing step by step. Each experiment includes circuit diagrams, code, and explanations.</p>

<h2>Experiment 1: Blinking LED with ESP8266 (NodeMCU)</h2>
<strong>Components:</strong><br>
- ESP8266 (NodeMCU)<br>
- LED (any color)<br>
- 220Ω resistor<br>
<p>The blinking LED experiment is the "Hello World" of embedded systems. It demonstrates how to control an LED using an ESP8266 (NodeMCU) board. ESP8266 uses GPIO pins, such as D5.</p>

<strong>How It Works:</strong><br>
<p>The <code>setup()</code> function configures D5 as an output pin. The <code>loop()</code> function turns the LED ON for 1 second and then OFF for 1 second, repeating indefinitely.</p>

<strong>How to Run This Experiment:</strong><br>
1️⃣ Connect the LED to D5 of ESP8266 (with a 220Ω resistor in series).<br>
2️⃣ Upload the provided code to the ESP8266 NodeMCU board.<br>
3️⃣ Observe the LED blinking every 1 second.<br>

<h2>Experiment 2: Connecting ESP8266 to Wi-Fi</h2>
<strong>Components:</strong><br>
- ESP8266 (NodeMCU)<br>
- Wi-Fi Network (SSID & Password)<br>
- Computer with Arduino IDE<br>

<p>This experiment demonstrates how to connect an ESP8266 NodeMCU to a Wi-Fi network.</p>

<strong>How It Works:</strong><br>
<p>The <code>setup()</code> function initializes the serial monitor and starts the Wi-Fi connection using the given SSID ("iot") and password ("jitendra1234"). Once connected, it prints "NodeMCU is Connected!" along with the assigned IP address.</p>

<strong>How to Run This Experiment:</strong><br>
1️⃣ Connect the ESP8266 NodeMCU to your computer via USB.<br>
2️⃣ Open the Arduino IDE and select the correct Board (NodeMCU 1.0) and Port.<br>
3️⃣ Replace "iot" and "jitendra1234" with your actual Wi-Fi SSID and Password.<br>
4️⃣ Upload the provided code to the ESP8266 NodeMCU.<br>
5️⃣ Open the Serial Monitor (9600 baud rate) to see the connection status.<br>

<h2>Experiment 3: Controlling an LED using ESP8266 Web Server</h2>
<strong>Components:</strong><br>
- ESP8266 (NodeMCU)<br>
- LED (any color)<br>
- 220Ω resistor<br>
- Wi-Fi Network (SSID & Password)<br>

<p>Access <code>http://&lt;ESP_IP&gt;/ledon</code> to turn the LED ON and <code>/ledoff</code> to turn it OFF.</p>

<strong>How to Run This Experiment:</strong><br>
1️⃣ Connect the LED to D5 of ESP8266.<br>
2️⃣ Upload the provided code.<br>
3️⃣ Note the ESP IP from Serial Monitor.<br>
4️⃣ Open in browser:<br>
<code>http://&lt;ESP_IP&gt;/ledon</code><br>
<code>http://&lt;ESP_IP&gt;/ledoff</code><br>

<h2>Experiment 4: Controlling LED in Access Point Mode</h2>
<strong>Components:</strong><br>
- ESP8266 (NodeMCU)<br>
- LED (any color)<br>
- 220Ω resistor<br>
- Wi-Fi-enabled device (Laptop/Mobile)<br>

<p>ESP8266 creates hotspot (SSID: "NodeMCU", Password: "123456789") and serves a webpage.</p>

<strong>How to Run This Experiment:</strong><br>
1️⃣ Connect the LED to D5.<br>
2️⃣ Upload the code.<br>
3️⃣ Note AP IP from Serial Monitor (usually 192.168.4.1).<br>
4️⃣ Connect to NodeMCU Wi-Fi.<br>
5️⃣ Open in browser:<br>
<code>http://192.168.4.1/ledon</code><br>
<code>http://192.168.4.1/ledoff</code><br>

<h2>Experiment 5: Controlling LEDs via Web Server</h2>
<strong>Components:</strong><br>
✔ ESP8266 NodeMCU<br>
✔ 2 LEDs<br>
✔ 2 × 220Ω resistors<br>

<p>Control LEDs on D5 and D6 using web server with buttons.</p>

<strong>How to Run This Experiment:</strong><br>
1️⃣ Connect LEDs to D5 and D6.<br>
2️⃣ Upload the code.<br>
3️⃣ Note IP from Serial Monitor.<br>
4️⃣ Open the IP in browser and control LEDs using buttons.<br>

<h2>Experiment 6: Sending DHT11 Data to ThingSpeak</h2>
<strong>Components:</strong><br>
✔ ESP8266 NodeMCU<br>
✔ DHT11 Sensor<br>
✔ ThingSpeak Account<br>

<p>Send temperature and humidity to ThingSpeak using Wi-Fi.</p>

<strong>How to Run This Experiment:</strong><br>
1️⃣ Connect DHT11:<br>
VCC → 3.3V<br>
GND → GND<br>
DATA → D5<br>
2️⃣ Create ThingSpeak channel.<br>
3️⃣ Replace credentials in code.<br>
4️⃣ Upload and view data on Serial Monitor and ThingSpeak.<br>

<h2>Experiment 7: DHT11 Data to ThingSpeak via HTTP</h2>
<strong>Components:</strong><br>
✔ ESP8266 NodeMCU<br>
✔ DHT11 Sensor<br>
✔ ThingSpeak Account<br>

<p>Use HTTP GET requests instead of library to send data to ThingSpeak.</p>

<strong>How to Run This Experiment:</strong><br>
1️⃣ Connect DHT11:<br>
VCC → 3.3V<br>
GND → GND<br>
DATA → D5<br>
2️⃣ Replace API key.<br>
3️⃣ Upload and monitor Serial Monitor.<br>

<h2>Experiment 8: COVID-19 Data on LCD Using ESP8266</h2>
<strong>Objective:</strong> Fetch COVID-19 data from ThingSpeak and display on 16x2 I2C LCD.<br>

<strong>Hardware:</strong><br>
✔ ESP8266 NodeMCU<br>
✔ 16x2 LCD Display (I2C)<br>
✔ Jumper Wires<br>
✔ Wi-Fi Connection<br>

<strong>How to Run This Project:</strong><br>
1️⃣ Connect LCD:<br>
SDA → D2<br>
SCL → D1<br>
VCC → 3.3V<br>
GND → GND<br>
2️⃣ Upload code.<br>
3️⃣ Monitor output and watch LCD update every 3 seconds!<br>

<p><strong>✅ Happy Learning! Build more IoT Projects using ESP8266 🚀</strong></p>
📬 Author: Jitendra Sharma
📧 Email: jitendrasharma7409@gmail.com
🔗 Follow for more: https://github.com/jitendrasharma-eng?tab=repositories | www.youtube.com/@ECodeLab-mv4jm | linkedin.com/in/jitendra-sharma-484072248
