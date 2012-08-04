HitTesting jquery plugin
========================

This plugin allow to test dom objects collision and coordinates hitTest. The collision detection works on mobile and on desktop. It manage image and canvas transparency on rencent web browsers.

The transparency is manage on canvas elements compatible web browsers. (on old web browsers, the tests are done on rectangular areas)

For live examples and more explanations visit : [http://e-smartdev.com/#!jsPluginList/hittestJQuery](http://e-smartdev.com/#!jsPluginList/hittestJQuery)

hitTestPoint(options):Boolean
-----------------------------

This function find if one dom JQuery object is under given coordinates.

Sample code:

**$('#domElementIdToTest').hitTestPoint({"x":positionX,"y":positionY, "transparency":true});**

If the point ({x:positionX, y:positionY}) hitTest with id="domElementIdToTest" object then the function return "true", otherwise "false". (in this example pixel transparency is manage)

objectHitTest(options):Boolean
------------------------------

This function find if one JQuery dom object hitTest with another one.

Sample code:

**$('#domElementIdToTest').objectHitTest({"object":$("$domElementToHitTestWith"), "transparency":true});**

If the id="domElementToHitTestWith" object hitTest with id="domElementIdToTest" object, then the function return "true", otherwise "false". (in this example pixel transparency is manage)

Rectangle class
---------------

This class allow to create a graphical rectangle. The instance properties of the rectangle are: x, y, width, height.

The functions of this class allow to manage several graphical tests on rectangle shapes.

Sample code:

**var rectangle = new Rectangle(0, 0, 100, 100);**

You could access the renctangle properties like this: console.log("x : "+rectangle.x+", y : "+rectangle.y+", width : "+rectangle.width+", height : "+rectangle.height).

functions: 

**rectContainsPoint(pointX, pointY):Boolean** - Determines whether the rectangle contains the given point

**intersects(rect):Boolean** - Determines whether the rectangle intersect with the given rectangle

**intersection(rect):Rectangle** - Determines the intersection between the two rectangles

getRect():Rectangle
-------------------
This function return a rectangle containing the JQuery object coordinates.

Sample code:

**var rectangle = $('#domElementId').getRect();**

This function call create a rectangle containing the (id="domElementId") JQuery object globals coordinates. 
