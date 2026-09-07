<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Dickens ihaji | Portfolio</title>

    <meta name="description" content="Personal portfolio website of Your Name.">
    <meta name="author" content="Your Name">

    <style>
        /* =========================
           RESET & GLOBAL STYLES
        ========================== */

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: Arial, Helvetica, sans-serif;
            line-height: 1.6;
            background: #0f172a;
            color: #f8fafc;
            transition: 0.3s ease;
        }

        a {
            text-decoration: none;
            color: inherit;
        }

        img {
            max-width: 100%;
            display: block;
        }

        .container {
            width: 90%;
            max-width: 1100px;
            margin: auto;
        }

        section {
            padding: 90px 0;
        }

        .section-title {
            text-align: center;
            font-size: 2.2rem;
            margin-bottom: 50px;
        }

        .section-title span {
            color: #38bdf8;
        }

        /* =========================
           NAVBAR
        ========================== */

        header {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            z-index: 1000;
            background: rgba(15, 23, 42, 0.9);
            backdrop-filter: blur(10px);
        }

        nav {
            height: 70px;
            display: flex;
            align-items: center;
            justify-content: space-between;
        }

        .logo {
            font-size: 1.5rem;
            font-weight: bold;
            color: #38bdf8;
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 30px;
        }

        .nav-links a {
            transition: 0.3s;
        }

        .nav-links a:hover {
            color: #38bdf8;
        }

        .menu-btn {
            display: none;
            font-size: 1.8rem;
            cursor: pointer;
        }

        /* =========================
           HERO
        ========================== */

        #home {
            min-height: 100vh;
            display: flex;
            align-items: center;
            padding-top: 100px;
        }

        .hero {
            display: grid;
            grid-template-columns: 1.5fr 1fr;
            align-items: center;
            gap: 50px;
        }

        .hero-text h1 {
            font-size: 3.5rem;
            line-height: 1.2;
            margin-bottom: 20px;
        }

        .hero-text h1 span {
            color: #38bdf8;
        }

        .hero-text h2 {
            font-size: 1.5rem;
            color: #94a3b8;
            margin-bottom: 20px;
        }

        .hero-text p {
            color: #cbd5e1;
            max-width: 600px;
            margin-bottom: 30px;
        }

        .buttons {
            display: flex;
            gap: 15px;
            flex-wrap: wrap;
        }

        .btn {
            display: inline-block;
            padding: 12px 25px;
            border-radius: 8px;
            font-weight: bold;
            transition: 0.3s;
        }

        .btn-primary {
            background: #38bdf8;
            color: #0f172a;
        }

        .btn-primary:hover {
            transform: translateY(-3px);
            background: #7dd3fc;
        }

        .btn-outline {
            border: 2px solid #38bdf8;
            color: #38bdf8;
        }

        .btn-outline:hover {
            background: #38bdf8;
            color: #0f172a;
        }

        .hero-image {
            display: flex;
            justify-content: center;
        }

        .profile-circle {
            width: 280px;
            height: 280px;
            border-radius: 50%;
            background: linear-gradient(135deg, #38bdf8, #6366f1);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 5rem;
            font-weight: bold;
            box-shadow: 0 0 60px rgba(56, 189, 248, 0.25);
        }

        /* =========================
           ABOUT
        ========================== */

        #about {
            background: #111827;
        }

        .about-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 50px;
            align-items: center;
        }

        .about-content h3 {
            font-size: 1.8rem;
            margin-bottom: 15px;
        }

        .about-content p {
            color: #cbd5e1;
            margin-bottom: 15px;
        }

        .about-info {
            display: grid;
            gap: 15px;
        }

        .info-card {
            background: #1e293b;
            padding: 20px;
            border-radius: 10px;
            border-left: 4px solid #38bdf8;
        }

        /* =========================
           SKILLS
        ========================== */

        .skills-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 25px;
        }

        .skill-card {
            background: #1e293b;
            padding: 30px;
            text-align: center;
            border-radius: 12px;
            transition: 0.3s;
        }

        .skill-card:hover {
            transform: translateY(-8px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.2);
        }

        .skill-card .icon {
            font-size: 2.5rem;
            margin-bottom: 15px;
        }

        .skill-card h3 {
            margin-bottom: 10px;
        }

        .skill-card p {
            color: #94a3b8;
        }

        /* =========================
           PROJECTS
        ========================== */

        #projects {
            background: #111827;
        }

        .projects-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 25px;
        }

        .project-card {
            background: #1e293b;
            border-radius: 12px;
            overflow: hidden;
            transition: 0.3s;
        }

        .project-card:hover {
            transform: translateY(-8px);
        }

        .project-image {
            height: 180px;
            background: linear-gradient(135deg, #38bdf8, #6366f1);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 3rem;
        }

        .project-content {
            padding: 25px;
        }

        .project-content h3 {
            margin-bottom: 10px;
        }

        .project-content p {
            color: #94a3b8;
            margin-bottom: 20px;
        }

        .project-link {
            color: #38bdf8;
            font-weight: bold;
        }

        /* =========================
           CONTACT
        ========================== */

        .contact-container {
            max-width: 700px;
            margin: auto;
        }

        .contact-form {
            display: grid;
            gap: 20px;
        }

        .contact-form input,
        .contact-form textarea {
            width: 100%;
            padding: 15px;
            border: 1px solid #334155;
            border-radius: 8px;
            background: #1e293b;
            color: white;
            font-size: 1rem;
            outline: none;
        }

        .contact-form input:focus,
        .contact-form textarea:focus {
            border-color: #38bdf8;
        }

        .contact-form textarea {
            min-height: 160px;
            resize: vertical;
        }

        /* =========================
           FOOTER
        ========================== */

        footer {
            background: #020617;
            text-align: center;
            padding: 30px 0;
            color: #94a3b8;
        }

        .social-links {
            margin-bottom: 15px;
            display: flex;
            justify-content: center;
            gap: 20px;
        }

        .social-links a {
            color: #38bdf8;
        }

        /* =========================
           RESPONSIVE DESIGN
        ========================== */

        @media (max-width: 768px) {

            .menu-btn {
                display: block;
            }

            .nav-links {
                position: absolute;
                top: 70px;
                left: 0;
                width: 100%;
                background: #0f172a;
                flex-direction: column;
                align-items: center;
                padding: 25px 0;
                display: none;
            }

            .nav-links.active {
                display: flex;
            }

            .hero {
                grid-template-columns: 1fr;
                text-align: center;
            }

            .hero-text h1 {
                font-size: 2.5rem;
            }

            .buttons {
                justify-content: center;
            }

            .about-content {
                grid-template-columns: 1fr;
            }

            .skills-grid {
                grid-template-columns: 1fr;
            }

            .projects-grid {
                grid-template-columns: 1fr;
            }

            .profile-circle {
                width: 220px;
                height: 220px;
                font-size: 4rem;
            }
        }
    </style>
</head>

<body>

    <!-- =========================
         NAVIGATION
    ========================== -->

    <header>
        <div class="container">
            <nav>

                <a href="#home" class="logo">
                    Dickens ihaji
                </a>

                <div class="menu-btn" onclick="toggleMenu()">
                    ☰
                </div>

                <ul class="nav-links" id="navLinks">
                    <li><a href="#home">Home</a></li>
                    <li><a href="#about">About</a></li>
                    <li><a href="#skills">Skills</a></li>
                    <li><a href="#projects">Projects</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>

            </nav>
        </div>
    </header>


    <!-- =========================
         HERO SECTION
    ========================== -->

    <section id="home">

        <div class="container">

            <div class="hero">

                <div class="hero-text">

                    <h2>Hello, I'm</h2>

                    <h1>
                        <span>Dickens ihaji</span>
                    </h1>

                    <h2>
                        The Quantity Surveyor
                    </h2>

                    <p>
                        I create modern, responsive and user-friendly
                        websites and digital experiences. Welcome to my
                        personal portfolio.
                    </p>

                    <div class="buttons">
                        <a href="#projects" class="btn btn-primary">
                            View My Work
                        </a>

                        <a href="#contact" class="btn btn-outline">
                            Contact Me
                        </a>
                    </div>

                </div>


                <div class="hero-image">

                
                    <div class="profile.jpg.png">
                        YN
                    </div>

                </div>

            </div>

        </div>

    </section>


    <!-- =========================
         ABOUT SECTION
    ========================== -->

    <section id="about">

        <div class="container">

            <h2 class="section-title">
                About <span>Me</span>
            </h2>

            <div class="about-content">

                <div>

                    <h3>
                        Turning ideas into digital experiences
                    </h3>

                    <p>
                        I'm a passionate developer who enjoys building
                        websites and applications that are fast,
                        accessible and easy to use.
                    </p>

                    <p>
                        I love learning new technologies, solving
                        problems and turning creative ideas into
                        real-world projects.
                    </p>

                </div>

                <div class="about-info">

                    <div class="info-card">
                        <strong>Name:</strong>
                        Dickens ihaji
                    </div>

                    <div class="info-card">
                        <strong>Email:</strong>
                        your@email.com
                    </div>

                    <div class="info-card">
                        <strong>Location:</strong>
                        Nairobi, Kenya
                    </div>

                    <div class="info-card">
                        <strong>Available for:</strong>
                        Freelance & Projects
                    </div>

                </div>

            </div>

        </div>

    </section>


    <!-- =========================
         SKILLS SECTION
    ========================== -->

    <section id="skills">

        <div class="container">

            <h2 class="section-title">
                My <span>Skills</span>
            </h2>

            <div class="skills-grid">

                <div class="skill-card">
                    <div class="icon">🌐</div>
                    <h3>SURVEYING</h3>
                    <p>
                        Building clean and semantic web pages.
                    </p>
                </div>

                <div class="skill-card">
                    <div class="icon">🎨</div>
                    <h3>CSS</h3>
                    <p>
                        Creating responsive and attractive interfaces.
                    </p>
                </div>

                <div class="skill-card">
                    <div class="icon">⚡</div>
                    <h3>JavaScript</h3>
                    <p>
                        Adding interactive and dynamic functionality.
                    </p>
                </div>

                <div class="skill-card">
                    <div class="icon">💻</div>
                    <h3>Web Development</h3>
                    <p>
                        Developing complete modern websites.
                    </p>
                </div>

                <div class="skill-card">
                    <div class="icon">📱</div>
                    <h3>Responsive Design</h3>
                    <p>
                        Websites that work across phones, tablets and PCs.
                    </p>
                </div>

                <div class="skill-card">
                    <div class="icon">🚀</div>
                    <h3>Problem Solving</h3>
                    <p>
                        Finding practical solutions to technical problems.
                    </p>
                </div>

            </div>

        </div>

    </section>


    <!-- =========================
         PROJECTS SECTION
    ========================== -->

    <section id="projects">

        <div class="container">

            <h2 class="section-title">
                My <span>Projects</span>
            </h2>

            <div class="projects-grid">

                <!-- Project 1 -->
                <div class="project-card">

                    <div class="project-image">
                        💻
                    </div>

                    <div class="project-content">

                        <h3>Portfolio Website</h3>

                        <p>
                            A responsive personal portfolio website
                            built using HTML, CSS and JavaScript.
                        </p>

                        <a href="#" class="project-link">
                            View Project →
                        </a>

                    </div>

                </div>


                <!-- Project 2 -->
                <div class="project-card">

                    <div class="project-image">
                        🛒
                    </div>

                    <div class="project-content">

                        <h3>Online Store</h3>

                        <p>
                            A modern e-commerce interface designed
                            for displaying products online.
                        </p>

                        <a href="#" class="project-link">
                            View Project →
                        </a>

                    </div>

                </div>


                <!-- Project 3 -->
                <div class="project-card">

                    <div class="project-image">
                        📊
                    </div>

                    <div class="project-content">

                        <h3>Dashboard</h3>

                        <p>
                            A clean dashboard interface for displaying
                            information and statistics.
                        </p>

                        <a href="#" class="project-link">
                            View Project →
                        </a>

                    </div>

                </div>

            </div>

        </div>

    </section>


    <!-- =========================
         CONTACT SECTION
    ========================== -->

    <section id="contact">

        <div class="container">

            <h2 class="section-title">
                Contact <span>Me</span>
            </h2>

            <div class="contact-container">

                <form class="contact-form"
                      onsubmit="sendMessage(event)">

                    <input
                        type="text"
                        placeholder="Your Name"
                        required
                    >

                    <input
                        type="email"
                        placeholder="Your Email"
                        required
                    >

                    <textarea
                        placeholder="Your Message"
                        required
                    ></textarea>

                    <button
                        type="submit"
                        class="btn btn-primary"
                    >
                        Send Message
                    </button>

                </form>

            </div>

        </div>

    </section>


    <!-- =========================
         FOOTER
    ========================== -->

    <footer>

        <div class="container">

            <div class="social-links">

                <a href="#" target="_blank">
                    GitHub
                </a>

                <a href="#" target="_blank">
                    LinkedIn
                </a>

                <a href="#" target="_blank">
                    Instagram
                </a>

            </div>

            <p>
                © 2026 Dickens ihaji. All Rights Reserved.
            </p>

        </div>

    </footer>


    <!-- =========================
         JAVASCRIPT
    ========================== -->

    <script>

        // Mobile navigation
        function toggleMenu() {

            const navLinks =
                document.getElementById("navLinks");

            navLinks.classList.toggle("active");

        }


        // Close mobile menu when a link is clicked
        document.querySelectorAll(".nav-links a")
            .forEach(link => {

                link.addEventListener("click", () => {

                    document
                        .getElementById("navLinks")
                        .classList.remove("active");

                });

            });


        // Contact form
        function sendMessage(event) {

            event.preventDefault();

            alert(
                "Thank you! Your message has been received."
            );

            event.target.reset();

        }

    </script>

</body>
</html>
