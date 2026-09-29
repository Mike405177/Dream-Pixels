<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>DreamPixel | Digital Experiences</title>

<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&display=swap" rel="stylesheet">

<style>

/* =====================================================
   DREAMPIXEL
   COMPLETE ONE-PAGE WEBSITE
===================================================== */

:root {
    --bg: #070b17;
    --bg2: #0d1326;
    --card: #111a31;
    --card2: #16213d;

    --purple: #8b5cf6;
    --purple2: #6d28d9;

    --blue: #38bdf8;
    --green: #22c55e;

    --white: #f8fafc;
    --text: #dce3f0;
    --muted: #94a3b8;

    --border: rgba(255,255,255,0.09);

    --max: 1150px;
}

/* =====================================================
   RESET
===================================================== */

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

html {
    scroll-behavior: smooth;
}

body {
    font-family: "Inter", sans-serif;
    background: var(--bg);
    color: var(--text);
    line-height: 1.6;
    overflow-x: hidden;
}

a {
    text-decoration: none;
    color: inherit;
}

button,
input,
textarea {
    font-family: inherit;
}

.container {
    width: min(92%, var(--max));
    margin: auto;
}

/* =====================================================
   BACKGROUND EFFECT
===================================================== */

body::before {
    content: "";

    position: fixed;

    width: 500px;
    height: 500px;

    top: -200px;
    left: -200px;

    background: rgba(139,92,246,0.12);

    filter: blur(100px);

    border-radius: 50%;

    pointer-events: none;

    z-index: -1;
}

body::after {
    content: "";

    position: fixed;

    width: 450px;
    height: 450px;

    right: -200px;
    bottom: -150px;

    background: rgba(56,189,248,0.08);

    filter: blur(100px);

    border-radius: 50%;

    pointer-events: none;

    z-index: -1;
}

/* =====================================================
   HEADER
===================================================== */

header {
    position: fixed;

    top: 0;
    left: 0;

    width: 100%;

    z-index: 1000;

    background: rgba(7,11,23,0.82);

    backdrop-filter: blur(18px);

    border-bottom: 1px solid var(--border);
}

.navbar {
    width: min(92%, var(--max));

    height: 72px;

    margin: auto;

    display: flex;

    align-items: center;

    justify-content: space-between;
}

/* LOGO */

.logo {
    font-size: 23px;

    font-weight: 800;

    letter-spacing: -1px;
}

.logo span {
    color: var(--purple);
}

.logo-dot {
    color: var(--green);
}

/* NAV */

.nav-links {
    display: flex;

    align-items: center;

    gap: 30px;
}

.nav-links a {
    position: relative;

    color: var(--muted);

    font-size: 14px;

    font-weight: 600;

    transition: 0.3s;
}

.nav-links a:hover {
    color: white;
}

.nav-links a::after {
    content: "";

    position: absolute;

    left: 0;
    bottom: -8px;

    width: 0;
    height: 2px;

    background: var(--purple);

    transition: 0.3s;
}

.nav-links a:hover::after {
    width: 100%;
}

/* MENU BUTTON */

.menu-btn {
    display: none;

    border: 0;

    background: transparent;

    color: white;

    font-size: 28px;

    cursor: pointer;
}

/* =====================================================
   HERO
===================================================== */

.hero {
    min-height: 100vh;

    display: flex;

    align-items: center;

    padding: 130px 0 80px;

    position: relative;

    overflow: hidden;
}

.hero-content {
    max-width: 760px;

    text-align: center;

    margin: auto;
}

.badge {
    display: inline-block;

    padding: 8px 15px;

    border-radius: 50px;

    border: 1px solid rgba(139,92,246,0.3);

    background: rgba(139,92,246,0.08);

    color: #c4b5fd;

    font-size: 13px;

    margin-bottom: 25px;
}

.hero h1 {
    font-size: clamp(45px, 8vw, 86px);

    line-height: 1.02;

    letter-spacing: -4px;

    font-weight: 800;

    margin-bottom: 25px;
}

.gradient-text {
    background:
        linear-gradient(
            90deg,
            #a78bfa,
            #38bdf8,
            #22c55e
        );

    -webkit-background-clip: text;

    -webkit-text-fill-color: transparent;
}

.hero p {
    max-width: 650px;

    margin: auto;

    color: var(--muted);

    font-size: 18px;

    line-height: 1.8;
}

.hero-buttons {
    display: flex;

    justify-content: center;

    flex-wrap: wrap;

    gap: 12px;

    margin-top: 35px;
}

/* =====================================================
   BUTTONS
===================================================== */

.btn {
    display: inline-flex;

    align-items: center;

    justify-content: center;

    gap: 8px;

    padding: 14px 22px;

    border-radius: 11px;

    font-size: 14px;

    font-weight: 700;

    border: 1px solid transparent;

    cursor: pointer;

    transition: 0.3s;
}

.btn-primary {
    background:
        linear-gradient(
            135deg,
            var(--purple),
            var(--purple2)
        );

    color: white;

    box-shadow:
        0 12px 35px rgba(139,92,246,0.22);
}

.btn-primary:hover {
    transform: translateY(-3px);

    box-shadow:
        0 18px 40px rgba(139,92,246,0.35);
}

.btn-secondary {
    background: rgba(255,255,255,0.04);

    border-color: var(--border);

    color: white;
}

.btn-secondary:hover {
    background: rgba(255,255,255,0.08);

    transform: translateY(-3px);
}

.btn-whatsapp {
    background: #16a34a;

    color: white;
}

.btn-whatsapp:hover {
    background: #15803d;

    transform: translateY(-3px);
}

/* =====================================================
   HERO STATS
===================================================== */

.hero-stats {
    display: grid;

    grid-template-columns:
        repeat(3, 1fr);

    max-width: 700px;

    margin: 70px auto 0;

    border: 1px solid var(--border);

    border-radius: 18px;

    background: rgba(255,255,255,0.025);

    overflow: hidden;
}

.hero-stat {
    padding: 20px;

    text-align: center;

    border-right: 1px solid var(--border);
}

.hero-stat:last-child {
    border-right: none;
}

.hero-stat strong {
    display: block;

    font-size: 23px;

    color: white;
}

.hero-stat span {
    color: var(--muted);

    font-size: 12px;
}

/* =====================================================
   GENERAL SECTIONS
===================================================== */

section {
    padding: 100px 0;
}

.section-heading {
    text-align: center;

    max-width: 650px;

    margin: 0 auto 50px;
}

.section-heading .small-title {
    color: var(--purple);

    font-size: 13px;

    font-weight: 700;

    text-transform: uppercase;

    letter-spacing: 2px;

    margin-bottom: 10px;
}

.section-heading h2 {
    color: white;

    font-size: clamp(32px, 5vw, 48px);

    letter-spacing: -2px;

    line-height: 1.1;

    margin-bottom: 15px;
}

.section-heading p {
    color: var(--muted);

    font-size: 15px;
}

/* =====================================================
   ABOUT
===================================================== */

.about-grid {
    display: grid;

    grid-template-columns: 1fr 1fr;

    gap: 50px;

    align-items: center;
}

.about-text h3 {
    color: white;

    font-size: 28px;

    margin-bottom: 18px;
}

.about-text p {
    color: var(--muted);

    margin-bottom: 20px;
}

.about-boxes {
    display: grid;

    grid-template-columns: 1fr 1fr;

    gap: 15px;
}

.about-box {
    padding: 25px;

    background: var(--card);

    border: 1px solid var(--border);

    border-radius: 15px;

    transition: 0.3s;
}

.about-box:hover {
    transform: translateY(-5px);

    border-color:
        rgba(139,92,246,0.4);
}

.about-icon {
    font-size: 28px;

    margin-bottom: 10px;
}

.about-box h4 {
    color: white;

    margin-bottom: 5px;
}

.about-box p {
    color: var(--muted);

    font-size: 13px;
}

/* =====================================================
   SERVICES
===================================================== */

.services-grid {
    display: grid;

    grid-template-columns:
        repeat(3, 1fr);

    gap: 20px;
}

.service-card {
    background: var(--card);

    border: 1px solid var(--border);

    border-radius: 18px;

    padding: 30px;

    transition: 0.3s;
}

.service-card:hover {
    transform: translateY(-8px);

    background: var(--card2);

    border-color:
        rgba(139,92,246,0.4);

    box-shadow:
        0 20px 50px rgba(0,0,0,0.25);
}

.service-icon {
    width: 55px;

    height: 55px;

    display: flex;

    align-items: center;

    justify-content: center;

    border-radius: 14px;

    background:
        rgba(139,92,246,0.12);

    font-size: 25px;

    margin-bottom: 20px;
}

.service-card h3 {
    color: white;

    margin-bottom: 10px;
}

.service-card p {
    color: var(--muted);

    font-size: 14px;

    line-height: 1.7;
}

/* =====================================================
   PORTFOLIO
===================================================== */

.portfolio-grid {
    display: grid;

    grid-template-columns:
        repeat(3, 1fr);

    gap: 20px;
}

.project {
    overflow: hidden;

    border-radius: 18px;

    background: var(--card);

    border: 1px solid var(--border);

    transition: 0.3s;
}

.project:hover {
    transform: translateY(-7px);

    border-color:
        rgba(139,92,246,0.4);
}

.project-image {
    height: 230px;

    overflow: hidden;

    position: relative;
}

.project-image img {
    width: 100%;

    height: 100%;

    object-fit: cover;

    transition: 0.5s;
}

.project:hover img {
    transform: scale(1.08);
}

.project-content {
    padding: 22px;
}

.project-content h3 {
    color: white;

    margin-bottom: 7px;
}

.project-content p {
    color: var(--muted);

    font-size: 13px;
}

/* =====================================================
   CTA
===================================================== */

.cta {
    padding-top: 30px;
}

.cta-box {
    text-align: center;

    padding: 70px 30px;

    border-radius: 25px;

    border: 1px solid var(--border);

    background:
        radial-gradient(
            circle at center,
            rgba(139,92,246,0.15),
            transparent 60%
        ),
        var(--card);
}

.cta-box h2 {
    font-size: clamp(30px, 5vw, 45px);

    color: white;

    margin-bottom: 15px;
}

.cta-box p {
    color: var(--muted);

    max-width: 600px;

    margin: auto auto 25px;
}

/* =====================================================
   CONTACT
===================================================== */

.contact-grid {
    display: grid;

    grid-template-columns: 0.8fr 1.2fr;

    gap: 30px;
}

.contact-card,
.contact-form {
    background: var(--card);

    border: 1px solid var(--border);

    border-radius: 18px;

    padding: 30px;
}

.contact-card h3,
.contact-form h3 {
    color: white;

    margin-bottom: 15px;
}

.contact-card p {
    color: var(--muted);

    font-size: 14px;

    margin-bottom: 25px;
}

.contact-item {
    display: flex;

    align-items: center;

    gap: 13px;

    margin-bottom: 17px;
}

.contact-item-icon {
    width: 42px;

    height: 42px;

    display: flex;

    align-items: center;

    justify-content: center;

    border-radius: 10px;

    background: rgba(139,92,246,0.1);
}

.contact-item div:last-child {
    color: var(--muted);

    font-size: 13px;
}

.contact-item strong {
    display: block;

    color: white;

    margin-bottom: 2px;
}

.contact-form {
    display: flex;

    flex-direction: column;

    gap: 15px;
}

.form-row {
    display: grid;

    grid-template-columns: 1fr 1fr;

    gap: 15px;
}

.form-group {
    display: flex;

    flex-direction: column;

    gap: 7px;
}

.form-group label {
    color: #cbd5e1;

    font-size: 13px;

    font-weight: 600;
}

.form-group input,
.form-group textarea {
    width: 100%;

    padding: 13px 15px;

    background: #0b1224;

    color: white;

    border: 1px solid var(--border);

    border-radius: 10px;

    outline: none;

    resize: vertical;

    transition: 0.3s;
}

.form-group textarea {
    min-height: 140px;
}

.form-group input:focus,
.form-group textarea:focus {
    border-color: var(--purple);

    box-shadow:
        0 0 0 3px rgba(139,92,246,0.08);
}

/* =====================================================
   POPUP
===================================================== */

.popup {
    display: none;

    position: fixed;

    inset: 0;

    z-index: 3000;

    background: rgba(0,0,0,0.75);

    backdrop-filter: blur(6px);

    align-items: center;

    justify-content: center;

    padding: 20px;
}

.popup.show {
    display: flex;
}

.popup-box {
    width: min(100%, 420px);

    background: var(--card);

    border: 1px solid var(--border);

    border-radius: 20px;

    padding: 35px;

    text-align: center;

    animation: popupIn 0.3s ease;
}

.popup-icon {
    font-size: 45px;

    margin-bottom: 15px;
}

.popup-box h3 {
    color: white;

    margin-bottom: 10px;
}

.popup-box p {
    color: var(--muted);

    font-size: 14px;

    margin-bottom: 20px;
}

@keyframes popupIn {

    from {
        opacity: 0;
        transform: scale(0.85);
    }

    to {
        opacity: 1;
        transform: scale(1);
    }

}

/* =====================================================
   FOOTER
===================================================== */

footer {
    border-top: 1px solid var(--border);

    background: #050810;

    padding: 30px 20px;

    text-align: center;

    color: var(--muted);

    font-size: 13px;
}

.footer-logo {
    color: white;

    font-weight: 800;

    font-size: 20px;

    margin-bottom: 8px;
}

.footer-logo span {
    color: var(--purple);
}

/* =====================================================
   RESPONSIVE TABLET
===================================================== */

@media (max-width: 900px) {

    .nav-links {
        gap: 18px;
    }

    .services-grid,
    .portfolio-grid {
        grid-template-columns:
            repeat(2, 1fr);
    }

    .about-grid {
        grid-template-columns: 1fr;
    }

    .contact-grid {
        grid-template-columns: 1fr;
    }

}

/* =====================================================
   RESPONSIVE MOBILE
===================================================== */

@media (max-width: 700px) {

    header {
        position: fixed;
    }

    .navbar {
        height: 65px;
    }

    .menu-btn {
        display: block;
    }

    .nav-links {
        position: absolute;

        top: 65px;

        left: 0;

        width: 100%;

        display: none;

        flex-direction: column;

        align-items: stretch;

        gap: 0;

        background:
            rgba(7,11,23,0.97);

        border-bottom:
            1px solid var(--border);

        padding: 10px 20px;
    }

    .nav-links.show {
        display: flex;
    }

    .nav-links a {
        padding: 14px 5px;

        border-bottom:
            1px solid var(--border);
    }

    .nav-links a:last-child {
        border-bottom: none;
    }

    .nav-links a::after {
        display: none;
    }

    .hero {
        padding-top: 110px;
    }

    .hero h1 {
        font-size: 48px;

        letter-spacing: -2px;
    }

    .hero p {
        font-size: 16px;
    }

    .hero-buttons {
        flex-direction: column;

        width: 100%;

        max-width: 330px;

        margin-left: auto;

        margin-right: auto;
    }

    .hero-buttons .btn {
        width: 100%;
    }

    .hero-stats {
        grid-template-columns: 1fr;

        width: 100%;
    }

    .hero-stat {
        border-right: none;

        border-bottom:
            1px solid var(--border);
    }

    .hero-stat:last-child {
        border-bottom: none;
    }

    section {
        padding: 75px 0;
    }

    .services-grid,
    .portfolio-grid {
        grid-template-columns: 1fr;
    }

    .about-boxes {
        grid-template-columns: 1fr;
    }

    .form-row {
        grid-template-columns: 1fr;
    }

    .contact-card,
    .contact-form {
        padding: 22px;
    }

}

/* =====================================================
   SMALL PHONES
===================================================== */

@media (max-width: 400px) {

    .logo {
        font-size: 20px;
    }

    .hero h1 {
        font-size: 40px;
    }

    .section-heading h2 {
        font-size: 31px;
    }

    .project-image {
        height: 200px;
    }

}

</style>
</head>

<body>

<!-- =====================================================
     HEADER
===================================================== -->

<header>

<div class="navbar">

    <a href="#home" class="logo">
        Dream<span>Pixel</span><span class="logo-dot">.</span>
    </a>

    <button
        class="menu-btn"
        id="menuBtn"
        aria-label="Open navigation"
    >
        ☰
    </button>

    <nav class="nav-links" id="navLinks">

        <a href="#home">Home</a>

        <a href="#about">About</a>

        <a href="#services">Services</a>

        <a href="#portfolio">Portfolio</a>

        <a href="#contact">Contact</a>

    </nav>

</div>

</header>


<!-- =====================================================
     HERO
===================================================== -->

<section class="hero" id="home">

<div class="container">

<div class="hero-content">

    <div class="badge">
        ✦ Digital creativity meets technology
    </div>

    <h1>
        We turn ideas into
        <span class="gradient-text">
            digital experiences.
        </span>
    </h1>

    <p>
        DreamPixel creates modern websites, digital brands,
        interfaces and experiences designed to help businesses
        stand out and grow online.
    </p>

    <div class="hero-buttons">

        <a
            href="#contact"
            class="btn btn-primary"
        >
            🚀 Start a Project
        </a>

        <a
            href="https://wa.me/2348061119565"
            target="_blank"
            class="btn btn-whatsapp"
        >
            💬 WhatsApp
        </a>

        <a
            href="#portfolio"
            class="btn btn-secondary"
        >
            View Our Work
        </a>

    </div>

</div>


<div class="hero-stats">

    <div class="hero-stat">

        <strong>Creative</strong>

        <span>
            Digital Solutions
        </span>

    </div>

    <div class="hero-stat">

        <strong>Modern</strong>

        <span>
            Responsive Design
        </span>

    </div>

    <div class="hero-stat">

        <strong>Focused</strong>

        <span>
            On Your Growth
        </span>

    </div>

</div>

</div>

</section>


<!-- =====================================================
     ABOUT
===================================================== -->

<section id="about">

<div class="container">

<div class="section-heading">

    <div class="small-title">
        About DreamPixel
    </div>

    <h2>
        Ideas deserve great design.
    </h2>

    <p>
        We combine creativity, technology and strategy
        to build digital experiences people remember.
    </p>

</div>


<div class="about-grid">

<div class="about-text">

    <h3>
        Building the digital future,
        one idea at a time.
    </h3>

    <p>
        DreamPixel is a creative digital team focused on
        helping businesses and individuals establish a
        strong presence online.
    </p>

    <p>
        From websites and branding to digital marketing,
        we turn ideas into practical digital experiences
        that are beautiful, responsive and easy to use.
    </p>

    <a
        href="#contact"
        class="btn btn-primary"
    >
        Work With Us
    </a>

</div>


<div class="about-boxes">

    <div class="about-box">

        <div class="about-icon">
            🎨
        </div>

        <h4>
            Creative
        </h4>

        <p>
            Designs that make your brand stand out.
        </p>

    </div>


    <div class="about-box">

        <div class="about-icon">
            ⚡
        </div>

        <h4>
            Fast
        </h4>

        <p>
            Efficient digital solutions built for you.
        </p>

    </div>


    <div class="about-box">

        <div class="about-icon">
            📱
        </div>

        <h4>
            Responsive
        </h4>

        <p>
            Websites that work beautifully on every screen.
        </p>

    </div>


    <div class="about-box">

        <div class="about-icon">
            🚀
        </div>

        <h4>
            Growth
        </h4>

        <p>
            Digital solutions designed around your goals.
        </p>

    </div>

</div>

</div>

</div>

</section>


<!-- =====================================================
     SERVICES
===================================================== -->

<section id="services">

<div class="container">

<div class="section-heading">

    <div class="small-title">
        What We Do
    </div>

    <h2>
        Our Services
    </h2>

    <p>
        Everything you need to build a strong digital presence.
    </p>

</div>


<div class="services-grid">

    <div class="service-card">

        <div class="service-icon">
            💻
        </div>

        <h3>
            Web Design
        </h3>

        <p>
            Modern, responsive websites built to look
            great and provide an excellent user experience.
        </p>

    </div>


    <div class="service-card">

        <div class="service-icon">
            🎨
        </div>

        <h3>
            Branding
        </h3>

        <p>
            Logos, colors and visual identities that
            communicate what makes your business unique.
        </p>

    </div>


    <div class="service-card">

        <div class="service-icon">
            📈
        </div>

        <h3>
            Digital Marketing
        </h3>

        <p>
            Strategies that help you reach more people,
            grow your audience and build your online presence.
        </p>

    </div>


    <div class="service-card">

        <div class="service-icon">
            📱
        </div>

        <h3>
            UI/UX Design
        </h3>

        <p>
            Clean interfaces and thoughtful user experiences
            designed around real people.
        </p>

    </div>


    <div class="service-card">

        <div class="service-icon">
            ⚙️
        </div>

        <h3>
            Web Development
        </h3>

        <p>
            Functional websites with modern technologies,
            interactive features and reliable performance.
        </p>

    </div>


    <div class="service-card">

        <div class="service-icon">
            🔥
        </div>

        <h3>
            Custom Projects
        </h3>

        <p>
            Have a unique idea? Let's work together and
            turn your concept into something real.
        </p>

    </div>

</div>

</div>

</section>


<!-- =====================================================
     PORTFOLIO
===================================================== -->

<section id="portfolio">

<div class="container">

<div class="section-heading">

    <div class="small-title">
        Our Work
    </div>

    <h2>
        Selected Projects
    </h2>

    <p>
        A few examples of the kinds of digital experiences
        we can create.
    </p>

</div>


<div class="portfolio-grid">


    <div class="project">

        <div class="project-image">

            <img
                src="https://picsum.photos/800/500?random=11"
                alt="E-commerce website"
                loading="lazy"
            >

        </div>

        <div class="project-content">

            <h3>
                E-Commerce Store
            </h3>

            <p>
                Modern online shopping experience
                with a clean interface.
            </p>

        </div>

    </div>


    <div class="project">

        <div class="project-image">

            <img
                src="https://picsum.photos/800/500?random=12"
                alt="Creative portfolio website"
                loading="lazy"
            >

        </div>

        <div class="project-content">

            <h3>
                Creative Portfolio
            </h3>

            <p>
                Personal brand website created
                for a creative professional.
            </p>

        </div>

    </div>


    <div class="project">

        <div class="project-image">

            <img
                src="https://picsum.photos/800/500?random=13"
                alt="Mobile application interface"
                loading="lazy"
            >

        </div>

        <div class="project-content">

            <h3>
                Mobile App UI
            </h3>

            <p>
                Modern interface concept for
                a food delivery application.
            </p>

        </div>

    </div>


    <div class="project">

        <div class="project-image">

            <img
                src="https://picsum.photos/800/500?random=14"
                alt="Business website"
                loading="lazy"
            >

        </div>

        <div class="project-content">

            <h3>
                Business Website
            </h3>

            <p>
                Professional website designed
                for a growing business.
            </p>

        </div>

    </div>


    <div class="project">

        <div class="project-image">

            <img
                src="https://picsum.photos/800/500?random=15"
                alt="Brand identity"
                loading="lazy"
            >

        </div>

        <div class="project-content">

            <h3>
                Brand Identity
            </h3>

            <p>
                Visual identity and digital
                branding for a new company.
            </p>

        </div>

    </div>


    <div class="project">

        <div class="project-image">

            <img
                src="https://picsum.photos/800/500?random=16"
                alt="Landing page"
                loading="lazy"
            >

        </div>

        <div class="project-content">

            <h3>
                Landing Page
            </h3>

            <p>
                High-impact landing page designed
                to introduce a digital product.
            </p>

        </div>

    </div>


</div>

</div>

</section>


<!-- =====================================================
     CTA
===================================================== -->

<section class="cta">

<div class="container">

<div class="cta-box">

    <h2>
        Have an idea?
    </h2>

    <p>
        Tell us what you're building and let's turn
        your idea into a digital experience.
    </p>

    <a
        href="#contact"
        class="btn btn-primary"
    >
        🚀 Let's Build Something
    </a>

</div>

</div>

</section>


<!-- =====================================================
     CONTACT
===================================================== -->

<section id="contact">

<div class="container">

<div class="section-heading">

    <div class="small-title">
        Get In Touch
    </div>

    <h2>
        Let's Build Something.
    </h2>

    <p>
        Have a project in mind? Send us a message and
        we'll get back to you.
    </p>

</div>


<div class="contact-grid">


<!-- CONTACT INFO -->

<div class="contact-card">

    <h3>
        Contact DreamPixel
    </h3>

    <p>
        We're ready to hear about your idea,
        business or next project.
    </p>


    <div class="contact-item">

        <div class="contact-item-icon">
            📧
        </div>

        <div>

            <strong>
                Email
            </strong>

            michaeleni29@gmail.com

        </div>

    </div>


    <div class="contact-item">

        <div class="contact-item-icon">
            📱
        </div>

        <div>

            <strong>
                WhatsApp
            </strong>

            +234 806 111 9565

        </div>

    </div>


    <div class="contact-item">

        <div class="contact-item-icon">
            📍
        </div>

        <div>

            <strong>
                Location
            </strong>

            Delta, Nigeria

        </div>

    </div>


    <a
        href="https://wa.me/2348061119565"
        target="_blank"
        class="btn btn-whatsapp"
        style="margin-top:15px;"
    >
        💬 Chat on WhatsApp
    </a>

</div>


<!-- FORM -->

<form
    class="contact-form"
    id="contactForm"
    action="https://formspree.io/f/xqkrjzab"
    method="POST"
>

    <h3>
        Send a Message
    </h3>


    <div class="form-row">

        <div class="form-group">

            <label>
                Your Name
            </label>

            <input
                type="text"
                name="name"
                placeholder="Enter your name"
                required
            >

        </div>


        <div class="form-group">

            <label>
                Email Address
            </label>

            <input
                type="email"
                name="email"
                placeholder="you@example.com"
                required
            >

        </div>

    </div>


    <div class="form-group">

        <label>
            Project
        </label>

        <input
            type="text"
            name="project"
            placeholder="What do you want us to build?"
        >

    </div>


    <div class="form-group">

        <label>
            Message
        </label>

        <textarea
            name="message"
            placeholder="Tell us about your project..."
            required
        ></textarea>

    </div>


    <button
        type="submit"
        class="btn btn-primary"
    >
        Send Message 🚀
    </button>

</form>

</div>

</div>

</section>


<!-- =====================================================
     SUCCESS POPUP
===================================================== -->

<div
    class="popup"
    id="successPopup"
>

<div class="popup-box">

    <div class="popup-icon">
        ✅
    </div>

    <h3>
        Message Sent!
    </h3>

    <p>
        Thanks for contacting DreamPixel.
        We'll get back to you soon.
    </p>

    <button
        class="btn btn-primary"
        onclick="closePopup()"
    >
        Close
    </button>

</div>

</div>


<!-- =====================================================
     FOOTER
===================================================== -->

<footer>

<div class="footer-logo">
    Dream<span>Pixel</span>.
</div>

<p>
    © 2026 DreamPixel. All rights reserved.
</p>

<p style="margin-top:5px;">
    Built with ❤️ & Unity in Delta, Nigeria.
</p>

</footer>


<!-- =====================================================
     JAVASCRIPT
===================================================== -->

<script>

/* ===============================
   MOBILE MENU
=============================== */

const menuBtn =
    document.getElementById("menuBtn");

const navLinks =
    document.getElementById("navLinks");


menuBtn.addEventListener("click", () => {

    navLinks.classList.toggle("show");

});


/* Close mobile menu after clicking */

document.querySelectorAll(".nav-links a")
.forEach(link => {

    link.addEventListener("click", () => {

        navLinks.classList.remove("show");

    });

});


/* ===============================
   CONTACT FORM
=============================== */

const form =
    document.getElementById("contactForm");

const popup =
    document.getElementById("successPopup");


form.addEventListener("submit", async function(event) {

    event.preventDefault();

    const submitButton =
        form.querySelector("button");

    submitButton.disabled = true;

    submitButton.textContent =
        "Sending...";


    try {

        const response =
            await fetch(
                form.action,
                {
                    method: "POST",

                    body:
                        new FormData(form),

                    headers: {
                        "Accept":
                            "application/json"
                    }
                }
            );


        if (response.ok) {

            form.reset();

            popup.classList.add("show");

        } else {

            alert(
                "Something went wrong. Please try again."
            );

        }

    } catch (error) {

        alert(
            "Unable to send your message. Please check your internet connection."
        );

    }


    submitButton.disabled = false;

    submitButton.textContent =
        "Send Message 🚀";

});


/* ===============================
   CLOSE POPUP
=============================== */

function closePopup() {

    popup.classList.remove("show");

}


/* Close popup by clicking outside */

popup.addEventListener("click", function(event) {

    if (event.target === popup) {

        closePopup();

    }

});


/* ===============================
   ESC KEY
=============================== */

document.addEventListener("keydown", function(event) {

    if (event.key === "Escape") {

        closePopup();

        navLinks.classList.remove("show");

    }

});

</script>

</body>
</html>
