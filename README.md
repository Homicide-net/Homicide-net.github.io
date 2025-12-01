
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Aurora Tech - Innovation Forward</title>
    <style>
        /* --- Basic Reset & Global Styles --- */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
            line-height: 1.6;
            background-color: #f4f4f9;
            color: #333;
        }

        .container {
            max-width: 1100px;
            margin: 0 auto;
            padding: 0 20px;
        }

        h1, h2 {
            color: #2c3e50;
            margin-bottom: 20px;
        }

        h1 { font-size: 2.5rem; }
        h2 { font-size: 2rem; text-align: center; margin-bottom: 40px; }

        /* --- Header & Navigation --- */
        .header {
            background: #fff;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
            position: sticky;
            top: 0;
            width: 100%;
            z-index: 1000;
        }

        .navbar {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 1rem 0;
        }

        .logo {
            font-size: 1.5rem;
            font-weight: bold;
            color: #3498db;
            text-decoration: none;
        }

        .nav-links {
            list-style: none;
            display: flex;
        }

        .nav-links li {
            margin-left: 20px;
        }

        .nav-links a {
            text-decoration: none;
            color: #333;
            font-weight: 500;
            transition: color 0.3s ease;
        }

        .nav-links a:hover {
            color: #3498db;
        }

        /* --- Hero Section --- */
        .hero {
            background: linear-gradient(to right, #3498db, #2ecc71);
            color: #fff;
            padding: 100px 0;
            text-align: center;
        }

        .hero h1 {
            color: #fff;
            font-size: 3rem;
        }

        .hero p {
            font-size: 1.2rem;
            margin-bottom: 30px;
        }

        .btn {
            display: inline-block;
            background: #fff;
            color: #3498db;
            padding: 12px 25px;
            text-decoration: none;
            border-radius: 5px;
            font-weight: bold;
            transition: transform 0.2s ease, box-shadow 0.2s ease;
        }

        .btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
        }

        /* --- Main Content Sections --- */
        .section {
            padding: 60px 0;
        }

        .section-light {
            background: #fff;
        }

        .section-dark {
            background: #ecf0f1;
        }

        /* --- Services Grid --- */
        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 30px;
            text-align: center;
        }

        .service-card {
            background: #fff;
            padding: 30px;
            border-radius: 8px;
            box-shadow: 0 4px 10px rgba(0,0,0,0.05);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .service-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 20px rgba(0,0,0,0.1);
        }

        .service-card h3 {
            color: #3498db;
            margin-bottom: 15px;
        }

        /* --- About Section --- */
        .about-content {
            display: flex;
            align-items: center;
            gap: 40px;
        }

        .about-text {
            flex: 1;
        }

        .about-image {
            flex: 1;
            max-width: 400px;
        }

        .about-image img {
            width: 100%;
            border-radius: 8px;
        }

        /* --- Contact Form --- */
        .contact-form {
            max-width: 600px;
            margin: 0 auto;
            display: flex;
            flex-direction: column;
            gap: 15px;
        }

        .contact-form input,
        .contact-form textarea {
            width: 100%;
            padding: 12px;
            border: 1px solid #ccc;
            border-radius: 5px;
            font-size: 1rem;
        }

        .contact-form textarea {
            resize: vertical;
            min-height: 150px;
        }

        .contact-form button {
            background: #3498db;
            color: #fff;
            border: none;
            padding: 15px;
            border-radius: 5px;
            font-size: 1.1rem;
            cursor: pointer;
            transition: background 0.3s ease;
        }

        .contact-form button:hover {
            background: #2980b9;
        }

        /* --- Footer --- */
        .footer {
            background: #2c3e50;
            color: #ecf0f1;
            text-align: center;
            padding: 30px 0;
        }

        /* --- Responsive Design --- */
        @media (max-width: 768px) {
            .navbar {
                flex-direction: column;
            }

            .nav-links {
                margin-top: 15px;
            }

            .hero h1 {
                font-size: 2.2rem;
            }

            .about-content {
                flex-direction: column;
            }
        }
    </style>
</head>
<body>

    <!-- 1. Header with Navigation -->
    <header class="header">
        <nav class="navbar container">
            <a href="#" class="logo">Aurora Tech</a>
            <ul class="nav-links">
                <li><a href="#home">Home</a></li>
                <li><a href="#services">Services</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <main>
        <!-- 2. Hero Section -->
        <section id="home" class="hero">
            <div class="container">
                <h1>Building the Future, Today.</h1>
                <p>We create innovative digital solutions that drive growth and efficiency for your business.</p>
                <a href="#contact" class="btn">Get Started</a>
            </div>
        </section>

        <!-- 3. Services Section -->
        <section id="services" class="section section-light">
            <div class="container">
                <h2>Our Services</h2>
                <div class="services-grid">
                    <div class="service-card">
                        <h3>Web Development</h3>
                        <p>Building fast, responsive, and beautiful websites with modern technologies like HTML5, CSS3, and JavaScript.</p>
                    </div>
                    <div class="service-card">
                        <h3>Cloud Solutions</h3>
                        <p>Migrating and managing your infrastructure on the cloud for better scalability, security, and cost-efficiency.</p>
                    </div>
                    <div class="service-card">
                        <h3>Data Analytics</h3>
                        <p>Turning your raw data into actionable insights with custom dashboards and machine learning models.</p>
                    </div>
                </div>
            </div>
        </section>

        <!-- 4. About Section -->
        <section id="about" class="section section-dark">
            <div class="container">
                <h2>About Aurora Tech</h2>
                <div class="about-content">
                    <div class="about-text">
                        <p>Founded in 2020, Aurora Tech is a team of passionate developers, designers, and strategists dedicated to solving complex problems. We believe in the power of technology to transform businesses and improve lives.</p>
                        <p>Our mission is to deliver exceptional value through innovation, integrity, and a relentless focus on our clients' success.</p>
                    </div>
                    <div class="about-image">
                        <!-- Using a placeholder image service -->
                        <img src="https://via.placeholder.com/500x300.png/3498db/
