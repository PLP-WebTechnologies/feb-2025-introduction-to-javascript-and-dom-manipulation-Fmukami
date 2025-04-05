# Introduction to JavaScript and DOM Manipulation

## Objectives

Write basic JavaScript functions.
Manipulate the DOM dynamically.
Respond to user interactions.

## Instructions

- Create a script.js file and link it to a HTML.
- Structure the document using DOCTYPE, html, head, and body.

>[!NOTE]
>  - Write JavaScript that:
>  - Changes text content dynamically.
>  - Modifies CSS styles via JavaScript.
>  - Adds or removes an element when a button is clicked.


# Tasks
- Create a well-structured HTML5 document.
- Use at least 5 different HTML elements.
- Ensure semantic correctness.

Happy Coding! 💻✨




<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Interactive JavaScript Example</title>
  <link rel="stylesheet" href="style.css" />
</head>
<body>

  <header>
    <h1>Welcome to My Interactive Page</h1>
  </header>

  <main>
    <section>
      <h2>Click the Button to Change Text</h2>
      <p id="text-content">This text will change when you click the button below.</p>
      <button id="change-text-btn">Change Text</button>
    </section>

    <section>
      <h2>Change the Background Color</h2>
      <button id="change-bg-btn">Change Background Color</button>
    </section>

    <section>
      <h2>Click to Add a New Element</h2>
      <button id="add-element-btn">Add a New Element</button>
      <div id="new-elements-container"></div>
    </section>
  </main>

  <footer>
    <p>&copy; 2025 Interactive Web Page</p>
  </footer>

  <script src="script.js"></script>
</body>
</html>

/* Body Styling */
body {
  font-family: Arial, sans-serif;
  background-color: #f4f4f4;
  padding: 20px;
}

header {
  text-align: center;
  margin-bottom: 30px;
}

h1 {
  font-size: 2.5rem;
  color: #333;
}

h2 {
  font-size: 1.8rem;
  color: #444;
}

button {
  padding: 10px 20px;
  font-size: 1rem;
  margin: 10px;
  background-color: #4CAF50;
  color: white;
  border: none;
  cursor: pointer;
  border-radius: 5px;
}

button:hover {
  background-color: #45a049;
}

#new-elements-container {
  margin-top: 20px;
  padding: 10px;
  background-color: #e8e8e8;
  border-radius: 5px;
}

// DOM manipulation for changing text content
document.getElementById('change-text-btn').addEventListener('click', function() {
  const textElement = document.getElementById('text-content');
  textElement.textContent = 'The text has been changed successfully!';
});

// DOM manipulation for changing background color
document.getElementById('change-bg-btn').addEventListener('click', function() {
  document.body.style.backgroundColor = 'lightblue';
});

// DOM manipulation for adding a new element
document.getElementById('add-element-btn').addEventListener('click', function() {
  const newElementContainer = document.getElementById('new-elements-container');
  
  const newDiv = document.createElement('div');
  newDiv.style.padding = '10px';
  newDiv.style.margin = '5px';
  newDiv.style.backgroundColor = '#fff';
  newDiv.style.border = '1px solid #ddd';
  newDiv.style.borderRadius = '5px';
  
  const newText = document.createTextNode('This is a new dynamically added element!');
  newDiv.appendChild(newText);
  
  newElementContainer.appendChild(newDiv);
});




