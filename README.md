# pdn-load-transient-test
Automated load transient testing script for PDN qualification using SCPI and PyVISA
PDN Load Transient Test Automation Script 
 
Overview:
This repository contains a simple Python script developed to demonstrate automated load transient testing for the Power Distribution Network (PDN) described in the assessment. The purpose of the script is to automate basic test actions such as configuring instruments, applying load conditions, and logging measurements. The automation uses SCPI commands through the PyVISA interface to communicate with laboratory instruments. 

Instruments: 
The automation concept assumes the following instruments available in the lab: 
Programmable DC Power Supply – Keithley 2230-30-1 
Programmable Electronic Load – Keithley 2380 Series 
Oscilloscope – Keysight DSOX6004A 
Digital Multimeter – Keithley DMM6500 

Automation Approach: 
The Python script performs: 
Initialize communication with instruments using VISA. 
Configure the programmable power supply to provide the required input voltage to the PDN board. 
Configure the programmable electronic load. 
Increase load current from no-load condition to rated load. 
Measure voltage and current values during the test. 
Log the measured values into a CSV file with timestamps. 

The oscilloscope is used to observe ripple and transient response of the voltage rails during load steps. In this example implementation, the oscilloscope is configured manually and used to visually verify waveform behavior. 

Code Reference: 
Some portions of the instrument communication structure are referenced from manufacturer automation examples provided by Tektronix / Keithley for instrument control using SCPI commands. 

Notes:
The script demonstrates the concept of automated PDN load transient testing. 
Actual VISA resource addresses may vary depending on the laboratory setup. 
The code structure can be extended further to automate waveform capture and detailed reporting.
