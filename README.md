<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="O.P GUPTA CONSTRUCTIONS - Professional Construction Services">
    <title>O.P GUPTA CONSTRUCTIONS</title>
    <style>
        /* Body and General Styles */
        body {
            margin: 0;
            font-family: 'Poppins', sans-serif;
            font-size: 18px; /* Fixed size in pixels */
        }

        /* Slideshow Styles */
        .slideshow-container {
            max-width: 100%;
            position: relative;
            margin: auto;
        }

        .mySlides {
            display: none;
        }

        img {
            width: 100%;
            height: auto;
        }

        /* Title Styles */
        .title {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            color: white;
            font-size: 60px; /* Fixed title font size in pixels */
            text-align: center;
            padding: 20px;
            background-color: rgba(0, 0, 0, 0.678);
        }

        /* Work Section */
        .work-section {
            padding: 20px;
            background-color: #f4f4f4;
            text-align: center;
        }

        .work-item {
            margin: 20px;
            padding: 15px; /* Increase padding */
            border: 1px solid #ccc;
            border-radius: 5px;
            display: inline-block;
            cursor: pointer; /* Make it look clickable */
            font-size: 24px; /* Fixed work item font size in pixels */
        }

        /* Arrows and Dots Styles */
        .prev, .next {
            cursor: pointer;
            position: absolute;
            top: 50%;
            width: auto;
            padding: 16px;
            margin-top: -22px;
            color: white;
            background-color: rgba(0, 0, 0, 0.6);
            font-weight: bold;
            border: none;
            font-size: 24px; /* Fixed arrow font size in pixels */
            transition: 0.6s ease;
            user-select: none;
        }

        .next {
            right: 0;
        }

        .dot-container {
            text-align: center;
            padding: 20px;
        }

        .dot {
            cursor: pointer;
            height: 15px;
            width: 15px;
            margin: 0 2px;
            background-color: #bbb;
            border-radius: 50%;
            display: inline-block;
            transition: background-color 0.6s ease;
        }

        .active, .dot:hover {
            background-color: #717171;
        }
    </style>
</head>
<body>

    <!-- Slideshow Section -->
    <div class="slideshow-container">
        <div class="mySlides">
            <img src="https://res.cloudinary.com/ds4uhhzpc/image/upload/v1729683820/freepik__upload__12266_hayiyt.jpg" alt="Construction Project 1">
            <div class="title">O.P GUPTA CONSTRUCTIONS PVT.LTD</div>
        </div>
        <div class="mySlides">
            <img src="https://res.cloudinary.com/ds4uhhzpc/image/upload/v1729683820/freepik__upload__12266_hayiyt.jpg" alt="Commercial Buildings">
        </div>
        <div class="mySlides">
            <img src="https://res.cloudinary.com/ds4uhhzpc/image/upload/v1729683820/freepik__upload__12266_hayiyt.jpg" alt="Infrastructure">
        </div>
        <a class="prev" onclick="plusSlides(-1)">&#10094;</a>
        <a class="next" onclick="plusSlides(1)">&#10095;</a>
    </div>

    <div class="dot-container">
        <span class="dot" onclick="currentSlide(1)"></span>
        <span class="dot" onclick="currentSlide(2)"></span>
        <span class="dot" onclick="currentSlide(3)"></span>
    </div>

    <!-- Work Section -->
    <div class="work-section">
        <h2>Our Work</h2>
        <div class="work-item" onclick="openFormPage()">New Form</div>
        <div class="work-item">Commercial Buildings</div>
        <div class="work-item">Infrastructure Development</div>
        <div class="work-item">Road Construction</div>
        <div class="work-item">Renovation Services</div>
    </div>

    <footer>
        <p>&copy; 2024 O.P Gupta Constructions. All Rights Reserved.</p>
    </footer>

    <!-- JavaScript for Slideshow and New Page Opening -->
    <script>
        let slideIndex = 1;
        showSlides(slideIndex);

        function plusSlides(n) {
            showSlides(slideIndex += n);
        }

        function currentSlide(n) {
            showSlides(slideIndex = n);
        }

        function showSlides(n) {
            let i;
            let slides = document.getElementsByClassName("mySlides");
            let dots = document.getElementsByClassName("dot");
            if (n > slides.length) {slideIndex = 1}
            if (n < 1) {slideIndex = slides.length}
            for (i = 0; i < slides.length; i++) {
                slides[i].style.display = "none";
            }
            for (i = 0; i < dots.length; i++) {
                dots[i].className = dots[i].className.replace(" active", "");
            }
            slides[slideIndex-1].style.display = "block";
            dots[slideIndex-1].className += " active";
        }

        // Function to open form page in new window/tab
        function openFormPage() {
            const formWindow = window.open("", "_blank"); // Opens a new blank tab
            formWindow.document.write(`
                <!DOCTYPE html>
                <html lang="en">
                <head>
                    <meta charset="UTF-8">
                    <meta name="viewport" content="width=device-width, initial-scale=1.0">
                    <meta name="description" content="Contact Form for O.P GUPTA CONSTRUCTIONS">
                    <title>Contact Us - O.P GUPTA CONSTRUCTIONS</title>
                    <style>
                        /* Body and General Styles */
                        body {
                            margin: 0;
                            font-family: 'Poppins', sans-serif;
                            font-size: 18px; /* Fixed size in pixels */
                            background-color: #f4f4f4;
                        }

                        /* Form Container Styles */
                        .form-container {
                            max-width: 600px;
                            margin: 50px auto;
                            padding: 20px;
                            background-color: white;
                            border-radius: 5px;
                            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
                        }

                        /* Input Field Styles */
                        .form-group {
                            margin-bottom: 15px;
                        }

                        label {
                            display: block;
                            margin-bottom: 5px;
                        }

                        input, textarea {
                            width: 100%;
                            padding: 10px;
                            border: 1px solid #ccc;
                            border-radius: 5px;
                            font-size: 16px;
                        }

                        /* Submit Button Styles */
                        .submit-btn {
                            background-color: #4CAF50; /* Green */
                            color: white;
                            border: none;
                            padding: 10px 15px;
                            text-align: center;
                            text-decoration: none;
                            display: inline-block;
                            font-size: 16px;
                            margin: 4px 2px;
                            cursor: pointer;
                            border-radius: 5px;
                            transition: background-color 0.3s;
                        }

                        .submit-btn:hover {
                            background-color: #45a049; /* Darker green */
                        }
                    </style>
                </head>
                <body>

                    <div class="form-container">
                        <h2>Contact Us</h2>
                        <form id="contactForm">
                            <div class="form-group">
                                <label for="name">Name:</label>
                                <input type="text" id="name" name="name" required>
                            </div>
                            <div class="form-group">
                                <label for="email">Email:</label>
                                <input type="email" id="email" name="email" required>
                            </div>
                            <div class="form-group">
                                <label for="contact">Contact Number:</label>
                                <input type="tel" id="contact" name="contact" required>
                            </div>
                            <div class="form-group">
                                <label for="address">Address:</label>
                                <textarea id="address" name="address" rows="4" required></textarea>
                            </div>
                            <button type="submit" class="submit-btn">Submit</button>
                        </form>
                    </div>

                </body>
                </html>
            `);
            formWindow.document.close(); // Close the document to finish rendering
        }
    </script>
</body>
</html>
