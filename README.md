# bbxsb
 <!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Beyblade X Scoreboard</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="container">
        <h1>Beyblade X Scoreboard</h1>
        <div class="teams">
            <div class="team">
                <h2>Player 1</h2>
                <button onclick="increaseScore('player1')">Score +1</button>
                <p id="player1-score">0</p>
            </div>
            <div class="team">
                <h2>Player 2</h2>
                <button onclick="increaseScore('player2')">Score +1</button>
                <p id="player2-score">0</p>
            </div>
        </div>
        <button onclick="resetScores()">Reset Scores</button>
    </div>
    <script src="script.js"></script>
</body>
</html>
body {
    font-family: Arial, sans-serif;
    background-color: #f0f0f0;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    margin: 0;
}

.container {
    text-align: center;
    background-color: white;
    padding: 20px;
    border-radius: 10px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}

h1 {
    color: #333;
}

.teams {
    display: flex;
    justify-content: space-around;
    margin-top: 20px;
}

.team {
    background-color: #eee;
    padding: 20px;
    border-radius: 5px;
    width: 150px;
}

button {
    padding: 10px;
    background-color: #4CAF50;
    color: white;
    border: none;
    border-radius: 5px;
    cursor: pointer;
}

button:hover {
    background-color: #45a049;
}

button:focus {
    outline: none;
}

p {
    font-size: 24px;
    font-weight: bold;
}
let player1Score = 0;
let player2Score = 0;

function increaseScore(player) {
    if (player === 'player1') {
        player1Score++;
        document.getElementById('player1-score').innerText = player1Score;
    } else if (player === 'player2') {
        player2Score++;
        document.getElementById('player2-score').innerText = player2Score;
    }
}

function resetScores() {
    player1Score = 0;
    player2Score = 0;
    document.getElementById('player1-score').innerText = player1Score;
    document.getElementById('player2-score').innerText = player2Score;
}
