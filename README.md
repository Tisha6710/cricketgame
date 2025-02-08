# cricketgame
I have created a cricket game.
<!DOCTYPE html>
<html lang="en">
<head>
    <title>CRICKET</title>
    <style>
        body {
            text-align: center;
            background-color: grey;
        }
        button {
            margin: 5px;
            padding: 10px 20px;
            font-size: 16px;
            cursor: pointer;
            background-color: pink;
        }
    </style>
</head>
<body>
    <h1>Cricket Game</h1>
    
    <button onclick="
        let computerChoice = generatecomputerChoice();
        let resultmessage;
        if (computerChoice === 'ball') {
            score.win++;
            resultmessage = 'User won.';
        } else if (computerChoice === 'bat') {
            score.tie++;
            resultmessage = 'It is a tie.';
        } else if (computerChoice === 'stump') {
            score.lost++;
            resultmessage = 'Computer wins.';
        }
        alert(`You have chosen bat. Computer choice is ${computerChoice}.\n${resultmessage}\n\nScore: Wins = ${score.win}, Losses = ${score.lost}, Ties = ${score.tie}`);
        console.log(`Score: Wins = ${score.win}, Losses = ${score.lost}, Ties = ${score.tie}`);
    ">Bat</button>

    <button onclick="
        let computerChoice = generatecomputerChoice();
        let resultmessage;
        if (computerChoice === 'ball') {
            score.tie++;
            resultmessage = 'It is a tie.';
        } else if (computerChoice === 'bat') {
            score.lost++;
            resultmessage = 'Computer has won.';
        } else if (computerChoice === 'stump') {
            score.win++;
            resultmessage = 'User won.';
        }
        alert(`You have chosen ball. Computer choice is ${computerChoice}.\n${resultmessage}\n\nScore: Wins = ${score.win}, Losses = ${score.lost}, Ties = ${score.tie}`);
        console.log(`Score: Wins = ${score.win}, Losses = ${score.lost}, Ties = ${score.tie}`);
    ">Ball</button>

    <button onclick="
        let computerChoice = generatecomputerChoice();
        let resultmessage;
        if (computerChoice === 'ball') {
            score.lost++;
            resultmessage = 'Computer has won.';
        } else if (computerChoice === 'bat') {
            score.win++;
            resultmessage = 'User won.';
        } else if (computerChoice === 'stump') {
            score.tie++;
            resultmessage = 'It is a tie.';
        }
        alert(`You have chosen stump. Computer choice is ${computerChoice}.\n${resultmessage}\n\nScore: Wins = ${score.win}, Losses = ${score.lost}, Ties = ${score.tie}`);
        console.log(`Score: Wins = ${score.win}, Losses = ${score.lost}, Ties = ${score.tie}`);
    ">Stump</button>

    <script>
        let score = { win: 0, lost: 0, tie: 0 };

        function generatecomputerChoice() {
            let randomNumber = Math.random() * 3;
            if (randomNumber >= 0 && randomNumber < 1) {
                return 'bat';
            } else if (randomNumber >= 1 && randomNumber < 2) {
                return 'ball';
            } else {
                return 'stump';
            }
        }
    </script>
</body>
</html>

