🌐 Document Object Model (DOM) — Brief Explanation

The DOM (Document Object Model) is a programming interface that allows JavaScript to interact with and manipulate HTML pages. It represents the page as a tree of objects, where each HTML element becomes a node that JavaScript can access and modify.

🌳 What is the DOM?

The DOM turns your HTML into a tree structure.

Each HTML element becomes a node.

JavaScript can use this structure to read, change, add, or delete elements.

This is how websites become interactive.

 Why DOM is Important

Using the DOM, JavaScript can:

Change text on the page

Update styles

Add new HTML elements

Remove elements

Handle events (clicks, inputs, keypresses, etc.)

🔍 Essential DOM Methods
**1. Selecting Elements**

document.getElementById("header-id");

document.getElementsByClassName("Container");

document.getElementsByTagName("p");

document.querySelector(".items-container");// first match

document.querySelectorAll("li");                 // all matches

**2. Changing Content**

document.getElementById("header-id").textContent = "New Heading!";

document.querySelector("p").innerHTML = "<b>Updated paragraph</b>";


**3. Changing Styles**
   
document.querySelector("h2").style.color = "blue";

document.querySelector("div").style.backgroundColor = "#eee";


**4. Creating and Adding Elements**
let li = document.createElement("li");

li.textContent = "New List Item";

document.querySelector(".items-container").appendChild(li);


**5. Removing Elements**

document.querySelector("h3").remove();


**6. Handling Events**

document.querySelector("h2").addEventListener("click", function() {

    alert("You clicked on H2!");
    

});

🎯 In Simple Words

HTML = structure

CSS = style

DOM + JavaScript = interactivity

The DOM is what allows JavaScript to talk to your HTML.
