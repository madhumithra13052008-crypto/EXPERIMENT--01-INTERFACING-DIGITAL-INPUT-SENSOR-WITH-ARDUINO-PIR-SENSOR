# EXPERIMENT--01-INTERFACING-DIGITAL-INPUT-SENSOR-WITH-ARDUINO-PIR-SENSOR
EXPERIMENT -01  INTERFACING DIGITAL INPUT SENSOR WITH ARDUINO PIR SENSOR

# Name:Madhumithra P
# Reg no:212225230159

## AIM:  To interface a digital input sensor (PIR Sensor )with arduino .
## COMPONENTS REQUIRED:

1.      Arduino Uno

2.     Bread board

3.      Tinker cad

## ALGORITHM:
  Start the program, declare an integer variable sensorstate and initialize it to 0. Configure digital pin 2 as INPUT and the built-in LED pin as OUTPUT. Initialize serial communication at 9600 baud rate. Read the PIR sensor output using digitalRead(2). If the sensor output is HIGH, turn ON the built-in LED and display "Sensor activated" on the Serial Monitor. Otherwise, turn OFF the built-in LED. Repeat the process continuously.

## PROCEDURE:
  Connect the VCC pin of the PIR sensor to 5V, GND pin to GND, and OUT pin to digital pin 2 of Arduino. Connect the Arduino to the computer using a USB cable. Open the Arduino IDE, type the given program, verify and upload it to the Arduino board. Open the Serial Monitor and set the baud rate to 9600. Move in front of the PIR sensor and observe the output. When motion is detected, the built-in LED glows and the message "Sensor activated" is displayed on the Serial Monitor. When no motion is detected, the LED turns OFF.
## PROGRAM:
```C++
int sensorstate = 0;

void setup()
{
  pinMode(2, INPUT);
  pinMode(LED_BUILTIN, OUTPUT);
  Serial.begin(9600);
}

void loop()
{
  sensorstate = digitalRead(2);
  
  if (sensorstate == HIGH) { 
    digitalWrite(LED_BUILTIN, HIGH);
    Serial.println("Sensor activated");
  }
  else
  {
    digitalWrite(LED_BUILTIN, LOW); // Fixed: Corrected 'LED_BUILTN' typo
  }
  delay(10);
}
```
## OUTPUT:
Led ON Working state:
<img width="684" height="516" alt="WhatsApp Image 2026-10-30 at 8 32 58 AM" src="https://github.com/user-attachments/assets/a333729f-8cf6-4a2c-97dd-f8b69f660242" />
## RESULT:
Thus,To interface a digital input sensor (PIR Sensor )with arduino was executed successfully and the output is verified.
