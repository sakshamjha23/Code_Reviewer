# AI Integrated Code Reviewer

An AI-powered web application that automatically reviews source code and provides useful feedback to developers. The system uses the **Gemini API** to analyze submitted code and identify potential syntax errors, logical issues, inefficient coding patterns, and possible improvements.

The application provides a simple **React.js interface** where users can submit their code and view AI-generated review results. A **Node.js and Express.js backend** handles API requests, code submissions, and communication with the Gemini AI service. **MongoDB** is used for data persistence.

## Features

* 🤖 **AI-Powered Code Review**
  Uses the Gemini API to analyze source code and generate review feedback.

* 🐞 **Error Detection**
  Identifies potential syntax errors and logical issues in submitted code.

* ⚡ **Code Optimization Suggestions**
  Detects inefficient coding patterns and suggests possible improvements.

* 💡 **Code Explanations**
  Provides explanations to help developers understand issues in their code.

* 🌐 **REST API Integration**
  Node.js and Express.js APIs handle communication between the frontend and backend.

* 🖥️ **Interactive React Interface**
  Users can submit code and view the generated review through a web-based interface.

* 🗄️ **MongoDB Integration**
  MongoDB is used for storing application-related data.

## How It Works

```text
                    User
                      │
                      ▼
              React.js Frontend
                      │
              Code Submission
                      │
                      ▼
             Express.js REST API
                      │
                      ▼
              Node.js Backend
                      │
          ┌───────────┴───────────┐
          │                       │
          ▼                       ▼
      MongoDB                 Gemini API
                                  │
                                  ▼
                          AI Code Analysis
                                  │
                                  ▼
                         Review & Suggestions
                                  │
                                  ▼
              React.js displays the result
```

## Tech Stack

### Frontend

* React.js
* JavaScript
* HTML
* CSS

### Backend

* Node.js
* Express.js
* REST APIs

### Database

* MongoDB

### AI

* Gemini API

### Development Tools

* Git
* GitHub
* VS Code

## Project Architecture

The project follows a client-server architecture.

### Frontend

The React.js frontend provides the user interface for:

* Entering or submitting source code
* Sending code to the backend
* Receiving the AI-generated review
* Displaying errors, explanations, and suggestions

### Backend

The Node.js and Express.js backend is responsible for:

* Receiving code submissions from the frontend
* Creating and handling REST API requests
* Communicating with the Gemini API
* Processing the AI-generated response
* Sending the review back to the frontend
* Handling database operations with MongoDB

### AI Service

The Gemini API analyzes the submitted source code and generates feedback related to:

* Syntax errors
* Logical issues
* Inefficient coding patterns
* Code quality
* Possible improvements
* Code explanations

## Example Workflow

Suppose the user submits:

```javascript
function findSum(arr) {
    let sum = 0;

    for(let i = 0; i <= arr.length; i++) {
        sum += arr[i];
    }

    return sum;
}
```

The application sends the code to the backend through a REST API.

The backend forwards the code to Gemini for analysis.

The AI can identify the potential array-boundary problem and explain that the loop should normally stop before `arr.length`.

It can then provide an improved version:

```javascript
function findSum(arr) {
    let sum = 0;

    for(let i = 0; i < arr.length; i++) {
        sum += arr[i];
    }

    return sum;
}
```

This allows the developer to understand **what is wrong, why it is wrong, and how it can be improved**.

## API Flow

The frontend communicates with the backend using REST APIs.

Example:

```text
POST /api/review
```

Request:

```json
{
  "code": "source code submitted by the user"
}
```

The backend processes the request and sends the code to the Gemini API.

The generated review is then returned to the React frontend.

## Installation and Setup

### Prerequisites

Make sure you have the following installed:

* Node.js
* npm
* MongoDB
* Git

You will also need a **Gemini API key**.

### 1. Clone the Repository

```bash
git clone https://github.com/sakshamjha23/Code_Reviewer.git
cd Code_Reviewer
```

### 2. Install Backend Dependencies

```bash
cd backend
npm install
```

### 3. Configure Environment Variables

Create a `.env` file in the backend directory.

```env
PORT=3000
MONGODB_URI=your_mongodb_connection_string
GEMINI_API_KEY=your_gemini_api_key
```

Do not upload your API key or `.env` file to GitHub.

### 4. Start the Backend

```bash
npm start
```

### 5. Install Frontend Dependencies

Open another terminal:

```bash
cd frontend
npm install
```

### 6. Start the Frontend

```bash
npm run dev
```

The application can then be opened using the local URL provided by Vite.

## Project Structure

```text
Code_Reviewer/
│
├── frontend/
│   ├── src/
│   ├── public/
│   ├── package.json
│   └── ...
│
├── backend/
│   ├── controllers/
│   ├── routes/
│   ├── services/
│   ├── models/
│   ├── server.js
│   ├── package.json
│   └── ...
│
├── .gitignore
└── README.md
```

> The exact folder names may vary depending on the current repository structure.

## Key Highlights

* Developed an **AI-powered source code review system**.
* Integrated **Gemini API** for automated code analysis.
* Implemented **REST APIs** using Node.js and Express.js.
* Built a responsive code submission interface using React.js.
* Integrated **MongoDB** for data persistence.
* Implemented automated identification of syntax errors, logical issues, and inefficient coding patterns.
* Generated explanations and improvement suggestions using AI.

## Future Enhancements

Some possible improvements for the project are:

* Support for multiple programming languages
* User authentication and authorization
* Review history for previously submitted code
* Code quality scoring
* Complexity analysis
* Automated test-case generation
* GitHub repository integration
* More detailed security vulnerability detection
* Deployment using cloud services

## Learning Outcomes

Through this project, I gained practical experience in:

* React.js frontend development
* Node.js and Express.js backend development
* REST API design and integration
* MongoDB database integration
* Third-party API integration
* Generative AI API usage
* Full-stack application development
* Handling communication between frontend, backend, database, and AI services

## Author

**Saksham Jha**

GitHub:
https://github.com/sakshamjha23
