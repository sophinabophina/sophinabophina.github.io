<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Creative Portfolio</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            /* Dark mode colors (default) */
            --nav-gradient-1: #1a365d;
            --nav-gradient-2: #2d3748;
            --home-stripe-1: #5d4e37;
            --home-plaid-1: rgba(139, 69, 19, 0.4);
            --home-plaid-2: rgba(26, 54, 93, 0.4);
            --home-plaid-3: rgba(114, 47, 55, 0.3);
            --home-plaid-4: rgba(74, 85, 104, 0.3);
            --projects-bg: #c1cfd9;
            --projects-plaid-1: rgba(108, 130, 148, 0.4);
            --projects-plaid-2: rgba(139, 157, 174, 0.4);
            --projects-plaid-3: rgba(124, 156, 181, 0.3);
            --projects-plaid-4: rgba(159, 176, 191, 0.3);
            --border-color-1: #8B4513;
            --border-color-2: #1a365d;
            --border-color-3: #722f37;
            --heading-color: #1a365d;
            --experience-stripe-1: #4f3c2b;
            --experience-stripe-2: #ccb19d;
            --experience-stripe-3: #4f3c2b;
            --experience-stripe-4: #ccb19d;
            --experience-stripe-5: #4f3c2b;
            --experience-heading: #722f37;
            --experience-role: #1a365d;
            --socials-bg: #d4a574;
            --socials-pattern-1: rgba(139, 69, 19, 0.4);
            --socials-pattern-2: rgba(26, 54, 93, 0.4);
            --socials-plaid-3: rgba(114, 47, 55, 0.3);
            --socials-plaid-4: rgba(74, 85, 104, 0.3);
            --contact-gradient-1: #8b7355;
            --contact-gradient-2: #a88b6f;
            --contact-pattern-1: rgba(114, 47, 55, 0.2);
            --contact-pattern-2: rgba(26, 54, 93, 0.2);
            --form-border: #722f37;
            --label-color: #1a365d;
            --input-focus: #722f37;
            --button-gradient-1: #1a365d;
            --button-gradient-2: #722f37;
            --button-shadow: rgba(26, 54, 93, 0.4);
            --button-shadow-hover: rgba(26, 54, 93, 0.6);
        }

        body.light-mode {
            /* Light mode colors - Cool grey tones */
            --nav-gradient-1: #7c9cb5;
            --nav-gradient-2: #8fa8bb;
            --home-stripe-1: #b8c5d6;
            --home-plaid-1: rgba(108, 130, 148, 0.4);
            --home-plaid-2: rgba(139, 157, 174, 0.4);
            --home-plaid-3: rgba(124, 156, 181, 0.3);
            --home-plaid-4: rgba(159, 176, 191, 0.3);
            --projects-bg: #5d4e37;
            --projects-plaid-1: rgba(139, 69, 19, 0.4);
            --projects-plaid-2: rgba(26, 54, 93, 0.4);
            --projects-plaid-3: rgba(114, 47, 55, 0.3);
            --projects-plaid-4: rgba(74, 85, 104, 0.3);
            --border-color-1: #6c8294;
            --border-color-2: #8b9dae;
            --border-color-3: #7c9cb5;
            --heading-color: #5a7184;
            --experience-stripe-1: #a4b8c8;
            --experience-stripe-2: #8b9dae;
            --experience-stripe-3: #7c9cb5;
            --experience-stripe-4: #b8c5d6;
            --experience-stripe-5: #9fb0bf;
            --experience-heading: #5a7184;
            --experience-role: #6c8294;
            --socials-bg: #d4dde6;
            --socials-pattern-1: rgba(108, 130, 148, 0.3);
            --socials-pattern-2: rgba(139, 157, 174, 0.3);
            --socials-plaid-3: rgba(124, 156, 181, 0.2);
            --socials-plaid-4: rgba(159, 176, 191, 0.2);
            --contact-gradient-1: #bcc9d6;
            --contact-gradient-2: #d4dde6;
            --contact-pattern-1: rgba(124, 156, 181, 0.2);
            --contact-pattern-2: rgba(139, 157, 174, 0.2);
            --form-border: #7c9cb5;
            --label-color: #5a7184;
            --input-focus: #6c8294;
            --button-gradient-1: #7c9cb5;
            --button-gradient-2: #8b9dae;
            --button-shadow: rgba(124, 156, 181, 0.4);
            --button-shadow-hover: rgba(124, 156, 181, 0.6);
        }

        body {
            font-family: 'Georgia', serif;
            color: #2d3748;
            overflow-x: hidden;
        }

        /* Navigation */
        nav {
            position: fixed;
            top: 0;
            width: 100%;
            background: linear-gradient(135deg, var(--nav-gradient-1) 0%, var(--nav-gradient-2) 100%);
            padding: 1.5rem 2rem;
            z-index: 1000;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }

        nav ul {
            list-style: none;
            display: flex;
            justify-content: center;
            gap: 2.5rem;
            flex-wrap: wrap;
        }

        nav a {
            color: white;
            text-decoration: none;
            font-size: 1.1rem;
            font-weight: 600;
            transition: transform 0.3s ease;
            display: inline-block;
        }

        nav a:hover {
            transform: translateY(-3px);
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
        }

        /* Section Base Styles */
        section {
            min-height: 100vh;
            padding: 6rem 2rem 4rem;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            position: relative;
        }

        h1 {
            font-size: 4rem;
            margin-bottom: 1rem;
            text-align: center;
        }

        h2 {
            font-size: 3rem;
            margin-bottom: 2rem;
            text-align: center;
        }

        /* Home Section - Plaid Pattern */
        #home {
            background-color: var(--home-stripe-1);
            background-image: 
                repeating-linear-gradient(90deg, transparent, transparent 35px, var(--home-plaid-1) 35px, var(--home-plaid-1) 70px),
                repeating-linear-gradient(0deg, transparent, transparent 35px, var(--home-plaid-2) 35px, var(--home-plaid-2) 70px),
                repeating-linear-gradient(90deg, transparent, transparent 10px, var(--home-plaid-3) 10px, var(--home-plaid-3) 20px),
                repeating-linear-gradient(0deg, transparent, transparent 10px, var(--home-plaid-4) 10px, var(--home-plaid-4) 20px);
            color: white;
            text-shadow: 3px 3px 6px rgba(0, 0, 0, 0.3);
        }

        #home::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: rgba(255, 255, 255, 0.1);
        }

        .home-content {
            position: relative;
            z-index: 1;
            text-align: center;
            background: white;
            padding: 3rem 4rem;
            border-radius: 20px;
            box-shadow: 0 15px 50px rgba(0, 0, 0, 0.3);
            max-width: 800px;
        }

        .home-content h1 {
            color: #2d3748;
            text-shadow: none;
        }

        .home-content .tagline {
            color: #4a5568;
            text-shadow: none;
        }

        .tagline {
            font-size: 1.5rem;
            margin-top: 1rem;
            font-style: italic;
        }

        .theme-toggle {
            position: fixed;
            top: 1.5rem;
            right: 2rem;
            z-index: 1001;
            margin-top: 0;
            background: white;
            color: #2d3748;
            border: 3px solid var(--button-gradient-1);
            padding: 0.75rem;
            border-radius: 50%;
            font-size: 1.5rem;
            width: 50px;
            height: 50px;
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.2);
            transition: all 0.3s ease;
        }

        .theme-toggle:hover {
            transform: translateY(-2px) scale(1.05);
            box-shadow: 0 6px 16px rgba(0, 0, 0, 0.3);
        }

        /* Projects Section - Checkerboard Pattern */
        #projects {
            background-color: var(--projects-bg);
            background-image: 
                repeating-linear-gradient(45deg, transparent, transparent 35px, var(--projects-plaid-1) 35px, var(--projects-plaid-1) 70px),
                repeating-linear-gradient(-45deg, transparent, transparent 35px, var(--projects-plaid-2) 35px, var(--projects-plaid-2) 70px);
        }

        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            max-width: 1200px;
            width: 100%;
        }

        .project-card {
            background: white;
            padding: 2rem;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.15);
            transition: transform 0.3s ease;
            border: 4px solid var(--border-color-1);
        }

        .project-card:nth-child(2) {
            border-color: var(--border-color-2);
        }

        .project-card:nth-child(3) {
            border-color: var(--border-color-3);
        }

        .project-card:hover {
            transform: translateY(-10px);
        }

        .project-card h3 {
            color: var(--heading-color);
            margin-bottom: 1rem;
            font-size: 1.8rem;
        }

        /* Experience Section - Vertical Stripes */
        #experience {
            background: linear-gradient(90deg, 
                var(--experience-stripe-1) 0%, var(--experience-stripe-1) 20%, 
                var(--experience-stripe-2) 20%, var(--experience-stripe-2) 40%, 
                var(--experience-stripe-3) 40%, var(--experience-stripe-3) 60%, 
                var(--experience-stripe-4) 60%, var(--experience-stripe-4) 80%,
                var(--experience-stripe-5) 80%, var(--experience-stripe-5) 100%);
            background-size: 200px 100%;
        }

        .experience-container {
            max-width: 900px;
            width: 100%;
        }

        .experience-item {
            background: white;
            padding: 2.5rem;
            margin-bottom: 2rem;
            border-radius: 15px;
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.15);
            border-left: 8px solid var(--border-color-2);
        }

        .experience-item:nth-child(even) {
            border-left-color: var(--border-color-3);
        }

        .experience-item h3 {
            color: var(--experience-heading);
            font-size: 1.8rem;
            margin-bottom: 0.5rem;
        }

        .experience-item .role {
            color: var(--experience-role);
            font-size: 1.3rem;
            margin-bottom: 0.5rem;
            font-style: italic;
        }

        .experience-item .date {
            color: #718096;
            margin-bottom: 1rem;
        }

        /* Socials Section - Plaid Pattern */
        #socials {
            background-color: var(--socials-bg);
            background-image: 
                repeating-linear-gradient(90deg, transparent, transparent 35px, var(--socials-pattern-1) 35px, var(--socials-pattern-1) 70px),
                repeating-linear-gradient(0deg, transparent, transparent 35px, var(--socials-pattern-2) 35px, var(--socials-pattern-2) 70px),
                repeating-linear-gradient(90deg, transparent, transparent 10px, var(--socials-plaid-3) 10px, var(--socials-plaid-3) 20px),
                repeating-linear-gradient(0deg, transparent, transparent 10px, var(--socials-plaid-4) 10px, var(--socials-plaid-4) 20px);
        }

        .socials-grid {
            display: flex;
            gap: 2rem;
            flex-wrap: wrap;
            justify-content: center;
        }

        .social-link {
            background: white;
            padding: 2rem 3rem;
            border-radius: 20px;
            text-decoration: none;
            color: #2d3748;
            font-size: 1.5rem;
            font-weight: 600;
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.2);
            transition: all 0.3s ease;
            border: 4px solid transparent;
        }

        .social-link:nth-child(1) { border-color: var(--border-color-2); }
        .social-link:nth-child(2) { border-color: var(--border-color-1); }
        .social-link:nth-child(3) { border-color: var(--border-color-3); }
        .social-link:nth-child(4) { border-color: var(--experience-stripe-4); }

        .social-link:hover {
            transform: scale(1.1) rotate(-3deg);
            box-shadow: 0 12px 30px rgba(0, 0, 0, 0.3);
        }

        /* Contact Section - Mixed Patterns */
        #contact {
            background: linear-gradient(135deg, var(--contact-gradient-1) 0%, var(--contact-gradient-2) 100%);
            background-image: 
                repeating-linear-gradient(45deg, transparent, transparent 20px, var(--contact-pattern-1) 20px, var(--contact-pattern-1) 40px),
                repeating-linear-gradient(-45deg, transparent, transparent 20px, var(--contact-pattern-2) 20px, var(--contact-pattern-2) 40px),
                linear-gradient(135deg, var(--contact-gradient-1) 0%, var(--contact-gradient-2) 100%);
        }

        .contact-form {
            background: white;
            padding: 3rem;
            border-radius: 20px;
            box-shadow: 0 15px 40px rgba(0, 0, 0, 0.2);
            max-width: 600px;
            width: 100%;
            border: 5px solid var(--form-border);
        }

        .form-group {
            margin-bottom: 1.5rem;
        }

        label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 600;
            color: var(--label-color);
            font-size: 1.1rem;
        }

        input, textarea {
            width: 100%;
            padding: 1rem;
            border: 3px solid #e2e8f0;
            border-radius: 10px;
            font-size: 1rem;
            font-family: 'Georgia', serif;
            transition: border-color 0.3s ease;
        }

        input:focus, textarea:focus {
            outline: none;
            border-color: var(--input-focus);
        }

        textarea {
            resize: vertical;
            min-height: 150px;
        }

        button {
            background: linear-gradient(135deg, var(--button-gradient-1) 0%, var(--button-gradient-2) 100%);
            color: white;
            padding: 1rem 3rem;
            border: none;
            border-radius: 50px;
            font-size: 1.2rem;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            box-shadow: 0 5px 15px var(--button-shadow);
            width: 100%;
        }

        button:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 25px var(--button-shadow-hover);
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            h1 {
                font-size: 2.5rem;
            }

            h2 {
                font-size: 2rem;
            }

            nav ul {
                gap: 1rem;
            }

            .tagline {
                font-size: 1.2rem;
            }
        }
    </style>
</head>
<body>
    <!-- Theme Toggle Button -->
    <button class="theme-toggle" onclick="toggleTheme()" aria-label="Toggle theme">
        <span id="theme-icon">🌙</span>
    </button>

    <!-- Navigation -->
    <nav>
        <ul>
            <li><a href="#home">Home</a></li>
            <li><a href="#projects">Projects</a></li>
            <li><a href="#experience">Experience</a></li>
            <li><a href="#socials">Socials</a></li>
            <li><a href="#contact">Contact</a></li>
        </ul>
    </nav>

    <!-- Home Section -->
    <section id="home">
        <div class="home-content">
            <h1>Welcome to My World</h1>
            <p class="tagline">Creating beautiful things with purpose and passion</p>
        </div>
    </section>

    <!-- Projects Section -->
    <section id="projects">
        <h2>My Projects</h2>
        <div class="projects-grid">
            <div class="project-card">
                <h3>Project One</h3>
                <p>An innovative solution that combines creativity with functionality. Built with modern technologies to deliver an exceptional user experience.</p>
            </div>
            <div class="project-card">
                <h3>Project Two</h3>
                <p>A collaborative platform that brings people together. Features include real-time updates, intuitive design, and seamless integration.</p>
            </div>
            <div class="project-card">
                <h3>Project Three</h3>
                <p>A passion project exploring the intersection of art and technology. Showcases unique design patterns and interactive elements.</p>
            </div>
        </div>
    </section>

    <!-- Experience Section -->
    <section id="experience">
        <h2>Experience</h2>
        <div class="experience-container">
            <div class="experience-item">
                <h3>Senior Creative Developer</h3>
                <div class="role">Leading innovative digital experiences</div>
                <div class="date">2022 - Present</div>
                <p>Designing and developing cutting-edge web applications with a focus on user experience and visual excellence. Mentoring junior developers and driving creative solutions.</p>
            </div>
            <div class="experience-item">
                <h3>Full Stack Developer</h3>
                <div class="role">Building robust applications</div>
                <div class="date">2020 - 2022</div>
                <p>Developed full-stack applications using modern frameworks and technologies. Collaborated with cross-functional teams to deliver high-quality products.</p>
            </div>
            <div class="experience-item">
                <h3>Junior Developer</h3>
                <div class="role">Starting the journey</div>
                <div class="date">2018 - 2020</div>
                <p>Learned the fundamentals of web development and contributed to various projects. Gained experience in front-end and back-end technologies.</p>
            </div>
        </div>
    </section>

    <!-- Socials Section -->
    <section id="socials">
        <h2>Connect With Me</h2>
        <div class="socials-grid">
            <a href="#" class="social-link">LinkedIn</a>
            <a href="#" class="social-link">GitHub</a>
            <a href="#" class="social-link">Twitter</a>
            <a href="#" class="social-link">Instagram</a>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact">
        <h2>Get In Touch</h2>
        <form class="contact-form" onsubmit="event.preventDefault(); alert('Thanks for reaching out! This is a demo form.');">
            <div class="form-group">
                <label for="name">Name</label>
                <input type="text" id="name" name="name" required>
            </div>
            <div class="form-group">
                <label for="email">Email</label>
                <input type="email" id="email" name="email" required>
            </div>
            <div class="form-group">
                <label for="message">Message</label>
                <textarea id="message" name="message" required></textarea>
            </div>
            <button type="submit">Send Message</button>
        </form>
    </section>

    <script>
        // Smooth scrolling for navigation links
        document.querySelectorAll('nav a').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                target.scrollIntoView({
                    behavior: 'smooth',
                    block: 'start'
                });
            });
        });

        // Theme toggle functionality
        function toggleTheme() {
            document.body.classList.toggle('light-mode');
            
            // Update icon
            const icon = document.getElementById('theme-icon');
            if (document.body.classList.contains('light-mode')) {
                icon.textContent = '☀️';
                localStorage.setItem('theme', 'light');
            } else {
                icon.textContent = '🌙';
                localStorage.setItem('theme', 'dark');
            }
        }

        // Load saved theme preference on page load
        window.addEventListener('DOMContentLoaded', () => {
            const savedTheme = localStorage.getItem('theme');
            const icon = document.getElementById('theme-icon');
            if (savedTheme === 'light') {
                document.body.classList.add('light-mode');
                icon.textContent = '☀️';
            } else {
                icon.textContent = '🌙';
            }
        });
    </script>
</body>
</html>
