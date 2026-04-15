<!DOCTYPE html>
<html>
<head>
    <title>Game Zone</title>
    <style>
        body {
            font-family: Arial;
            text-align: center;
            background: #111;
            color: white;
        }
        h1 {
            margin-top: 20px;
        }
        button {
            padding: 15px;
            margin: 10px;
            font-size: 16px;
            background: #00b4d8;
            border: none;
            color: white;
            cursor: pointer;
        }
        #gameArea {
            margin-top: 20px;
        }
    </style>
</head>

<body>

<h1>🎮 Game Zone</h1>

<button onclick="guessGame()">Guess Number</button>
<button onclick="rpsGame()">Rock Paper Scissors</button>

<div id="gameArea"></div>

<script>
function guessGame() {
    let num = Math.floor(Math.random() * 10) + 1;
    let guess = prompt("Guess a number (1-10):");

    if (guess == num) {
        alert("Correct! 🎉");
    } else {
        alert("Wrong! Number was " + num);
    }
}

function rpsGame() {
    let choices = ["rock", "paper", "scissors"];
    let computer = choices[Math.floor(Math.random() * 3)];
    let user = prompt("Enter rock, paper or scissors:");

    if (user === computer) {
        alert("Draw!");
    } else if (
        (user === "rock" && computer === "scissors") ||
        (user === "paper" && computer === "rock") ||
        (user === "scissors" && computer === "paper")
    ) {
        alert("You Win! 🎉");
    } else {
        alert("You Lose! Computer chose " + computer);
    }
}
</script>

</body>
</html>
