Fractal Tree
============

How to draw a tree  

![alt text](tree.JPG)  

Imagine you were describing how to draw a tree. You might say: 

* Draw a vertical line  
* At the top of the line, draw two smaller lines ("branches") in a v shape  
* At the ends of each of those two branches, draw two even smaller branches  
* Keep repeating the process, drawing smaller and smaller branches until the branches are too small to draw  

This process of repeating the same design at a continually decreasing scale is an example of a Fractal. Using fractals to draw trees can give some interesting and beautiful patterns. In this assignment we will use a recursive branching function to create a fractal tree.

Suggested steps to completing this assignment:
----------------------------------------------
1. Fork and clone down this repository   

2. Run the program. It should draw a single green line on the screen. This will be the "trunk" of the Fractal Tree. Notice the three `private` variables. Changing the numbers in these `private` variables will change the appearance of the tree, i.e. how much smaller the branches are, how small the branches will get and the angle between the branches.
3. Now we'll write a function to draw the branches on the tree Here's some pseudocode describing the `drawBranches` function:  

	* declare two local `double` variables: `angle1` and `angle2`. These will hold the angles of the branches. Initialize one to `angle` plus `branchAngle` and the other to `angle` minus `branchAngle`. This will create the V shape of the branches.  
	* reduce `branchLength` by multiplying it by `fractionLength`. This will be the (shorter) length of the new branch.  
	* While the starting point of the new branches is just the endpoint of the previous branch or trunk, we'll have to use some trig to calculate the branches endpoints before we can draw them. Declare four local variables `endX1` `endY1` `endX2` `endY2`. We can calculate the endpoints with code like:

		`int endX1 = (int)(branchLength*Math.cos(angle1) + x);`  
		`int endY1 = (int)(branchLength*Math.sin(angle1) + y);`  
	* Now, draw two lines, both starting from (`x`,`y`) but ending at the two different end points you just calculated.  

4. Now go back to the `draw` function, and uncomment the call to `drawBranches`. You'll fill in the four arguments: `320` and `380` (the endpoint of the trunk is the starting point of the two branches) `100` (the length of the trunk) `3*Math.PI/2` (The angle of the trunk--a vertical angle in Java's system of radian measure). You should now see two branches in a V shape on the end of the trunk.
5. Now, the magic starts! We're going to use recursion to put branches on the branches! At the end of the `drawBranches` function write code so that if `branchLength` is larger than `smallestBranch`, `drawBranches` is called twice, once for each of the endpoints, e.g. (`endX1`,`endY1`). Be sure to use the two different angles for the two different branches. You should now see a fully formed Fractal Tree!



Adding Keyboard input
----------------------
The program becomes more interesting when you can adjust `branchAngle` `fractionLength` and `smallestBranch`. Add a `keyTyped()` function that allows the user to adjust those values and then call `redraw()` to draw the screen again.  

Extensions: You can have the width of the branches change with the length. You can also introduce a little bit of randomness for more realism. You could also add a third, middle branch to make a more realistic looking tree. There are also many other types of Fractal Trees. Browse the internet and see what ideas you can come up with, your fractal tree doesn't have to look like any other.

Samples of Student Work
-----------------------
[Winnie](http://winnie3269.github.io/FractalTree/)  
[Nicole](http://nicolethai.github.io/FractalTree/)  
[Jimmy](http://furiouspenguins.github.io/FractalTree/)  
[Elliot](http://elliottdebruin.github.io/FractalTree/)  
[Aliya](http://aliyachambless.github.io/FractalTree/)  
[Jeanette](http://roquefortt.github.io/FractalTree/)  
[Noah](http://noahzpepper.github.io/FractalTree/)  
[Edmond](http://edmondsitu.github.io/FractalTree/)  
[Andrew](http://andrewtheo.github.io/FractalTree/)  
[Alica](http://aliciazz.github.io/SierpinskiTriangle/)  
[Aidan](http://hakyojin.github.io/FractalTree/)  
[Dmitry](http://dkuliaev.github.io/FractalTree/)  
[Christopher](http://cjlim2007apcs.github.io/FractalTree/)  
[Lin](http://lin00.github.io/FractalTree/)  
[Theo](http://awesomestickman.github.io/FractalTree/)  
[Alexander](http://alzhu1.github.io/FractalTree/)  
[Rowan](http://rocassius.github.io/FractalTree/)   
[Sasha](http://sashagonzalez.github.io/FractalTree/)  
[Calvin](http://icalvin12.github.io/FractalTree/)  
[Gigi](http://gigibyte327.github.io/FractalTree/)  
[David](http://mostexcellent.github.io/FractalTree/)   
[Michel](http://limichel.github.io/FractalTree/)   
[Cora](http://coramonokandilos.github.io/FractalTree/)  
[Nathan](http://naguan.github.io/FractalTree/)  
[Ethan](http://emdarcher.github.io/FractalTree/)   
[Oliver](http://olivernoss.github.io/FractalTree/)  
[Erika](http://bekutaa.github.io/FractalTree/)  
[Celena](http://celenac.github.io/FractalTree/)  
[Chris](http://chrisma1.github.io/FractalTree/)  
[Camilia](http://cakacimi.github.io/FractalTree/)  
[Yufan](http://yuxu1.github.io/FractalTree/)   
[Thomas](http://tomikam.github.io/FractalTree/)   
[Philip](http://philiphuang2.github.io/FractalTree/)   
[Lily](http://magicallilicorn.github.io/FractalTree/)  
[Lee](http://shleewhite.github.io/FractalTree/)   
[Zachary](http://zachooz.github.io/FractalTree/)  
[Jingbin](http://ben441318936.github.io/FractalTree/)  
[Clarence](http://clarencechen.github.io/FractalTree/)   
[Kenta](http://redtorch.github.io/FractalTree/)  
[Lucy](http://luchen825.github.io/FractalTree/)  
[Christine](http://christinechao.github.io/FractalTree/)  
[David](http://goliathuros.github.io/FractalTree/)  
[Antonio](http://adcarmona.github.io/FractalTree/)  
[Teresa](http://teresamibarra.me/FractalTree/)  
[Aaron](http://aaronchowapcs.github.io/FractalTree/)  
[Rain](http://pioggia.github.io/FractalTree/)  
[Kirby](http://kichoy.github.io/FractalTree/)   
