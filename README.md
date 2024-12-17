 Ex.08 Design of Interactive Image Gallery
## Date:16-12-24

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
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Simple Celebrity Gallery</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            background-color: #000;
            color: #fff;
        }
        h1 {
            text-align: center;
            margin-top: 20px;
            font-size: 2rem;
        }
        .gallery {
            display: flex;
            justify-content: center;
            margin-top: 20px;
            gap: 10px;
        }
        .gallery-item {
            border: 2px solid #fff;
            width: 200px;
            height: 300px;
            overflow: hidden;
            cursor: pointer;
        }
        .gallery-item img {
            width: 100%;
            height: 100%;
        }
        .caption {
            text-align: center;
            background-color: rgba(0, 0, 0, 0.5);
            padding: 5px;
            color: #fff;
        }
        .lightbox {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.8);
            align-items: center;
            justify-content: center;
            z-index: 1000;
        }
        .lightbox img {
            max-width: 90%;
            max-height: 90%;
            border: 3px solid #fff;
        }
        .lightbox.active {
            display: flex;
        }
        .lightbox span {
            position: absolute;
            top: 20px;
            right: 30px;
            font-size: 2rem;
            color: #fff;
            cursor: pointer;
        }
    </style>
</head>
<body>
    <h1>Celebrity Photo Gallery</h1>
    <div class="gallery">
        <div class="gallery-item">
            <a href="javascript:void(0);" onclick="openLightbox('dhoni.webp')">
                <img src="dhoni.webp" alt="M S Dhoni">
                <div class="caption">M S Dhoni</div>
            </a>
        </div>
        <div class="gallery-item">
            <a href="javascript:void(0);" onclick="openLightbox('virat.jpg')">
                <img src="virat.jpg" alt="Virat Kohli">
                <div class="caption">Virat Kohli</div>
            </a>
        </div>
        <div class="gallery-item">
            <a href="javascript:void(0);" onclick="openLightbox('jaddu.jpeg')">
                <img src="jaddu.jpeg" alt="Jedaja">
                <div class="caption">Jedaja</div>
            </a>
        </div>
        <div class="gallery-item">
            <a href="javascript:void(0);" onclick="openLightbox('pathirana.webp')">
                <img src="pathirana.webp" alt="Pathirana">
                <div class="caption">Pathirana</div>
            </a>
        </div>
        <div class="gallery-item">
            <a href="javascript:void(0);" onclick="openLightbox('rohit.jpg')">
                <img src="rohit.jpg" alt="Rohit Sharma">
                <div class="caption">Rohit Sharma</div>
            </a>
        </div>
    </div>

    <div id="lightbox" class="lightbox">
        <span onclick="closeLightbox()">&times;</span>
        <img id="lightbox-img" src="" alt="Lightbox Image">
    </div>

    <script>
        function openLightbox(imageSrc) {
            var lightbox = document.getElementById('lightbox');
            var lightboxImage = document.getElementById('lightbox-img');
            lightboxImage.src = imageSrc;
            lightbox.classList.add('active');
        }

        function closeLightbox() {
            var lightbox = document.getElementById('lightbox');
            lightbox.classList.remove('active');
        }
    </script>
</body>
</html>
```

## OUTPUT
![Screenshot 2024-12-17 093919](https://github.com/user-attachments/assets/654caf48-fd16-4f83-94b5-8bd2b4f7e089)

![Screenshot 2024-12-17 093931](https://github.com/user-attachments/assets/373eee85-83a8-4804-bdff-4fdc19f43e0a)

## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
