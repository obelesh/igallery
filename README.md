# Ex.08 Design of Interactive Image Gallery
## Date:

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
<html>

<head>
    <title>Enhanced Image Gallery</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            margin: 0;
            padding: 0;
            background: url('pink bg.jpg') no-repeat center center fixed;
            background-size: cover;
            display: flex;
            flex-direction: column;
            align-items: center;
            min-height: 100vh;
        }

        .head {
            text-align: center;
            padding: 10px;
            background: linear-gradient(90deg, #ff0080, #8000ff);
            width: 100%;
            height: 100px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }

        .head h1 {
            font-size: 2.5rem;
            color: #ffffff;
            animation: fadeIn 1.5s ease;
        }

        .gal {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
            gap: 15px;
            padding: 20px;
            margin: 20px 0 10px 0;
            width: 90%;
            max-width: 1200px;
        }

        .gal-item {
            border-radius: 10px;
            overflow: hidden;
            position: relative;
            cursor: pointer;
            border: 10px solid #ffffff;
            margin-right: 40px;
            border-radius: 20px;
            transform: scale(1);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .gal-item img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            display: block;
        }

        .gal-item:hover {
            transform: scale(1.05);
            box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2);
        }

        .gal-item::after {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(to bottom right, rgba(255, 255, 255, 0.2), rgba(0, 0, 0, 0.2));
            opacity: 0;
            transition: opacity 0.3s ease;
        }

        .gal-item:hover::after {
            opacity: 1;
        }

        footer {
            text-align: center;
            margin-top: 20px;
            padding: 10px;
            width: 100%;
            height: 50px;
            background: linear-gradient(90deg, #8000ff, #ff0080);
            color: #ffffff;
            box-shadow: 0 -4px 6px rgba(0, 0, 0, 0.1);
            position: fixed;
            bottom: 0;
        }

        #lightbox {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.8);
            justify-content: center;
            align-items: center;
            z-index: 1000;
            animation: fadeIn 0.5s ease;
        }

        #lightbox img {
            max-width: 90%;
            max-height: 80%;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.5);
        }

        #lightbox .close {
            position: absolute;
            top: 10px;
            right: 10px;
            background: #ff0080;
            color: #fff;
            border: none;
            font-size: 2rem;
            cursor: pointer;
            border-radius: 50%;
            padding: 5px 10px;
            animation: pulse 1.5s infinite;
        }

        @keyframes fadeIn {
            from {
                opacity: 0;
            }

            to {
                opacity: 1;
            }
        }

        @keyframes pulse {

            0%,
            100% {
                transform: scale(1);
            }

            50% {
                transform: scale(1.1);
            }
        }
    </style>
    <script>
        function openLightbox(imageSrc) {
            alert("")
            document.getElementById('lbox-img').src = imageSrc;
            document.getElementById('lightbox').style.display = 'flex';
        }

        function closeLightbox() {
            document.getElementById('lightbox').style.display = 'none';
        }
    </script>
</head>

<body>

    <div class="head">
        <h1>Image Gallery</h1>
    </div>

    <div class="gal">
        <div class="gal-item"
            onclick="openLightbox('https://i.pinimg.com/736x/d3/8b/5e/d38b5e59a8cfadd11577671970cc4ada.jpg')">
            <img src="https://i.pinimg.com/736x/d3/8b/5e/d38b5e59a8cfadd11577671970cc4ada.jpg" alt="Image 1">
        </div>
        <div class="gal-item"
            onclick="openLightbox('https://wallpapers.com/images/hd/hrithik-roshan-stills-from-war-movie-aiopqx07qe40jov3.jpg')">
            <img src="https://wallpapers.com/images/hd/hrithik-roshan-stills-from-war-movie-aiopqx07qe40jov3.jpg"
                alt="Image 2">
        </div>
        <div class="gal-item"
            onclick="openLightbox('https://cdna.pcpartpicker.com/static/forever/images/userbuild/417703.cbfc1f8b0cc40bb36ca50fd9f07e8ee5.jpg')">
            <img src="https://cdna.pcpartpicker.com/static/forever/images/userbuild/417703.cbfc1f8b0cc40bb36ca50fd9f07e8ee5.jpg"
                alt="Image 3">
        </div>
        <div class="gal-item"
            onclick="openLightbox('https://i.pinimg.com/236x/51/4a/2e/514a2ea45a80dcd716f3a9db3cf6ff41.jpg')">
            <img src="https://i.pinimg.com/236x/51/4a/2e/514a2ea45a80dcd716f3a9db3cf6ff41.jpg" alt="Image 4">
        </div>
        <div class="gal-item"
            onclick="openLightbox('https://i.pinimg.com/originals/0e/fa/18/0efa18641d797eaa86594becd7c966ca.jpg')">
            <img src="https://i.pinimg.com/originals/0e/fa/18/0efa18641d797eaa86594becd7c966ca.jpg" alt="Image 5">
        </div>
    </div>

    <div id="lightbox">
        <button class="close" onclick="closeLightbox()">X</button>
        <img src="" id="lbox-img" alt="Full Image">
    </div>

    <footer class = "foot">
        <p><b>Designed by S Rajath (24900186)</b></p>
    </footer>

</body>

</html>

```

## OUTPUT:
![Screenshot 2024-12-21 160814](https://github.com/user-attachments/assets/cc2d5401-54d6-4108-acd2-28a4e54e6649)
![Screenshot 2024-12-21 160831](https://github.com/user-attachments/assets/3ee3e548-9090-424e-8d69-698585e3e0af)
![Screenshot 2024-12-21 160845](https://github.com/user-attachments/assets/aa7faecb-f2b8-4b56-99b9-6c924d0acc10)


## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
