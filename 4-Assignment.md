# Assignment Week 5

## Modify the first easing code example (geometric) to toggle easing on and easing off when triggered by an analog event.

```javascript
#define ledPin 12
#define buttonPin 5
float progress, easeTime;
unsigned int triggerTime, currentTime;


void setup(){
  triggerTime = 0;
  easeTime = 3000.0;
  progress = 0;
  pinMode(ledPin, OUTPUT);
  Serial.begin(9600);
}

void loop() {
  current_time = millis();
  progress = (currentTime - triggerTime) / easeTime;

    if (progress <= 1){
      analogWrite(ledPin, int(255 * pow(progress, 2)));
    }

    if (progress >= 1){
      analogWrite(ledPin, int(255 * (1/pow(progress, 6))));
      if (progress == 2.25){
        triggerTime = currentTime;
        }
    }
}
```

![First_assignmet]()

## Modify the second easing code example (progress) to use sin() to do a single smooth pulse in response to an analog event.

```javascript
// declare the vars.
#define ledPin 12

#define buttonPin 5
const int debounce = 20;
unsigned int lastButtonTime, triggerTime, currentTime;
boolean lastButtonRead, buttonPressed, buttonRead;
float easeTime, progress;


void setup() {
  // declare the state of the vars.
  easeTime = 2500.0;
  triggerTime = int(easeTime);
  lastButtonTime = 0;
  currentTime = 0;
  buttonRead = LOW;
  lastButtonRead = LOW;
  buttonPressed = false;
  pinMode(ledPin, OUTPUT);
  pinMode(buttonPin, INPUT);
}

void loop() {
  current_time = millis();
  float out;

  if (buttonIsPressed()) {
    triggerTime = currentTime;
  progress = (currentTime - triggerTime) / easeTime;
      out = sin(progress) * 127.5 + 127.5;
      analogWrite(ledPin, out);
    }
}

boolean buttonIsPressed() {
boolean buttonState;
  if (currentTime - lastButtonTime > debounce) {
    buttonRead = digitalRead(buttonPin);
    lastButtonTime = currentTime;
  }

  if (lastButtonRead == LOW && buttonRead == HIGH) {
    buttonState = true;
  }

  else {
    buttonState = false;
  }

  lastButtonRead = buttonRead; // save the buttonState
  return buttonState;
}
```

## use pow(x, 2) and sin() to make an LED breathe

```javascript
int ledPin = 12;
int buttonPin = 5;    
int process;    
int before = HIGH;
int state = LOW;   

long lastPressed = 0;         
long debounce = 150;

void setup() {

  pinMode(buttonPin, INPUT);
  pinMode(ledPin, OUTPUT);
  Serial.begin(9600);
}

void loop() {

  process = digitalRead(buttonPin);

  if ((process == HIGH) && (before == LOW) && (millis() - lastPressed > debounce)) {
    if (state == HIGH){
      state = LOW;}
      else if (state == LOW){
      state = HIGH;}

    lastPressed = millis();
  }

  digitalWrite(ledPin, state);

  before = process;
}
```

# Journal Week 5


Are there particular interactions you're interested in?
I think there are no Interactions that I am not interested in.

Are there particular contexts that you want to engage with?
I would love to work in an urban context!

What kind of research have you already been doing?
Urban Sensing
What is senseable in our urban environment what is invisible to us and how can we visualize it.
The project Immaterials by Timo Arnall, Jørn Knutsen and Einar Sneve Martinussen deals with a different kind of visualization through a longer exposure time with their camera, which is to me a very interesting tool to show data at a specific geographical point.
They built a WiFi measuring rod that visualizes WiFi signal strength as a bar of lights. When moved through space the rod displays changes in the WiFi signal. Long-exposure photographs of the moving rod reveal cross sections of a network’s signal strength. However, if I think more further in terms of a final project I would like to find a similar tool to represent data in our urban space that is invisible to us. In this example they used Wifi signals but what else is measurable in New York City? Bluetooth signals? Noise? Fine dust?

Digital Ethereal: https://twistedsifter.com/2014/07/visualizing-wifi-signals/
Immaterials: http://yourban.no/2011/02/22/immaterials-light-painting-wifi/

![Pic1_Immaterials](https://ttropschuh.myportfolio.com/journal-week-5)
![Pic2_Immaterials](https://pro2-bar-s3-cdn-cf6.myportfolio.com/ca83548a-7b2c-4be6-9666-6b6b66eff60b/7047fc44-349b-44f0-bf04-07362c6fb4d6_rw_600.jpg?h=7bb4931252f01964806ffdc7819ec7eb)

Hardware Hacking
If I look at a motherboard from my MacBook it reminds me of tiny streets that lead to different stations inside a very complex system if tin, plastic and crazy chemicals I don’t know. I also don’t know the name of the stations and I have no clue about their purpose. I want to dig deeper into understanding electronic circuits by taking already excising electronic products apart, explore them with the multi meter, maybe repair them and then use the hardware in a different context. As the context is depending in the hacked hardware I cant tell in what direction this project will lead me. This would be a more learning by making project which will evolve with my knowledge about the inside of black boxes that surround us.
My idea got inspired by Andrew "Bunnie" Huang and his Essay “Hacking the Xbox” and his book “The Hardware Hacker” which will however also be my supporting reading for this project.

Maybe helpful: https://www.youtube.com/user/rossmanngroup

![Hardwarehacking](https://pro2-bar-s3-cdn-cf5.myportfolio.com/ca83548a-7b2c-4be6-9666-6b6b66eff60b/6714bbdd-b169-4c83-b5a7-29bf82b37c14_rw_1200.jpg?h=59c3fda0630128edc07c73c3fcab7295)
