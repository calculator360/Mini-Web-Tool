<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mini Web Tool - Free Online Tools for Everyone</title>
    <meta name="description" content="Mini Web Tool offers a collection of free online tools including PDF tools, image converters, YouTube utilities, and more to simplify your digital tasks.">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary-color: #667eea;
            --secondary-color: #764ba2;
            --accent-color: #5EE7DF;
            --text-color: #4a4a4a;
            --light-text: #777;
            --bg-color: #f9f9f9;
            --card-bg: #ffffff;
            --footer-bg: #2c3e50;
            --shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            --transition: all 0.3s ease;
        }
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        body {
            background-color: var(--bg-color);
            color: var(--text-color);
            line-height: 1.6;
        }
        /* Header Styles */
        .site-header {
            background: linear-gradient(135deg, var(--primary-color) 0%, var(--secondary-color) 100%);
            color: white;
            padding: 25px 0;
            text-align: center;
            box-shadow: var(--shadow);
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        .header-container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        .header-title {
            font-size: 2.5rem;
            margin-bottom: 10px;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.2);
            font-weight: 700;
        }

        .header-subtitle {
            font-size: 1.2rem;
            font-weight: 300;
            max-width: 800px;
            margin: 0 auto;
            opacity: 0.9;
        }

        /* Navigation */
        .main-nav {
            background-color: rgba(255, 255, 255, 0.95);
            padding: 15px 0;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
        }

        .nav-container {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0 20px;
            flex-wrap: wrap;
        }

        .nav-logo {
            font-size: 1.5rem;
            font-weight: 700;
            color: var(--secondary-color);
            text-decoration: none;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .nav-logo i {
            font-size: 1.8rem;
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 15px;
            flex-wrap: wrap;
        }

        .nav-link {
            text-decoration: none;
            color: var(--text-color);
            font-weight: 600;
            padding: 8px 15px;
            border-radius: 5px;
            transition: var(--transition);
            font-size: 0.95rem;
        }

        .nav-link:hover, .nav-link.active {
            background-color: var(--secondary-color);
            color: white;
        }

        .search-bar {
            position: relative;
            width: 100%;
            max-width: 400px;
            margin: 15px auto 0;
        }

        .search-input {
            width: 100%;
            padding: 12px 20px;
            border: none;
            border-radius: 30px;
            background-color: #f1f1f1;
            font-size: 16px;
            transition: var(--transition);
            padding-left: 45px;
        }

        .search-input:focus {
            outline: none;
            box-shadow: 0 0 0 2px var(--secondary-color);
            background-color: white;
        }

        .search-icon {
            position: absolute;
            left: 15px;
            top: 50%;
            transform: translateY(-50%);
            color: var(--light-text);
        }

        /* Main Content */
        .page-content {
            max-width: 1200px;
            margin: 30px auto;
            padding: 0 20px;
        }

        .section-title {
            font-size: 2rem;
            text-align: center;
            margin-bottom: 30px;
            color: var(--text-color);
            position: relative;
            padding-bottom: 15px;
        }

        .section-title::after {
            content: "";
            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 4px;
            background: linear-gradient(90deg, var(--primary-color) 0%, var(--secondary-color) 100%);
            border-radius: 2px;
        }

        /* Hero Section */
        .hero-section {
            background: linear-gradient(135deg, rgba(102, 126, 234, 0.1) 0%, rgba(118, 75, 162, 0.1) 100%);
            border-radius: 15px;
            padding: 40px;
            margin-bottom: 40px;
            text-align: center;
            position: relative;
            overflow: hidden;
        }

        .hero-content {
            position: relative;
            z-index: 2;
        }

        .hero-title {
            font-size: 2.5rem;
            margin-bottom: 15px;
            color: var(--secondary-color);
        }

        .hero-description {
            font-size: 1.1rem;
            max-width: 800px;
            margin: 0 auto 25px;
            color: var(--text-color);
        }

        .hero-buttons {
            display: flex;
            justify-content: center;
            gap: 15px;
            flex-wrap: wrap;
        }

        .hero-button {
            display: inline-block;
            padding: 12px 25px;
            border-radius: 30px;
            font-weight: 600;
            text-decoration: none;
            transition: var(--transition);
        }

        .primary-button {
            background: linear-gradient(135deg, var(--primary-color) 0%, var(--secondary-color) 100%);
            color: white;
        }

        .primary-button:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(118, 75, 162, 0.3);
        }

        .secondary-button {
            background-color: white;
            color: var(--secondary-color);
            border: 2px solid var(--secondary-color);
        }

        .secondary-button:hover {
            background-color: var(--secondary-color);
            color: white;
        }

        /* Tools Grid */
        .tools-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 20px;
            margin-top: 30px;
        }

        .tool-card {
            background-color: var(--card-bg);
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
            transition: var(--transition);
            text-align: center;
            height: 100%;
            display: flex;
            flex-direction: column;
            border: 1px solid rgba(0, 0, 0, 0.05);
        }

        .tool-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.15);
        }

        .tool-icon {
            height: 120px;
            display: flex;
            align-items: center;
            justify-content: center;
            background: linear-gradient(135deg, var(--primary-color) 0%, var(--secondary-color) 100%);
            color: white;
            font-size: 2.5rem;
        }

        .tool-icon img {
            max-width: 60%;
            max-height: 60%;
            object-fit: contain;
            filter: drop-shadow(0 2px 4px rgba(0, 0, 0, 0.2));
        }

        .tool-icon.analytics {
            background: linear-gradient(135deg, #6DC8F3 0%, #4A91E2 100%);
        }

        .tool-icon.seo {
            background: linear-gradient(135deg, #FFB88C 0%, #FF9A8B 100%);
        }

        .tool-icon.converter {
            background: linear-gradient(135deg, #5EE7DF 0%, #2DBAC0 100%);
        }

        .tool-icon.generator {
            background: linear-gradient(135deg, #B224EF 0%, #7579FF 100%);
        }

        .tool-icon.calculator {
            background: linear-gradient(135deg, #FF57B9 0%, #A704FD 100%);
        }

        .tool-icon.checker {
            background: linear-gradient(135deg, #3EECAC 0%, #37D8A7 100%);
        }

        .tool-details {
            padding: 20px 15px;
            flex-grow: 1;
            display: flex;
            flex-direction: column;
        }

        .tool-name {
            font-size: 1.2rem;
            margin-bottom: 10px;
            color: var(--text-color);
            font-weight: 600;
        }

        .tool-description {
            color: var(--light-text);
            margin-bottom: 15px;
            line-height: 1.5;
            font-size: 0.95rem;
            flex-grow: 1;
        }

        .tool-button {
            display: inline-block;
            background: linear-gradient(90deg, var(--primary-color) 0%, var(--secondary-color) 100%);
            color: white;
            text-decoration: none;
            padding: 10px 20px;
            border-radius: 30px;
            font-weight: 600;
            transition: var(--transition);
            border: none;
            cursor: pointer;
            font-size: 0.95rem;
            margin-top: auto;
            align-self: center;
        }

        .tool-button:hover {
            transform: scale(1.05);
            opacity: 0.9;
            box-shadow: 0 5px 15px rgba(118, 75, 162, 0.3);
        }

        /* Categories Section */
        .categories-section {
            margin: 50px 0;
        }

        .categories {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 15px;
            margin-top: 25px;
        }

        .category-tag {
            background-color: var(--card-bg);
            padding: 10px 20px;
            border-radius: 30px;
            font-weight: 600;
            color: var(--text-color);
            box-shadow: var(--shadow);
            transition: var(--transition);
            cursor: pointer;
            font-size: 0.95rem;
            text-decoration: none;
            border: 1px solid rgba(0, 0, 0, 0.05);
        }

        .category-tag:hover, .category-tag.active {
            background: linear-gradient(90deg, var(--primary-color) 0%, var(--secondary-color) 100%);
            color: white;
            transform: translateY(-3px);
        }

        /* Features Section */
        .features-section {
            margin: 50px 0;
        }

        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin-top: 30px;
        }

        .feature-card {
            background-color: var(--card-bg);
            border-radius: 10px;
            padding: 30px;
            box-shadow: var(--shadow);
            transition: var(--transition);
            text-align: center;
            border: 1px solid rgba(0, 0, 0, 0.05);
        }

        .feature-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.1);
        }

        .feature-icon {
            font-size: 2.5rem;
            color: var(--secondary-color);
            margin-bottom: 20px;
        }

        .feature-title {
            font-size: 1.3rem;
            margin-bottom: 15px;
            color: var(--text-color);
        }

        .feature-description {
            color: var(--light-text);
            font-size: 0.95rem;
        }

        /* Subscribe Section */
        .subscribe-section {
            margin: 50px 0;
            padding: 40px;
            background: linear-gradient(135deg, rgba(102, 126, 234, 0.1) 0%, rgba(118, 75, 162, 0.1) 100%);
            border-radius: 15px;
            text-align: center;
        }

        .subscribe-title {
            font-size: 1.8rem;
            margin-bottom: 15px;
            color: var(--text-color);
        }

        .subscribe-description {
            color: var(--light-text);
            max-width: 600px;
            margin: 0 auto 25px;
        }

        .subscribe-form {
            display: flex;
            max-width: 500px;
            margin: 0 auto;
            flex-wrap: wrap;
            justify-content: center;
        }

        .email-input {
            flex: 1;
            min-width: 250px;
            padding: 12px 20px;
            border: 2px solid #e1e1e1;
            border-radius: 30px;
            font-size: 16px;
            transition: var(--transition);
        }

        .email-input:focus {
            outline: none;
            border-color: var(--secondary-color);
        }

        .subscribe-button {
            background: linear-gradient(90deg, var(--primary-color) 0%, var(--secondary-color) 100%);
            color: white;
            border: none;
            padding: 12px 25px;
            border-radius: 30px;
            font-weight: 600;
            cursor: pointer;
            transition: var(--transition);
            margin-left: 10px;
            min-width: 150px;
        }

        .subscribe-button:hover {
            opacity: 0.9;
            transform: translateY(-2px);
        }

        /* Footer */
        .site-footer {
            background-color: var(--footer-bg);
            color: white;
            padding: 50px 0 20px;
            margin-top: 50px;
        }

        .footer-container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 40px;
        }

        .footer-col {
            margin-bottom: 20px;
        }

        .footer-logo {
            font-size: 1.8rem;
            font-weight: 700;
            margin-bottom: 15px;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .footer-logo i {
            color: var(--primary-color);
        }

        .footer-about {
            margin-bottom: 20px;
            line-height: 1.6;
            color: #ccc;
            font-size: 0.95rem;
        }

        .footer-social {
            display: flex;
            gap: 15px;
            margin-bottom: 20px;
        }

        .social-icon {
            width: 40px;
            height: 40px;
            background-color: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.1rem;
            transition: var(--transition);
            color: white;
            text-decoration: none;
        }

        .social-icon:hover {
            background-color: var(--primary-color);
            transform: translateY(-3px);
        }

        .footer-heading {
            font-size: 1.2rem;
            margin-bottom: 20px;
            position: relative;
            padding-bottom: 10px;
        }

        .footer-heading::after {
            content: "";
            position: absolute;
            left: 0;
            bottom: 0;
            width: 40px;
            height: 3px;
            background-color: var(--primary-color);
        }

        .footer-links {
            list-style: none;
        }

        .footer-link {
            margin-bottom: 12px;
        }

        .footer-link a {
            color: #ccc;
            text-decoration: none;
            transition: var(--transition);
            font-size: 0.95rem;
        }

        .footer-link a:hover {
            color: white;
            padding-left: 5px;
        }

        .footer-contact-item {
            display: flex;
            align-items: center;
            gap: 10px;
            margin-bottom: 15px;
            color: #ccc;
            font-size: 0.95rem;
        }

        .contact-icon {
            color: var(--primary-color);
            font-size: 1.1rem;
        }

        .footer-copyright {
            text-align: center;
            padding-top: 30px;
            margin-top: 30px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            color: #999;
            font-size: 0.9rem;
        }

        /* Loading Animation */
        .loading {
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 40px;
        }

        .spinner {
            width: 40px;
            height: 40px;
            border: 4px solid rgba(102, 126, 234, 0.2);
            border-radius: 50%;
            border-top-color: var(--primary-color);
            animation: spin 1s ease-in-out infinite;
        }

        @keyframes spin {
            to { transform: rotate(360deg); }
        }

        /* Responsive Styles */
        @media (max-width: 768px) {
            .header-title {
                font-size: 2rem;
            }
            
            .header-subtitle {
                font-size: 1rem;
            }
            
            .nav-container {
                flex-direction: column;
                gap: 15px;
            }
            
            .nav-links {
                width: 100%;
                justify-content: center;
            }
            
            .hero-title {
                font-size: 2rem;
            }
            
            .hero-description {
                font-size: 1rem;
            }
            
            .section-title {
                font-size: 1.6rem;
            }
            
            .tools-grid {
                grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
            }
            
            .tool-icon {
                height: 100px;
            }
            
            .subscribe-form {
                flex-direction: column;
                gap: 10px;
            }
            
            .subscribe-button {
                margin-left: 0;
                margin-top: 10px;
                width: 100%;
            }
            
            .footer-container {
                grid-template-columns: 1fr;
                text-align: center;
            }
            
            .footer-heading::after {
                left: 50%;
                transform: translateX(-50%);
            }
            
            .footer-social {
                justify-content: center;
            }
        }

        @media (max-width: 480px) {
            .tools-grid {
                grid-template-columns: 1fr;
            }
            
            .hero-buttons {
                flex-direction: column;
                gap: 10px;
            }
            
            .hero-button {
                width: 100%;
            }
            
            .features-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header class="site-header">
        <div class="header-container">
            <h1 class="header-title">Mini Web Tool</h1>
            <p class="header-subtitle">Your one-stop destination for free online tools to simplify your digital life</p>
        </div>
    </header>

    <!-- Navigation -->
    <nav class="main-nav">
        <div class="nav-container">
            <a href="https://www.miniwebtool.live/" class="nav-logo">
                <i class="fas fa-tools"></i>
                <span>MiniWebTool</span>
            </a>
            <ul class="nav-links">
                <li><a href="https://www.miniwebtool.live/" class="nav-link active">Home</a></li>
                <li><a href="https://www.miniwebtool.live/p/all-tools.html" class="nav-link">All Tools</a></li>
                <li><a href="https://www.miniwebtool.live/p/about-us.html" class="nav-link">About</a></li>
                <li><a href="https://www.miniwebtool.live/p/contact-us.html" class="nav-link">Contact</a></li>
            </ul>
            <div class="search-bar">
                <i class="fas fa-search search-icon"></i>
                <input type="text" class="search-input" placeholder="Search for tools..." id="searchInput">
            </div>
        </div>
    </nav>

    <!-- Main Content -->
    <main class="page-content">
        <!-- Hero Section -->
        <section class="hero-section">
            <div class="hero-content">
                <h2 class="hero-title">Powerful Tools at Your Fingertips</h2>
                <p class="hero-description">Mini Web Tool offers a comprehensive collection of free online utilities to help you with PDFs, images, YouTube, and more. No installation required - just click and use!</p>
                <div class="hero-buttons">
                    <a href="#popular-tools" class="hero-button primary-button">Explore Tools</a>
                    <a href="https://www.miniwebtool.live/p/all-tools.html" class="hero-button secondary-button">View All</a>
                </div>
            </div>
        </section>

        <!-- Popular Tools Section -->
        <section id="popular-tools">
            <h2 class="section-title">Popular Tools</h2>
            <div class="tools-grid" id="popularToolsContainer">
                <!-- Popular tools will be loaded here by JavaScript -->
                <div class="loading">
                    <div class="spinner"></div>
                </div>
            </div>
        </section>

        <!-- Categories Section -->
        <section class="categories-section">
            <h2 class="section-title">Browse by Category</h2>
            <div class="categories">
                <a href="https://www.miniwebtool.live/p/pdf-tools.html" class="category-tag">PDF Tools</a>
                <a href="https://www.miniwebtool.live/p/online-image-tools.html" class="category-tag">Image Tools</a>
                <a href="https://www.miniwebtool.live/p/youtube-tool.html" class="category-tag">YouTube Tools</a>
                <a href="https://www.miniwebtool.live/p/developer-tools.html" class="category-tag">Developer Tools</a>
                <a href="https://www.miniwebtool.live/p/general-web-tools.html" class="category-tag">Web Tools</a>
                <a href="https://www.miniwebtool.live/p/finance-calculator.html" class="category-tag">Finance Tools</a>
            </div>
        </section>

        <!-- All Tools Section -->
        <section id="all-tools">
            <h2 class="section-title">All Tools</h2>
            <div class="tools-grid" id="allToolsContainer">
                <!-- All tools will be loaded here by JavaScript -->
                <div class="loading">
                    <div class="spinner"></div>
                </div>
            </div>
        </section>

        <!-- Features Section -->
        <section class="features-section">
            <h2 class="section-title">Why Choose Mini Web Tool?</h2>
            <div class="features-grid">
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-bolt"></i>
                    </div>
                    <h3 class="feature-title">Fast & Efficient</h3>
                    <p class="feature-description">Our tools are optimized for speed, delivering instant results without any delays or unnecessary processing time.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-lock"></i>
                    </div>
                    <h3 class="feature-title">Secure & Private</h3>
                    <p class="feature-description">Your data never leaves your browser. We don't store your files or information on our servers.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">
                        <i class="fas fa-mobile-alt"></i>
                    </div>
                    <h3 class="feature-title">Mobile Friendly</h3>
                    <p class="feature-description">All our tools work perfectly on any device, whether you're using a computer, tablet, or smartphone.</p>
                </div>
            </div>
        </section>

        <!-- Subscribe Section -->
        <section class="subscribe-section">
            <h2 class="subscribe-title">Stay Updated</h2>
            <p class="subscribe-description">Subscribe to our newsletter to get notified about new tools and updates.</p>
            <form class="subscribe-form">
                <input type="email" class="email-input" placeholder="Enter your email address" required>
                <button type="submit" class="subscribe-button">Subscribe</button>
            </form>
        </section>
    </main>

    <!-- Footer -->
    <footer class="site-footer">
        <div class="footer-container">
            <div class="footer-col">
                <div class="footer-logo">
                    <i class="fas fa-tools"></i>
                    <span>MiniWebTool</span>
                </div>
                <p class="footer-about">Mini Web Tool provides a collection of free, easy-to-use online tools to help you with various tasks without any installation or registration required.</p>
                <div class="footer-social">
                    <a href="#" class="social-icon"><i class="fab fa-facebook-f"></i></a>
                    <a href="#" class="social-icon"><i class="fab fa-twitter"></i></a>
                    <a href="#" class="social-icon"><i class="fab fa-instagram"></i></a>
                    <a href="#" class="social-icon"><i class="fab fa-linkedin-in"></i></a>
                </div>
            </div>
            <div class="footer-col">
                <h3 class="footer-heading">Quick Links</h3>
                <ul class="footer-links">
                    <li class="footer-link"><a href="https://www.miniwebtool.live/">Home</a></li>
                    <li class="footer-link"><a href="https://www.miniwebtool.live/p/all-tools.html">All Tools</a></li>
                    <li class="footer-link"><a href="https://www.miniwebtool.live/p/about-us.html">About Us</a></li>
                    <li class="footer-link"><a href="https://www.miniwebtool.live/p/privacy-policy.html">Privacy Policy</a></li>
                    <li class="footer-link"><a href="https://www.miniwebtool.live/p/terms-and-conditions.html">Terms of Service</a></li>
                </ul>
            </div>
            <div class="footer-col">
                <h3 class="footer-heading">Popular Tools</h3>
                <ul class="footer-links">
                    <li class="footer-link"><a href="https://www.miniwebtool.live/2025/03/pdf-file-compression.html">PDF Compression</a></li>
                    <li class="footer-link"><a href="https://www.miniwebtool.live/2025/03/image-compressor.html">Image Compressor</a></li>
                    <li class="footer-link"><a href="https://www.miniwebtool.live/2025/03/youtube-embed-code-generator.html">YouTube Embed</a></li>
                    <li class="footer-link"><a href="https://www.miniwebtool.live/2025/03/typing-speed-tester.html">Typing Speed Test</a></li>
                    <li class="footer-link"><a href="https://www.miniwebtool.live/2025/03/internet-speed-test.html">Internet Speed Test</a></li>
                </ul>
            </div>
            <div class="footer-col">
                <h3 class="footer-heading">Contact Us</h3>
                <div class="footer-contact-item">
                    <i class="fas fa-envelope contact-icon"></i>
                    <span>contact@miniwebtool.live</span>
                </div>
                <div class="footer-contact-item">
                    <i class="fas fa-map-marker-alt contact-icon"></i>
                    <span>123 Web Street, Digital City</span>
                </div>
            </div>
        </div>
        <div class="footer-copyright">
            &copy; 2023 Mini Web Tool. All rights reserved.
        </div>
    </footer>

    <script>
        document.addEventListener('DOMContentLoaded', function() {
            // Fetch popular tools
            fetchPopularTools();
            
            // Fetch all tools
            fetchAllTools();
            
            // Search functionality
            const searchInput = document.getElementById('searchInput');
            searchInput.addEventListener('input', function() {
                const searchTerm = this.value.toLowerCase();
                filterTools(searchTerm);
            });
        });

        // Function to fetch popular tools
        async function fetchPopularTools() {
            try {
                // In a real implementation, you would fetch this from an API
                // For demonstration, we're using a static list
                const popularTools = [
                    {
                        title: "PDF Compression",
                        description: "Reduce PDF file size while maintaining quality",
                        url: "https://www.miniwebtool.live/2025/03/pdf-file-compression.html",
                        icon: "https://blogger.googleusercontent.com/img/a/AVvXsEgsFNCATs2yNRQjSg7BqYgHa5NiKq1PwQ5rJzafjeyHaMCzkAM4leBTbuI8Dw8dYEGkxv_N9dKJqdBCESgN53FpDc4owToZ6D0n59lKwvgXS2lE1Mzq4AMzlM6oADkz9RbZjHl3L_k14z_zbWNX09sgGPbFau29Z0BMBSnLmuvZcslHoahoQ8C6lrHJUFk=s512",
                        category: "pdf"
                    },
                    {
                        title: "Image Compressor",
                        description: "Compress images without losing quality",
                        url: "https://www.miniwebtool.live/2025/03/image-compressor.html",
                        icon: "https://blogger.googleusercontent.com/img/a/AVvXsEhpmhZyClX2p6-kKzzwuKinHzSV2Xayafhrp5C7scZIugC6pQR7FYYClSdkEr8O2znhVx1hTbVs-t_FvQRlPw3vosZDdoyzkZ7IFxqtdtFfBtrdHA0aLB5BlRyrUpiu-LmU3BkUm4JDVHJPV-KIPrcVGiOriMBS6mxC2tsDt4XjA8trPL1gplMcSv6b7DY=s512",
                        category: "image"
                    },
                    {
                        title: "YouTube Embed",
                        description: "Generate embed code for YouTube videos",
                        url: "https://www.miniwebtool.live/2025/03/youtube-embed-code-generator.html",
                        icon: "https://play-lh.googleusercontent.com/azYV5lXeVhp4G17YkH7zeZ5c4gQYOzSj2CgYpIpJps2J5OTOtOIyUlXzMCDWjQ9QYHE",
                        category: "youtube"
                    },
                    {
                        title: "Typing Speed Test",
                        description: "Test and improve your typing speed",
                        url: "https://www.miniwebtool.live/2025/03/typing-speed-tester.html",
                        icon: "https://play-lh.googleusercontent.com/hSuOQgMElmnsBMw-F5ZrqWSnpf3nZ2AmZPdNALD7G2CRKSxM8ia07ogmkIrAqHIvzKR5",
                        category: "web"
                    },
                    {
                        title: "Internet Speed Test",
                        description: "Check your internet connection speed",
                        url: "https://www.miniwebtool.live/2025/03/internet-speed-test.html",
                        icon: "https://play-lh.googleusercontent.com/9FlRUJNwJZ2Dn2G0Hi-4eadm---Uqo6lK2HYCFh08kJktqwW_h1vVC5wrvywWW6piGGX",
                        category: "web"
                    },
                    {
                        title: "QR Code Reader",
                        description: "Scan and decode QR codes instantly",
                        url: "https://www.miniwebtool.live/2025/03/qr-code-reader.html",
                        icon: "https://play-lh.googleusercontent.com/4ciwCWHhgxfSIPRoLHICpCnuRBRjydYgqMBvLla0q3vhjJpy8wOr-Aa9WX-435Ef-Hk",
                        category: "web"
                    }
                ];

                displayTools(popularTools, 'popularToolsContainer');
            } catch (error) {
                console.error('Error fetching popular tools:', error);
                document.getElementById('popularToolsContainer').innerHTML = '<p>Error loading tools. Please try again later.</p>';
            }
        }

        // Function to fetch all tools
        async function fetchAllTools() {
            try {
                // In a real implementation, you would fetch this from an API
                // For demonstration, we're using a static list
                const allTools = [
                    {
                        title: "PDF Compression",
                        description: "Reduce PDF file size while maintaining quality",
                        url: "https://www.miniwebtool.live/2025/03/pdf-file-compression.html",
                        icon: "https://blogger.googleusercontent.com/img/a/AVvXsEgsFNCATs2yNRQjSg7BqYgHa5NiKq1PwQ5rJzafjeyHaMCzkAM4leBTbuI8Dw8dYEGkxv_N9dKJqdBCESgN53FpDc4owToZ6D0n59lKwvgXS2lE1Mzq4AMzlM6oADkz9RbZjHl3L_k14z_zbWNX09sgGPbFau29Z0BMBSnLmuvZcslHoahoQ8C6lrHJUFk=s512",
                        category: "pdf"
                    },
                    {
                        title: "PDF Merge",
                        description: "Merge multiple PDF files into one",
                        url: "https://www.miniwebtool.live/2025/03/pdf-merge-online.html",
                        icon: "https://play-lh.googleusercontent.com/rERC-MTpbBLqsTKwpBF83An0oEQK-2QkecZQkeiIrUCitIU2Z6xpf4KNZl5sQ-keIQ",
                        category: "pdf"
                    },
                    {
                        title: "Text to PDF",
                        description: "Convert text documents to PDF format",
                        url: "https://www.miniwebtool.live/2025/03/text-to-pdf.html",
                        icon: "https://play-lh.googleusercontent.com/MnUHEBtTVxXz18bPHQO3Qj5EVKT377JlfyKeFUzK22tEHwzLO7vcG9a3pRc-erjbxr1q",
                        category: "pdf"
                    },
                    {
                        title: "Image Compressor",
                        description: "Compress images without losing quality",
                        url: "https://www.miniwebtool.live/2025/03/image-compressor.html",
                        icon: "https://blogger.googleusercontent.com/img/a/AVvXsEhpmhZyClX2p6-kKzzwuKinHzSV2Xayafhrp5C7scZIugC6pQR7FYYClSdkEr8O2znhVx1hTbVs-t_FvQRlPw3vosZDdoyzkZ7IFxqtdtFfBtrdHA0aLB5BlRyrUpiu-LmU3BkUm4JDVHJPV-KIPrcVGiOriMBS6mxC2tsDt4XjA8trPL1gplMcSv6b7DY=s512",
                        category: "image"
                    },
                    {
                        title: "Text to Image",
                        description: "Convert text into image files",
                        url: "https://www.miniwebtool.live/2025/03/text-to-image-converter.html",
                        icon: "https://images.sftcdn.net/images/t_app-icon-m/p/71e40a35-f326-48ca-9efe-07899be6adc6/2771825331/text-to-image-icon.png",
                        category: "image"
                    },
                    {
                        title: "Image Resizer",
                        description: "Resize images to any dimension",
                        url: "https://www.miniwebtool.live/2025/03/image-resizer.html",
                        icon: "https://play-lh.googleusercontent.com/4ciwCWHhgxfSIPRoLHICpCnuRBRjydYgqMBvLla0q3vhjJpy8wOr-Aa9WX-435Ef-Hk",
                        category: "image"
                    },
                    {
                        title: "Image Converter",
                        description: "Convert images between different formats",
                        url: "https://www.miniwebtool.live/2025/03/image-converter.html",
                        icon: "https://icons.iconarchive.com/icons/alecive/flatwoken/512/Apps-Accessories-Media-Converter-icon.png",
                        category: "image"
                    },
                    {
                        title: "Image to PDF",
                        description: "Convert images to PDF documents",
                        url: "https://www.miniwebtool.live/2025/03/image-to-pdf-converter.html",
                        icon: "https://play-lh.googleusercontent.com/0m-0LpXWAZgJOg1Tm4k_KhMZSqgNXhxsLcZnTAJXpp5tyOTqaf-yrV4Vx5gHIQTYdSo",
                        category: "image"
                    },
                    {
                        title: "Compress to 50KB",
                        description: "Compress images to under 50KB",
                        url: "https://www.miniwebtool.live/2025/03/compress-image-to-50kb.html",
                        icon: "https://image.pi7.org/static/img/pi750kbjpeg.png",
                        category: "image"
                    },
                    {
                        title: "Image Cropper",
                        description: "Crop images to your desired size",
                        url: "https://www.miniwebtool.live/2025/03/image-cropper.html",
                        icon: "https://play-lh.googleusercontent.com/Pn43-wReLAxjFe8VPeIPlA_84h4S743DLBQg4-dFVrojFBhulkTZR1_pIkYIYGcbgA",
                        category: "image"
                    },
                    {
                        title: "Typing Speed Test",
                        description: "Test and improve your typing speed",
                        url: "https://www.miniwebtool.live/2025/03/typing-speed-tester.html",
                        icon: "https://play-lh.googleusercontent.com/hSuOQgMElmnsBMw-F5ZrqWSnpf3nZ2AmZPdNALD7G2CRKSxM8ia07ogmkIrAqHIvzKR5",
                        category: "web"
                    },
                    {
                        title: "Internet Speed Test",
                        description: "Check your internet connection speed",
                        url: "https://www.miniwebtool.live/2025/03/internet-speed-test.html",
                        icon: "https://play-lh.googleusercontent.com/9FlRUJNwJZ2Dn2G0Hi-4eadm---Uqo6lK2HYCFh08kJktqwW_h1vVC5wrvywWW6piGGX",
                        category: "web"
                    },
                    {
                        title: "Random Celebrity",
                        description: "Generate random celebrity names",
                        url: "https://www.miniwebtool.live/2025/03/random-celebrity-generator.html",
                        icon: "https://appsliced.co/img_as/images/apps/534260257_150.jpg?img=_1.3",
                        category: "web"
                    },
                    {
                        title: "QR Code Reader",
                        description: "Scan and decode QR codes instantly",
                        url: "https://www.miniwebtool.live/2025/03/qr-code-reader.html",
                        icon: "https://play-lh.googleusercontent.com/4ciwCWHhgxfSIPRoLHICpCnuRBRjydYgqMBvLla0q3vhjJpy8wOr-Aa9WX-435Ef-Hk",
                        category: "web"
                    },
                    {
                        title: "Barcode Reader",
                        description: "Scan and decode barcodes",
                        url: "https://www.miniwebtool.live/2025/03/barcode-reader.html",
                        icon: "https://img.freepik.com/free-vector/scan-product-barcode_78370-3849.jpg",
                        category: "web"
                    },
                    {
                        title: "Barcode Generator",
                        description: "Create custom barcodes",
                        url: "https://www.miniwebtool.live/2025/03/barcode-generator.html",
                        icon: "https://play-lh.googleusercontent.com/LKXw2o_WMormwXjl4tshL9nr6aAFYgQSwV4s4QHbKBkGZR41SaVqgKmcCPJYkxz39zfN",
                        category: "web"
                    },
                    {
                        title: "IFSC Code Lookup",
                        description: "Find bank details using IFSC code",
                        url: "https://www.miniwebtool.live/2025/03/ifsc-code-to-bank-details.html",
                        icon: "https://play-lh.googleusercontent.com/8cT0Y4kkdFuywFo8SxjC7Kv6I3fl2vUitoT9WDDlpZ4fTlV9oHuOnh8rF26ox1H4Mw",
                        category: "finance"
                    },
                    {
                        title: "Currency Exchange",
                        description: "Check currency exchange rates",
                        url: "https://www.miniwebtool.live/2025/03/airport-currency-exchange-rate.html",
                        icon: "https://play-lh.googleusercontent.com/7Mfyiu2sCJri41mlICsLWgPNtOq6mSlmskT5YphmXGilIkaPSChxNfuPWY53IBHLdA",
                        category: "finance"
                    },
                    {
                        title: "Stylish Fonts",
                        description: "Generate stylish text fonts",
                        url: "https://www.miniwebtool.live/2025/03/instagram-vip-bio-stylish-fonts.html",
                        icon: "https://play-lh.googleusercontent.com/QmYqemi5fpbv-nww6dCwtsJeVEXrIfEmkEPOPZD0TVfGQZmf5Vd_P69s3W6fddEh4E5T",
                        category: "web"
                    },
                    {
                        title: "Speedometer",
                        description: "Live GPS speedometer online",
                        url: "https://www.miniwebtool.live/2025/03/gps-speedometer-online.html",
                        icon: "https://play-lh.googleusercontent.com/WxnHp5LU9RRCcj2cWsyzQX8xuPEGBHHUDdkfltjK9M7ZB6BwVCwGnaD2bFckjcZI9g",
                        category: "web"
                    },
                    {
                        title: "Trending Hashtags",
                        description: "Generate trending hashtags",
                        url: "https://www.miniwebtool.live/2025/03/trending-hashtag-generator.html",
                        icon: "https://cdn-icons-png.flaticon.com/512/8135/8135696.png",
                        category: "web"
                    },
                    {
                        title: "Pin Code Locator",
                        description: "Find location by postal code",
                        url: "https://www.miniwebtool.live/2025/03/pin-code-my-location.html",
                        icon: "https://play-lh.googleusercontent.com/QROmWLg7Ko1EzhNWh45lrl-6cFL8FDP1Uo129781wkVRSsZ3wnDiu_GEqyGhZew7tm0",
                        category: "web"
                    },
                    {
                        title: "UPI QR Generator",
                        description: "Create UPI payment QR codes",
                        url: "https://www.miniwebtool.live/2025/03/npci-qr-code-generator.html",
                        icon: "https://digitional.com/wp-content/uploads/2024/07/Upi-generate-aadhar.png",
                        category: "finance"
                    },
                    {
                        title: "IP Address Finder",
                        description: "Find your current IP address",
                        url: "https://www.miniwebtool.live/2025/03/whats-my-ip-address.html",
                        icon: "https://cdn-icons-png.freepik.com/512/6159/6159318.png",
                        category: "web"
                    },
                    {
                        title: "URL Video Player",
                        description: "Play videos from URL directly",
                        url: "https://www.miniwebtool.live/2025/03/online-video-player-from-url.html",
                        icon: "https://play-lh.googleusercontent.com/hruuFq8giU1BFxp04AmIfQJMYeANSHD-P_bL_cS0bEQT8PBHY-vGYebAibpdWrJQWw",
                        category: "web"
                    },
                    {
                        title: "Online Notepad",
                        description: "Simple text editor in browser",
                        url: "https://www.miniwebtool.live/2025/03/online-notepad.html",
                        icon: "https://play-lh.googleusercontent.com/8cT0Y4kkdFuywFo8SxjC7Kv6I3fl2vUitoT9WDDlpZ4fTlV9oHuOnh8rF26ox1H4Mw",
                        category: "web"
                    },
                    {
                        title: "YouTube Embed",
                        description: "Generate embed code for videos",
                        url: "https://www.miniwebtool.live/2025/03/youtube-embed-code-generator.html",
                        icon: "https://play-lh.googleusercontent.com/azYV5lXeVhp4G17YkH7zeZ5c4gQYOzSj2CgYpIpJps2J5OTOtOIyUlXzMCDWjQ9QYHE",
                        category: "youtube"
                    },
                    {
                        title: "YouTube Tags",
                        description: "Extract tags from YouTube videos",
                        url: "https://www.miniwebtool.live/2025/03/youtube-tags-extractor.html",
                        icon: "https://play-lh.googleusercontent.com/CW-_0AmeipJ7hUVeZBmAjIHixQCDp2vliFC5jT6vHOETm45GnxJ7pe9XK3vG207tUPI",
                        category: "youtube"
                    },
                    {
                        title: "YouTube Title Copy",
                        description: "Copy YouTube video titles",
                        url: "https://www.miniwebtool.live/2025/03/youtube-title-copy.html",
                        icon: "https://www.toolsoverflow.com/favicon/favicon.svg",
                        category: "youtube"
                    },
                    {
                        title: "YouTube Description",
                        description: "Copy YouTube descriptions",
                        url: "https://www.miniwebtool.live/2025/03/youtube-description-copy.html",
                        icon: "https://play-lh.googleusercontent.com/vJvwBbfhqmKKLq4HhJoSxcvpHZT4A8c5zHIRSt4SNDGa8UAgdWQD3Ky58FUaYuCyfSJK=w240-h480-rw",
                        category: "youtube"
                    },
                    {
                        title: "YouTube Thumbnail",
                        description: "Download YouTube thumbnails",
                        url: "https://www.miniwebtool.live/2025/03/youtube-thumbnail-download.html",
                        icon: "https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiU6iq3wSiRCUWXhLoWM76bH-WBSwtags3e15NaACuvcg-W9XUKxp73kte-KbZvq9jyQuVlJ0JbSqDczK-U2uNMVU3zhIexNg37H7RZYCeR18bKPpuBhZUsR_t6b48xL_glqynDLZnV9SeZNjiVDoxyw1SUqP7R6pLKAfgvXmH8O_OldHEZxu1_6EQXvkE/s512/play.webp",
                        category: "youtube"
                    },
                    {
                        title: "YouTube Tag Generator",
                        description: "Generate tags for YouTube videos",
                        url: "https://www.miniwebtool.live/2025/03/youtube-tag-generator-free.html",
                        icon: "https://play-lh.googleusercontent.com/GAHfUGP_sBVo3qiw-Zm45FMCOfCPJC3kamC6Sf_VgvHhb2R2T6EOeaOl1RNwWIHD8zo",
                        category: "youtube"
                    },
                    {
                        title: "YouTube View Generator",
                        description: "Generate YouTube view counts",
                        url: "https://www.miniwebtool.live/2025/03/youtube-view-generator-free.html",
                        icon: "https://play-lh.googleusercontent.com/i--7wqUgVv9FwA1xib2qDkI4SKdSqWGxk8ECbAQsDX4exdyiaVDpGNWbTcXH_qmjG7ph",
                        category: "youtube"
                    },
                    {
                        title: "YouTube to MP3",
                        description: "Convert YouTube videos to MP3",
                        url: "https://www.miniwebtool.live/2025/03/youtube-to-mp3-converter.html",
                        icon: "https://img.utdstc.com/icon/817/387/8173871cd991f9f109403223895edf16c20eb61fac03bf3863387468d5264efe:200",
                        category: "youtube"
                    }
                ];

                displayTools(allTools, 'allToolsContainer');
            } catch (error) {
                console.error('Error fetching all tools:', error);
                document.getElementById('allToolsContainer').innerHTML = '<p>Error loading tools. Please try again later.</p>';
            }
        }

        // Function to display tools in the container
        function displayTools(tools, containerId) {
            const container = document.getElementById(containerId);
            if (!container) return;
            
            container.innerHTML = '';
            
            tools.forEach(tool => {
                const toolCard = document.createElement('div');
                toolCard.className = 'tool-card';
                
                // Determine icon class based on category
                let iconClass = '';
                if (tool.category === 'pdf') iconClass = 'analytics';
                else if (tool.category === 'image') iconClass = 'converter';
                else if (tool.category === 'youtube') iconClass = 'generator';
                else if (tool.category === 'finance') iconClass = 'calculator';
                else iconClass = 'checker';
                
                toolCard.innerHTML = `
                    <div class="tool-icon ${iconClass}">
                        <img src="${tool.icon}" alt="${tool.title}" />
                    </div>
                    <div class="tool-details">
                        <h3 class="tool-name">${tool.title}</h3>
                        <p class="tool-description">${tool.description}</p>
                        <a href="${tool.url}" class="tool-button">Use Tool</a>
                    </div>
                `;
                
                container.appendChild(toolCard);
            });
        }

        // Function to filter tools based on search term
        function filterTools(searchTerm) {
            const allToolCards = document.querySelectorAll('#allToolsContainer .tool-card');
            
            allToolCards.forEach(card => {
                const toolName = card.querySelector('.tool-name').textContent.toLowerCase();
                const toolDesc = card.querySelector('.tool-description').textContent.toLowerCase();
                
                if (toolName.includes(searchTerm) {
                    card.style.display = 'flex';
                } else if (toolDesc.includes(searchTerm)) {
                    card.style.display = 'flex';
                } else {
                    card.style.display = 'none';
                }
            });
        }
    </script>
</body>
</html>
