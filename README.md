# LaundryMachine-
Design of a Laundry Machine on LabVIEW with three different washing programs: 

The Laundry Machine Programs:
  1.Fast wash:
      Initialization, Rinsing, Washing, Rinsing
  2.Thorough Wash:
      Initialization, Rinsing, Washing, Rinsing, Squeezing, Drying
  3.Custom Wash:
      Allows the user the chose the order, steps and time allocated for each to end.
      
The machine components are:
1-Water tank sensor
2- Water pump
3- Soap sensor
4- Agitator (10 rpm, 20 rpm, 50 rpm)
5- Door lock (Boolean)
6- Weight sensor
7- Air temperature
8- Air compressor
9- Internal water sensor
10-Program knob selector
11-Timer
12-Thermometer
13-Weight sensor
14-Resistor for air
15-Resistor for water

Initialization:
· Locks door
· Checks for clothes weight
o If the value was zero, pop-up a message indicating so
o Stop the code
· Checks the water tank for water availability (10 L)
o In case there was no water a pop-up message will appear
o The program keeps checking for water
o When the water tank is filled the program continues
· Checks water temperature
· Set water temperature
o When setting the temperature the resistor is able to increase it by 2oC/min
· Checks soap availability (1 Kg)
o In case there was no soap a pop-up message will appear
o The program keeps checking for soap
o When the soap tank is filled the program continues

Rinsing:
· Pop-up a message indicating “Rinsing Stage”
· Water is added to the clothes at the rate of 25 L/h
· The agitator is activated at 10 rpm
· The whole process takes 1 min
· Pop-up a message indicating : ”Rinsing Stage Done”

Washing:
· Pop-up a message indicating “Washing Stage”
· Water is added to the clothes at the rate of 25 L/h
· Soap is added simultaneously at a rate of 500 g/h
· After 30 seconds of water and soap filling
· The agitator is activated at 20 rpm
· The whole process takes 1.5 min
· Pop-up a message indicating : ”Washing Stage Done”

Squeezing:
· Pop-up a message indicating “Squeezing Stage”
· The agitator will run for 2 min at 50 rpm
· The drain will get rid of the filthy water at a rate of 20 L/ h
· Pop-up a message indicating : ”Squeezing Stage Done”

Drying:
· Pop-up a message indicating “Drying Stage”
· Turn on the resistor
· After 20 seconds, turn on the air compressor
· After 15 seconds, turn on the agitator at 50 rpm
· The whole process takes 2 min
· The resistor keeps increasing the thermometer temperature by 5oC/ s, the air temperature should b adjusted
at 45oC, thus you should create a feedback that will allow you to turn the resistor on and off to keep the air
temperature stable (thermostat)
· Pop-up a message indicating : ”Drying Stage Done”
