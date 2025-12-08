
```html
<!DOCTYPE html>
<html>
<head>
    <title>All DOM Examples</title>
</head>
<body>

    <h2>1. Change Text Example</h2>
    <h3 id="changeHeading">Original Text</h3>
    <button id="changeBtn">Change Text</button>
    <hr>

    <h2>2. Add Element Example</h2>
    <button id="addBtn">Add Paragraph</button>
    <div id="addContainer"></div>
    <hr>

    <h2>3. Remove Element Example</h2>
    <p id="removeText">This text will be removed.</p>
    <button id="removeBtn">Remove Text</button>
    <hr>

    <h2>4. Form Validation Example</h2>
    <input type="text" id="username" placeholder="Enter your name">
    <button id="submitBtn">Submit</button>
    <p id="message"></p>

    <!-- External JavaScript -->
    <script src="script.js"></script>

</body>
</html>
```

```javascript
// 1. Change Text
document.getElementById("changeBtn").addEventListener("click", function() {
    const heading = document.getElementById("changeHeading");
    heading.textContent = "Text Changed Successfully!";
    heading.style.color = "blue";
    heading.style.fontSize = "24px";
});

// 2. Add Element
document.getElementById("addBtn").addEventListener("click", function() {
    const newPara = document.createElement("p");
    newPara.textContent = "A new paragraph was added!";
    document.getElementById("addContainer").appendChild(newPara);
});

// 3. Remove Element
document.getElementById("removeBtn").addEventListener("click", function() {
    const removeText = document.getElementById("removeText");
    if (removeText) {
        removeText.remove();
    }
});

// 4. Form Validation
document.getElementById("submitBtn").addEventListener("click", function() {
    const name = document.getElementById("username").value;
    const message = document.getElementById("message");

    if (name === "") {
        message.textContent = "Please enter your name!";
        message.style.color = "red";
    } else {
        message.textContent = "Welcome, " + name + "!";
        message.style.color = "green";
    }
});
