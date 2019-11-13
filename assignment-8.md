# Assignment 8

Build a working demo of a data visualization with bi-directional serial communication between the Arduino and Processing.

## Get input from the potentiometer and visualize it with a circle.
### Arduino Sketch
```java

int potPin = 0;
void setup() {

  Serial.begin(9600);
}

void loop() {
  int sensorValue = analogRead(potPin);   
  //Because the processing 'serial.read()' only support the value between 0-255,
  //so I need to put a scale of 0-1023 numerical scale between 0-255
  int Voltage = map(sensorValue,0,1023,0,255);
  Serial.write(Voltage);  
  //Serial.println(Voltage);  
  delay(100);
}


```

### Processing Sketch

```java
import processing.serial.*;

Serial myPort;
int Voltage;

void setup(){
  size (700, 700);
 //fullScreen();
  String portName = Serial.list()[0];
  myPort = new Serial(this, "COM8", 9600);
}

void draw(){
  background(0);
  if(myPort.available() > 0){
   Voltage = myPort.read();

   ellipse(width/2, height/2, Voltage*2, Voltage*2);
   fill(100);
  }



print(Voltage);
delay(100);

}
```

![](https://raw.githubusercontent.com/TTropschuh/ElectronicsWithPhil/master/poti_circle.gif)
