# Precision Aquaculture
Design and Development of a Real-time water quality monitoring system for precision aquaculture using Arduino Uno, DS18B20 Temperature sensor and pH -4502c sensor. The entire circuitry will be placed in a specially designed 3D printed confinement for in-field applications. 

Documentation:
Libraries used:

    OneWire: This library allows communication with devices using the one-wire protocol. In this case, it's used to communicate with the DS18B20 temperature sensor. 
    
    DallasTemperature: This library provides functions to interact with Dallas Temperature ICs (DS18B20 in this case).

Pin Connections:

    DS18B20 temperature sensor:
    
        VCC pin: Connect to 5V pin of Arduino.
        GND pin: Connect to GND pin of Arduino.
        DATA pin: Connect to digital pin 2 of Arduino.

    pH-4502C sensor:
    
        VCC pin: Connect to 5V pin of Arduino.
        GND pin: Connect to GND pin of Arduino.
        Analog Output pin: Connect to analog pin A0 of Arduino.

Functions:

    setup(): This function is called once when the Arduino starts. It initializes the serial communication and starts the DallasTemperature library.

    loop(): This function is called repeatedly after the setup() function. It reads the temperature from the DS18B20 sensor and the pH value from the pH-4502C sensor. It then prints the values to the serial monitor and adds a delay of 1 second.

    convertToPH(int pHValue): This function converts the analog reading from the pH sensor to the corresponding pH value. It uses a linear equation based on the calibration of the sensor.

Usage:

    Connect the DS18B20 temperature sensor and the pH-4502C sensor to the Arduino Uno as per the pin connections mentioned above.

    Install the OneWire and DallasTemperature libraries in the Arduino IDE. You can do this by going to Sketch > Include Library > Manage Libraries and searching for the libraries by name.

    Open a new sketch in the Arduino IDE and paste the code provided above.

    Upload the sketch to your Arduino Uno.

    Open the serial monitor by clicking Tools > Serial Monitor or pressing Ctrl+Shift+M (or Cmd+Shift+M on Mac). Set the baud rate to 9600.

    You should see the temperature and pH values being printed in the serial monitor.

