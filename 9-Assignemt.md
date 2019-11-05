
# Physical Computing Week 09

The two Arduinos boards are connected via the RX and TX pins (first Arduino’s TX pin to another’s RX pin and vice versa), ground is connected to ground and 5V to 5V.

![ArduinotoArduino](https://miro.medium.com/max/5200/0*Zu7FM8mU-2W6Cdic.png)


### Code for the Sender Arduino:

```javascript
void setup() {
 Serial.begin(9600);
}void loop() {
 Serial.println("A"),
 delay(1000);
 Serial.println("B"),
 delay(1000);
}
```

### Code for the Receiver Arduino:

```javascript
int data;
void setup() {
 Serial.begin(9600);
 pinMode(13, OUTPUT);}void loop() {
if (Serial.available()){
   data = Serial.read();
   if (data=='A'){
     digitalWrite(13,HIGH);
     } else if (data=='B') {
     digitalWrite(13,LOW);
     }
   }
}
```

![Video Doku](https://youtu.be/rWm5jiHD99w)

# Staying Alive

Staying alive! - Creating a visual heart rate monitor, inspired by the oscillation of guitar strings. Six particle sensors measure the audience's heart rate; the sensor values are sent to a Processing sketch, where they inform the respective string's curvature.

![Image](https://i.ytimg.com/vi/8YGQmV3NxMI/maxresdefault.jpg)

We'll need the following parts for the realization of the project:
Particle Sensor (6)
Description: “The MAX30105 is an integrated particle-sensing module. It includes internal LEDs, photodetectors, optical elements, and low-noise electronics with ambient light rejection. The MAX30105 provides a complete system solution to ease the design-in process of smoke detection applications including fire alarms. Due to its extremely small size, the MAX30105 can also be used as a smoke detection sensor for mobile and wearable devices. The MAX30105 operates on a single 1.8V power supply and a separate 5.0V power supply for the internal LEDs. It communicates through a standard I2C-compatible interface. The module can be shut down through software with zero standby current, allowing the power rails to remain powered at all times.”
(From datasheet: https://cdn.sparkfun.com/assets/learn_tutorials/5/7/7/MAX30105_3.pdf)
Rubber band
Arduino UNO (2 - particle sensors require two analog pins each)
LED for debugging

## Blockdiagram

![Blockdiagram](https://raw.githubusercontent.com/TTropschuh/ElectronicsWithPhil/master/Blockdiagram.PNG)


The following project will provide us guidance when working on the Processing sketch:


## Arduino pseudo sketch

```javascript
// Library to send to processing
// Library for the Particle Sensor MX30105

void setup(){
Serial.begin(9600);
}

void loop(){
  int particlesensor1 = analogRead(A0);
  int particlesensor2 = analogRead(A1);
  int particlesensor3 = analogRead(A2);

  Serial.write(particlesensor);
    Serial.write(particlesensor2);
    Serial.write(particlesensor3);
  delay(100);
}
```


## Processing pseudo sketch

```javascript

import processing.serial.*; //communicate with arduino via Serial

Serial myPort;

float xPos = 0; // horizontal position of the graph
float yPos = 0; // vertical position of the graph

void setup() {

  size(1280, 800);
  background(255);
  noCursor();
  String portName = Serial.list()[8]; // 8 is the portnumber
  myPort = new Serial(this, portName, 9600);
}


void serialEvent (Serial myPort) {
  int inByte = myPort.read();  // get the byte
  println(inByte);   // print it

  yPos = height - inByte;
}


  void draw () {
   // draw the line in a pretty color:
  stroke(#ffff);

  for(int i = 0; i < fft.specSize(); i++)
  {
    ellipse(i, 100, 7, fft.getBand(i) * 100); // draw ellipse
  }


  if (xPos >= width) {
    xPos = 0;
    background(255);

      } else {
    xPos++;
  }


}

```
