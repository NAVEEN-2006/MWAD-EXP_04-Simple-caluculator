# MWAD-EXP_04-Simple-caluculator
## AIM
To  develop a Simple Calculator using React.js with clean and responsive design, ensuring a smooth user experience across different screen sizes.

## ALGORITHM
### STEP 1
Create a React App.

### STEP 2
Open a terminal and run:
  <ul><li>npx create-react-app simple-calculator</li>
  <li>cd simple-calculator</li>
  <li>npm start</li></ul>

### STEP 3
Inside the src/ folder, create a new file Calculator.js and define the basic structure.

### STEP 4
Plan the UI: Display screen, number buttons (0-9), operators (+, -, *, /), clear (C), and equal (=).

### STEP 5
Create a new file Calculator.css in src/ and add the styling.

### STEP 6
Open src/App.js and modify it.

### STEP 7
Start the development server.
  npm start

### STEP 8
Open http://localhost:3000/ in the browser.

### STEP 9
Test the calculator by entering numbers and operations.

### STEP 10
Fix styling issues and refine content placement.

### STEP 11
Deploy the website.

### STEP 12
Upload to GitHub Pages for free hosting.

## PROGRAM
~~~
// src/Calculator.js
import React, { useState } from "react";
import "./Calculator.css";

export default function Calculator() {
  const [input, setInput] = useState("");

  const handleClick = (value) => {
    setInput(input + value);
  };

  const handleClear = () => {
    setInput("");
  };

  const handleCalculate = () => {
    try {
      setInput(eval(input).toString()); // eval used for simplicity
    } catch (error) {
      setInput("Error");
    }
  };

  return (
    <div className="calculator">
      <div className="display">{input || "0"}</div>
      <div className="buttons">
        <button onClick={handleClear} className="clear">C</button>
        <button onClick={() => handleClick("/")}>/</button>
        <button onClick={() => handleClick("*")}>*</button>
        <button onClick={() => handleClick("-")}>-</button>

        <button onClick={() => handleClick("7")}>7</button>
        <button onClick={() => handleClick("8")}>8</button>
        <button onClick={() => handleClick("9")}>9</button>
        <button onClick={() => handleClick("+")}>+</button>

        <button onClick={() => handleClick("4")}>4</button>
        <button onClick={() => handleClick("5")}>5</button>
        <button onClick={() => handleClick("6")}>6</button>
        <button onClick={handleCalculate} className="equal">=</button>

        <button onClick={() => handleClick("1")}>1</button>
        <button onClick={() => handleClick("2")}>2</button>
        <button onClick={() => handleClick("3")}>3</button>
        <button onClick={() => handleClick("0")} className="zero">0</button>
        <button onClick={() => handleClick(".")}>.</button>
      </div>
    </div>
  );
}

~~~
~~~
// src/App.js
import React from "react";
import Calculator from "./Calculator";

function App() {
  return (
    <div>
      <h2 style={{textAlign:"center", marginTop:"20px"}}>Simple Calculator</h2>
      <Calculator />
    </div>
  );
}

export default App;

~~~
~~~
/* src/Calculator.css */
body {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  margin: 0;
  background: #ffa1a1; /* dark background */
  font-family: Arial, sans-serif;
}

.calculator {
  justify-content: center;
  width: 320px;
  margin: 50px auto;
  border-radius: 12px;
  box-shadow: 0 4px 12px rgba(0,0,0,0.2);
  overflow: hidden;
  background: #fcfcfc;
  color: #fff;
}

.display {
  background: #000000;
  padding: 20px;
  font-size: 2rem;
  text-align: right;
  min-height: 60px;
}

.buttons {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
}

button {
  padding: 20px;
  font-size: 1.2rem;
  border: 1px solid #333;
  background: #444;
  color: #fff;
  cursor: pointer;
  transition: 0.2s;
}

button:hover {
  background: #666;
}

.clear {
  grid-column: span 2;
  background: #e74c3c;
}

.equal {
  grid-row: span 2;
  background: #2ecc71;
}

.zero {
  grid-column: span 2;
}

~~~
## OUTPUT
<img width="1919" height="1135" alt="image" src="https://github.com/user-attachments/assets/d92f1c93-d29f-4656-8c90-ac11fb5fab73" />


## RESULT
The program for developing a simple calculator in React.js is executed successfully.
