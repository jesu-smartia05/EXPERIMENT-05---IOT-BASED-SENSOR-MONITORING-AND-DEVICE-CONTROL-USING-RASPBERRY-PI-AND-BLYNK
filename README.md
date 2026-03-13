 # EXPERIMENT-05-IOT BASED SENSOR MONITORING AND DEVICE CONTROL USING RASPBERRY PI AND BLYNK

---

### **NAME: JESU SMARTIA A**  
### **DEPARTMENT:B.E.CSE(IOT)**  
### **ROLL NO: 212223110016**  
### **DATE OF EXPERIMENT: 11.03.2026**  

---

## **AIM:**  
To interface **IR and LDR sensors** with **Raspberry Pi 4** to monitor sensor values in the Blynk mobile application and control output devices such as **LED, buzzer, and relay** through the **Blynk platform**.

---

## **APPARATUS REQUIRED:**  
1.	Raspberry Pi 4
2.	IR Sensor Module
3.	LDR Sensor Module
4.	Relay Module
5.	Buzzer
6.	LED
7.	Resistors (220Ω)
8.	Breadboard
9.	Connecting Wires
10.	Power Supply
11.	Wi-Fi Internet Connection
12.	Blynk Mobile Application
13. Computer with Thonny IDE  

---

## **THEORY:**  
<img width="1293" height="744" alt="image" src="https://github.com/user-attachments/assets/3c04afa6-1517-45d2-88f1-e671d9ed1ffb" />

 ### FIGURE-01 RASPI PI 4 PINOUT DIAGRAM: 

The Raspberry Pi 4 Model B is built around a Broadcom BCM2711 system-on-chip that integrates a quad-core ARM Cortex-A72 (64-bit) CPU, VideoCore VI GPU, memory controller, and peripheral interfaces, forming a compact yet complete computer architecture where the SoC connects internally to RAM, USB 3.0 controller, Gigabit Ethernet, HDMI display, and wireless modules. Its 40-pin GPIO header provides a flexible pin configuration consisting of power pins (5 V and 3.3 V), multiple ground pins, and general-purpose input/output pins that operate at 3.3 V logic and can be programmed for digital I/O or alternate functions. Key alternate functions include I²C (SDA, SCL) for sensor communication, SPI (MOSI, MISO, SCLK, CS) for high-speed peripheral interfacing, UART (TX, RX) for serial communication, and PWM for control applications.  For communication, I2C (SDA, SCL), SPI (MOSI, MISO, SCK), and UART (TX, RX) interfaces are mapped across different GPIO pins, allowing seamless connectivity with sensors and peripherals. All GPIO pins support PWM (Pulse Width Modulation), making it useful for motor control, LED brightness adjustment, and sound applications. The BOOTSEL button enables USB mass storage mode for firmware flashing, while the DEBUG pins (SWD interface) provide debugging capabilities. With its low power consumption, flexible GPIO options, and rich interface support, the Raspberry Pi Pico is widely used for IoT, embedded systems, robotics, and automation projects.This architecture and pin multiplexing allow the Raspberry Pi 4 to act as both a general-purpose computing platform and an embedded controller, supporting rapid prototyping, hardware interfacing, and IoT applications.

   The Internet of Things (IoT) allows devices to communicate and exchange data over the internet. In this experiment, Raspberry Pi 4 acts as the central processing unit that reads input signals from sensors and communicates with the Blynk cloud platform. The IR sensor detects the presence of objects, while the LDR sensor detects the intensity of light. These sensor values are transmitted to the Blynk mobile application for real-time monitoring. Based on the sensor data or manual commands from the Blynk app, Raspberry Pi controls output devices such as an LED, buzzer, and relay through its GPIO pins. This experiment demonstrates remote monitoring and control using IoT technology.

### **Circuit Diagram Explanation:**  
The IR sensor and LDR sensor are connected to the input GPIO pins of the Raspberry Pi. These sensors detect environmental conditions such as object presence and light intensity and send digital signals to the Raspberry Pi.
The LED, buzzer, and relay module are connected to the output GPIO pins. These devices act as output indicators or control devices. The relay can control external electrical loads, while the LED and buzzer provide visual and audio alerts.
Raspberry Pi connects to the internet through Wi-Fi and communicates with the Blynk cloud server. The Blynk mobile application displays the sensor values and allows the user to control the output devices remotely. When a command is given from the Blynk app, Raspberry Pi processes the command and activates or deactivates the connected output devices.

<img width="1042" height="695" alt="image" src="https://github.com/user-attachments/assets/05b34c40-1e93-4eb0-892d-ea30fcd6c59d" />


 ### FIGURE-02 CIRCUIT DIAGRAM: 
 
### **IR Sensor:**  
  An **Infrared Sensor (IR Sensor)** is an electronic device used to detect the presence of objects by using **infrared light**. It consists mainly of an **IR transmitter (IR LED)** and an **IR receiver (photodiode or phototransistor)**. The transmitter emits infrared rays, and when these rays strike an object, they are reflected back and detected by the receiver. Based on this reflection, the sensor determines whether an object is present or absent. IR sensors are widely used in applications such as **obstacle detection, automatic doors, security systems, and line-following robots** due to their fast response and simple operation.
<img width="422" height="204" alt="image" src="https://github.com/user-attachments/assets/b6ff30ce-190e-4e6e-a608-4d8ee9b6985d" />
### FIGURE-03 IR Sensor

### **LDR Sensor:**  
   An **Light Dependent Resistor (LDR)** is a light-sensitive electronic sensor whose electrical resistance changes according to the intensity of incident light. When the surrounding light level increases, the resistance of the LDR decreases, allowing more current to flow through the circuit; conversely, in low-light or dark conditions its resistance becomes very high and restricts current flow. This property makes the LDR useful for automatically detecting and responding to light levels in applications such as automatic street lights, brightness control systems, security alarms, and light-activated switching circuits.
<img width="656" height="188" alt="image" src="https://github.com/user-attachments/assets/18f0925b-50a1-4ad1-981d-9a67b20e274d" />
### FIGURE-04 LDR Sensor

### **Relay Model:**  
   A **relay module** is an electrically operated switch used to control high-voltage or high-current devices using a low-power control signal from a microcontroller such as a Raspberry Pi or Arduino. It works based on an electromagnetic principle: when a small voltage is applied to the relay coil, it generates a magnetic field that pulls a switch contact to either open or close the circuit. This allows the microcontroller to safely control external loads like lamps, motors, or appliances without direct electrical connection. Relay modules usually include control pins (VCC, GND, IN) and switching terminals such as Normally Open (NO), Normally Closed (NC), and Common (COM).
<img width="430" height="286" alt="image" src="https://github.com/user-attachments/assets/49866a32-4dd4-4cd8-98bf-522a41920c8c" />
### FIGURE-05 Relay Model

### **LED:**  
   A **Light Emitting Diode (LED)** is a semiconductor electronic component that emits light when an electric current passes through it. It operates on the principle of electroluminescence, where electrons recombine with holes inside the semiconductor material and release energy in the form of light. LEDs are widely used in **electronic circuits as indicators, displays, and lighting device**s because they consume very low power, have a **long lifespan, generate less heat, and switch very fast compared to conventional light source**s. They are available in different colors such as **red, green, blue, and white** depending on the semiconductor material used.
<img width="522" height="236" alt="image" src="https://github.com/user-attachments/assets/b7b23183-1397-4a57-8098-49195063128b" />
### FIGURE-06 LED

### **Buzzer:**  
   A **buzzer** is an electronic audio signaling device used to produce sound for alerts, alarms, or indications in electronic circuits. It converts electrical energy into sound energy and is commonly used in devices such as alarms, timers, computers, and embedded systems. Buzzers are mainly of two types: **active buzzers**, which generate sound when a DC voltage is applied, and **passive buzzers**, which require an external signal or frequency to produce sound. They are widely used in microcontroller and Raspberry Pi projects to provide audible notifications when a specific event or condition occurs.

<img width="609" height="202" alt="image" src="https://github.com/user-attachments/assets/bcc5542a-1a7f-4a97-9268-31219fc0a649" />


 ### FIGURE-07 Buzzer: 

---
### **Procedure:** 
1.	Install the required libraries such as **Blynk and GPIO libraries in the Raspberry Pi** .
2.	Connect the IR sensor and LDR sensor to the input GPIO pins of the Raspberry Pi.
3.	Connect the LED, buzzer, and relay module to the output GPIO pins.
4.	Create a project in the Blynk mobile application.
5.	Add widgets such as **labels for sensor values and buttons for device control**.
6.	Copy the **Blynk authentication token** from the app.
7.	Write the Python program in Raspberry Pi to read sensor values and send them to the Blynk cloud.
8.	Configure the program to receive commands from the Blynk app to control the LED, buzzer, and relay.
9.	Run the program in Raspberry Pi.
10.	Observe the sensor values in the Blynk application and control the output devices using the app interface.
### **Algorithm / Program Flow:** 
1.	Start the program.
2.	Import the required libraries for GPIO control and Blynk communication.
3.	Configure the GPIO pins of the Raspberry Pi for input and output devices.
4.	Initialize the Blynk authentication token and connect Raspberry Pi to the Blynk cloud server through the internet.
5.	Read the input values from the IR sensor and LDR sensor.
6.	Send the sensor values to the Blynk mobile application using virtual pins.
7.	Continuously monitor the Blynk app for user commands.
8.	If a command is received from the Blynk app:
o	Turn ON/OFF the LED.
o	Activate or deactivate the buzzer.
o	Switch the relay ON or OFF.
9.	Repeat the process to continuously monitor sensors and control devices.
10.	Stop the program when required.

---

## **CIRCUIT DIAGRAM:**  
### **Connections:**  
### **GPIO Pin Connection Table:** 
|  Device  | 	Raspberry Pi GPIO Pin	  |  Purpose
---
|  IR Sensor Output	  | 	GPIO 17		  |  Detect object presence
---
|  LDR Sensor Output	  | 	GPIO 27		  |  Detect light intensity
---
|  Relay Module	  | 	GPIO 22		  |  Control external load
---
|  LED	  | 	GPIO 23		  |  Visual indication
---
|  Buzzer	  | 	GPIO 24		  |  Sound alert
---
|  VCC	  | 	5V Pin		  |  Power supply
---
|  GND	  | 	GND Pin		  |  Common ground

---
---

## ** Python Code for Raspberry Pi + Blynk**  
```
import RPi.GPIO as GPIO
import BlynkLib
import time

# ---------------- BLYNK CONFIG ----------------
BLYNK_AUTH = "R4Hu-JaeFN7a1dc3uu2dNSqLKFVlrZqF"

blynk = BlynkLib.Blynk(
    BLYNK_AUTH,
    server="blynk.cloud",
    port=80
)

# ---------------- GPIO SETUP ----------------
GPIO.setwarnings(False)
GPIO.setmode(GPIO.BCM)

# Inputs
IR_PIN = 18
LDR_PIN = 23

GPIO.setup(IR_PIN, GPIO.IN)
GPIO.setup(LDR_PIN, GPIO.IN)

# Outputs
RELAY_PIN = 24
LED_PIN = 8
BUZZER_PIN = 25

GPIO.setup(RELAY_PIN, GPIO.OUT)
GPIO.setup(LED_PIN, GPIO.OUT)
GPIO.setup(BUZZER_PIN, GPIO.OUT)

# Initial OFF states
GPIO.output(RELAY_PIN, 1)   # Relay OFF (Active LOW)
GPIO.output(LED_PIN, 0)
GPIO.output(BUZZER_PIN, 0)

# ---------------- CONTROL FUNCTIONS ----------------

# Relay (Active LOW)
def relay_control(value):
    if int(value[0]) == 1:
        GPIO.output(RELAY_PIN, 0)   # ON
    else:
        GPIO.output(RELAY_PIN, 1)   # OFF
    print("Relay:", value[0])

# LED (Active HIGH)
def led_control(value):
    GPIO.output(LED_PIN, int(value[0]))
    print("LED:", value[0])

# Buzzer (Active HIGH)
def buzzer_control(value):
    GPIO.output(BUZZER_PIN, int(value[0]))
    print("Buzzer:", value[0])

# Register handlers
blynk.on("V2", relay_control)
blynk.on("V3", led_control)
blynk.on("V4", buzzer_control)

# ---------------- MAIN LOOP ----------------
while True:
    blynk.run()

    ir_value = GPIO.input(IR_PIN)
    ldr_value = GPIO.input(LDR_PIN)

    print("IR:", ir_value, " LDR:", ldr_value)

    # Send to Blynk
    blynk.virtual_write(0, ir_value)
    blynk.virtual_write(1, ldr_value)

    time.sleep(1)
```
---

###  Relay On Image
<img width="867" height="1156" alt="image" src="https://github.com/user-attachments/assets/109c7e4a-ff1c-4fc2-8d15-6ad5b8ffd93c" />

###  LED On Image
<img width="867" height="1156" alt="image" src="https://github.com/user-attachments/assets/183783c0-17a7-470f-a881-8dac3718f49a" />

###  Buzzer On Image
<img width="867" height="1156" alt="image" src="https://github.com/user-attachments/assets/642460f0-5865-493d-8b0e-22b78fd9498b" />

###  Screenshot for IR Sensor
<img width="721" height="1280" alt="image" src="https://github.com/user-attachments/assets/5b4cd592-b67d-401f-a3ce-3c74aec0c51e" />

###  Screenshot for LDR Sensor
<img width="721" height="1280" alt="image" src="https://github.com/user-attachments/assets/37c4dbf8-782f-4a91-83fd-30f5e7f42620" />

###  Screenshot for Relay ON
<img width="540" height="1115" alt="image" src="https://github.com/user-attachments/assets/91b871ab-add8-4450-96ac-225e556f9fb8" />

<img width="1204" height="1600" alt="image" src="https://github.com/user-attachments/assets/57e0a2ff-2acf-4eda-9f6f-6a9226362441" />

###  Screenshot for Relay OFF
<img width="721" height="1280" alt="image" src="https://github.com/user-attachments/assets/6970daed-39a8-4578-bc49-733287febe7f" />

<img width="1204" height="1600" alt="image" src="https://github.com/user-attachments/assets/09171173-6fcf-40dd-818f-52be4db005c7" />


###  Screenshot for Buzzer ON
<img width="540" height="1078" alt="image" src="https://github.com/user-attachments/assets/9cbed0d8-8c1a-453a-8d79-3a6932a9a6ee" />

<img width="1204" height="1600" alt="image" src="https://github.com/user-attachments/assets/efe6c689-c1fd-4c74-93b8-87037675e94d" />


###  Screenshot for Buzzer OFF
<img width="721" height="1280" alt="image" src="https://github.com/user-attachments/assets/503ce812-49b2-4897-bc43-856ca5d73022" />

<img width="1204" height="1600" alt="image" src="https://github.com/user-attachments/assets/1b01967b-5566-4f43-a06f-b9fa27b794d0" />


###  Screenshot for LED ON
<img width="540" height="1099" alt="image" src="https://github.com/user-attachments/assets/dca8d675-ca4f-47dc-be0c-802b044fb9b2" />

<img width="1204" height="1600" alt="image" src="https://github.com/user-attachments/assets/2cd2be1e-c314-4aed-87ca-0063d38da050" />

###  Screenshot for LED OFF
<img width="721" height="1280" alt="image" src="https://github.com/user-attachments/assets/e7b30ed9-6b43-4367-bc99-04ff20f1fc28" />

<img width="1204" height="1600" alt="image" src="https://github.com/user-attachments/assets/f44ce5bf-9e2b-4db5-92c9-f8cf62a512b2" />

## **RESULT:**  
Thus, the sensor values from the **IR and LDR sensors** were successfully monitored in the **Blynk mobile application using Raspberry Pi 4**, and the** output devices (LED, buzzer, and relay)** were controlled through the **Blynk interface based on the sensor inputs** and user commands.

---

