# Assignment Week 6

## Complete - Driving a Motor with the H-bridge Class Exercise "Bidirectional DC Motor"

```javascript
int en1 = 12;
int MotorIn = 11;
int MotorOut = 10;
int dir = 5;
int potiValue = 0;

void setup()
{
  pinMode(MotorIn, OUTPUT);
  pinMode(MotorOut, OUTPUT);
  pinMode(en1, OUTPUT);
  pinMode(dir, INPUT_PULLUP);
}

void loop()
{
  int speed = map(analogRead(potiValue), 0, 1023, 0, 255);
  boolean reverse = digitalRead(switchPin);
  setMotor(speed, reverse);
}

void setMotor(int speed, boolean reverse)
{
  analogWrite(en1, speed);
  digitalWrite(MotorIn, !reverse);
  digitalWrite(MotorOut, reverse);
}
```

## Complete - Adafruit Servo Walkthrough

![Video](https://raw.githubusercontent.com/TTropschuh/ElectronicsWithPhil/master/IMG_7816.gif)

# Journal Week 6


## Project [IN]VISIBLE for the Midterm

### Make the invisible, visible.

New York City is from a sensual perspective overwhelming. Everywhere we are perceiving something. We see adds, people crossing our way and smell the city in sometimes a good but mostly in a bad way. In this project I want to focus on humans’ sensual experiences that are not visible and hard to grasp. To narrow this a little bit down I set myself the topic “Pollution” which is and will always be in a city like New York a hot topic. The main aim in this midterm project is to make the data perceivable in an optical way. The collected data should not get dusty in an exel sheet but rather be caught in its context: The streets of New York.  

#### What is pollution?
Definition from Webster:
The action of polluting especially by environmental contamination with man-made waste
Definition from Cambridge dictionary:
damage caused to water, air, etc. by harmful substances or waste.

#### Conclusion:
To pollute things means to make something morally unclean or to defile.
This means basically everything that is unclean counts as polluted. Lets make a quick brainstorming in what ways urban spaces can be polluted:

![](https://pro2-bar.myportfolio.com/v1/assets/ca83548a-7b2c-4be6-9666-6b6b66eff60b/af0096ba-0664-472f-afc2-1061e793754f.PNG?h=5d2f6fe5e2e0da19297dde6bacdfb64c)
![](https://pro2-bar.myportfolio.com/v1/assets/ca83548a-7b2c-4be6-9666-6b6b66eff60b/2114707b-24d2-4133-8810-4f5ba4c95d39.PNG?h=1babc7c0cc871d7a693b06364e2aa51c)


## FOCUSPOINT --> Electric Spectrum pollution in urban spaces

![](https://pro2-bar-s3-cdn-cf6.myportfolio.com/ca83548a-7b2c-4be6-9666-6b6b66eff60b/a1c9b661-eba7-447b-b49a-915c1073cfec_rw_600.gif?h=7f1d20438b296acc6c5ba96862f351e5)

I know, sound is not part of the electric spectrum. Although I didn’t want to exclude it. Noise requires some kind of medium to travel through, such as air. This means, no air, no sound.  Maybe I should rename the project in Wave pollution…not sure yet.


## Wave Pollution in urban spaces

### Project Sound of Silence
#### Step 1. Get the sound!
Sound is measured in decibel.  Therefore, I will need the following components:
- Electric condenser microwave
- Amplifier LM386 Low Voltage Audio Power Amplifier
- Capacitors (a bunch...)
- Resistors

Source: https://circuitdigest.com/microcontroller-projects/arduino-sound-level-measurement

![](https://pro2-bar.myportfolio.com/v1/assets/ca83548a-7b2c-4be6-9666-6b6b66eff60b/56ebad15-a330-4ec1-bcad-1b1844e7e22d.png?h=b1659131dbcaf158460160bdc90c50c0)
↑↑↑↑↑↑↑↑↑↑↑↑↑↑↑↑↑↑↑↑↑↑↑↑↑↑↑↑↑↑↑↑↑↑↑↑↑↑↑↑↑↑↑↑↑↑↑↑↑↑↑
 I stole this circuit diagram. I need more time to fully understand it.


#### Step 2. Light it up!
To visualize the sound in a certain urban context I will need a visible output. Aka Light. In the project Immaterials I mentioned in the journal before they used one LED stripe on a vertical stick with a length of nearly 4 meters to capture the Wifi signals as an amplitude. However, this kind of visualizations doesn’t really capture where the signal is coming from. The source in this context can also be interesting factor that can be made visible with this technic. Currently I am not sure in which form the light should appear but I know it will be definitely light.

Components I will need:
- LED Stripe
- Button
- Powerbank
- Capacitor (100 µF)
- Resistor (220 ohm)
- Arduino Micro (small because I need to connect it to a device that I needs to be easy to carry around.)

Source: https://www.youtube.com/watch?v=UVISnxXh_VY

![](https://pro2-bar-s3-cdn-cf3.myportfolio.com/ca83548a-7b2c-4be6-9666-6b6b66eff60b/40c404d6-5ecb-4361-a561-259dcc460fe6_rw_1200.jpg?h=bef79b5a8b069a60fea61f2f1e924ae8)


### Potential Problems I might face:
I think the most complex part is to fully understand the first step of measuring the sound and write the code of a proper translation of the values into decibel. I need to check out if there is an existing library.
Another problem that can come up is if I just use one microphone as an input, the data won’t be really reliable. The best would be to connect to microphone and then calculate an average of that.
