![Header](/README/header.gif)

# About

**Jack doesn't waste** is a university project built in [p5.js](https://p5js.org/) during the course *Creative Coding* at the Politecnico di Milano. The goal was to develop an interactive app about an ***out of scale*** topic. 

# Project idea

The theme we choose is the **waste of water for domestic consumption**. The user has the chance to take an experience otherwise impossible through a guided path that allows him to find out how much water he uses. <br>
Jack drives the user in 3 different rooms of the house (bathroom, kitchen and laundry room). There the user has to answer questions about his weekly use of water. The experience ends showing him how much water was used and wasted in 1 week. The water waste is graphically represented using as unit a tub full of water.  

# Development

To code the app we mostly used Javascript (in [p5.js](https://p5js.org/)) and in support to it we also used HTML and CSS.

## Resources

### [p5.play.js](http://p5play.molleindustria.org/)

Initiated by Paolo Pedercini, this library provides a *Sprite* class to manage visual objects in 2D space, to create animations and to help mouse and keyboard interactions. p5.play.js is perfect for the creation of games and playthings.

We used this library to add animations to Jack and to the other objects, as well as to simulate a playful experience giving the chance to interact with the characters.

The following examples were written using this library:

* **Create animation**
```
Jack.addAnimation("moving", "images/Jack_walk1.png", "images/Jack_walk2.png");
```
![Jack_moving](/README/Jack_moving.gif)

* **Set velocity to animation**
```
if(mouseX > Jack.position.x + 10) {
    Jack.changeAnimation("moving");
    Jack.mirrorX(1);
    Jack.velocity.x = 5
}
 ```
![Jack_walking](/README/Jack_walking.gif)

* **Change animation**
```
Dish.addAnimation("Dish_none", "images/dish.png");

if (pressHands==true){
    Dish.changeAnimation("Sink");
} else if (pressDishwasher==true){
    Dish.changeAnimation("Dishwasher");
}
```
![GitHub Logo](/README/changeanimation.gif)

* **SetInterval and onMouseOver** <br><br>
The *glow effect* of the objects is visible after 3 seconds from the end of a previous action 
```
timeSinkGlow = setInterval(sinkGlow,timeGlow)
```
or going above the object with the mouse.
```
Sink.onMouseOver = function() {this.changeAnimation("SinkGlow");}
```
<br>
![glow_time](/README/glow_time.gif)![glow_mouse](/README/glow_mouse.gif)
<br>

### [p5.sound.js](https://p5js.org/reference/#/libraries/p5.sound)
We used this library to load and analyze the sound. <br><br>
We added this function
````
analyzer.setInput(mySound);
```
to analyze the sound and to play or pause it.<br><br>
The **music** is a Royalty Free Music from [Bensound](http://www.bensound.com/royalty-free-music/track/cute).

### [wavePercent](http://codepen.io/ElaineXu/pen/jAzGAw)
This is not a library, but an open source code from [CodePen](http://codepen.io/) created by [Elaine](http://codepen.io/ElaineXu/). We used and modified this animation to fill the screen of water before the results.

![wavepercent](/README/wavepercent.gif)![waves](/README/waves.gif)

## Data
asjdoha

## Challenges
To preserve a new style when the buttons are clicked we used Javascript to change CSS class.
```
.button {
    background: none;
    border: 2.5px solid;
    color: #677f8c;
}
.selected {	
    background-color: #677f8c;
    border: #677f8c 2.5px solid;
    color: white;
}


buttonTub.addClass("button");
buttonShower.addClass("button");

if(pressShower===true){
    document.getElementById("buttonShower").className = "selected"; 
    document.getElementById("buttonTub").className = "button";
} else if(pressTub===true){
    document.getElementById("buttonShower").className = "button";
    document.getElementById("buttonTub").className = "selected";
}
```
![className](/README/classname.gif)<br>
We used CSS to assign an image as a background of the buttons and to make them responsive.
```
@media screen and (max-width: 1024px)
.info {
    background-image: url(images/info_20.png);
}
.sound {
    background-image: url(images/audio_play_20.png);
}

@media screen and (min-width: 1024px)
.info {
    background-image: url(images/info_25.png);
}
.sound {
    background-image: url(images/audio_play_25.png);
}
```
![className](/README/responsive.gif)

# Team
**Jack doesn't waste** is developed by:
* Mara Cominardi [@phoenis](https://github.com/phoenis) 
* Chiara Riente [@chiarariente](https://github.com/chiarariente) 
* Sara Pizzatti [@sarapizzatti93](https://github.com/sarapizzatti93) 


And you, do you know how much water do you use? 
