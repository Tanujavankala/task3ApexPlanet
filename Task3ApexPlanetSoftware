<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Advanced Styling and JS</title>
  <style>
    body {
      font-family: 'Segoe UI', sans-serif;
      margin: 0;
      padding: 0;
      background: #f0f0f0;
      color: #333;
      display: flex;
      flex-direction: column;
      align-items: center;
    }

    header {
      background: #0b7285;
      color: white;
      width: 100%;
      padding: 1rem;
      text-align: center;
    }

    .container {
      padding: 20px;
      max-width: 800px;
      width: 90%;
      background: white;
      box-shadow: 0 0 10px rgba(0,0,0,0.1);
      margin: 2rem 0;
      border-radius: 8px;
    }

    button {
      background: #0b7285;
      color: white;
      border: none;
      padding: 10px 20px;
      margin: 10px 0;
      cursor: pointer;
      border-radius: 5px;
      transition: background 0.3s;
    }

    button:hover {
      background: #087f5b;
    }

    .quiz, .joke {
      margin-top: 20px;
    }

    @media (max-width: 600px) {
      body {
        padding: 10px;
      }

      .container {
        width: 100%;
      }

      button {
        width: 100%;
      }
    }
  </style>
</head>
<body>
  <header>
    <h1>Advanced Styling and JavaScript</h1>
  </header>

  <div class="container">
    <h2>1. Responsive Design Applied</h2>
    <p>This layout adjusts beautifully on mobile, tablet, and desktop using media queries.</p>

    <h2>2. Interactive Quiz</h2>
    <button onclick="startQuiz()">Start Quiz</button>
    <div class="quiz" id="quizBox"></div>

    <h2>3. Fetch a Joke from API</h2>
    <button onclick="fetchJoke()">Get a Random Joke</button>
    <div class="joke" id="jokeBox"></div>
  </div>

  <script>
    // Quiz logic
    const quizData = [
      {
        question: "What does HTML stand for?",
        answer: "Hyper Text Markup Language"
      },
      {
        question: "What language is used for styling web pages?",
        answer: "CSS"
      },
      {
        question: "What language is used to add interactivity?",
        answer: "JavaScript"
      }
    ];

    let quizIndex = 0;

    function startQuiz() {
      if (quizIndex < quizData.length) {
        const current = quizData[quizIndex];
        const userAnswer = prompt(current.question);
        if (userAnswer !== null) {
          const isCorrect = userAnswer.trim().toLowerCase() === current.answer.toLowerCase();
          alert(isCorrect ? "Correct!" :'Wrong! Answer: ${current.answer}');
          quizIndex++;
          startQuiz(); // Continue to next question
        }
      } else {
        document.getElementById("quizBox").innerText = "Quiz Completed!";
        quizIndex = 0;
      }
    }

    // Fetch joke from public API
    async function fetchJoke() {
      const res = await fetch('https://official-joke-api.appspot.com/random_joke');
      const data = await res.json();
      document.getElementById("jokeBox").innerHTML = `<strong>${data.setup}</strong><br>${data.punchline}`;
    }
  </script>
</body>
</html>
