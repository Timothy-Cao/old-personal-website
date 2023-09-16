---
title: ""
permalink: "/blog/puzzle"
layout: page
---

<a href="/personal/blog" style="position: fixed; bottom: 20px; right: 20px; background-color: #6495ED; color: white; padding: 10px 15px; text-decoration: none; border-radius: 5px;">← Back</a>

<style>
  .bubble-section {
    background-color: #333;
    border-radius: 15px;
    box-shadow: 0 0 10px rgba(255, 255, 255, 0.1);
    padding: 20px;
    margin-bottom: 20px;
  }
</style>

<!-----------------------------SCIENCE QUIZ ----------------------------->
<div class="bubble-section">

<h2><span style="color: #89CFF0;">Make Bill Nye Proud: General Science Knowledge</span></h2>

<button id="next-question-button" onclick="fetchNewQuiz()">Next Question</button>

<div class="quiz-container">
    <h2>General Science Knowledge Quiz</h2>
    <p>Select the correct answer by clicking on the option.</p>
    <div id="science-quiz">
    </div>
</div>

<script>
  function fetchNewQuiz() {
    // Clear previous question
    const quizContainer = document.getElementById('science-quiz');
    quizContainer.innerHTML = '';

    // Fetch the new question
    fetch('https://opentdb.com/api.php?amount=1&category=17&difficulty=hard')
      .then(response => response.json())
      .then(data => {
        const question = data.results[0];
        const options = [...question.incorrect_answers, question.correct_answer];
        options.sort(() => Math.random() - 0.5);

        const questionContainer = document.createElement('div');
        questionContainer.classList.add('quiz-question');
        questionContainer.innerHTML = `
          <p>${question.question}</p>
          <ul class="quiz-options">
            ${options.map(option => `
              <li data-correct="${option === question.correct_answer ? 'true' : 'false'}">${option}</li>
            `).join('')}
          </ul>
          <p class="quiz-feedback"></p>
        `;

        const optionElements = questionContainer.querySelectorAll('.quiz-options li');
        optionElements.forEach(option => {
          option.addEventListener('click', function() {
            const correct = this.getAttribute('data-correct') === 'true';
            const feedback = this.parentElement.nextElementSibling;
            feedback.textContent = correct ? 'Correct!' : 'Incorrect!';
            feedback.style.color = correct ? 'green' : 'red';

            optionElements.forEach(elem => {
              elem.style.pointerEvents = 'none';
              if (elem.getAttribute('data-correct') === 'true') {
                elem.style.color = 'green';
              }
            });
          });
        });

        quizContainer.appendChild(questionContainer);
      })
      .catch(error => {
        console.error('Error fetching quiz:', error);
      });
  }

  fetchNewQuiz();
</script>
</div>




<style>
  button {
    margin-bottom: 10px;
  }
  .quiz-options li {
    cursor: pointer;
    list-style-type: none;
    padding: 5px;
    border: 1px solid #ccc;
    margin: 5px 0;
  }
  #quiz-popup {
    background-color: rgba(0, 0, 0, 0.5); 
    border-radius: 10px;
    padding: 20px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.5); 
    max-width: 80%;
    overflow: auto;
  }
  .quiz-question {
    margin: 20px 0;
  }
  .quiz-feedback {
    margin-top: 10px;
  }
</style>


<!-----------------------------TETRIS PUZZLE ----------------------------->
<div class="bubble-section">

<h2><span style="color: #89CFF0;">Tetris Puzzles</span></h2>
<p>A surprisingly hard puzzle that may arise from PCO</p>
<img src="../assets/images/tetris_puzzle1.png" style="width: 300px; height: 400px;"><br>
<a href="https://jstris.jezevec10.com/?play=6&map=51132" target="_blank">Play it yourself!</a>
<div>
  <button onclick="toggleSpoiler('tetrisSpoiler1')">Show/Hide Hint</button>
  <div id="tetrisSpoiler1" style="display:none;">
    Piece order: O L I Z S. Three of the pieces need to be spun in.
  </div>
</div>
</div>

<script>
function toggleSpoiler(spoilerId) {
    const spoiler = document.getElementById(spoilerId);
    if (spoiler.style.display === "none") {
        spoiler.style.display = "block";
    } else {
        spoiler.style.display = "none";
    }
}
</script>
<!-----------------------------CHESS PUZZLE ----------------------------->
<div class="bubble-section">
<h2><span style="color: #89CFF0;">Chess Puzzles</span></h2>
<p>Difficulty: 2100</p>
<img src="../assets/images/chess_puzzle1.png" style="width: 400px; height: 400px;">
<div>
  <button onclick="toggleSpoiler('chessSpoiler1')">Show/Hide Solution</button>
  <div id="chessSpoiler1" style="display:none;">
    1... Bg4 2. Rxe8+ Rxe8 3. h3 Bxh5 4. Bd6 Nf8 5. Bxc5 Rb8 6. Bd5 Rb5 7. d4 Nd7 8. c4 Rb1+ 9. Kh2
  </div>
</div>
</div>
<!-----------------------------LOGIC PUZZLE ----------------------------->
<div class="bubble-section">
<h2><span style="color: #89CFF0;">Logic Puzzles</span></h2>
<p>WIP</p>
</div>
<!-----------------------------FERMI PUZZLE ----------------------------->
<div class="bubble-section">
<h2><span style="color: #89CFF0;">Fermi Estimations</span></h2>
<p>WIP</p>
</div>
