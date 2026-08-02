---
layout: null
---


<html lang="en">
<head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Portfolio</title>
    <link rel="stylesheet" href="index.css">
    
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Varela+Round:wght@400&family=Inter:wght@300;400;500;600&display=swap" rel="stylesheet">
</head>
<body>
    <!-- Top Navigation Bar -->
    <nav class="navbar">
        <div class="navbar-container">
            <div class="navbar-left">
                <image src="/blog/images/m_icon.png" class="logo"> </image>
                <span class="name">atthew Hadkins</span>
            </div>
            <div class="navbar-right">
                <a href="#welcome" class="nav-link active">Welcome</a>
                <a href="#projects" class="nav-link">Projects</a>
            </div>
        </div>
    </nav>

    <!-- Welcome Section -->
    <section id="welcome" class="welcome-section">
        <div class="welcome-container">
            <div class="welcome-content">
                <h1>Hi, I'm Matt</h1>
                <p class="subtitle">Fourth Year Electrical and Electronics Engineering Student</p>
                <p class="description">
                    Welcome to my portfolio. I'm passionate about creating innovative solutions that bridge the gap 
                    between creative vision and technical execution. With experience across full-stack development, 
                    embedded systems, and collaborative team projects, I bring a unique perspective to every challenge. 
                    From designing applications that connect healthcare professionals to building systems that count commuters, 
                    each project has shaped my approach to thoughtful, user-centered design.
                </p>
            </div>
            <div class="welcome-image">
                
                <img src="/blog/images/welcome.jpg" alt="Creative workspace">
            </div>
        </div>
    </section>

    <!-- Projects Grid Section -->
    <section id="projects" class="projects-section">
        <div class="projects-container">
            <h2>Featured Projects</h2>
            
            

            <div class="projects-grid">
                {% for post in site.posts %}
                    <a href="/blog{{ post.url }}" class="project-card">
                        <div class="project-image">
                            <img src="/blog/images/thumbnails/{{ post.slug | remove: '.md' | remove: '.markdown' }}.jpg" alt="{{ post.title }}" onerror="this.src='https://images.unsplash.com/photo-1517694712202-14dd9538aa97?w=500&q=80'">
                            <div class="project-overlay">
                                <p>{{ post.excerpt | strip_html | truncatewords: 20 }}</p>
                            </div>
                        </div>
                        <div class="project-info">
                            <h3>{{ post.title }}</h3>
                            <p class="project-type">{{ post.date | date: "%B %Y" }}</p>
                        </div>
                    </a>
                {% endfor %}
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="footer">
        <div class="footer-content">
            <p>Get in touch</p>
            <div class="footer-links">
                <a href="mailto:mjhadkins42@gmail.com">Email</a>
                <span class="divider">•</span>
                <a href="tel:+61407293991">Phone</a>
            </div>
            <p class="copyright">© 2024 M. Hadkins. All rights reserved.</p>
        </div>
    </footer>

    <script>
        // Smooth scroll and active nav link
        document.querySelectorAll('.nav-link').forEach(link => {
            link.addEventListener('click', function(e) {
                e.preventDefault();
                const targetId = this.getAttribute('href').substring(1);
                const targetSection = document.getElementById(targetId);
                
                document.querySelectorAll('.nav-link').forEach(l => l.classList.remove('active'));
                this.classList.add('active');
                
                targetSection.scrollIntoView({ behavior: 'smooth' });
            });
        });

        // Update active nav link on scroll
        window.addEventListener('scroll', function() {
            const sections = document.querySelectorAll('section');
            const navLinks = document.querySelectorAll('.nav-link');
            
            let current = '';
            sections.forEach(section => {
                const sectionTop = section.offsetTop;
                if (pageYOffset >= sectionTop - 200) {
                    current = section.getAttribute('id');
                }
            });

            navLinks.forEach(link => {
                link.classList.remove('active');
                if (link.getAttribute('href').substring(1) === current) {
                    link.classList.add('active');
                }
            });
        });
    </script>
</body>
</html>