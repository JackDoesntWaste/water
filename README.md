![GitHub Logo](/README/header.png)

# About

Title is a university project built in [p5.js](https://p5js.org/) during the course *Creative Coding* at the Politecnico di Milano. <br>
The goal was to develop an interactive app about an ***out of scale*** topic. 

# Project idea

The theme is the **waste of water** in home environment. The user has the chance to take an experience otherwise impossible through a guided path that allows/helps him to find out how much water he wastes. <br>
Jack drives the user in 3 different rooms of the house (bathroom, kitchen and laundry room) where the user has to answer questions about his weekly use of water. The experience ends showing him how much water was used and wasted in 1 week on average. <br>
The water waste is graphically represented using as unit a tub full of water.  

# Development

(e qui dire tutto sul codice, le librerie utilizzate in js, l'aggiunta di CSS e qualcosa in html (le onde) ecc ecc. ((magari aggiungere dei pezzi di codice e img come Jack che hai già inserito)) Dire anche come abbiamo calcolato effettivamente la quantità d'acqua.

## Data
asjdoha

## Challenges
Bottoni (responsive, changeClasse) -> css, js

## Resources
### [p5.js](https://p5js.org/)
### [p5.dom.js](https://p5js.org/reference/#/libraries/p5.dom)
### [p5.sound.js](https://p5js.org/reference/#/libraries/p5.sound)
We used this library to load and analyze the sound. For example `analyzer.setInput(mySound);` allows us to play and stop the music in certain cases.

### [p5.play.js](http://p5play.molleindustria.org/)
provides sprites, animations, input and collision functions for games and gamelike applications. Created by Paolo Pedercini. 

We used this library to create animations for our project, to move and interact with Jack.

#### Create animation
```
Jack.addAnimation("moving", "images/Jack_walk1.png", "images/Jack_walk2.png");
```
![Jack_moving](/README/Jack_moving.gif)

#### Set velocity to animation
```
if(mouseX > Jack.position.x + 10 && moving==true) {
    Jack.changeAnimation("moving");
    Jack.mirrorX(1);
    Jack.velocity.x = 5
}
 ```
![Jack_walking](/README/Jack_walking.gif)

#### Change animation
```
    if (pressDone3==true) {
            Dish.changeAnimation("Dish_none");
            moving=true;  //<<AGGIUNGI
        } else if (pressHands==true){
            Dish.changeAnimation("Sink");
        } else if (pressDishwasher==true){
            Dish.changeAnimation("Dishwasher");
        }
```
![GitHub Logo](/README/changeanimation.gif)

#### SetInterval and onMouseOver<br>
The glow è settato col tempo `timeSinkGlow = setInterval(sinkGlow,timeGlow)` e al passaggio del mouse `Sink.onMouseOver = function() {this.changeAnimation("SinkGlow");}`<br><br>
![glow_mouse](/README/glow_mouse.gif)![glow_time](/README/glow_time.gif)

### [wavePercent](http://codepen.io/ElaineXu/pen/jAzGAw)
created by [Elaine](http://codepen.io/ElaineXu/). We used and modified this animation, to fill the screen.

![wavepercent](/README/wavepercent.gif)![waves](/README/waves.gif)


Dire magari la fonte del file musicale? 

# AUTHORS/TEAM
...is developed by:
* Mara Cominardi [@phoenis](https://github.com/phoenis) 
* Chiara Riente [@chiarariente](https://github.com/chiarariente) 
* Sara Pizzatti [@sarapizzatti93](https://github.com/sarapizzatti93) 
