<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Software Developer Portfolio</title>
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;700&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Roboto', sans-serif;
            margin: 0;
            line-height: 1.6;
            color: #450e0e;
        }

        .hero {
            background: linear-gradient(135deg, #6a11cb, #2575fc);
            color: white;
            text-align: center;
            padding: 100px 20px;
        }

        .hero-title {
            font-size: 3rem;
            margin: 0;
        }

        .hero-subtitle {
            font-size: 1.5rem;
            margin-top: 10px;
        }

        .navbar {
            background: #333;
            color: white;
            padding: 10px 20px;
            display: flex;
            justify-content: center;
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        .navbar ul {
            list-style: none;
            margin: 0;
            padding: 0;
            display: flex;
        }

        .navbar li {
            margin: 0 15px;
        }

        .navbar a {
            color: white;
            text-decoration: none;
            font-weight: bold;
        }

        .section {
            padding: 50px 20px;
            text-align: center;
        }

        .section h2 {
            margin-bottom: 20px;
            font-size: 2rem;
            color: #2575fc;
        }

        .about p, .skills-list, .jobs-list, .contact-list {
            max-width: 800px;
            margin: 0 auto;
        }

        .skills-list, .jobs-list {
            list-style: none;
            padding: 0;
        }

        .skills-list li, .jobs-list li {
            margin: 10px 0;
            font-size: 1.1rem;
        }

        .projects .project {
            border: 1px solid #ddd;
            border-radius: 8px;
            padding: 20px;
            margin: 20px auto;
            max-width: 800px;
            text-align: left;
        }

        .projects .btn {
            display: inline-block;
            background: #2575fc;
            color: white;
            padding: 10px 15px;
            text-decoration: none;
            border-radius: 5px;
            margin-top: 10px;
        }

        .projects .btn:hover {
            background: #6a11cb;
        }

        .footer {
            background: #333;
            color: white;
            padding: 20px;
            text-align: center;
        }

        .footer h2 {
            margin-bottom: 10px;
        }

        .footer a {
            color: #6a11cb;
            text-decoration: none;
        }

        .footer a:hover {
            color: #2575fc;
        }

        .whatsapp-button {
            position: fixed;
            bottom: 20px;
            right: 20px;
            background-color: #25d366;
            color: white;
            padding: 15px;
            border-radius: 50%;
            text-align: center;
            font-size: 20px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            cursor: pointer;
            transition: transform 0.3s ease;
            text-decoration: none;
        }

        .whatsapp-button:hover {
            transform: scale(1.1);
        }
    </style>
</head>
<body>
    <header class="hero">
        <div class="container">
            <h1 class="hero-title">Hello, I'm OLADIPO AYOBAMI VICTOR</h1>
            <p class="hero-subtitle">Software Developer | Problem Solver | Tech Enthusiast</p>
        </div>
    </header>

    <nav class="navbar">
        <ul>
            <li><a href="#about">About Me</a></li>
            <li><a href="#skills">Skills</a></li>
            <li><a href="#jobs">Job Roles</a></li>
            <li><a href="#projects">Projects</a></li>
            <li><a href="#contact">Contact</a></li>
        </ul>
    </nav>

    <section id="about" class="section about">
        <div class="container">
            <h2>About Me</h2>
            <p>I am a passionate software developer with expertise in crafting clean and efficient code. I love solving challenging problems and building innovative solutions that make a difference.</p>
        </div>
    </section>

    <section id="skills" class="section skills">
        <div class="container">
            <h2>Technical Skills</h2>
            <ul class="skills-list">
                <li>Programming Languages: JavaScript, Python, Java</li>
                <li>Frameworks: React, Django, Spring Boot</li>
                <li>Tools: Git, Docker, Jenkins</li>
                <li>Database: PostgreSQL, MongoDB</li>
                <li>Cloud: AWS, Azure</li>
            </ul>
        </div>
    </section>

    <section id="jobs" class="section jobs">
        <div class="container">
            <h2>Job Roles</h2>
            <ul class="jobs-list">
                <li>Front-End Developer: Building visually stunning and responsive UIs.</li>
                <li>Back-End Developer: Developing scalable server-side logic and APIs.</li>
                <li>Full-Stack Developer: Bridging the gap between front-end and back-end systems.</li>
                <li>DevOps Engineer: Automating deployments and managing infrastructure.</li>
                <li>Software Architect: Designing and implementing high-level software frameworks.</li>
            </ul>
        </div>
    </section>

    <section id="projects" class="section projects">
        <div class="container">
            <h2>Projects</h2>
            <div class="project">
                <h3>Project Name</h3>
                <p>Description of the project, technologies used, and its impact.</p>
                <a href="#" class="btn">View Project</a>
            </div>
            <!-- Repeat for additional projects -->
        </div>
    </section>

    <footer id="contact" class="footer">
        <div class="container">
            <h2>Contact Me</h2>
            <p>Feel free to reach out for collaborations or just a friendly chat!</p>
            <ul class="contact-list">
                <li>Email: <a href="mailto:your.email@example.com">oladipoayobami08@gmail.com </a></li>
              </ul>
        </div>
    </footer>

    <a href="https://wa.me/2347071104445" target="_blank" class="whatsapp-button">📞</a>

    <script>
        // Smooth scrolling for navigation links
        document.querySelectorAll('.navbar a').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });

        // Floating button effect for projects section
        const projectButtons = document.querySelectorAll('.projects .btn');
        projectButtons.forEach(button => {
            button.addEventListener('mouseover', () => {
                button.style.transform = 'scale(1.1)';
                button.style.transition = 'transform 0.3s ease';
            });
            button.addEventListener('mouseout', () => {
                button.style.transform = 'scale(1)';
            });
        });

        // Sticky navbar shadow effect on scroll
        const navbar = document.querySelector('.navbar');
        window.addEventListener('scroll', () => {
            if (window.scrollY > 50) {
                navbar.style.boxShadow = '0 4px 6px rgba(0, 0, 0, 0.1)';
            } else {
                navbar.style.boxShadow = 'none';
            }
        });
    </script>
</body>
</html>

        
 
