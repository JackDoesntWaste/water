![GitHub Logo](/README/header.jpg)

# About :fish:

Title is a university project, developed during the course Creative Coding at the Politecnico di Milano.
The goal was to design an interactive app about an *Out of scale* topic. 


## Project idea

The theme is the **waste of water** in home environment. The user has the chance to take an experience otherwise impossible through a guided path that allows/helps him to find out how much water he wastes. 
Jack drives the user in 3 different rooms of the house (bathroom, kitchen and laundry room) where the user has to answer questions about his weekly use of water. The experience ends showing him how much water was used and wasted in 1 week on average.
The water waste is graphically represented using as unit a tub full of water.  

## Development

(e qui dire tutto sul codice, le librerie utilizzate in js, l'aggiunta di CSS e qualcosa in html (le onde) ecc ecc. ((magari aggiungere dei pezzi di codice e img come Jack che hai già inserito)) Dire anche come abbiamo calcolato effettivamente la quantità d'acqua.

### Difficulties
L’inserimento di codici esterni.
L’uso delle condizioni (?!)
l’unione di diversi codici
bottoni (tipo da disattivare)

### Resources
#### [p5](https://p5js.org/)
#### [p5.dom](https://p5js.org/reference/#/libraries/p5.dom)
#### [p5.sound](https://p5js.org/reference/#/libraries/p5.sound)
We used this library to load and analyze the sound. For example `analyzer.setInput(mySound);` allows us to play and stop the music in certain cases.

#### [p5.play](http://p5play.molleindustria.org/)
provides sprites, animations, input and collision functions for games and gamelike applications. Created by Paolo Pedercini. 

> We used this library to create animations for our project, to move and interact with Jack.

CREAZIONE ANIMAZIONE (JACK cammina)
```
Jack.addAnimation("moving", "images/Jack_walk1.png", "images/Jack_walk2.png");
```
![GitHub Logo](/README/Jack_moving.gif)

VELOCITA' (JACK CAMMINA e si muove)
```
if(mouseX > Jack.position.x + 10 && moving==true) {
    Jack.changeAnimation("moving");
    Jack.mirrorX(1);
    Jack.velocity.x = 5
}
 ```
![GitHub Logo](/README/Jack_walking.gif)

CHANGE ANIMATION (piatti)
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

GLOW
The glow è settato col tempo `timeGardenGlow = setInterval(gardenGlow,timeGlow);` e al passaggio del mouse `Garden.onMouseOver = function() {this.changeAnimation("GardenGlow");}`

#### [wavePercent](http://codepen.io/ElaineXu/pen/jAzGAw)
wavePercent created by [Elaine](http://codepen.io/ElaineXu/). We used and modified this animation, to fill the screen.

![wavePercent](/README/Circular-Water-Fill-Loading-Animation.gif)


Dire magari la fonte del file musicale?

## AUTHORS/TEAM
noi e i nostri contatti.


I think you should use an
`<addr>` element here instead.

Any word wrapped with two tildes (like ~~this~~) will appear crossed out.

As Kanye West said:

> We're living the future so
> the present is our past.
