LP# IOT-Based smart irrigation system
Overview: IoT Based Smart Agriculture & Automatic Irrigation System
Agriculture plays a vital role in the development of agricultural countries. Some issues
concerning agriculture have been always hindering the development of the country.
Consequently, the only solution to this problem is smart agriculture by modernizing the current
traditional methods of agriculture.
Hence the method is making agriculture smart using automation and IoT technologies. Internet
of Things (IoT) enables various applicaƟons of crop growth monitoring and selecƟon, automatic
irrigaƟon decision support, etc. We proposed ESP8266 IoT AutomaƟc irrigaƟon system to
modernize and improve the productivity of the crop.
This presentaƟon explains how to make IoT Smart Agriculture with Automatic Irrigation System
using some simple sensors that are available in the market. We will use CapaciƟve Soil Moisture
Sensor to measure moisture coontent present in the soil. Similarly to measure Air Temperature
and Humidity, we prefer DHT11 Humidity Temperature Sensor. Using a 5V Power relay we will
control the Water Pump. Whenever the sensor detects a low quantity of moisture in the soil,
the motor turns on automatically. Hence, will automatically irrigate the field. Once the soil
becomes wet, the motor turns off. We can monitor all this happening remotely via Thingspeak
Server online from any part of the world.
Bill of Materials
We will need the following electronics components for making this project
S.N. Components Name QuanƟty
1 NodeMCU ESP8266 Board 1
2 CapaciƟve Soil Moisture Sensor 1
3 DHT11 Sensor 1
5 1 Channel 5V Relay Module 1
6 5V DC Motor Pump 1
7 Connecting Wires 10
8 Breadboard 1
Capacitive Soil Moisture Sensor
This is an analog capacitive soil moisture sensor which measures soil moisture levels by
capacitive sensing. This means the capacitance is varied on the basis of water content present
in the soil. We can convert the capacitance into voltage level basically from 1.2V minimum to
3.0V maximum. The advantage of CapaciƟve Soil Moisture Sensor is that they are made of a
corrosion-resistant material giving it a long service life. The sensor can be used to make
Automatic Plant Watering System.
Features & Specifications
1. Supports 3-Pin Sensor interface
2. Analog output
3. Operating Voltage: DC 3.3-5.5V
4. Output Voltage: DC 0-3.0V
5. Interface: PH2.0-3P
6. Size: 99x16mm/3.9×0.63഼
DC 3-6V Micro Submersible Mini Water Pump
The DC 3-6 V Mini Micro Submersible Water Pump is a low cost, small size Submersible Pump
Motor. It operates from a 2.5 ~ 6V power supply. It can take up to 120 liters per hour with a
very low current consumpƟon of 220mA. Just connect the tube pipe to the motor outlet,
submerge it in water, and power it.
Features & SpecificaƟons
1. OperaƟng Voltage: 2.5 ~ 6V
2. OperaƟng Current: 130 ~ 220mA
3. Flow Rate: 80 ~ 120 L/H
4. Maximum LiŌ : 40 ~ 110 mm
5. Outlet Outside Diameter: 7.5 mm
6. Outlet Inside Diameter: 5 mm
   
Circuit Connection

Connect the soil moisture sensor to A0 of Nodemcu and DHT11 to D4 Pin. The motor connects
to Relay. To control the relay, we use the D5 Pin of NodeMCU. Connect the OLED display to the
I2C pin of NodeMCU. You can power the Motor and Relay using the 5V pin of NodeMCU. The
DHT11 Sensor, CapaciƟve Soil Moisture Sensor, and OLED Display require a 3.3V Supply only.
Seƫng Up ThingSpeak Server
Now we need to setup the ThingSpeak Account. To set up ThingSpeak follow the following
Steps:

Step 1: Visit hƩps://thingspeak.com/ and create your account by filling up the details.

Step 2: Create a New Channel by Clicking on “Channel” & fill up the following details as shown
in the image below.

Step 3: Click on API Key, you will see the “Write API Key“. Copy the API Key. This is very
important, it will be required in Code Part.

Step 4: You can click on the “Private View” & customize the display window as you want.
So, that’s all from the Thingspeak Setup Part. Now let us move to the programming Part.

Testing & Results

This water pump need to be fully submerged in water. The outlet pipe is kept in a field for
irrigation. Similarly soil Moisture sensor is dipped in soil.
As soon as you power on the device, the OLED will start displaying the Soil Humidity, Air
Humidity, and also Air Temperature. It shows the real-Time Data. When the soil moisture
content is reduced the water pumps turn on and irrigate the field unƟl the required moisture is
achieved.
We can monitor the data online from any part of the world using ThingSpeak Server. To do that,
go to the private view of the ThingSpeak server. You can check the soil Moisture, Humidity, and
Temperature as well as relay status. 
__________________________________________________________________________________________________________________________

If you liked this repository don't forget to give a ⭐.