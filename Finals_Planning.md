## Narrative description

New York City is from a sensual perspective overwhelming. Everywhere we are perceiving something. We see adds, people crossing our way and smell the city in sometimes a good but mostly in a bad way. In this project I want to focus on humans’ sensual experiences that are not visible and hard to grasp. To narrow this a little bit down I set myself the topic “Pollution” which is and will always be in a city like New York a hot topic. The main aim in this midterm project is to make the data perceivable in an optical way. The collected data should not get dusty in an exel sheet but rather be caught in its context: The streets of New York.

__How does the viewer percieve the Project?__
The viewer will be confronted with photographs in a exhibition context. The interactive piece intself is just a tool to visualize the topic I want to thematize: Waves in the city. Buy visualizing something invisible I would like to bring the topic closer to your physical world. The final photos should be the beginning of a discussion about electronics that are hardly to think way of our daily lifes. This tool itself I build and use to visualize the invisible is the physical interactive part of the project without people really noticing beeing part of it. The interactivity on the public space itself is passiv. The final visualization should then start the active part


what is the physical present?
The Light Stick (or Star wars like visualization weapon)

![Gif of star wars](https://external-content.duckduckgo.com/iu/?u=http%3A%2F%2Fbestanimations.com%2FSci-Fi%2FStarWars%2Fstar-wars-animated-gif-40.gif&f=1&nofb=1)



## Technical Description

List components and parts (data sheet, tutorials);

#### Parts:
-	Resistor (Find the right one) 1 and 10 Mega Ohms --> maybe make a pre-assembled kit?
-	LED strip (APA 102C LEDs)
  [Nice Description](https://www.pololu.com/product/2557)
  [Data sheet](https://www.pololu.com/file/0J891/APA102C.pdf)
  [Libary for Arduino](https://github.com/pololu/apa102-arduino)
  Length: .5 meter
  24 Bit color control
  Uses Serial Peripheral Interface
  Each LED needs 50mA
  Power supply 5V / 3 amps

-	Button
-	Wire as antenna (selfmade) 

This guy already built an antenna. --> http://www.aaronalai.com/emf-detector
-	Camera to make the Lightpainting (borrow from equipment service)
-	External Power source [This could work.](https://www.amazon.com/Attom-Tech-Portable-External-Emergency/dp/B07JZCZSH9/ref=sxbs_sxwds-stvp?keywords=power+bank+5v+3+amp&pd_rd_i=B07JZCZSH9&pd_rd_r=137a34d2-0440-4871-900d-dd0c28478eec&pd_rd_w=BGb0X&pd_rd_wg=O6jPf&pf_rd_p=a6d018ad-f20b-46c9-8920-433972c7d9b7&pf_rd_r=A46MDZ92TSF9QRZ90Q80&qid=1574281168)

How do the components interact?

Button Input --> Wait half a second --> Get Data from Antenna --> Map to LED strip for 2 seconds --> Reset


## Conceptual Description

Context and reason of the Project

Im Flugzeug heißt es Flugmodus an. Im Bett lieber mal in den Nachtmodus schalten, denn die Stahlung kann ja vielleicht doch Auswikrunge auf den Menschen haben. Doch wissen wir das? Es gibt Menschen die sind vorallem auf electrische Stahlung sehr sensibel und können gar nicht mehr in einer von Technologie getriebenen Gesellschaft leben. Doch es ist immer noch nicht nachgewiesen, dass elektrische Strahlung einen Einfluss auf unsere Gesundheit hat. Es gibt zwar Theorien aber eigentlich sind die alle nichtssagen bzw werden von vielen Ärzten nicht als offiziell angesehen.
Ein extremes Beispiel ist Blabla. Er lebt seit Jahren abseits von der Gesellschaft im Wald, weil er die Stahlung einfach nicht aushält. Sein Körper reagiert mich extremen Kopfweh und Schwächeanfällen.
Abseits von dem FAkt dass wir nicht wissen was die Stahlung mit unserem Körper macht, ist diese für uns nicht greifbar. Dies ist auch der Grund warum damit nicht ernst ungegangen wird. Ist es nicht sichtbar, ist es nicht existent. Dieses Projekt soll genau diese Stahlung von der wir mehr wissen sollten sichtbar machen. Ob diese nun gesundheitlich schädlich für uns ist oder nicht, ist in diesem Projekt nicht das Hauptthema jedoch soll es helfen eine mögliche Gefahr zu visualisieren.

"Are you already in flightmode? is the stuartesse asking. In bed it's better to switch to night mode, because this is what media recommends us to do and we dont want to be desturbed. But do what about health reasons? Some people are particularly sensitive to electrical steeling and can no longer live in a society driven by technology. But it has still not been proven that electric radiation has an influence on our health. There are theories, but actually they are all meaningless or not proved official by many doctors.
An extreme example is Ulrich Weiner. He has been living away from society in the forest for years, because he simply can't stand the radiation. His body reacts to extreme headaches and weakness attacks. Find the full story [here](https://ul-we.de/about-me/) ![house of Ulrich](https://ul-we.de/wp-content/uploads/2011/05/P1010226.jpg)
Apart from the fact that we do not know what the radiation does to our body, it is not tangible for us. This is also the reason why it is not taken seriously. If it is not visible, it does not exist. This pis where my project jumps in. Whether this is harmful to our health or not is not the main topic in this project, but it should help to visualize a possible danger.


### Project Immaterials
![Immaterials](https://external-content.duckduckgo.com/iu/?u=http%3A%2F%2Fs3.amazonaws.com%2Flighthouse.s3.amazonaws.com%2Fassets%2F1071%2Fprimary.jpg%3F1374069487&f=1&nofb=1)
This project uses the same technique to visualize somethin invisible. They are measuring Wifi signals in outdoor areas and use lightpainting as a tool to visualize those signals in a geographical context.
Find the description [here](http://www.lighthouse.org.uk/programme/immaterials).

### Project Immaterials the form of metadata
![](https://onformative.com/assets/work/immaterials_05.jpg)

Find the description [here](https://onformative.com/work/immaterials).


## Block Diagram of Elements and Interactions

![Schematic](https://raw.githubusercontent.com/TTropschuh/ElectronicsWithPhil/master/photo_2019-11-20_16-47-58.jpg)

## Conceptual Renderings of the Project
![](https://raw.githubusercontent.com/TTropschuh/ElectronicsWithPhil/master/walker.png)
