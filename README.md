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
    <title>NBA Photo Gallery</title>
    <style>
        body 
        {
            font-family: Arial, sans-serif;
            text-align: center;
            background-color: rebeccapurple;
            margin: 0;
            padding: 0;
        }

        h1 
        {
            margin: 20px;
            color: black;
        }

        .gallery 
        {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 15px;
            margin: 20px;
        }

        .gallery-image 
        {
            width: 200px;
            height: 150px;
            object-fit: cover;
            border: 2px solid white;
            cursor: pointer;
            transition: transform 0.3s ease;
        }

        .gallery-image:hover 
        {
            transform: scale(1.05);
        }

        .slider-container 
        {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.9);
            z-index: 1000;
            justify-content: center;
            align-items: center;
        }

        #slider-image 
        {
            max-width: 90%;
            max-height: 80%;
            margin: auto;
        }

        .close-btn 
        {
            position: absolute;
            top: 20px;
            right: 30px;
            font-size: 40px;
            color: white;
            cursor: pointer;
        }

        .prev-btn, .next-btn 
        {
            position: absolute;
            top: 50%;
            color: white;
            font-size: 40px;
            cursor: pointer;
            user-select: none;
        }

        .prev-btn 
        {
            left: 30px;
        }

        .next-btn 
        {
            right: 30px;
        }

        .prev-btn:hover, .next-btn:hover, .close-btn:hover 
        {
            color: red;
        }

        footer 
        {
            text-align: center;
            padding: 20px;
            background-color: red;
            color: white;
        }

    </style>
</head>
<body>
    <h1>NBA Photo Gallery</h1>
    <div class="gallery">
        <img src="1.jpg" class="gallery-image" alt="Image 1" onclick="openSlider(0)">
        <img src="2.jpg" class="gallery-image" alt="Image 2" onclick="openSlider(1)">
        <img src="3.jpg" class="gallery-image" alt="Image 3" onclick="openSlider(2)">
        <img src="4.jpg" class="gallery-image" alt="Image 4" onclick="openSlider(3)">
        <img src="5.jpg" class="gallery-image" alt="Image 5" onclick="openSlider(4)">
        <img src="6.jpg" class="gallery-image" alt="Image 6" onclick="openSlider(5)">
        <img src="7.jpg" class="gallery-image" alt="Image 7" onclick="openSlider(6)">
        <img src="8.jpeg" class="gallery-image" alt="Image 8" onclick="openSlider(7)">
    </div>

    <div id="slider" class="slider-container">
        <span class="close-btn" onclick="closeSlider()">&times;</span>
        <img id="slider-image" src="" alt="Slider Image">
        <a class="prev-btn" onclick="changeImage(-1)">&#10094;</a>
        <a class="next-btn" onclick="changeImage(1)">&#10095;</a>
    </div>

    <footer>
        <p>MITRAN R (24006381)</p>
    </footer> 
    <script>
        let currentIndex = 0;
        const images = [
            "1.jpg",
            "2.jpg",
            "3.jpg",
            "4.jpg",
            "5.jpg",
            "6.jpg",
            "7.jpg",
            "8.jpeg"
        ];

        function openSlider(index) 
        {
            currentIndex = index;
            document.getElementById('slider-image').src = images[currentIndex];
            document.getElementById('slider').style.display = 'flex';
        }

        function closeSlider() 
        {
            document.getElementById('slider').style.display = 'none';
        }

        function changeImage(step) 
        {
            currentIndex += step;

            // Wrap around when reaching the start or end
            if (currentIndex < 0) currentIndex = images.length - 1;
            if (currentIndex >= images.length) currentIndex = 0;

            document.getElementById('slider-image').src = images[currentIndex];
        }
        
    </script>
</body>
</html>


```

## OUTPUT:

![Screenshot 2024-12-21 213540](https://github.com/user-attachments/assets/2530cea4-4df8-4e99-91a9-13750d4b048c)
![Screenshot 2024-12-21 211130](https://github.com/user-attachments/assets/9309698e-dc45-4f3c-9dcb-41d989835490)
![Screenshot 2024-12-21 211145](https://github.com/user-attachments/assets/a1ab475a-2318-4531-9bd0-f947704d3903)
![Screenshot 2024-12-21 211155](https://github.com/user-attachments/assets/59f4fc51-e04f-4202-90b4-e2c5dbce59f8)
![Screenshot 2024-12-21 211204](https://github.com/user-attachments/assets/36364ead-d94e-46fb-864d-fcb5f239c45d)
![Screenshot 2024-12-21 211223](https://github.com/user-attachments/assets/c7184377-d7df-4c20-8f83-dd9ce703dc17)
![Screenshot 2024-12-21 211233](https://github.com/user-attachments/assets/92f6997a-5005-4906-89f1-742457171977)
![Screenshot 2024-12-21 211242](https://github.com/user-attachments/assets/80df24e2-3a33-4f60-8c19-475ae3d400bc)

## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
