IoT Light Control Using MQTT

This project is an interactive web application designed to control a virtual light bulb using the MQTT protocol. It includes a web-based interface with animated lighting effects and a Python script that emulates an ESP8266 IoT device, responding to MQTT commands.



Features

Intuitive web-based UI with real-time light bulb animation

MQTT-powered communication for seamless IoT integration

Instant ON/OFF toggle with visual feedback

Flickering effect when turning on the light

Python script simulating an IoT-enabled device

Project Structure

index.html – Web-based control panel for the light system

light_simulation.py – Python script mimicking an ESP8266 device

README.md – Setup instructions and project documentation

Technical Details

Implements MQTT.js for WebSockets-based MQTT communication in the browser

Uses Paho MQTT library for Python-based device emulation

Connects to an MQTT broker at 157.173.101.159

Publishes commands via /student_group/light_control

Listens for status updates on /student_group/light_status

Setup & Installation

Prerequisites

A JavaScript-enabled web browser

Python 3.x with the paho-mqtt package installed

Internet access to connect to 157.173.101.159

Running the Web Interface

Open index.html in a browser

The UI connects to the MQTT broker via WebSockets (port 9001)

Use the buttons to switch the light ON or OFF

Running the Python IoT Simulation

Install dependencies:

pip install paho-mqtt

Launch the simulation script:

python light_simulation.py

The script connects to the MQTT broker on port 1883 and processes commands

MQTT Topics

/student_group/light_control – Sends ON/OFF commands

/student_group/light_status – Receives light state updates

How It Works

The web application publishes ON/OFF messages to /student_group/light_control.

The Python script subscribes to this topic and executes commands accordingly.

The script then sends the light’s status to /student_group/light_status.

The UI updates its animation based on the received status.

Troubleshooting

If the web app fails to connect, check the MQTT broker’s status.

Ensure port 9001 is accessible for WebSockets communication.

Verify port 1883 is open for MQTT connections in Python.

Inspect browser console logs for connection issues.



Acknowledgments

MQTT.js for handling browser-based MQTT communication

Paho MQTT for managing Python-based MQTT operations