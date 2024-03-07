---
created: 2023-12-31
status: 🔴
tags:
  - input
  - siat
links: "[[My Inputs]]"
professor: Eric
semester: Fall 2021
---
## Summary
### Context
- 
### Main Takeaways
- 
### Questions/Connections/Thoughts
- 
## Notes


DRAWING PRIMITIVES in Panel class using Graphics

drawLine(x1, x2, y1, y2)

drawRect(x, y, w, h)

drawOval(x, y, w, h)

drawArc(x, y, w, h, start angle, arc angle)

drawPolygon(xArray, yArray, number of points)

  

TRANSFORMATION

translate(double x, double y)

rotate(double angle)

scale(double x, double y)

  

AffineTransform af = g.getTransform();

setTransform(af);

  

ENCAPSULATION

  
  
  

MOUSE INTERACTION, ARRAYS, ARRAYLIST, GEOMETRIC SHAPES

  

MOUSE INTERACTION

  

MOUSE EVENT

MouseEvent = object with location, modifier key, click count info

e.getX() / e.getY() = gets coordinates of mouse

e.getClickCount() = gets number of clicks

e.isShiftDown() / e.isControlDown() / e.isAltDown() = booleans for specific keys

  

MOUSE LISTENER

MouseListener(MouseEvent e)

MousePressed(MouseEvent e)

MouseClicked(MouseEvent e)

MouseReleased(MouseEvent e)

= you must extend all methods

MouseMotionListener(MouseEvent e)

MouseDragged(MouseEvent e)

MouseMoved(MouseEvent e)

-JPanel class implements MouseListener

-this.addMouseListener(this) in constructor

-define all methods in JPanel class body

  

MOUSE ADAPTER

MouseAdapter(MouseEvent e) 

MouseMotionAdapter(MouseEvent e)

MouseInputAdapter(MouseEvent e) //both motion and events

-define custom MyMouseListener class that extends MouseAdapter within JPanel class

-in JPanel constructor:

MyMouseListener myMo = new MyMouseAdapter()

addMouseListener(myMo);

addMouseListener(MyMouseAdapter())

  

ARRAY = contiguous collection of same type data

-arrayName.length = gives length of array

-cannot remove/add indices

-can only hold one data type

  

PRIMITIVES  = array is object, holds primitives

int [] nums = new int[5]{1, 2, 3};

double [] nums = new double[5];

float [] nums = new float[5];

String [] nums = new String[5];

  

OBJECTS = array is object containing references to other objects (starts as null)

Dog [] dogs = new Dog[5];

  

ARRAYLIST = dynamically resizable type agnostic collection of data

.add(Object o) / .get(i) / .remove(Object o) / .size() / .clone() only references are copied

-can pass in any class, if want to use methods must typecast

ArrayList<LadyBug> bugs = new ArrayList<LadyBug>();

  

DESTROY OBJECT

.remove(bug);

bug = null; (trash collector will pick it up)

  

PROCESSING

ITERATIVE LOOP = use if not removing

for (int p: primes) p.doSomething()

  

GRAPHICS2D = have an initializeShapes( ) and draw(Graphics2D g) function

draw(shape)

fill(shape)

  

PRIMITIVES (double or float precision)

Ellipse2D.Double setFrame(x, y, w, h)

Line2D.Double setLine(x1, y1, x2, y2)

Rectangle2D.Double setFrame(x, y, w, h)

Arc2D.Double setArc(x, y, w, h, start angle, angle extent, closure type)

Arc2D.OPEN (vertical cut)

Arc2D.CHORD (pacman)

Arc2D.PIE (pie slice)

QuadCurve2D.Double setCurve(x1, y1, ctrlx, ctrly, x2, y2)

CubicCurve2D.Double setCurve(x1, y1, ctrlx, ctrly, ctrlx2, ctrly2, x2, y2)

  

USING SHAPES

1. declare variables private Ellipse2D.Double orb;
    
2. initialize orb = new Ellipse2D.Double();
    
3. set orb.setFrame(x, y, w, h)
    
4. use g.draw(orb)
    

  

ADVANCED COLLISION DETECTION, LINEAR SEARCH ALGORITHM

  

COLLISION DETECTION

  

SHAPE interface checks collision

contains(Rectangle2D r)

contains(double x, double y)

intersects(Rectangle2D r)

Rectangle2D getBounds2D()

  

AREA class implements Shape gets figure outline

  

GETTING OUTLINE

static outline created in initializeShapes() function

Area outline  = new Area();

outline.add(new Area(shapes of figure));

outline.getBounds2D() = returns figure’s bounding box

  

TRANSFORMING OUTLINE

Shape getOutline() method used to get dynamic bounding box

AffineTransform af = new AffineTransform();

af.translate(same as figure)

af.rotate(same as figure)

af.scale(same as figure)

Shape createTransformedShape(outline)

//making outline dynamically transformed with figure (returns Path2D.Double)

  

GET BOUNDING BOX

called in collision detection function

transformedOutline.getBounds2D()

  

CHECK COLLISION

if (a.intersects(b.getBounds2D()) && b.intersects(a.getBounds2D()) {collision}

//if a outline intersects b bounding box and b outline intersects a bounding box

  

YOU CAN ALSO USE THIS FOR WALL COLLISION DETECTION. JUST MAKE RECTANGLES ALONG PANEL EDGES.

  

RESOLUTION

void resolveCollision(Bug otherBug) { 

float angle = (float) Math.atan2(pos.y-otherBug.pos.y, pos.xotherBug.pos.x); 

  

//if current bug smaller, turn it away by the angle 

if(scale < otherBug.scale) 

{ vel = PVector.fromAngle(angle); vel.mult(maxSpeed); } 

else { 

//Otherwise send the otherBug away in the opposite direction: 

angle+PI otherBug.vel = PVector.fromAngle(angle+(float)Math.PI); otherBug.vel.mult(maxSpeed); } }

  

LINEAR SEARCH

-start at first index, keep looking until find desired, when found overwrite the variable and check again

  

//smallest int in an array

int linearSearch(int[] array){

int smallest = array[0];

for (int i = 1; i < array.length; i ++){

if (array[i] < smallest){

smallest = array[i];

}

return smallest }}

  

//closest object

int linearSearch(ArrayList<Seeds> seeds){

Seed closest = seeds.get(0);

float closestDist = PVector.dist(this.getPos(), closest.getPos());

for (Seed s: seeds){

if (PVector.dist(this.getPos(), s.getPos()) < closestDist){

closest = s;

closestDist = PVector.dist(this.getPos(), closest.getPos());

}

return closest }}

  

CODE REFACTORING, COLLISIONS AMONG COLLECTIONS OF OBJECTS, COLLISION AVOIDANCE

  

CODE REFACTORING

  

COLLISION METHOD 

defined by ACTIVE object

ROT#1: called by ACTIVE when runs against inactive (boundary detection)

ROT#2: called by CONTROLLER when two different types both change state

1. update all active and passive
    
2. iterate over active list
    

iterate over passive list

if (active.collides(passive){

active.respond(passive);

passive.respond(active); //may not be necessary

COLLISIONS AMONG COLLECTIONS OF OBJECTS

WITHIN SAME COLLECTION = nested loop, must rule out checking against self (i = i + 1)

WITHIN DIFFERENT COLLECTION = nested loop, start both at 0

  

COLLISION AVOIDANCE

FORCE MODEL cause changes in acceleration, which affects velocity

Force = coef / (distance from edge)^2

coef = value provided based on rot

distance from edge = calculated using Line2D method ptLineDist(double px,

double py) where px, py is center of object

power of two = Math.pow(n, p)

  

1. Represent walls with Line2D objects
    
2. In object class make method to calculate PVector of wall force to push away creature
    

PVector wallPush(){

PVector force = new PVector();

float coef = 50.0f;

double dist = 0;

dist = Panel.rightEdge.ptLineDist(pos.x, pos.y) - dim.x /2 * scale; //right edge

force.add(new PVector((float)(-coef / Math.pow(dist, 2)), 0.0f));

  

dist = Panel.leftEdge.ptLineDist(pos.x, pos.y) - dim.x /2 * scale; //left edge

force.add(new PVector((float)(+coef / Math.pow(dist, 2)), 0.0f));

  

dist = Panel.topEdge.ptLineDist(pos.x, pos.y) - dim.h /2 * scale; //top edge

force.add(new PVector(0.0f, (float)(+coef / Math.pow(dist, 2))));

  

dist = Panel.bottomEdge.ptLineDist(pos.x, pos.y) - dim.h /2 * scale; //bottom edge

force.add(new PVector(0.0f, (float)(-coef / Math.pow(dist, 2))));

  

return force;}

  

3. In object moveTo(Food f) method call wallPush() method to return wall acc force
    

PVector wallForceAcc = wallPush().div(float)scale);      //a = force / mass, mass = scale

float velValue = vel.mag();

vel.add(wallForceAcc); //make it turn per wall steer acc

vel.normalize().mult(velValue); maintain same magnitude

pos.add(vel);

  

OBSTACLE DETECTION

FIELD OF VIEW

  

FEELER

1. create obstacle outline
    
2. create feeler as PVector in direction of velocity, length proportional to velocity magnitude
    

private void updateFeeler(){

float size = dim.x/2 + speedLimit*FEELER_RANGE;

feelerVector = vel.copy().normalize().mult(size); //copy of vel preserves original

feeler.setLine(0.0, 0.0, feelerVector.mag(), 0);}

3. obstacle class generates steering force
    

public PVector pushAwayForce(PVector feelerEndPoint){

PVector forceVector = null;

if (outline.contains(feelerEndPoint.x, feelerEndPoint.y)){

forceVector = PVector.sub(feelerEndPoint, pos).normalize().mult(0.4f);}

//returns force direction from object center towards feelerEndPoint, set

amount as per ROT

else { forceVector = new PVector(0,0);

return forceVector;}

4. create method for feeler to probe obstacle in fish class
    

private PVector obstaclePushForce(Obstacle o){

PVector feelerEnd = PVector.add(location, feelerVector);

PVector obstacleForce = ob.pushAwayForce(feelerEnd);

return obstacleForce;}

5. in object moveTo(Food f) call obstaclePushForce()
    

PVector obstacleSteerAcc = obstaclePushForce(Panel.o).div((float)scale);

float velValue = vel.mag();

pos.add(wallSteerAcc);

pos.add(obtacleSteerAcc);

speed.normalize().mult(velValue);

updateFeeler();

pos.add(vel);

  

INHERITANCE AND POLYMORPHISM

  

INHERITANCE “IS A” relationships

inherit from only one parent

PUBLIC accessible everywhere

PROTECTED accessible to package and subclass

PRIVATE copied but inaccessible in child

SUPER = refers to superclass object

THIS = refers to class object

  

POLYMORPHISM creating more than one form of field/variable

OVERRIDING

subclass redefines parent methods with same signature

(overloading is redefining a method with different signature)

INCLUSION

variable of superclass can reference subclass object (mixed arrays)

can only use methods defined by parent with superclass variable (use instanceof

and typecast into subclass variable if necessary)

  

FSM, KEY INTERACTION, TEXT WITH FONT

  

FINITE STATE MACHINE (FSM) major tool for AI in games

only one state active at a time, contains:

1. STATES use public static final for state names
    
2. TRANSITION CONDITIONS
    
3. TRANSITION FUNCTIONS
    

KEYBOARD INTERACTIONS

  

KeyEvent indicated that keystroke occurred in component

KEY_PRESSED

KEY_RELEASED

getKeyCode() VK_key represents ASCII code for characters

Modifiers = VK_UP, VK_DOWN, VK_SHIFT...

KEY_TYPED (for non-english unicode)

getKeyChar()

  

KeyListener interface implemented in JPanel using addKeyListener(KeyListener k)

keyPressed(KeyEvent e)

keyReleased(KeyEvent e)

keyTyped(KeyEvent e)

  

KeyAdapter make custom inner class extending KeyAdapter, set it as keyListener

this.addKeyListener(mkl);

setFocusable(true) //this makes it focus on your window

  

FONT CLASS public Font(String name, int style, int size)

style = PLAIN, BOLD, ITALIC or combination with |

ACTIVATE 

Font font = new Font(“Arial”, Font.BOLD, 40);

g.setFont(Font f)

DRAW

g.drawString(String str, int x, int y) where x, y is start of baseline

  

CHANGE STYLE make new font object with argument specified

deriveFont(int Style)

deriveFont(float size)

deriveFont(int Style, float size)

  

FontMetrics

g.getFontMetrics(font) returns a FontMetrics object

stringWidth(str) returns width of String (for centering text)

  

ANONYMOUS INNER CLASS for classes you use only once

private JPanel panel = new Panel(){}

define and instantiate class at same time 

either extends superclass or implements interface

  
  
  
  
  
  
  
  
  
  
  
  

Ellipse2D.Double = orb;

Area outline;

  

initializeShapes(){

orb = new Ellipse2D.Double();

  

orb.setFrame(-25, -25, -50, -50);

  

outline = new Area(orb);

outline.add(new Area(others));

  
  

getOutline(){

AffineTransform af = new AffineTransform().

af.translate(same)

af.rotate(same)

af.scale(same)

af.createTransformedShape(outline)

}

  

checkCollision(other o){

if (getOutline().intersects(b.getOutline().getBounds2D()) &&

b.getOutline().intersects(getOutline().getBounds2D()){

hit = true;)

  

Object smallest = array[i];

for (int i = 0; i < array.length; i ++){

if (array[i] < smallest){

smallest = array[i];

  
  

draw(){

AffineTranform af = g.getTransform();

g.draw(orb)

g.setColor(Color.RED);

g.fill(orb)

  

g.setTransform(af);

}

  

PULL UP OPERATION

When classes have redundant/same methods and fields, pull up into superclass

  

INTERFACE

Declares methods without implementation

No constructor

Must implement all methods declared by interface when implementing

Class can implement multiple interfaces

Allows for grouping of dissimilar objects with common behaviour

Can only hold constants

Cannot be instantiated, can be used as type for processing mixed ArrayList (can only call interface defined methods

ABSTRACT CLASS

Some (or all) methods not defined in parent class (eliminates dummy implementation)

Must be implemented in subclass or subclass is abstract also

Italicized in UML diagrams

For grouping similar objects with some fields/methods same

Can hold fields

Can have no abstract methods

Cannot instantiate it

PACKAGES

Manage class/interface organization

Naming: all lowercase, delimited by periods

Public package members accessible within same package, import class to use other package members (or static import)

  

EXCEPTION HANDLING

TYPES OF ERRORS:

1. COMPILER typos, compiler finds them
    
2. SEMANTIC works but does the wrong thing
    
3. RUNTIME runtime environment catches, but can cause crash
    

EXCEPTIONS:

NULLPOINTER uninitialized variable

INDEXOUTOFBOUNDS bad loop logic

IO file reading/accessing error

HANDLING:

TRY CATCH BLOCK:

Tries some code, catches the error and provides a custom error response (informative about what went wrong)

  

IMAGES IN JAVA

  

1. LOAD DATA
    

use BufferedImage that extends Image class

ImageIO.read(File input), throws exception if error, so use try catch block

  

2. DISPLAY IMAGE
    

render using Graphics drawImage() method

boolean drawImage(image i, x, y, imageObserver) leave last one null

boolean drawImage(image i, x, y, w, h,  imageObserver)

img.getWidth() / img.getHeight()

Image getRGB(intx, int y) and setRGB(int x, int y, int RGB)

  

SOUND IN JAVA

Use minim (can work with all types, can loop)

Create MinimHelper class to pass to Minim

  

CUSTOM SHAPES: POLYGONS

GENERALPATH class to make own shapes from lines

void moveTo(dx, dy)

void lineTo(dx, dy)

void closePath()

Put points into arrays to iterate through (set curr pt to 0, loop through all, close path)

  

RANDOM CLASS  
make new random object, use to generate random int, boolean, double etc…

random.nextInt(n) generates int between 0 and n-1

  

GENERATIVE ART

algorithmically determined computer generated artwork

deconstructing/reconstructing shapes with randomness or using noise

PERLIN NOISE

randomness generator good at simulating organic/random behaviours and textures

smoother than straight up randomness

Processing has noise() function we can use where float is seed passed in

float noise(float x) (mountain from side)

float noise(float x, float y) (mountains from top)

float noise(float x, float y, float z)

result always between 0.0 and 1.0, scale to make meaningful

  

RECURSION

Method calls itself until base case (otherwise infinite recursion)

FRACTAL SHAPES: self similar shapes (each part looks like whole)

  

DESIGN PATTERNS

Prescribed solutions to common problems in coding

  

1. FACTORY PATTERN (CREATIONAL)
    

Use one class to make all other class objects 

Don’t expose class signature to client

Make variations with create method that takes string (type) input

Problems of Direct Instantiation:

Must know signature, clunky, new keyword, if signature changes all code breaks

Solution:

ABSTRACT FACTORY CLASS declares create methods  
CONCRETE FACTORY CLASS (extends abstract) defines create methods

Changing signature in concrete doesn’t change it in abstract (code doesn’t break)

Instantiate one concrete object factory to make all other objects from.

  

2. DECORATOR PATTERN (EXTENSIONAL/STRUCTURAL)
    

Attach/wrap an object with a decorator to add functionality/elements at runtime

Create Decorator interface and Decorator class for each iteration, make instance of base decorator instance, pass in the (interface type) base to each new decorator to add functionality.

Only need to call draw once because it’s all the same object, just with added functionality on top

  
  

  
  
