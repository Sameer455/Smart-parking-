# Smart-parking-
Bharat intern

![image](https://github.com/Sameer455/Smart-parking-/assets/136076879/c367bf43-4429-48e8-93d1-aacbe11989db)

Libraries: The script imports the required libraries for the various components and services it uses. These libraries include WiFi support for the ESP8266, Servo for controlling the servo motors, LiquidCrystal_I2C for interacting with the LCD display, Wire for I2C communication, and FirebaseArduino for interacting with Firebase.

Defines and Variables: The program then defines several constants and initializes several variables. The constants include the Firebase host and authentication key, WiFi SSID and password, pins for different devices, and the total number of parking spaces. The variables include two Servo objects (for gate control), an LCD object, variables for counting and storing available spaces, strings for sending status updates to Firebase, and several others for reading sensor values and controlling the servos.

Setup: In the setup function, the script sets up the WiFi connection, starts the Serial monitor for debugging, initializes the pins for the devices, sets up the LCD display, connects to Firebase, and initializes the servo motors.

Main Loop: The main loop function handles the program's core functionality. Here's what it does:

It uses an ultrasonic sensor to measure the distance of the nearest object.
It checks if a car has entered the parking area. If so, it increments a count, displays a message on the LCD, opens the entrance gate (controlled by a servo motor), and sends a status update to Firebase.
It checks if a car has exited the parking area. If so, it decrements the count, displays a message on the LCD, opens the exit gate (controlled by another servo motor), and sends a status update to Firebase.
It checks if the distance measured by the ultrasonic sensor is less than 6cm (indicating a car is parked in the spot). If so, it turns on an LED. If the distance is more than 6cm, it turns the LED off.
It calculates the number of available spaces by subtracting the count of parked cars from the total spaces, and updates this information on the LCD.
This code essentially makes an intelligent parking system that automates the process of tracking available parking spaces and controlling the entrance and exit of vehicles, and updates the data in real-time on Firebase
