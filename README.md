<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Charades Generator</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            margin: 0;
            padding: 0;
            background-color: #f4f4f4;
        }
        .container {
            padding: 50px;
        }
        button {
            padding: 15px 25px;
            font-size: 18px;
            cursor: pointer;
            background-color: #4CAF50;
            color: white;
            border: none;
            border-radius: 5px;
            margin-top: 20px;
        }
        button:hover {
            background-color: #45a049;
        }
        .prompt {
            font-size: 24px;
            margin-top: 30px;
            padding: 20px;
            background-color: #fff;
            border-radius: 10px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }
    </style>
</head>
<body>

<div class="container">
    <h1>Charades Game</h1>
    <button onclick="generatePrompt()">Generate Charades Prompt</button>
    <div class="prompt" id="charadesPrompt"></div>
</div>

<script>
    const prompts = [
        {
            prompt: "A person is walking outside wearing a heavy coat, scarf, and gloves while shivering.",
            action: "Act out: Wrapping arms around yourself, shivering, rubbing hands together.",
            hints: "Hints: Pretend to see your breath, blow into hands, act like a cold wind is hitting you."
        },
        {
            prompt: "A student rushes into the classroom, breathing heavily, with their backpack half-zipped and papers sticking out.",
            action: "Act out: Running in, gasping for air, adjusting a backpack, looking at an imaginary clock.",
            hints: "Hints: Wipe imaginary sweat from forehead, mimic being startled by a bell ringing."
        },
        {
            prompt: "Someone is sitting at a lunch table, holding their stomach and looking at an untouched tray of food.",
            action: "Act out: Holding stomach, making a queasy face, pushing food away.",
            hints: "Hints: Put a hand over your mouth like you're about to be sick, shake head at food."
        },
        {
            prompt: "A person is standing outside with an umbrella, but they suddenly run for cover while looking up.",
            action: "Act out: Standing with an imaginary umbrella, looking up, then running suddenly.",
            hints: "Hints: Point up at the sky, act like something wet hits you, shake off 'rain' from clothes."
        },
        {
            prompt: "Someone is watching a scary movie alone at night, sitting on the edge of their seat.",
            action: "Act out: Sitting down, looking intensely at an invisible screen, jumping suddenly.",
            hints: "Hints: Put hands on cheeks like you're scared, act like you hear a strange noise behind you."
        },
        {
            prompt: "You walk into the classroom, and everyone is sitting quietly, looking at the board, while the teacher is standing with a serious expression.",
            action: "Act out: Walking into a room, stopping suddenly, looking around nervously.",
            hints: "Hints: Point at an imaginary clock, place a finger on lips for 'quiet,' fold arms like a strict teacher."
        },
        {
            prompt: "You see a person running with an open umbrella, but the sun is shining and the sky is clear.",
            action: "Act out: Running while holding an imaginary umbrella, looking over your shoulder, acting surprised.",
            hints: "Hints: Mimic a strong wind pushing you, act like you're being chased by something."
        }
    ];

    function generatePrompt() {
        const randomIndex = Math.floor(Math.random() * prompts.length);
        const randomPrompt = prompts[randomIndex];
        document.getElementById('charadesPrompt').innerHTML = `
            <strong>Prompt:</strong> ${randomPrompt.prompt}<br>
            <strong>Action:</strong> ${randomPrompt.action}<br>
            <strong>Hints:</strong> ${randomPrompt.hints}
        `;
    }
</script>

</body>
</html>
