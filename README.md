# CO3 - React Exercise - Export and Import

### NAME : Sree Viveka V S

### REG NO : 2305001031

## Project Description

To develop a React application that demonstrates JavaScript ES6 Export and Import concepts using separate modules and reusable React components.

## Technologies Used

- React JS
- JavaScript (ES6)
- HTML5
- CSS3
- Vite

## Concepts

- JavaScript ES6 Modules
- Named Export
- Named Import
- Default Export
- Importing Variables
- Importing Functions
- React Components
- Component Rendering

## Project Structure

- `App.jsx` – Displays student information and the output of the imported function.
- `App.css` – Defines the styling and appearance of the application.
- `index.css` – Provides global styles for the webpage.
- `main.jsx` – Main entry point that renders the React application.
- `student.js` – Contains exported student details and a reusable function.

## Source Code

### 1. student.js

```javascript
export const studentName = "Sree Viveka";
export const department = "Computer Science and Engineering";
export const college = "Saveetha Engineering College";

export function displayStudent() {
    return `Hello! I am ${studentName}, studying ${department} at ${college}.`;
}
```

### 2. App.jsx

```jsx

import React from "react";
import { studentName, department, college, displayStudent } from "./student.js";
import "./App.css";

function App() {
    return (
        <div className="container">
            <h1>React Export and Import</h1>

            <div className="card">
                <h2>Student Details</h2>
                <p><strong>Name:</strong> {studentName}</p>
                <p><strong>Department:</strong> {department}</p>
                <p><strong>College:</strong> {college}</p>

                <h3>Imported Function Output</h3>
                <p>{displayStudent()}</p>
            </div>
        </div>
    );
}

export default App;

```

### 3. App.css

```css

.container {
    text-align: center;
    padding: 50px 20px;
}

h1 {
    color: #2457a6;
}

.card {
    background: #f0f5ff;
    padding: 30px;
    max-width: 550px;
    margin: 30px auto;
    border-radius: 12px;
    box-shadow: 0 4px 12px rgba(0,0,0,0.1);
}

h2 {
    color: #2457a6;
}

h3 {
    color: #16804a;
}

p {
    font-size: 17px;
    line-height: 1.6;
}

```

### 4. index.css

```css

body {
    margin: 0;
    font-family: Arial, sans-serif;
    background-color: #ffffff;
    color: #333;
}

```

### 5. main.jsx

```jsx
import React from "react";
import ReactDOM from "react-dom/client";
import App from "./App.jsx";
import "./index.css";

ReactDOM.createRoot(document.getElementById("root")).render(
    <React.StrictMode>
        <App />
    </React.StrictMode>
);
```

## Author

Sree Viveka

## Purpose

Developed as part of the Skill Assessment to demonstrate the use of Export and Import features in React applications.

## Output Screenshot
<img width="1600" height="721" alt="WhatsApp Image 2026-11-13 at 9 27 57 AM" src="https://github.com/user-attachments/assets/e12edb7e-5d14-4370-9fdb-857e20a1f3c8" />
