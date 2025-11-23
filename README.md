SCORA – Quiz & Survey Management System
Overview

SCORA is a web-based system for managing quizzes, surveys, and educational documents. It allows users to:

Sign up and log in

Access quizzes, surveys, or documents using a unique code

Complete quizzes and view results instantly

The system is built with HTML, CSS, and JavaScript, and uses the browser's localStorage to store data.

Features
User Features

Sign Up / Sign In

Users can create accounts with email and password.

Login credentials are validated and stored in localStorage.

Access Content by Code

Enter a unique code to access any content: quiz, survey, or document.

Opens the selected content in a new page (quiz.html#<code>).

Take Quiz / Survey

Multiple-choice questions for quizzes.

Surveys can collect responses without scoring.

Results displayed after submission (percentage for quizzes, confirmation for surveys).

Admin Features

Create Quiz / Survey

Add quizzes or surveys with a unique serial code.

Set number of questions, timeout, and correct options.

Generate Random Code

Each quiz or survey can generate a unique code for easy sharing.

Project Structure
SCORA/
│
├─ index.html          # Main page / Home page with quiz list
├─signup.html          # User sign-up page
├─signin.html          # User sign-in page
├─join.html            # Join page by code (Quiz / Survey / Document)
├─quiz.html            # Take quiz or survey page
├─style.css            # Styles for all pages
├─project.js           # Main JavaScript handling authentication, quiz creation, and quiz/survey access
├─images/              # Icons and images
└─README.md            # Project documentation

How to Use
1. Running the Project

Clone the repository:

git clone https://github.com/Khlood-Rajaa/SCORA.git


Open index.html or signin.html in your browser.

2. User Flow

Sign Up → Sign In → Main page (quiz list)

Or enter a code on the join page → access quiz, survey, or document

Take quiz → view score

Take survey → submit answers and see confirmation

3. Admin Flow

Create quiz or survey → add questions → generate random code

Users can access the content using the code

Data Storage

Users (formData):

[
  { "fname": "John", "lname": "Doe", "email": "john@example.com", "pwd": "1234" }
]


Quizzes / Surveys (quizes):

[
  {
    "id": 1,
    "title": "CSS Quiz",
    "serial": "abc1",
    "count": 5,
    "timeout": "8",
    "questions": [
      { 
        "id": 1, 
        "title": "What does CSS stand for?", 
        "options": ["Creative Style Sheets","Colorful Style Sheet","Computer Style Sheet","Cascading Style Sheet"], 
        "correct": "4" 
      }
    ]
  }
]

Technologies Used

HTML5

CSS3

JavaScript (ES6+)

Browser localStorage for data persistence

Future Improvements

Support non-scored surveys and document access fully.

Save user results to an external database.

Admin dashboard for content management.

More interactive and responsive UI design.
