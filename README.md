# Image-Carousel-18JS
 https://www.youtube.com/watch?v=-5yNF2J0Coc&list=PLtMugc7g4GaqAVDZwQ_t1H6500ZGJzOgW&index=6

# [Preview](https://hiratsuna.github.io/Image-Carousel-18JS/)

## html
- [font awesome](https://cdnjs.com/libraries/font-awesome)

## css
- [link](https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css) `https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css`

## js


----
`<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <title>Image Carousel #6</title>
    
    <!-- Inline CSS styles -->
    <style>
        /* Styling for the container holding the image carousel */
        .container {
            width: 65%;
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            flex-direction: column;
            position: relative;
        }

        /* Hiding all the image elements initially */
        .image {
            display: none;
        }

        /* Styling for the previous navigation arrow */
        #prev {
            position: absolute;
            color: rgb(3, 133, 255);
            top: 43%;
            left: 0;
            cursor: pointer;
            padding: 16px;
            font-weight: bold;
            font-size: 1rem;
            transition: 0.6s ease;
            border-radius: 0 3px 3px 0;
            user-select: none;
        }

        /* Styling for the next navigation arrow */
        #next {
            position: absolute;
            color: rgb(0, 119, 255);
            top: 43%;
            right: 0;
            cursor: pointer;
            padding: 16px;
            font-weight: bold;
            font-size: 1rem;
            transition: 0.6s ease;
            border-radius: 0 3px 3px 0;
            user-select: none;
        }

        /* Styling when hovering over the previous and next navigation arrows */
        #prev:hover, #next:hover {
            background-color: rgba(0, 0, 0, 0.5);
        }

        /* Styling for the dots indicating the currently displayed image */
        .dots {
            text-align: center;
            margin-top: 2%;
        }

        /* Styling for the individual dot */
        .dot {
            height: 15px;
            width: 15px;
            background-color: #ff00bf;
            display: inline-block;
            border-radius: 50%;
            margin: 0 2px;
            transition: background-color 0.6s ease;
        }

        /* Styling for the active dot */
        .active {
            background-color: #f881e8;
        }

        /* Fade animation for the images */
        .fade {
            animation: fade 1.5s;
        }

        @keyframes fade {
            from { opacity: 0.4; }
            to { opacity: 1; }
        }

        /* Media query for responsive design when the viewport width is 768px or less */
        @media(max-width:768px){
            .container{
                width: 100%;
            }
        }
    </style>
</head>
<body>

<!-- A container to hold the image carousel -->
<div class="container">

    <!-- Image elements representing the carousel slides -->
    <div class="image fade">
        <img src="1.png" alt="Question 1" width="100%">
    </div>

    <div class="image fade">
        <img src="2.png" alt="Question 2" width="100%">
    </div>

    <div class="image fade">
        <
    <div class="image fade">
        <img src="3.png" alt="Question 3" width="100%">
    </div>

    <div class="image fade">
        <img src="4.png" alt="Question 4" width="100%">
    </div>

    <div class="image fade">
        <img src="5.png" alt="Question 5" width="100%">
    </div>

    <div class="image fade">
        <img src="6.png" alt="Question 6" width="100%">
    </div>

    <div class="image fade">
        <img src="7.png" alt="Question 7" width="100%">
    </div>

    <div class="image fade">
        <img src="8.png" alt="Question 8" width="100%">
    </div>

    <!-- Navigation arrows for moving to the previous and next images -->
    <i id="prev" onclick="show_image(-1)" class="fa-solid fa-circle-chevron-left"></i>
    <i id="next" onclick="show_image(1)" class="fa-solid fa-circle-chevron-right"></i>

    <!-- Dots for indicating the currently displayed image -->
    <div class="dots">
        <span class="dot"></span>
        <span class="dot"></span>
        <span class="dot"></span>
        <span class="dot"></span>
        <span class="dot"></span>
        <span class="dot"></span>
        <span class="dot"></span>
        <span class="dot"></span>
    </div>

</div>

<!-- JavaScript code for image carousel functionality -->
<script>
    // Variable to keep track of the current image index
    var index = 0;

    // Function to display the image at the specified index
    function show_image(i) {
        index += i;

        // Get all the image elements
        var images = document.getElementsByClassName("image");

        // Get all the dot elements
        var dots = document.getElementsByClassName("dot");

        // Hide all the images
        for (i = 0; i < images.length; i++) {
            images[i].style.display = "none";
        }

        // Remove the "active" class from all the dots
        for (i = 0; i < dots.length; i++) {
            dots[i].className = dots[i].className.replace(" active", "");
        }

        // Ensure the index stays within the valid range of images
        if (index > images.length - 1)
            index = 0;

        if (index < 0)
            index = images.length - 1;

        // Display the current image and set its corresponding dot as active
        images[index].style.display = "block";
        dots[index].className += " active";
    }
</script>
</body>
</html>`
