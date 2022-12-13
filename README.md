# Evolution-Sim

This is a simulation of organisms that demonstrates evolution and natural selection

<h2>The World</h2>

The world text based display that shows up in the console that looks like this:

![Screen Shot 2022-12-13 at 11 00 28 AM](https://user-images.githubusercontent.com/58442585/207421609-d1640d6c-815e-4162-b8a5-aa7f15e8dbbf.png)


Each letter represents a unique Organism, and each hashtag (#) represents a singular food.
Indices for columns are formatted strangely due to spacing constraints, so just read them vertically.

Time is seperated into 'days' and 'ticks', each day consists of a number of ticks in which Organisms can move around.


<h2>Organisms</h2>
  
The creatures in the simulation are simply called Organisms.
  
Each Organism has the following properties:
    
  - <ins>Vision [V]</ins>: This is how many tiles away they can see (including diagonally). Having higher vision means they can see food farther away from themself.
  - <ins>Reproduction [R]</ins>: This is their odds of reproducing at the end of each day.
  - <ins>Food [F]</ins>: This is how much food it has collected that specific day.
  - <ins>Age [A]</ins>: This is how many days it has been alive for.
  
In addition, these properties effect how much food they need.

Each 'vision' that an Organism has increases the amount of food it needs to stay alive at the end of the day (Food required to survive = vision + 1)
Each 'reproduction' increases the amount of food required to have a chance to reproduce (Food required to reproduce = reproduction + vision + 1)

So for example an Organism with:
  Vision = 3
  Reproduction = 2
  
  Would need 4 (vision + 1) food to stay alive, and 6 (reproduction + vision + 1) to have a chance to reproduce.
  
At a high level, vision allows you to find more food but also increases the amount of food needed, while reproduction increases your odds of reproducing, but also increases requirements to even have a chance.

When an Organism reproduces, there is a small chance that it mutates one of its properties (vision/reproduction), this is what leads to evolution and natural selection.

<h2>Running the Simulation</h2>
When you run the program, the first thing you will be asked is if you want to use custom parameters.
This option is whether or not you want it to use the default paramaters or to define your own (default values are still shown in parenthesis).

If you choose yes, you will be asked the following:
  - <ins>World Size</ins>: The dimensions of the world
  - <ins>Starting Organisms</ins>: The starting number of Organisms
  - <ins>Amount of Food</ins>: The amount of food that will be generated each day
  - <ins>Number of Ticks Per Day</ins>: How long each day lasts (the number of moves each Organism gets in a day)
  - <ins>Number of Days to Simulate</ins>: This is the total length of the simulation


At the start of each day, you will be asked if you want to 'quick run' any days. This option allows you to simulate many days quickly without manually going through each one. The 'display ticks' suboption will toggle whether or not each individual tick of each day or just the final state is displayed when running them.

If you chose not to quick run days, then you will have to press 'ENTER' to manually progress through each tick in the day, allowing you to see the Organisms move around

After each tick, the information of each Organism will be displayed, relating to the letter displayed on the board.

At the end of each day, it will show what Organisms have died or reproduced, as well as the properties of the new Organisms.  
<br>
<br>
Made by Josh Farkas in Advanced Programming Topics, 2022
