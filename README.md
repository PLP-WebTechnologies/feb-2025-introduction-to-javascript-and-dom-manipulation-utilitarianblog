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

# Solution
## index.html

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>JavaScript DOM Manipulation</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            margin: 20px;
        }
        #dynamicText {
            font-size: 20px;
            color: blue;
            margin: 20px;
        }
        .hidden {
            display: none;
        }
    </style>
</head>
<body>

    <h1>Welcome to My JavaScript Demo</h1>
    <p id="dynamicText">This text will change dynamically.</p>

    <button onclick="changeText()">Change Text</button>
    <button onclick="changeStyle()">Change Style</button>
    <button onclick="toggleElement()">Show/Hide Element</button>

    <div id="toggleDiv" class="hidden">
        <p>This is a dynamically toggled element.</p>
    </div>

    <script src="script.js"></script>

</body>
</html>

## script.js

// Function to change text dynamically
function changeText() {
    document.getElementById("dynamicText").textContent = "Text changed successfully!";
}

// Function to modify CSS styles dynamically
function changeStyle() {
    let textElement = document.getElementById("dynamicText");
    textElement.style.color = "red";
    textElement.style.fontSize = "24px";
    textElement.style.fontWeight = "bold";
}

// Function to add/remove an element dynamically
function toggleElement() {
    let toggleDiv = document.getElementById("toggleDiv");
    if (toggleDiv.classList.contains("hidden")) {
        toggleDiv.classList.remove("hidden");
    } else {
        toggleDiv.classList.add("hidden");
    }
}
