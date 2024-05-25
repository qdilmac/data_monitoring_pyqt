# Monitoring Sensor Data GUI with Pyside

## Description
I wrote this project to create a simple Pyside GUI and read data from an MPU6050 sensor connected to an ESP32 microcontroller. The sensor data (accelerometer and gyroscope readings) are displayed on the GUI's designated LCD displays.
This was a small "unknown" for me but I'm happy that I solved the problem. It took some time but I managed it in couple hours. If this helps you out in any way, feel free to use it!

Update 26/05 -> The project took a different route that I have expected but I'm not complaining. The GCS concept is one of the main parts of my robotics (UGV, UAV, Robotic Arm etc.) projects. So every second that i spent on this is worth the time!

## Updates
14/05/2024 -> Added simple led to the circuit to not only read but also send serial data to control components. Will be useful in future for remote control applications.

18/05/2024 -> Added camera feed with multithreading. The project changed course and now it started to resemble a complete gui with camera feed, sensor data monitoring and sending data over serial.

19/05/2024 -> Added another thread for data monitoring. This solved stuttering in camera feed.

20/05/2024 -> Added face detection.

26/05/2024 -> Organized the repo into folders for different versions. Started working on second version.

## TO-DO
Test or implement communication over a network. Eliminate the need for wired serial connection. -> <b>WIP</b>

Add face detection to test processed image monitoring -> <b>DONE</b>

Add angle estimation using Kalman filtering. -> <b>WIP</b>

Update GUI for v2-> <b>DONE</b>

## Problems
To use camera feed without 1 second pauses I need to find efficient way to read data without stopping camera feed every second. I might be able to use another thread for it. -> <b>SOLVED</b>

"TypeError: '>=' not supported between instances of 'PySide6.QtGui.QImage' and 'int'". Even tho the type of FaceDetection signal is integer, this error occurs. But program works well without any problem. -> <b>UNSOLVED</b> 

## Requirements
- Python 3
- PyQT / Pyside
- pySerial
- QTDesigner (easier UI design)
- MPU6050
- ESP32s
