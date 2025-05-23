# Tower of Hanoi

A classic Tower of Hanoi puzzle game implemented as a web application using HTML, CSS, and vanilla JavaScript. This interactive implementation allows users to solve the puzzle manually or watch an automated solution.

## 📝 Table of Contents
- [Demo](#demo)
- [Features](#features)
- [Game Rules](#game-rules)
- [Code Structure](#code-structure)
- [Algorithm](#algorithm)
- [Contributing](#contributing)

## 🎮 Demo

[Live Demo](https://ashanjayamal.github.io/Tower-of-Hanoi/)

## ✨ Features

- **Multiple Difficulty Levels**: Choose between 3, 4, or 5 disks
- **Move Counter**: Tracks the number of moves made
- **Minimum Moves Display**: Shows the minimum number of moves required to solve the puzzle
- **Timer**: Keeps track of how long you've been playing
- **Undo Functionality**: Go back to previous states
- **Auto-Solve Feature**: Watch the puzzle being solved automatically
- **Responsive Design**: Works on various screen sizes
- **Visual Feedback**: Highlights selected towers and provides error messages for invalid moves

## 📋 Game Rules

1. Only one disk can be moved at a time
2. Each move consists of taking the upper disk from one of the towers and placing it on top of another tower
3. No disk may be placed on top of a smaller disk
4. The goal is to move all disks from the first tower to another tower in the minimum number of moves



No dependencies or build process required!

## 🚀 Usage

1. Choose a difficulty level by clicking on the "3 Disks", "4 Disks", or "5 Disks" button
2. Click on a tower with disks to select it
3. Click on another tower to move the top disk there
4. Use the "Reset Game" button to start over
5. Use the "Undo Move" button to go back one move
6. Use the "Auto Solve" button to watch the puzzle being solved automatically

## 🏗️ Code Structure

The application consists of a single HTML file with embedded CSS and JavaScript:

### HTML Structure
- Header with title
- Difficulty level selection buttons
- Game statistics display (moves, minimum moves, time)
- Game container with three towers
- Control buttons (Reset, Undo, Auto Solve)
- Message display area

### CSS Styling
- Responsive layout using flexbox
- Tower and disk styling
- Button and interactive element styling
- Visual feedback for user interactions

### JavaScript Components
- Game state management
- Tower and disk manipulation
- Move validation
- Win condition checking
- Timer functionality
- Undo feature implementation
- Auto-solve algorithm using recursion

## 🧮 Algorithm

The Tower of Hanoi puzzle is solved using a recursive algorithm:

1. To move n disks from source to destination using an auxiliary tower:
   - Move n-1 disks from source to auxiliary
   - Move the largest disk from source to destination
   - Move n-1 disks from auxiliary to destination

```javascript
function solveTowerOfHanoi(n, source, destination, auxiliary) {
    if (n === 1) {
        console.log(`Move disk 1 from ${source} to ${destination}`);
        return;
    }
    solveTowerOfHanoi(n - 1, source, auxiliary, destination);
    console.log(`Move disk ${n} from ${source} to ${destination}`);
    solveTowerOfHanoi(n - 1, auxiliary, destination, source);
}
```

The minimum number of moves required to solve the Tower of Hanoi puzzle with n disks is 2^n - 1.


## 🙏 Acknowledgements

- The Tower of Hanoi puzzle was invented by the French mathematician Édouard Lucas in 1883
- Inspiration for the design and implementation came from various Tower of Hanoi implementations across the web
