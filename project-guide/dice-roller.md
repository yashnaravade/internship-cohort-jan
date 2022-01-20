# Dice Roller

In this tutorial, you will learn to build a dice roller with the help of Javascript.
The Dice Game is a two-player game. Both players roll the dice, and the game is won by the player with the highest phase value.

### Project Structure

The structure of this projects is going to be pretty simple. We'll first start off with the barebones of a HTML file. Then add CSS on top of it.
Then we will write some JavaScript to add funnctionality and make the Dice roller work.



### Assets
As dice has 6 faces, you will need 6 images, each for one face of the dice.
You can find and download the images here:
https://commons.wikimedia.org/wiki/Category:Dice_faces

### Steps by step guide to build project

### Live Demo Link

### Source Code

HTML Code:

<!DOCTYPE html>
<html lang="en">
  
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content=
        "width=device-width, initial-scale=1.0">
    <title>Dice Game</title>
</head>
  
<body>
    <div class="container">
        <h1>Let's Play</h1>
  
        <div class="dice">
            <p class="Player1">Player 1</p>
            <img class="img1" src="dice6.png">
        </div>
  
        <div class="dice">
            <p class="Player2">Player 2</p>
            <img class="img2" src="dice6.png">
        </div>
    </div>
  
    <div class="container bottom">
        <button type="button" class="butn"
            onClick="rollTheDice()">
            Roll the Dice
        </button>
    </div>
    <div class="container bottom">
        <button type="button" class="butn" 
            onClick="editNames()">
            Edit Names
        </button>
    </div>
</body>
  
</html>


### CSS code:

<style>
    .container {
        width: 70%;
        margin: auto;
        text-align: center;
    }
  
    .dice {
        text-align: center;
        display: inline-block;
        margin: 10px;
    }
  
    body {
        background-color: #042f4b;
        margin: 0;
    }
  
    h1 {
        margin: 30px;
        font-family: "Lobster", cursive;
        text-shadow: 5px 0 #232931;
        font-size: 4.5rem;
        color: #4ecca3;
        text-align: center;
    }
  
    p {
        font-size: 2rem;
        color: #4ecca3;
        font-family: "Indie Flower", cursive;
    }
  
    img {
        width: 100%;
    }
  
    .bottom {
        padding-top: 30px;
    }
  
    .butn {
        background: #4ecca3;
        font-family: "Indie Flower", cursive;
        border-radius: 7px;
        color: #ffff;
        font-size: 30px;
        padding: 16px 25px 16px 25px;
        text-decoration: none;
    }
  
    .butn:hover {
        background: #232931;
        text-decoration: none;
    }
</style>

### JavaScript Code:

<script>
  
    // Player name
    var player1 = "Player 1";
    var player2 = "Player 2";
  
    // Function to change the player name
    function editNames() {
        player1 = prompt("Change Player1 name");
        player2 = prompt("Change player2 name");
  
        document.querySelector("p.Player1").innerHTML = player1;
        document.querySelector("p.Player2").innerHTML = player2;
    }
  
    // Function to roll the dice
    function rollTheDice() {
        setTimeout(function () {
            var randomNumber1 = Math.floor(Math.random() * 6) + 1;
            var randomNumber2 = Math.floor(Math.random() * 6) + 1;
  
            document.querySelector(".img1").setAttribute("src",
                "dice" + randomNumber1 + ".png");
  
            document.querySelector(".img2").setAttribute("src",
                "dice" + randomNumber2 + ".png");
  
            if (randomNumber1 === randomNumber2) {
                document.querySelector("h1").innerHTML = "Draw!";
            }
  
            else if (randomNumber1 < randomNumber2) {
                document.querySelector("h1").innerHTML
                                = (player2 + " WINS!");
            }
  
            else {
                document.querySelector("h1").innerHTML
                                = (player1 + " WINS!");
            }
        }, 2500);
    }
</script>
  
  ### Complete Code: 
  After combining the above three sections (HTML, CSS, and JavaScript) code, we will get the complete Dice Game.


