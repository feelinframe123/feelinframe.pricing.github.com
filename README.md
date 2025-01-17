# feelinframe.pricing.github.com
Paket Foto Outdoor Wisuda Feel.Inframe Photography
/* README.md */
# Feel.Inframe Photography Website

A responsive photography portfolio website built with HTML and CSS.

## Features
- Responsive design
- Modern UI/UX
- Service showcase
- Package pricing
- Contact information
- Special promo section

## Setup
1. Clone the repository
2. Open index.html in your browser
3. All styles are in styles.css

/* index.html */
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Feel.Inframe Photography - Professional Photography Services">
    <meta name="keywords" content="photography, wedding, graduation, portrait, Indonesia">
    <title>Feel.Inframe Photography</title>
    <!-- Font Awesome with Integrity Hash -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css" 
          integrity="sha512-iecdLmaskl7CVkqkXNQ/ZH/XLlvWZOJyj7Yy7tcenmpD1ypASozpmT/E0iPtmFIB46ZmdtAc9eNBvH0H/ZpiBw==" 
          crossorigin="anonymous" referrerpolicy="no-referrer" />
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600;700&display=swap" rel="stylesheet">
    <!-- Custom CSS -->
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <!-- Navigation with proper ARIA labels -->
    <nav class="navbar" role="navigation" aria-label="Main navigation">
        <div class="nav-container">
            <div class="logo" role="banner">Feel.Inframe</div>
            <button class="mobile-menu-button" aria-label="Toggle menu" aria-expanded="false">
                <i class="fas fa-bars"></i>
            </button>
            <ul class="nav-links">
                <li><a href="#home" aria-current="page">Home</a></li>
                <li><a href="#services">Services</a></li>
                <li><a href="#packages">Packages</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </div>
    </nav>

    <!-- Hero Section with proper heading hierarchy -->
    <section id="home" class="hero" role="region" aria-labelledby="hero-title">
        <div class="hero-content">
            <div class="promo-badge">
                <span>✨ Special Promo</span>
            </div>
            <h1 id="hero-title">FEEL.INFRAME PHOTOGRAPHY</h1>
            <p>Abadikan momen spesialmu dengan sentuhan profesional dan estetik yang memukau</p>
            <a href="#packages" class="cta-button">Explore Packages</a>
        </div>
    </section>

    <!-- Features Section with semantic HTML -->
    <section id="services" class="features" role="region" aria-labelledby="services-title">
        <div class="container">
            <h2 id="services-title" class="section-title">Our Services</h2>
            <div class="features-grid">
                <!-- Feature cards with proper ARIA -->
                <article class="feature-card" role="article">
                    <i class="fas fa-camera" aria-hidden="true"></i>
                    <h3>Premium Quality</h3>
                    <p>Hasil foto berkualitas tinggi dengan editing profesional</p>
                </article>
                <!-- [Additional feature cards...] -->
            </div>
        </div>
    </section>

    <!-- Packages Section with proper pricing structure -->
    <section id="packages" class="packages" role="region" aria-labelledby="packages-title">
        <div class="container">
            <h2 id="packages-title" class="section-title">Our Packages</h2>
            <div class="packages-grid">
                <!-- Package cards with proper ARIA -->
                <article class="package-card" role="article">
                    <h3>PAKET FOTO BASIC</h3>
                    <div class="price">Rp 350K<span>/jam</span></div>
                    <ul class="benefits" role="list">
                        <li>1 jam sesi foto</li>
                        <!-- [Additional benefits...] -->
                    </ul>
                    <a href="https://wa.me/6282345695620" 
                       class="book-button" 
                       rel="noopener noreferrer" 
                       target="_blank">Book Now</a>
                </article>
                <!-- [Additional package cards...] -->
            </div>
        </div>
    </section>

    <!-- Contact Section with secure links -->
    <section id="contact" class="contact" role="region" aria-labelledby="contact-title">
        <div class="container">
            <h2 id="contact-title" class="section-title">Contact Us</h2>
            <div class="contact-links">
                <a href="https://instagram.com/feel.inframe" 
                   class="social-link" 
                   rel="noopener noreferrer" 
                   target="_blank">
                    <i class="fab fa-instagram" aria-hidden="true"></i>
                    <span>@feel.inframe</span>
                </a>
                <a href="https://wa.me/6282345695620" 
                   class="social-link" 
                   rel="noopener noreferrer" 
                   target="_blank">
                    <i class="fab fa-whatsapp" aria-hidden="true"></i>
                    <span>+62-823-4569-5620</span>
                </a>
            </div>
        </div>
    </section>

    <!-- Footer with proper copyright -->
    <footer class="footer" role="contentinfo">
        <div class="container">
            <p>&copy; 2024 Feel.Inframe Photography. All rights reserved.</p>
        </div>
    </footer>

    <!-- Simple JavaScript for mobile menu -->
    <script>
        document.querySelector('.mobile-menu-button').addEventListener('click', function() {
            const navLinks = document.querySelector('.nav-links');
            const isExpanded = this.getAttribute('aria-expanded') === 'true';
            this.setAttribute('aria-expanded', !isExpanded);
            navLinks.classList.toggle('show');
        });
    </script>
</body>
</html>

/* styles.css */
/* Reset with modern best practices */
*, *::before, *::after {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

/* CSS Variables for better maintainability */
:root {
    --primary-color: #c4b5fd;
    --primary-dark: rgba(124, 58, 237, 0.9);
    --background-dark: #030712;
    --text-light: #f3f4f6;
    --text-gray: #9ca3af;
    --card-background: rgba(17, 24, 39, 0.5);
    --border-color: rgba(124, 58, 237, 0.1);
}

/* Base styles with proper fallbacks */
body {
    font-family: 'Poppins', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, sans-serif;
    line-height: 1.6;
    background-color: var(--background-dark);
    color: var(--text-light);
    min-height: 100vh;
    overflow-x: hidden;
}

/* Container with proper max-width */
.container {
    width: 100%;
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 1rem;
}

/* Responsive navigation */
.navbar {
    position: fixed;
    width: 100%;
    top: 0;
    z-index: 1000;
    background: rgba(3, 7, 18, 0.95);
    backdrop-filter: blur(10px);
    -webkit-backdrop-filter: blur(10px);
    border-bottom: 1px solid var(--border-color);
}

/* Mobile menu button (hidden by default) */
.mobile-menu-button {
    display: none;
    background: none;
    border: none;
    color: var(--text-light);
    cursor: pointer;
    padding: 0.5rem;
}

/* [Additional CSS remains the same but with proper variables and vendor prefixes] */

/* Media Queries for Responsiveness */
@media (max-width: 768px) {
    .mobile-menu-button {
        display: block;
    }

    .nav-links {
        display: none;
        position: absolute;
        top: 100%;
        left: 0;
        width: 100%;
        background: var(--background-dark);
        padding: 1rem;
    }

    .nav-links.show {
        display: block;
    }

    .nav-links li {
        margin: 1rem 0;
    }

    .hero h1 {
        font-size: 2.5rem;
    }

    .packages-grid {
        grid-template-columns: 1fr;
    }
}

/* Print styles */
@media print {
    .navbar,
    .cta-button,
    .floating-promo {
        display: none;
    }
}