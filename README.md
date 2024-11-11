# Time Block Challenge Game

**Time Block Challenge Game** is an interactive React-based game where players select a time block and attempt to stop a countdown timer as close to zero as possible. The player with the highest score, based on how near their stop time is to the timer's expiration, wins. This project demonstrates my skills in React, specifically using **Refs** for controlling timer behavior and **Portals** for rendering modal components outside the main DOM hierarchy.

## Game Rules

1. **Start Game**: Players can select one of the available time blocks (e.g., 5 seconds, 10 seconds, 15 seconds).
2. **Start Timer**: Once a time block is selected, a countdown timer begins.
3. **Stop Timer**: Players must click a "Stop" button to stop the timer. The closer they are to the timer’s expiration, the higher the score.
4. **Winner**: The player with the score nearest to the timer’s end wins the round. The score is determined by the difference between the time remaining and the total time of the selected time block. Lower differences mean higher scores.

---

## Features

- **Dynamic Time Selection**: Players can choose different time blocks to test their skills.
- **Real-Time Timer**: The game provides a countdown timer that the player can try to stop as close as possible to the end.
- **Interactive Feedback**: After stopping the timer, players receive feedback on how close their stop time was to the target.
- **Score Calculation**: Scores are calculated based on how accurate the player was in stopping the timer.

---

## Technologies Used

- **React**: The primary library for building the app.
- **React Refs**: Used for accessing and manipulating DOM elements directly in a declarative React way, such as for controlling the timer and button interactions.
- **React Portals**: Used for rendering UI elements like modals or overlays outside the main DOM hierarchy but still within the React app's context.
- **State Management**: Managed using React’s `useState` hook to handle game state, timer state, and player scores.
- **CSS**: For basic styling and layout.

---

## How It Works: Refs & Portals

This project leverages **Refs** and **Portals** to improve the user experience and manage the interaction between components effectively.

### **Using Refs**

In this game, I utilized React **Refs** for the following purposes:

- **Timer Control**: The countdown timer component is controlled via a ref, which allows for direct manipulation of the timer's state (start, stop) without needing to pass state through props.
- **Button Click Events**: A ref is used to handle the event when a player clicks to stop the timer, ensuring that the button interaction happens immediately in response to user input.

By using Refs, I can avoid prop-drilling and make the app more efficient, particularly in managing imperative actions like controlling timers or interacting with UI elements without unnecessary re-renders.

### **Using Portals**

React **Portals** are used to render UI elements outside the normal component hierarchy. In this project, I used a portal for the **Game Over Modal** that appears when the player stops the timer. By rendering the modal in a portal, I can ensure that it appears on top of the game UI without being affected by the parent component’s styles or layout.

This makes the modal's positioning and styling more manageable, and it allows for more flexibility in rendering modals or other overlays outside of the normal DOM flow.

---

## Installation

To run the project locally, follow these steps:

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/time-block-challenge.git
2. Navigate to the project directory:
   ```bash
    cd time-block-challenge
3. Install dependencies:
   ```bash
   npm install
4. Start the development server:
   ```bash
   npm start
5. Open your browser and navigate to http://localhost:3000 to play the game.

---

## Contributing

If you have any suggestions, improvements, or find bugs, feel free to fork the repository and open a pull request or open an issue. Contributions are always welcome!
   
