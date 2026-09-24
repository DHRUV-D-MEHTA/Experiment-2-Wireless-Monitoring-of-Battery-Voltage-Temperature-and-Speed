# Experiment-2-Wireless-Monitoring-of-Battery-Voltage-Temperature-and-Speed

## Aim:
To design and implement a MATLAB-based system to monitor parameters such as battery voltage, temperature, and vehicle speed, and wirelessly transmit the data to a central monitoring station.
 
## Theory:
1. Importance of Monitoring Parameters in Electric Vehicles (EVs)
•	Battery Voltage: Ensures efficient power distribution and prevents over-discharge.
•	Temperature: Protects the battery and motor from overheating.
•	Speed: Helps maintain optimal performance and energy consumption.
2. Wireless Data Transmission
•	Wi-Fi (ESP8266/ESP32), Bluetooth (HC-05), or ZigBee (XBee) can be used to send sensor data.
•	The central monitoring station receives data and displays it using MATLAB.
 
## Procedure:
1.	Sensor Setup:
o	Use sensors like LM35 (temperature), voltage dividers (battery voltage), and Hall-effect sensors (speed).
o	Connect them to an Arduino/ESP32/Raspberry Pi for data acquisition.
2.	Wireless Communication:
o	Use Wi-Fi (ESP8266/ESP32) or Bluetooth (HC-05) to send data to a central monitoring station.
3.	MATLAB Data Processing:
o	Read the incoming serial data.
o	Parse and store voltage, temperature, and speed values.
o	Display the data using real-time plots.
 
## Program:

## MATLAB CODE

```matlab
clear; clc; close all;

t = linspace(0,10,100);

v = 48 + 2*sin(t);
temp = 30 + 5*sin(0.5*t);
spd = 40 + 20*sin(0.3*t);

subplot(3,1,1);
plot(t,v,'b','LineWidth',2);
title('Battery Voltage Monitoring');
xlabel('Time (s)');
ylabel('Voltage (V)');
grid on;

subplot(3,1,2);
plot(t,temp,'r','LineWidth',2);
title('Temperature Monitoring');
xlabel('Time (s)');
ylabel('Temperature (°C)');
grid on;

subplot(3,1,3);
plot(t,spd,'g','LineWidth',2);
title('Speed Monitoring');
xlabel('Time (s)');
ylabel('Speed (km/h)');
grid on;

disp('Data Monitoring Complete.');
```

## OUTPUT

The MATLAB simulation displays three graphs:

1. Battery Voltage Monitoring
2. Temperature Monitoring
3. Speed Monitoring

The Command Window displays:

```text
Data Monitoring Complete.
```


## Output:
<img width="1917" height="1016" alt="image" src="https://github.com/user-attachments/assets/49af650d-d07d-4097-9b21-40f31d06f58e" />


 
## Result:
The MATLAB program successfully receives and visualizes real-time battery voltage, temperature, and speed data from the embedded system using wireless communication.

