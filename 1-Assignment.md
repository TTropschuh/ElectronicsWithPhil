# Assignment Two

## Circuits in general

What is a circuit? BAsically it is a path that return to the beginning. If this is not the case, I'm gonna have a problem.
Cool term I found: "Knife Switches". Opening and closing a circuit with a cooper plate pushing into the socket.

![knife switch](https://external-content.duckduckgo.com/iu/?u=http%3A%2F%2Fimg1.etsystatic.com%2F000%2F0%2F5243317%2Fil_fullxfull.286022649.jpg&f=1&nofb=1)

Things a circuit needs:
- Insulation --> prevents unintended connections between parts of the circuit.
- Load --> where the energy is converted into work. It is also sometimes called the "sink".
- Source --> Provides the electromotive source.

## Series circuit

The parts of a simple circuit are all connected in series, but the series circuit has more components than the simple circuit, having multiple loads, and sometimes multiple sources.

Example: Torch.

It only has one path.  

Lets build one!

I wont work with an external power supply. Just my USB Port.
Facts about my USB Port: It will supply around 5 Voltage with a current of 500 mA.

But to light up 3 white LEDs I will need in total 9.9V because each of them will need 3.3V to do its job.
Well, thats a problem..

Apple example: I have 10 apples. A machine throws the amount of apples with 100 km/h. But if this machine has a pipe where the apples have to go throw, this of course is slowing the apples down, caused by friction. Maybe compareable? But I think the water example makes more sense as current is more compareable to something liquid.

Circuit Diagram:

![series Circuit sketch](https://github.com/TTropschuh/ElectronicsWithPhil/blob/master/sketch_series_circuit.PNG)

![series Circuit diagram](https://github.com/TTropschuh/ElectronicsWithPhil/blob/master/schaltplan_series_circuit.PNG)

![Series Circuit in real](https://raw.githubusercontent.com/TTropschuh/ElectronicsWithPhil/master/photo_2019-11-03_11-25-05.jpg)

## Parallel circuit

So it would be better to work with a parallel circuit. Here I need a less powerful supply than with the series curcuit. But! I have to take care of the resistance! An LED can only handle 3.3 Voltage. When I have a power supply of 5V I need to do a little math there.

(Power Supply Voltage-LED Voltage)/Current = Desired resistor value

(5V - 3.3V)/0,05= 5,4 Ohm

Just in case: I will use 10 Ohm Resistors for each of the LEDs.

![parallel Circuit sketch](https://github.com/TTropschuh/ElectronicsWithPhil/blob/master/sketch_parallel_circuit.PNG)

![parallel Circuit diagram](https://github.com/TTropschuh/ElectronicsWithPhil/blob/master/Schaltplan_parallel_circuit.PNG)


![parallel Circuit in real](https://raw.githubusercontent.com/TTropschuh/ElectronicsWithPhil/master/photo_2019-11-03_11-26-27.jpg)



## Switch built from a novel material

Novel material could be anything that is conductive. I chose a penny that light up an LED.

![penny example](https://github.com/TTropschuh/ElectronicsWithPhil/blob/master/penny_example.jpg)
![penny example](https://github.com/TTropschuh/ElectronicsWithPhil/blob/master/penny_sketch.jpg)
