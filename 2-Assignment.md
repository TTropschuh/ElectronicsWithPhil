# Assignemt 3

## A button and a LED. A never ending Romance.


Millies? What's that?

As delay has some side effects like stopping all the actions in the arduino till it is finished it maybe can be conviniend to just stop one action for a specific time. This is where the timing commands come into function.



### If button is pressed for 3 seconds, one LED should light up.

```java

int LED1 = 12;
int button = 2;

boolean LED1State = false;

long buttonTimer = 0;
long longPressTime = 3000;

boolean buttonActive = false;
boolean longPressActive = false;

void setup() {

  pinMode(LED1, OUTPUT);
  pinMode(button, INPUT);

}

void loop() {

  if (digitalRead(button) == HIGH) {

    if ((millis() - buttonTimer > longPressTime) && (longPressActive == false)) {

      longPressActive = true;
      LED1State = !LED1State;
      digitalWrite(LED1, LED1State);

    }
  }
}

```

![button is pressed](https://raw.githubusercontent.com/TTropschuh/ElectronicsWithPhil/master/IMG_7778.gif)

### If a button is pressed and held for 6 seconds and a second button is pressed, make the LED do some special behavior.


### Explore combining behaviors.

### How many different LED behaviors can you get out of just two switches and measuring how long they're pressed?


https://forum.arduino.cc/index.php?topic=503368.0
