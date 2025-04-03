# **Country Quiz**

A fun and educational web-based quiz game designed to test your knowledge of world countries and their flags. Challenge yourself to name countries based on their flags while keeping track of your score.

---

## **Features**
- **Randomized Questions**:
  - Flags are randomly chosen from a database for each question.
- **Dynamic Scoring**:
  - Keeps track of the total number of correct answers during a session.
- **Immediate Feedback**:
  - Provides real-time validation of answers, indicating whether they are correct or incorrect.
- **Restart Mechanism**:
  - Automatically prompts the user to restart the game when they answer incorrectly.
- **Responsive Design**:
  - Designed for a smooth and engaging user experience on both desktop and mobile devices.

---

## **How to Play**
1. A random flag is displayed on the screen.
2. Type the name of the country associated with the flag in the input box.
3. Submit your answer:
   - If correct, your score increases, and the next flag is shown.
   - If incorrect, the game ends, and your final score is displayed.
4. Restart the game to improve your score.

---

## **Technologies Used**
- **Node.js**: Backend runtime environment.
- **Express.js**: Framework for routing and middleware.
- **PostgreSQL**: Database for storing flags and country details.
- **EJS (Embedded JavaScript Templates)**: For rendering dynamic content.
- **CSS**: For styling the front-end interface.
- **JavaScript**:
  - Implements game logic and handles input validation on the frontend.
  - Provides dynamic feedback for user answers.
- **body-parser**: Middleware to handle form submissions.
- **dotenv**: For securely managing environment variables.

---

## **Getting Started**

### **Prerequisites**
- **Node.js**: To run the server-side code.
- **PostgreSQL**: Ensure PostgreSQL is installed and running.

---

### **Installation**
1. Clone the repository:
   ```bash
   git clone https://github.com/Ayu1404/Country-Quiz.git
   cd Country-Quiz
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Set up the `.env` file in the root directory with your PostgreSQL credentials:
   ```plaintext
   DB_USER=your_database_user
   DB_HOST=your_database_host
   DB_NAME=your_database_name
   DB_PASSWORD=your_database_password
   DB_PORT=your_database_port
   ```

4. Populate the database:
   - Ensure the `flags` table contains the required data:
     - **name**: Full name of the country.
     - **flag**: Unicode or emoji representation of the country's flag.

5. Start the server:
   ```bash
   node app.js
   ```

6. Open your browser and navigate to:
   ```plaintext
   http://localhost:3000
   ```

---

## **Database Schema**
The **flags** table is structured as follows:
| Column Name | Data Type | Description                  |
|-------------|-----------|------------------------------|
| **id**      | INTEGER   | Unique identifier for each flag. |
| **name**    | TEXT      | Full name of the country.    |
| **flag**    | TEXT      | Emoji or symbol of the flag. |

---

## **Project Structure**
### **Server-Side (app.js)**:
- **GET `/`**:
  - Displays the first random question and initializes the game.
- **POST `/submit`**:
  - Validates the submitted answer against the current question.
  - Updates the total score and generates the next question.

### **Front-End (index.ejs)**:
- **Dynamic Content**:
  - Displays the current flag and input form for answers.
  - Shows real-time feedback for correct/incorrect answers.
- **Restart Mechanism**:
  - Automatically restarts the game when the user provides an incorrect answer.

---

## **Usage**
1. **Start the Quiz**:
   - Open the app in your browser and begin answering questions.
2. **Submit Answers**:
   - Use the input box to type your answer and press submit.
3. **Track Your Score**:
   - View your current score at the top of the screen.
4. **Restart**:
   - Restart the game automatically after an incorrect answer.

---

## **Contributing**
Contributions are welcome! To contribute:
1. Fork this repository.
2. Create a new branch:
   ```bash
   git checkout -b feature/your-feature-name
   ```
3. Commit your changes:
   ```bash
   git commit -m "Add your feature"
   ```
4. Push to your branch:
   ```bash
   git push origin feature/your-feature-name
   ```
5. Open a pull request.

---

## **License**
This project is licensed under the MIT License, allowing you to modify and distribute the project with proper attribution.

---

## **Acknowledgments**
- Inspired by the love of geography and learning about countries.
- Thanks to the open-source tools and frameworks that made this project possible.
