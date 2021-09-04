# ESP32-Blynk-2-IR-remote-control-relay-with-manual-Switches
IoT-based Smart Home Automation using the new Blynk 2.0 ESP32 LDR &amp; temperature sensor to control an 8-channel relay module from the manual switch, IR remote &amp; smartphone using the Blynk IoT App.

During the article, I have shown all the steps to make this Blynk home automation system.

## Tutorial video link for this IoT-based Home Automation project
https://youtu.be/Vgyj3cCAioI

This Blynk ESP32 control smart relay has the following features:

1. Control home appliances with WiFi (Blynk IoT App).
2. Control home appliances with Blynk web dashboard.
3. Control home appliances with IR remote.
4. Control home appliances with manual switches or push buttons.
5. Monitor real-time room temperature in the Blynk IoT App
6. Monitor real-time feedback in the Blynk IoT App.
7. Control appliances without WiFi

So, you can easily make this home automation project at home just by using an ESP32 and relay module. Or you can also use a custom-designed PCB for this project.

## Required Components:
1. ESP32 DEVKIT V1 board
2. 8-channel SPDT 5V Relay Module
3. TSOP1838 IR receiver (with metallic case)
4. DHT11 sensor
5. LDR
6. Manual Switches or Pushbuttons

If you use the custom-designed PCB for this project, then please refer to the following required components list.

## Required Components for the PCB
1. ESP32 DEVKIT V1
2. TSOP1838 IR receiver (with metallic case)
3. DHT11 sensor
4. LDR
5. Relays 5v (SPDT) (8 no)
6. BC547 Transistors (8 no)
7. PC817 Optocuplors (8 no)
8. 510-ohm 0.25-watt Resistor (8 no) (R1 - R8)
9. 1k 0.25-watt Resistors (10 no) (R9 - R18)
10. LED 5-mm (10 no)
11. 1N4007 Diodes (8 no) (D1 - D8)
12. Push Buttons (9 no) or Switches
13. Terminal Connectors
14. Jumper
15. 5V DC supply

## Required Software:
1. Arduino IDE
2. Blynk IoT

## Circuit Diagram of the ESP32 Projects
This is the complete circuit diagram for this home automation project. I have explained the circuit in the tutorial video.

The circuit is very simple, I have used the GPIO pins D23, D22, D21, D19, D18, D5, D25 & D26 to control the 8 relays.

And the GPIO pins D13, D12, D14, D27, D33, D32, D15 & D4 are connected with Switches to control the 8 relays manually.

And the output pin of the IR Receiver is connected with GPIO D35.

And the output pin of the DHT11 sensor is connected with the RX2 (GPIO16) pin, and the LDR is connected with GPIO D34 of the ESP32.

I have used the INPUT_PULLUP function in Arduino IDE instead of using the pull-up resistors.

I have used a 5V 5A DC power supply.

## Control Relays Using Blynk IoT App with Internet
If the ESP32 is connected with WiFi, then you can control the home appliances from Blynk IoT App.

You also use multiple smartphones to control the appliances with Blynk App. For that, you have to log in same Blynk account from all the smartphones.

In this way, all smartphones will be sink to the Blynk server. You can control, monitor the real-time status of the relays, room temperature & humidity from anywhere in the world in the Blynk IoT App.

If the ESP32 not connected with WiFi, still you can control the appliances with IR remote and Manual Switch without internet.


## ESP32 Control Relay With IR Remote
You can always control the relays from the IR remote. For this project, you can use any IR remote.

I will explain how to get the IR codes (HEX codes) from any remote in the following steps.

## Control Relays Manually using IR remote & Switches without Internet
You can always control the relays from the IR remote and switches. 
For this project, you can use any IR remote.

I have explained how to get the IR codes (HEX codes) from any remote in the following steps.

If the WiFi is connected then you can also monitor the real-time feedback in the Blynk IoT App.

## Download the PCB Gerber File
To make the circuit compact and give a professional look, I have designed the PCB after testing all the features of the smart relay module on the breadboard.

You can download the PCB Gerber file of this home automation project from the following link:

https://github.com/techstudycell/ESP32-Blynk-2-IR-remote-control-relay-with-manual-Switches/tree/main/PCB_Gerber

## Order the PCB from JLCPCB
After downloading the Garber file you can easily order the PCB

1. Visit https://jlcpcb.com/RAB and Sign in / Sign up
2. Click on the QUOTE NOW button.
3. Click on the "Add gerber file" button. Then browse and select the Gerber file you have downloaded.
4. Set the required parameter like Quantity, PCB masking color, etc.
5. After selecting all the Parameters for PCB click on SAVE TO CART button.
6. Type the Shipping Address.
7. Select the Shipping Method suitable for you.
8. Submit the order and proceed with the payment.
9. You can also track your order from the JLCPCB.com

My PCBs took 2 days to get manufactured and arrived within a week using the DHL delivery option. PCBs were well packed and the quality was really good at this affordable price.

## Solder All the Components on PCB
After that, I have soldered all the components as per the circuit diagram.

Then connect the ESP32 board, DHT11 SENSOR, LDR, and 1838 IR receiver with PCB.

## Setup FREE Blynk Cloud Account and Create Template for ESP32
For this smart house project, I have used the Blynk IoT Cloud Free plan.

Click on the following link to create a Blynk Cloud account.

https://blynk.cloud/dashboard/register

1. Enter email ID, then click on "Sign Up".
2. You will receive a verification email.
3. Click on Create Password in the email, Then set the password, click on Next.
4. Enter your first name, click on Done.
5. After that Blynk cloud dashboard will open.

After that you have to create template, Datatreams and configute the Web and Mobile dashboard. Please refer to following article for step by step intruction.
https://iotcircuithub.com/blynk-iot-platform-setup-esp8266-esp32/

## Get the IR Codes (HEX Code) From Remote

Now, to get the HEX codes from the remote, first, we have to connect the IR receiver output pin with GPIO D35.

And give the 5V across the VCC and GND. The IR receiver must have a metallic casing, otherwise, you may face issues.

Download the code for getting the HEX codes

https://github.com/techstudycell/ESP32-Blynk-2-IR-remote-control-relay-with-manual-Switches/tree/main/Code/Code_IR_Button_HEX_Code

Then follow the following steps to get the HEX codes

1. Install the IRremote library in Arduino IDE
2. Download the attached code, and upload it to ESP32.
3. Open Serial Monitor with Baud rate 9600.
4. Now, press the IR remote button.
5. The respective HEX code will populate in the serial monitor.
6. Save all the HEX codes in a text file.

## Program the ESP32 for This Blynk Project

Download the Codes for this ESP32 project

https://github.com/techstudycell/ESP32-Blynk-2-IR-remote-control-relay-with-manual-Switches/tree/main/Code/Code_ESP32_Blynk2_IR_DHT11_LDR_8Relays_Switch


Download and install the following libraries in Arduino IDE

1. Blynk 1.0.1 Library: https://github.com/blynkkk/blynk-library
2. IRremote Library (3.3.0): https://github.com/Arduino-IRremote/Arduino-IRremote
3. DHT Library (1.4.2): https://github.com/adafruit/DHT-sensor-library

You have to keep all the 9 files in the same folder.

1. Open the .ino file in Arduino IDE.
2. In the code, you have to update the BLYNK_TEMPLATE_ID and BLYNK_DEVICE_NAME.
3. Then update the HEX code in the ir_remote function as shown in the tutorial video.
4. After that, select the DOIT ESP32 DEVKIT V1 board and proper PORT.
5. Then upload the code to ESP32 Board.
6. While uploading the code to ESP32, if you see the Connecting....___ text, then press the BOOT button of the ESP32.

# Update the WiFi Credentials Through OTA
After programming the ESP32, you have to update the WiFi credentials from the Blynk IoT app.

In the tutorial video, I have explained all the steps to update the WiFi credentials to ESP32 through OTA.

Please refer to tutorial video ( https://youtu.be/Vgyj3cCAioI ) for more details.

## Finally!! the Blynk Smart Home System Is Ready
Now you can control your home appliances in a smart way.

I hope you have liked this new Blynk home automation project. I have shared all the required information for this project.

I will really appreciate it if you share your valuable feedbacks. Also if you have any query please write in the comment section.

Thank you & Happy Learning.
