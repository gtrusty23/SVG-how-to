# Scalable Vector Graphics (SVG) Tutorial
## Background
Scalable Vector Graphics (SVG) is a XML-based vector image format, usually meant for two-dimensional images.
All modern web browsers have support for SVG, so theres a good chance you've seen it being used on a website.

This tutorial is meant to be an easy introduction to SVG, as such, I won't be going over animation using SVG.

## Using SVG

### Requirements

Since SVG is used in HTML, you need to use a rich text editor in order to create SVG images.
For this tutorial I will be using Notepad++, though any text editor will work.

### The How-To

In order to create a SVG, you must create a line like so
```
<svg width="?" height="?">

</svg>
```
The question marks mean you can choose how big you want the image to be
<br>
We will be putting our image in between the two lines
<br>
We can use a variety of shapes in order to create our image.
<br>
<br>
For this tutorial we will be creating a basic smiley face using circles and rectangles.
#### Creating a Circle
In order to create a circle, you must create a seperate line in between the two lines we created earlier, this line will be indented.
<br>
A circle's code looks like this
```
<circle cx="?" cy="?" r="?" stroke="named-color" stroke-width="?" fill="named-color" />
```
The "cx" and "cy" are the position of the circle. The "r" is the radius of the circle.
<br>
Stroke is the line surrounding the circle, the stroke width is how big the stroke is.
<br>
The fill is the color of the circle itself.
<br>
The "named-color" will use the names of colors for the circle, so stuff like purple, orange, etc.
<br>
For our smiley face, we will be using yellow for both the stroke and the fill.

#### Creating a Rectangle
For our rectangles, we will create a new line for them like circles
<br>
A rectangle's code looks like this
```
<rect x="?" y="?" width="?" height="?" 
style="fill:rgb(0,0,0);stroke-width:?;stroke:rgb(0,0,0)" />
```
The "x" and "y" are the position of the rectangle.
<br>
The width and height are what they say they are. If you wish to create a square, make these two values the same.
<br>
<br>
The coloring method is different from the circle and can cause confusion, luckily, this is easy to understand.
<br>
The stroke-width, stroke, and fill return from the circle, but instead of using color names, they use RGB values.
<br>
RGB meaning Red, Green, and Blue. These values can range from 0 to 255, and result in different color combinations.
<br>
<br>
For our smiley face, we will be using these rectangles for eyes, so keep the values of RGB at 0 for black.
<br>
Change the stroke-width to however big you want your eyes to be, for me, I will input 3.

### Creating the Face
Now that we know how to create shapes, its time to create the face.
If you have text before your image, create a new line and type in this.
```
<br>
```
This creates a new line, and will prevent the image from occupying the same line as the text (unless you want that of course)
<br>
To start input the svg line we used earlier. You can make this as big or as small as you want, I will be using 300 to make the face a moderate size.
```
<svg width="300" height="300">
```
Press enter, and a new line with an indention will be created, this means we are in the svg code.
<br>
Next, create the main circle the face is on.
```
<svg width="300" height="300">
  <circle cx="100" cy="100" r="80" stroke="yellow" stroke-width="20" fill="yellow" />
```
I would recommend putting the cx and cy values to 100, since this puts it near the start of the line.
<br>
Next, create the left eye using a rectangle.
```
<svg width="300" height="300">
  <circle cx="100" cy="100" r="80" stroke="yellow" stroke-width="20" fill="yellow" />
  <rect x="70" y="50" width="10" height="60" 
  style="fill:rgb(0,0,0);stroke-width:3;stroke:rgb(0,0,0)" />
```
Next, create the right eye by using the same code as before, only increasing the x value so that it moves right.
```
<svg width="300" height="300">
  <circle cx="100" cy="100" r="80" stroke="yellow" stroke-width="20" fill="yellow" />
  <rect x="70" y="50" width="10" height="60" 
  style="fill:rgb(0,0,0);stroke-width:3;stroke:rgb(0,0,0)" />
  <rect x="120" y="50" width="10" height="60" 
  style="fill:rgb(0,0,0);stroke-width:3;stroke:rgb(0,0,0)" />
```
We will now create the smile. We will be using two circles and a rectangle to accomplish this.
```
<svg width="300" height="300">
  <circle cx="100" cy="100" r="80" stroke="yellow" stroke-width="20" fill="yellow" />
  <rect x="70" y="50" width="10" height="60" 
  style="fill:rgb(0,0,0);stroke-width:3;stroke:rgb(0,0,0)" />
  <rect x="120" y="50" width="10" height="60" 
  style="fill:rgb(0,0,0);stroke-width:3;stroke:rgb(0,0,0)" />
  <circle cx="100" cy="130" r="20" stroke="black" stroke-width="3" fill="black" />
  <rect x="70" y="109" width="70" height="15" 
  style="fill:rgb(255,255,0);stroke-width:3;stroke:rgb(255,255,0)" />
  <circle cx="100" cy="130" r="10" stroke="yellow" stroke-width="3" fill="yellow" />
```
Finally, end the svg code by creating a new line, removing the indention, and typing this 
```
</svg>
```
This end the code, and lets the image be created.
<br>
With this code it should create this image
