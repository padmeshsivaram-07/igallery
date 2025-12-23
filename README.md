# Ex.08 Design of Interactive Image Gallery
## Date:23.12.25

## AIM:
To design a web application for an inteactive image gallery with minimum five images.

## DESIGN STEPS:

### Step 1:
Clone the github repository and create Django admin interface.

### Step 2:
Change settings.py file to allow request from all hosts.

### Step 3:
Use CSS for positioning and styling.

### Step 4:
Write JavaScript program for implementing interactivity.

### Step 5:
Validate the HTML and CSS code.

### Step 6:
Publish the website in the given URL.

## PROGRAM :
```
gallery.html

{% load static %}
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Interactive Photo Gallery</title>
  <style>
    .gallery img {
      width: 200px;
      margin: 10px;
      cursor: pointer;
      transition: transform 0.3s;
      border-radius: 8px;
      box-shadow: 0 2px 5px rgba(0,0,0,0.3);
    }
    .gallery img:hover {
      transform: scale(1.1);
    }
    *{
    margin:0;
    border:0;
}
body{
    background:linear-gradient(135deg,#000cff,#2a5298,#00c6ff)
}
.image{

    display:grid;
    grid-template-columns:repeat(5,2fr);
}
img{
    position:relative;
    top:200px;
    width: 170px;
    left: 30px;
    height: 200px;
    border:solid 10px rgba(58,135,171,0.83);
    transition:transform 0.3s ease;
    cursor:pointer;   
}
h1,h2{
    position:relative;
    top:400px;
    left:20px;
    font-family:Cambria,Cochin,Georgia,Times,'Times New Roman',serif;
    font-size:35px;
    color:azure;
}
    #lightbox {
      position: fixed;
      top:0; left:0; right:0; bottom:0;
      background: rgba(0,0,0,0.8);
      display:none;
      justify-content:center;
      align-items:center;
      z-index: 999;
    }
    #lightbox img {
      max-width: 90%;
      max-height: 90%;
      border-radius: 10px;
      box-shadow: 0 0 15px white;
    }
  </style>
</head>
<body>
    <div class="gallery">
  {% for img in images %}
    <img src="{% static 'gallery/images/'|add:img %}" alt="Photo" onclick="openLightbox(this.src)">
  {% endfor %}
</div>

        <br>
        <br>
        <br>
        <br>
        <br>
        <br>
        <br>
        <h1 align="center">&copy;image gallaryDesigned by:</h1>
        <h2 align="center">PADMESH SIVARAM R (25012017)</h2>
<h1>Interactive Photo Gallery</h1>


<div id="lightbox" onclick="closeLightbox()">
  <img id="lightbox-img" src="" alt="Large view">
</div>

<script>
  function openLightbox(src) {
    document.getElementById('lightbox-img').src = src;
    document.getElementById('lightbox').style.display = 'flex';
  }
  function closeLightbox() {
    document.getElementById('lightbox').style.display = 'none';
  }
</script>

</body>
</html>

```

## OUTPUT:
![alt text](<Screenshot 2025-12-23 160838.png>)
## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
