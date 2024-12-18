# Ex.08 Design of Interactive Image Gallery
# Date:16/11/24
# AIM:
To design a web application for an inteactive image gallery with minimum five images.

# DESIGN STEPS:
## Step 1:
Clone the github repository and create Django admin interface.

## Step 2:
Change settings.py file to allow request from all hosts.

## Step 3:
Use CSS for positioning and styling.

## Step 4:
Write JavaScript program for implementing interactivity.

## Step 5:
Validate the HTML and CSS code.

## Step 6:
Publish the website in the given URL.

# PROGRAM :
```
HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Interactive Image Gallery</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header>
        <h1>NATURE</h1>
    </header>
    <div class="gallery">
        <div class="gallery-item" onclick="openModal(this)">
            <img src="gallery 1.jpg" >
        </div>
        <div class="gallery-item" onclick="openModal(this)">
            <img src="gal 2.jpg"  >
        </div>
        <div class="gallery-item" onclick="openModal(this)">
            <img src="gal 3.jpg" >
        </div>
        <div class="gallery-item" onclick="openModal(this)">
            <img src="gal 4.jpg" >
        </div>
    </div>

    <div id="modal" class="modal">
        <span class="close" onclick="closeModal()">&times;</span>
        <img class="modal-content" id="modalImage">
        <div id="caption"></div>
    </div>

    <script src="style.js"></script>
</body>
</html>
```
```
CSS
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    background-color: #f4f4f4;
    min-height: 100vh;
}

header h1 {
    margin: 40px 0;
    color: #333;
    font-size: 2rem;
    text-align: center;
    font-weight: bold;
    font-family: cursive;
}

.gallery {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
    gap: 15px;
    max-width: 90%;
}

.gallery-item {
    overflow: hidden;
    position: relative;
}

.gallery-item img {
    width: 100%;
    height: 150px; /* Fixed height for equal size */
    object-fit: cover; /* Ensures images maintain aspect ratio while filling the space */
    border-radius: 8px;
    cursor: pointer;
    transition: transform 0.3s ease;
}

.gallery-item img:hover {
    transform: scale(1.1);
}

.modal {
    display: none;
    position: fixed;
    z-index: 1000;
    left: 0;
    top: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.8);
    justify-content: center;
    align-items: center;
}

.modal-content {
    max-width: 90%;
    max-height: 80%;
    border-radius: 8px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
}

.modal .close {
    position: absolute;
    top: 20px;
    right: 40px;
    color: white;
    font-size: 35px;
    font-weight: bold;
    cursor: pointer;
}

#caption {
    color: white;
    margin-top: 15px;
    text-align: center;
    font-size: 16px;
}
```
```
JAVASCRIPT 
function openModal(element) {
    const modal = document.getElementById("modal");
    const modalImage = document.getElementById("modalImage");
    const caption = document.getElementById("caption");

    modal.style.display = "flex";
    modalImage.src = element.querySelector("img").src;
    caption.textContent = element.querySelector("img").alt;
}

function closeModal() {
    const modal = document.getElementById("modal");
    modal.style.display = "none";
}
```
# OUTPUT:
![alt text](<Screenshot 2024-12-18 212528.png>)
# RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
