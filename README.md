<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Marc Revilloza - Personal Website</title>
    <style>
        body {
            font-family: 'Poppins', sans-serif;
            margin: 0;
            padding: 0;
            background-color: lightyellow; /* Light yellow background */
            scroll-behavior: smooth;
            overflow-x: hidden;
        }

        header {
            height: 60vh;
            display: flex;
            justify-content: center;
            align-items: center;
            position: relative;
            background: linear-gradient(135deg, #800000, #b22222); /* Simplified gradient */
            color: white;
            text-align: center;
            clip-path: polygon(0 0, 100% 0, 100% 80%, 0 100%);
            border-bottom: 5px solid #ffcc00; /* Yellow border */
            overflow: hidden;
        }

        header h1 {
            font-size: 4rem;
            text-transform: uppercase;
            letter-spacing: 2px;
            color: #e0e0e0; /* Softer white for text */
            text-shadow: 0 0 5px rgba(255, 255, 255, 0.7), 0 0 10px rgba(255, 255, 255, 0.5);
        }

        header p {
            font-size: 1.5rem;
            margin-top: 10px;
            background-color: rgba(128, 0, 0, 0.6); /* Semi-transparent maroon */
            color: #ffcc00;
            padding: 10px 20px;
            border-radius: 10px;
            display: inline-block;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.5);
        }

        nav {
            position: fixed;
            top: 20px;
            left: 20px;
            background: rgba(255, 255, 255, 0.8); /* Semi-transparent white */
            padding: 10px 20px;
            border-radius: 10px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            z-index: 10;
        }

        nav a {
            color: #800000;
            text-decoration: none;
            margin: 0 10px;
            font-size: 1.1rem;
            transition: color 0.3s, transform 0.3s;
        }

        nav a:hover {
            color: #ffcc00;
            transform: scale(1.1);
        }

        .container {
            max-width: 1200px;
            margin: auto;
            padding: 20px;
            padding-bottom: 80px; /* Add padding to account for floating icon */
        }

        section {
            padding: 60px 20px;
            background: white;
            margin: 20px 0;
            border-radius: 10px;
            box-shadow: 0 15px 25px rgba(0, 0, 0, 0.1);
            position: relative;
            overflow: hidden;
            transition: transform 0.5s ease-in-out, opacity 0.5s ease-in-out;
            opacity: 0;
            transform: translateY(50px);
        }

        section.visible {
            opacity: 1;
            transform: translateY(0);
        }

        section:hover {
            transform: scale(1.05);
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.3);
        }

        section::before {
            content: '';
            position: absolute;
            width: 120%;
            height: 200px;
            background: #ffcc00; /* Yellow decorative element */
            top: -80px;
            left: -50%;
            transform: rotate(-15deg);
            opacity: 0.2;
        }

        section h2 {
            margin-bottom: 20px;
            color: #800000; /* Maroon for titles */
        }

        footer {
            background-color: #800000; /* Maroon footer */
            color: white;
            text-align: center;
            padding: 20px;
            margin-top: 40px;
            position: relative;
            border-top: 2px solid #ffcc00; /* Yellow line separating footer from main content */
        }

        .footer-content {
            position: relative;
            display: inline-block;
            padding-bottom: 40px; /* Space for the icon */
        }

        .footer-text {
            margin: 0;
            font-size: 1rem;
            color: #ffcc00;
        }

        footer .fab {
            position: fixed; /* Changed to fixed for floating effect */
            bottom: 20px;
            right: 20px;
            width: 60px;
            height: 60px;
            background: #ffcc00;
            color: #800000;
            border-radius: 50%;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.3);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 24px;
            text-decoration: none;
            z-index: 10; /* Ensure it is above other content */
        }

        footer .fab:hover {
            background: #800000;
            color: #ffcc00;
            transform: scale(1.1);
            box-shadow: 0 6px 12px rgba(0, 0, 0, 0.4);
        }
    </style>
</head>
<body>

    <header>
        <h1>Marc Revilloza</h1>
        <p>1st-year Computer Science Student at UPHSD-Molino</p>
    </header>

    <nav>
        <a href="#about" onclick="toggleSection('about')">About Me</a>
        <a href="#specialization" onclick="toggleSection('specialization')">Specialization</a>
        <a href="#philosophy" onclick="toggleSection('philosophy')">Philosophy</a>
        <a href="#contact" onclick="toggleSection('contact')">Contact</a>
    </nav>

    <div class="container">
        <section id="about" class="section">
            <h2>About Me</h2>
            <p>Hello, I’m Marc Revilloza, a first-year Computer Science student at UPHSD-Molino. I initially completed my Senior High School at Perpetual Help System Dalta - Molino before transferring to UPHSD-Las Piñas to pursue Civil Engineering. Due to some reason, I had to pause my studies there. Now, I’ve returned to UPHSD-Molino to continue my academic journey in Computer Science. Although I’m still new and growing in this field, I’m committed to my progress and confident in my ability to succeed. I believe in embracing challenges as opportunities for growth and pursuing knowledge with determination.</p>
        </section>

        <section id="specialization" class="section">
            <h2>Specialization: Data Science</h2>
            <p>I aim to master Data Science, extracting valuable insights from data to solve real-world problems. My journey combines programming, machine learning, and statistics.</p>
        </section>

        <section id="philosophy" class="section">
            <h2>Philosophy</h2>
            <p>"The meaning of life is to find meaning in it." This guides my exploration of ideas, curiosity, and relentless drive to pursue growth and innovation.</p>
        </section>

        <section id="contact" class="section">
            <h2>Contact Information</h2>
            <p>Feel free to reach me at <a href="mailto:marcp.revilloza@gmail.com" class="btn">marcp.revilloza@gmail.com</a></p>
            <p>Connect with me on <a href="https://www.linkedin.com/in/marc-restan-revilloza-0a8b11328/" class="btn">LinkedIn</a></p>
        </section>
    </div>

    <footer>
        <div class="footer-content">
            <p class="footer-text">Made by GinEverywhere</p>
        </div>
        <a href="mailto:marcp.revilloza@gmail.com" class="fab">✉</a>
    </footer>

    <script>
        function toggleSection(id) {
            const sections = document.querySelectorAll('.section');
            sections.forEach(section => section.classList.remove('visible'));
            document.getElementById(id).classList.add('visible');
        }

        document.addEventListener('scroll', function() {
            var sections = document.querySelectorAll('.section');
            sections.forEach(function(section) {
                var rect = section.getBoundingClientRect();
                if (rect.top < window.innerHeight && rect.bottom > 0) {
                    section.classList.add('visible');
                } else {
                    section.classList.remove('visible');
                }
            });
        });

        // Initial load
        document.querySelectorAll('.section').forEach(section => section.classList.add('visible'));
    </script>
</body>
</html>
