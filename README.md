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
index.html

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Gallery</title>
    <style>
        #flexbox
        {
            /* border: 5px solid pink; */
            padding: 100px;
            background-image: url("bg.jpeg");
        }
        #container1
        {
            /* margin-left:25%; */
            display: flex;
            background-color: whitesmoke; 
            gap: 20px;
            justify-content: center;
            padding: 10px;
            box-shadow: 0 2px 3px;
        }
        #container2
        {
            gap: 20px;
            display: flex;
            background-color: whitesmoke; 
            justify-content: center;
            /* border: 5px inset black; */
            padding: 10px;
            box-shadow:0 2px 3px;
        }
        .img
        {
            height: 150px;
            width: 250px;
            /* transform: rotate(-10deg); */
            image-rendering:optimizeQuality;    
            border: 2px inset whitesmoke;    
            border-radius: 10px;
            box-shadow:  0 0 10px black ;
            transition: 0.5s;
        }
        .img:hover
        {
            content: 'hello';
            transform: scale(1.3);
        }
        #divs
        {
            display: inline;
        }
        #image
        {
            z-index: 100;
            display: none;
            background: rgba(0,0,0,0.5);
            position: fixed;
            width: 100%;
            /* transform: rotate(20deg); */
            height: 100%;
            top: 0;
            bottom: 0;
            align-items: center;
            justify-content: center;    
        }
        #image img{
            width: 600px;
            height: auto;
        }
        #title
        {
            background-color: wheat;
            border-radius: 10px;
            width: 500px;
            box-shadow: 0 3px 10px;
            position: absolute;
            top: 20px;
            left: 500px;
        }
    </style>
</head>
<body>
    <section id="image">
            <img src="vijay.jpeg" alt="" id="display" onclick="closes()">
    </section>
<div id="flexbox">

    <h1 align="center" ><span id="title">MY PHOTO GALLERY </span></h1>

    <div id="container1">
        <div class="divs"><img class="img" src="vijay1.jpeg" onclick="opens(this.src)" alt=""></div>
        <div class="divs"><img class="img" src="vijay2.webp" onclick="opens(this.src)"   alt=""></div>
        <div class="divs"><img class="img" src="vijay3.jpeg"  onclick="opens(this.src)"  alt=""></div>
        <div class="divs" ><img class="img" src="vijay4.jpeg" onclick="opens(this.src)"   alt=""></div>
    </div>
    <div id="container2">
        <div class="divs" ><img class="img" src="vijay5.webp" onclick="opens(this.src)"  alt=""></div>
        <div class="divs"><img class="img" src="vijay6.jpg" onclick="opens(this.src)"  alt=""></div>
        <div class="divs" ><img class="img" src="vijay7.jpeg" onclick="opens(this.src)"  alt=""></div>
       <div class="divs"><img class="img" src="vijay10.jpeg" onclick="opens(this.src)"  alt=""> </div>
    </div>
    
</div>
<footer align="center" style="background-color:gray">
    <p>Designed & Developed by Ameen Basha &copy; </p>
</footer>
    <script>
            var a =document.getElementById("image");
            var b=document.getElementById("display");
            function opens(c)
            {
                a.style.display='flex';
                b.src=c;
            }
            function closes()
            {
                a.style.display='none';
            }
    </script>
</body>
</html>

```

## OUTPUT:
![Screenshot 2024-12-21 155237](https://github.com/user-attachments/assets/c420100c-f9a2-406e-a917-68f640e9bcf2)

![Screenshot 2024-12-21 155252](https://github.com/user-attachments/assets/fa2c3c36-aa98-47fb-b1ea-53988b1260d1)

## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
