<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Learn ESP8266 with IoT from Basics</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            color: #333;
            max-width: 800px;
            margin: 0 auto;
            padding: 20px;
        }
        h1, h2, h3 {
            color: #2c3e50;
        }
        h1 {
            border-bottom: 2px solid #3498db;
            padding-bottom: 10px;
        }
        h2 {
            background-color: #f8f9fa;
            padding: 8px;
            border-left: 4px solid #3498db;
        }
        code {
            background-color: #f0f0f0;
            padding: 2px 4px;
            border-radius: 3px;
            font-family: monospace;
        }
        .component-list {
            background-color: #f8f9fa;
            padding: 10px;
            border-radius: 5px;
            margin: 10px 0;
        }
        .experiment {
            margin-bottom: 30px;
        }
        .how-it-works {
            background-color: #e8f4fc;
            padding: 15px;
            border-radius: 5px;
            margin: 15px 0;
        }
        .steps {
            background-color: #e8f4fc;
            padding: 15px;
            border-radius: 5px;
            margin: 15px 0;
        }
        .step {
            margin-bottom: 8px;
        }
        .emoji {
            font-size: 1.2em;
            margin-right: 5px;
        }
    </style>
</head>
<body>
    <h1>Learn ESP8266 with IoT from Basics</h1>
    <p>This repository contains 8 hands-on experiments to help beginners learn ESP8266 with IoT and hardware interfacing step by step. Each experiment includes circuit diagrams, code, and explanations.</p>

    <div class="experiment">
        <h2>Experiment 1: Blinking LED with ESP8266 (NodeMCU)</h2>
        <div class="component-list">
            <h3>Components:</h3>
            <ul>
                <li>ESP8266 (NodeMCU)</li>
                <li>LED (any color)</li>
                <li>220Ω resistor</li>
            </ul>
        </div>
        <p>The blinking LED experiment is the "Hello World" of embedded systems. It demonstrates how to control an LED using an ESP8266 (NodeMCU) board. ESP8266 uses GPIO pins, such as D5.</p>
        
        <div class="how-it-works">
            <h3>How It Works:</h3>
            <p>The setup() function configures D5 as an output pin. The loop() function turns the LED ON for 1 second and then OFF for 1 second, repeating indefinitely.</p>
        </div>
        
        <div class="steps">
            <h3>How to Run This Experiment:</h3>
            <div class="step"><span class="emoji">1️⃣</span> Connect the LED to D5 of ESP8266 (with a 220Ω resistor in series).</div>
            <div class="step"><span class="emoji">2️⃣</span> Upload the provided code to the ESP8266 NodeMCU board.</div>
            <div class="step"><span class="emoji">3️⃣</span> Observe the LED blinking every 1 second.</div>
        </div>
    </div>

    <div class="experiment">
        <h2>Experiment 2: Connecting ESP8266 to Wi-Fi</h2>
        <div class="component-list">
            <h3>Components:</h3>
            <ul>
                <li>ESP8266 (NodeMCU)</li>
                <li>Wi-Fi Network (SSID & Password)</li>
                <li>Computer with Arduino IDE</li>
            </ul>
        </div>
        <p>This experiment demonstrates how to connect an ESP8266 NodeMCU to a Wi-Fi network. The ESP8266 can connect to a Wi-Fi router, allowing it to communicate over the internet or a local network.</p>
        
        <div class="how-it-works">
            <h3>How It Works:</h3>
            <p>The setup() function initializes the serial monitor and starts the Wi-Fi connection using the given SSID ("iot") and password ("jitendra1234"). The ESP8266 keeps checking until it successfully connects to the Wi-Fi network. Once connected, it prints "NodeMCU is Connected!" along with the assigned IP address.</p>
        </div>
        
        <div class="steps">
            <h3>How to Run This Experiment:</h3>
            <div class="step"><span class="emoji">1️⃣</span> Connect the ESP8266 NodeMCU to your computer via USB.</div>
            <div class="step"><span class="emoji">2️⃣</span> Open the Arduino IDE and select the correct Board (NodeMCU 1.0) and Port.</div>
            <div class="step"><span class="emoji">3️⃣</span> Replace "iot" and "jitendra1234" with your actual Wi-Fi SSID and Password.</div>
            <div class="step"><span class="emoji">4️⃣</span> Upload the provided code to the ESP8266 NodeMCU.</div>
            <div class="step"><span class="emoji">5️⃣</span> Open the Serial Monitor (9600 baud rate) to see the connection status.</div>
        </div>
    </div>

    <div class="experiment">
        <h2>Experiment 3: Controlling an LED using ESP8266 Web Server</h2>
        <div class="component-list">
            <h3>Components:</h3>
            <ul>
                <li>ESP8266 (NodeMCU)</li>
                <li>LED (any color)</li>
                <li>220Ω resistor</li>
                <li>Wi-Fi Network (SSID & Password)</li>
            </ul>
        </div>
        <p>This experiment demonstrates how to control an LED using a web server hosted on an ESP8266 NodeMCU. The ESP8266 connects to a Wi-Fi network and listens for incoming HTTP requests. When a user accesses http://&lt;ESP_IP&gt;/ledon, the LED turns ON. When accessing http://&lt;ESP_IP&gt;/ledoff, the LED turns OFF.</p>
        
        <div class="how-it-works">
            <h3>How It Works:</h3>
            <ol>
                <li>The ESP8266 connects to a Wi-Fi network using the provided SSID ("iot") and password ("jitendra1234").</li>
                <li>It starts an HTTP server on port 80.</li>
                <li>When a client (web browser) sends a request, the ESP8266 reads it and checks for "/ledon" or "/ledoff".</li>
                <li>Based on the request, it turns the LED ON or OFF.</li>
                <li>The server continues listening for new requests.</li>
            </ol>
        </div>
        
        <div class="steps">
            <h3>How to Run This Experiment:</h3>
            <div class="step"><span class="emoji">1️⃣</span> Connect the LED to D5 of ESP8266 (with a 220Ω resistor in series).</div>
            <div class="step"><span class="emoji">2️⃣</span> Upload the provided code to the ESP8266 NodeMCU.</div>
            <div class="step"><span class="emoji">3️⃣</span> Open the Serial Monitor (9600 baud rate) and note the ESP8266's IP address.</div>
            <div class="step"><span class="emoji">4️⃣</span> Open a web browser and enter:
                <ul>
                    <li><code>http://&lt;ESP_IP&gt;/ledon</code> → LED turns ON</li>
                    <li><code>http://&lt;ESP_IP&gt;/ledoff</code> → LED turns OFF</li>
                </ul>
            </div>
            <div class="step"><span class="emoji">5️⃣</span> Observe the LED behavior.</div>
        </div>
    </div>

    <div class="experiment">
        <h2>Experiment 4: Controlling an LED using ESP8266 in Access Point Mode</h2>
        <div class="component-list">
            <h3>Components:</h3>
            <ul>
                <li>ESP8266 (NodeMCU)</li>
                <li>LED (any color)</li>
                <li>220Ω resistor</li>
                <li>Wi-Fi-enabled device (Laptop/Mobile)</li>
            </ul>
        </div>
        <p>This experiment demonstrates how to control an LED using a web server hosted on an ESP8266 NodeMCU. Unlike the previous experiment, this ESP8266 creates its own Wi-Fi network (Access Point mode) instead of connecting to an existing Wi-Fi network.</p>
        
        <div class="how-it-works">
            <h3>How It Works:</h3>
            <ol>
                <li>The ESP8266 creates a Wi-Fi hotspot (SSID: "NodeMCU", Password: "123456789").</li>
                <li>A web server starts on port 80.</li>
                <li>Any device can connect to the "NodeMCU" Wi-Fi and send HTTP requests to control the LED.</li>
                <li>When a user accesses:
                    <ul>
                        <li><code>http://192.168.4.1/ledon</code> → LED turns ON</li>
                        <li><code>http://192.168.4.1/ledoff</code> → LED turns OFF</li>
                    </ul>
                </li>
            </ol>
        </div>
        
        <div class="steps">
            <h3>How to Run This Experiment:</h3>
            <div class="step"><span class="emoji">1️⃣</span> Connect the LED to D5 of ESP8266 (with a 220Ω resistor in series).</div>
            <div class="step"><span class="emoji">2️⃣</span> Upload the provided code to the ESP8266 NodeMCU.</div>
            <div class="step"><span class="emoji">3️⃣</span> Open the Serial Monitor (9600 baud rate) and note the ESP8266's Access Point (AP) IP address (Default: 192.168.4.1).</div>
            <div class="step"><span class="emoji">4️⃣</span> On your mobile/laptop, connect to the "NodeMCU" Wi-Fi using password "123456789".</div>
            <div class="step"><span class="emoji">5️⃣</span> Open a web browser and enter:
                <ul>
                    <li><code>http://192.168.4.1/ledon</code> → LED turns ON</li>
                    <li><code>http://192.168.4.1/ledoff</code> → LED turns OFF</li>
                </ul>
            </div>
            <div class="step"><span class="emoji">6️⃣</span> Observe the LED behavior.</div>
        </div>
    </div>

    <div class="experiment">
        <h2>Experiment 5: Controlling LEDs via Web Server</h2>
        <div class="component-list">
            <h3>Components:</h3>
            <ul>
                <li>✔ ESP8266 NodeMCU</li>
                <li>✔ 2 LEDs (any color)</li>
                <li>✔ 2 × 220Ω resistors</li>
            </ul>
        </div>
        <p>This experiment demonstrates how to control LEDs using an ESP8266-based web server. When you open a webpage on your browser, you can turn the LEDs ON/OFF with buttons.</p>
        
        <div class="how-it-works">
            <h3>How It Works</h3>
            <p><strong>1️⃣ setup() - Initialize ESP8266 & Wi-Fi</strong><br>
            Connects the ESP8266 to the Wi-Fi network (iot, password: jitendra1234).<br>
            Prints "NodeMCU is connected!" along with the IP address on the Serial Monitor.<br>
            Starts the web server and sets LED pins (D5, D6) as OUTPUT.</p>
            
            <p><strong>2️⃣ loop() - Handle Web Requests</strong><br>
            When a client (browser) connects, ESP8266 reads the HTTP request.<br>
            If the request matches /led1on, /led1off, /led2on, or /led2off, it controls the LEDs accordingly.<br>
            Sends a webpage with buttons for controlling the LEDs.</p>
        </div>
        
        <div class="steps">
            <h3>How to Run This Experiment</h3>
            <div class="step"><span class="emoji">1️⃣</span> Connect the LEDs to ESP8266 on pins D5 and D6 (with 220Ω resistors).</div>
            <div class="step"><span class="emoji">2️⃣</span> Upload the provided code to ESP8266 using Arduino IDE.</div>
            <div class="step"><span class="emoji">3️⃣</span> Open Serial Monitor and note the ESP8266 IP address.</div>
            <div class="step"><span class="emoji">4️⃣</span> Enter the IP address in your browser (e.g., http://192.168.1.100).</div>
            <div class="step"><span class="emoji">5️⃣</span> Click the buttons to turn LEDs ON/OFF!</div>
        </div>
    </div>

    <div class="experiment">
        <h2>Experiment 6: Sending DHT11 Sensor Data to ThingSpeak</h2>
        <div class="component-list">
            <h3>Components:</h3>
            <ul>
                <li>✔ ESP8266 NodeMCU</li>
                <li>✔ DHT11 Temperature & Humidity Sensor</li>
                <li>✔ ThingSpeak IoT Cloud Account</li>
            </ul>
        </div>
        <p>This experiment demonstrates how to measure temperature and humidity using a DHT11 sensor and send the data to ThingSpeak for real-time monitoring.</p>
        
        <div class="how-it-works">
            <h3>How It Works</h3>
            <p><strong>1️⃣ setup() - Connect to Wi-Fi & Initialize Sensor</strong><br>
            The ESP8266 connects to the Wi-Fi network (iot, password: jitendra1234).<br>
            The DHT11 sensor is initialized on pin D5.<br>
            The ESP8266 connects to ThingSpeak, a cloud platform for IoT data logging.</p>
            
            <p><strong>2️⃣ loop() - Read Sensor & Send Data to ThingSpeak</strong><br>
            Reads temperature and humidity from the DHT11 sensor.<br>
            Prints the sensor values to the Serial Monitor.<br>
            Sends temperature and humidity data to ThingSpeak using writeField().<br>
            Waits 2 seconds before the next update.</p>
        </div>
        
        <div class="steps">
            <h3>How to Run This Experiment</h3>
            <div class="step"><span class="emoji">1️⃣</span> Connect the DHT11 sensor to ESP8266:
                <ul>
                    <li>VCC → 3.3V</li>
                    <li>GND → GND</li>
                    <li>DATA → D5</li>
                </ul>
            </div>
            <div class="step"><span class="emoji">2️⃣</span> Create a ThingSpeak account and set up a channel.</div>
            <div class="step"><span class="emoji">3️⃣</span> Replace myChannelNumber and myWriteAPIKey with your ThingSpeak details.</div>
            <div class="step"><span class="emoji">4️⃣</span> Upload the code to ESP8266 using Arduino IDE.</div>
            <div class="step"><span class="emoji">5️⃣</span> Open Serial Monitor to see real-time sensor readings.</div>
            <div class="step"><span class="emoji">6️⃣</span> Go to your ThingSpeak channel and observe the temperature & humidity graphs!</div>
        </div>
    </div>

    <div class="experiment">
        <h2>Experiment 7: Sending DHT11 Sensor Data to ThingSpeak Using HTTP Requests</h2>
        <div class="component-list">
            <h3>Components:</h3>
            <ul>
                <li>✔ ESP8266 NodeMCU</li>
                <li>✔ DHT11 Temperature & Humidity Sensor</li>
                <li>✔ ThingSpeak IoT Cloud Account</li>
            </ul>
        </div>
        <p>This experiment demonstrates how to send temperature and humidity data to ThingSpeak using HTTP GET requests instead of the ThingSpeak library.</p>
        
        <div class="how-it-works">
            <h3>How It Works</h3>
            <p><strong>1️⃣ setup() - Connect to Wi-Fi & Initialize Sensor</strong><br>
            The ESP8266 connects to the Wi-Fi network (iot, password: jitendra1234).<br>
            The DHT11 sensor is initialized on pin D5.</p>
            
            <p><strong>2️⃣ loop() - Read Sensor & Send Data to ThingSpeak via HTTP</strong><br>
            Reads temperature and humidity from the DHT11 sensor.<br>
            Prints the sensor values to the Serial Monitor.<br>
            Constructs custom HTTP URLs for temperature (field1) and humidity (field2).<br>
            Uses the ESP8266HTTPClient library to send HTTP GET requests to ThingSpeak API.<br>
            Checks and prints the HTTP response code (should be 200 for success).<br>
            Waits 2 seconds before sending the next value.</p>
        </div>
        
        <div class="steps">
            <h3>How to Run This Experiment</h3>
            <div class="step"><span class="emoji">1️⃣</span> Connect the DHT11 sensor to ESP8266:
                <ul>
                    <li>VCC → 3.3V</li>
                    <li>GND → GND</li>
                    <li>DATA → D5</li>
                </ul>
            </div>
            <div class="step"><span class="emoji">2️⃣</span> Create a ThingSpeak account and set up a channel.</div>
            <div class="step"><span class="emoji">3️⃣</span> Replace api_key with your own ThingSpeak Write API Key.</div>
            <div class="step"><span class="emoji">4️⃣</span> Upload the code to ESP8266 using Arduino IDE.</div>
            <div class="step"><span class="emoji">5️⃣</span> Open Serial Monitor to see the data being sent.</div>
            <div class="step"><span class="emoji">6️⃣</span> Go to your ThingSpeak channel and observe the temperature & humidity graphs updating in real-time!</div>
        </div>
    </div>

    <div class="experiment">
        <h2>Experiment 8: Project: COVID-19 Data Display on LCD Using ESP8266</h2>
        <p><strong>📌 Objective:</strong> Fetch COVID-19 statistics from ThingSpeak API and display them on a 16x2 I2C LCD.</p>
        
        <div class="component-list">
            <h3>🛠️ Hardware Requirements</h3>
            <ul>
                <li>ESP8266 NodeMCU</li>
                <li>16x2 LCD Display (I2C)</li>
                <li>Jumper Wires</li>
                <li>Wi-Fi Connection</li>
            </ul>
        </div>
        
        <div class="how-it-works">
            <h3>📝 Code Overview</h3>
            <p><strong>1️⃣ setup() - Connect to Wi-Fi & Initialize LCD</strong><br>
            Connects ESP8266 to the Wi-Fi network (iot, password: jitendra1234).<br>
            Initializes the 16x2 LCD using the I2C protocol (0x27 address).<br>
            Prints the local IP address of ESP8266 on the Serial Monitor.</p>
            
            <p><strong>2️⃣ loop() - Fetch COVID-19 Data & Display on LCD</strong><br>
            Sends an HTTP GET request to ThingSpeak API (url1).<br>
            Receives data as a single string (data).<br>
            Uses StringSplitter library to separate values (cases, deaths, recoveries).<br>
            Cleans the extracted values by removing unwanted characters.<br>
            Displays each value (Cases, Deaths, Recoveries) one by one on the LCD with a 3-second delay.</p>
        </div>
        
        <div class="steps">
            <h3>How to Run This Project</h3>
            <div class="step"><span class="emoji">1️⃣</span> Connect the I2C LCD to ESP8266:
                <ul>
                    <li>SDA → D2</li>
                    <li>SCL → D1</li>
                    <li>VCC → 3.3V</li>
                    <li>GND → GND</li>
                </ul>
            </div>
            <div class="step"><span class="emoji">2️⃣</span> Upload the Code to ESP8266 using Arduino IDE.</div>
            <div class="step"><span class="emoji">3️⃣</span> Monitor Serial Output for debugging.</div>
            <div class="step"><span class="emoji">4️⃣</span> Watch the data update on the LCD every 3 seconds!</div>
        </div>
    </div>
</body>
</html>
