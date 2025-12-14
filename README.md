// -------------------------------
// JavaScript Quiz Game Assignment
// -------------------------------

// 1. Quiz Questions Array
const quizQuestions = [
    {
        question: "What is the capital of India?",
        answer: "delhi"
    },
    {
        question: "Which programming language runs in the browser?",
        answer: "javascript"
    },
    {
        question: "What keyword is used to declare a variable in JavaScript? (var/let/const)",
        answer: "var"
    },
    {
        question: "What does HTML stand for?",
        answer: "hypertext markup language"
    },
    {
        question: "What symbol is used for single-line comments in JavaScript?",
        answer: "//"
    }
];

// 2. Function to run the quiz
function runQuiz() {

    // 3. Initialize score
    let score = 0;

    // 4. Loop through each question
    for (let i = 0; i < quizQuestions.length; i++) {

        // 5. Prompt for user input
        let userAnswer = prompt(quizQuestions[i].question);

        // If user presses cancel
        if (userAnswer === null) {
            alert("You exited the quiz.");
            return;
        }

        // 6. Normalize the input
        userAnswer = userAnswer.toLowerCase().trim();

        // 7. Check the answer
        if (userAnswer === quizQuestions[i].answer) {
            score++; // increase score
            // 8. Provide immediate feedback
            alert("Correct! 🎉");
        } else {
            alert("Wrong ❌\nCorrect Answer: " + quizQuestions[i].answer);
        }
    }

    // 9. Display final score
    alert("Quiz Completed!\nYour Score: " + score + " / " + quizQuestions.length);
}

// 10. Run the quiz in the browser console
runQuiz();
