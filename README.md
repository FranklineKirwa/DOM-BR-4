<h1>DOM</h1>
Is a programming interface for web documents. It represents the structure of a document as a tree of objects, allowing programs and scripts to dynamically access and update the content, structure, and style of web pages.

<h1>How to access the DOM</h1>

1.document.getElementById(id): Selects an element by its ID.

Example:
index.html

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <h1 id ="title"></h1>


<script src="script.js"></script>
</body>
</html>

scrip.js
let title=document.getElementById(`title`)
  title.textContent="green";
  title.style.color="blue"

2.document.getElementsByClassName(className): Selects elements by their class name.

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <h1 class="title"></h1>


<script>
    let title=document.getElementsByClassName(`title`)[0];
  title.textContent="Yellow";
  title.style.color="blue"
</script>
</body>
</html>


3.document.getElementsByTagName(tagName): Selects elements by their tag name.

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <h1></h1>


<script>
    let title=getElementsByTagName(`h1`)[0];
  title.textContent="Yellow";
  title.style.color="blue"
</script>
</body>
</html>


4.document.querySelector(selector): Selects the first element that matches the CSS selector.

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <h1 class="title"></h1>


<script>
    document.querySelector(".title").style.backgroundColor = "red";

</script>
</body>
</html>

5.document.querySelectorAll(selector): Selects all elements that match the CSS selector.


<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <h1></h1>
    <h1></h1>



<script>
    const title=document.querySelectorAll("h1");
    title.forEach(title => {
        title.style.color = "red";
    });

</script>
</body>
</html>

<h1>Creating HTML nodes</h1>

To add a new element to the HTML DOM, you must create the element (element node) first, and then append it to an existing element.

<script>
const para = document.createElement("p");//code creates a new <p> element
const node = document.createTextNode("This is new.");//To add text to the <p> element, you must create a text node first. This code creates a text node
para.appendChild(node);//Then you must append the text node to the <p> element
const element = document.getElementById("div1");//append the new element to an existing element.


element.appendChild(para);//This code appends the new element to the existing element
</script>

<h1>Creating new HTML Elements - insertBefore()</h1>

The appendChild() method,appended the new element as the last child of the parent.


<h1>Javascript events</h1>

A JavaScript can be executed when an event occurs, like when a user clicks on an HTML element.

To execute code when a user clicks on an element, add JavaScript code to an HTML event attribute:

onclick=JavaScript
