<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ToolKit Pro | Online Image & PDF Tools</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary: #4361EE;
            --primary-light: #6B72FF;
            --primary-dark: #3A56D4;
            --secondary: #FF5E7D;
            --accent: #00C9A7;
            --light: #F8F9FF;
            --dark: #1A1B25;
            --gray: #6C757D;
            --light-gray: #EDF2F7;
            --card-bg: #FFFFFF;
            --border-radius: 12px;
            --shadow-sm: 0 2px 8px rgba(0, 0, 0, 0.05);
            --shadow-md: 0 4px 12px rgba(0, 0, 0, 0.1);
            --shadow-lg: 0 15px 30px rgba(0, 0, 0, 0.15);
            --transition: all 0.3s cubic-bezier(0.25, 0.8, 0.25, 1);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Poppins', sans-serif;
            line-height: 1.6;
            color: var(--dark);
            background-color: var(--light);
            -webkit-font-smoothing: antialiased;
        }

        .container {
            width: 100%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Header */
        header {
            background: var(--card-bg);
            box-shadow: var(--shadow-sm);
            padding: 16px 0;
            position: sticky;
            top: 0;
            z-index: 100;
        }

        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            display: flex;
            align-items: center;
            gap: 10px;
            font-size: 1.5rem;
            font-weight: 700;
            color: var(--primary);
            text-decoration: none;
        }

        .logo-icon {
            font-size: 1.8rem;
            color: var(--primary);
        }

        nav ul {
            display: flex;
            list-style: none;
            gap: 24px;
        }

        nav a {
            text-decoration: none;
            color: var(--dark);
            font-weight: 500;
            transition: var(--transition);
            position: relative;
            padding: 8px 0;
        }

        nav a:hover {
            color: var(--primary);
        }

        nav a::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 0;
            height: 2px;
            background: var(--primary);
            transition: var(--transition);
        }

        nav a:hover::after {
            width: 100%;
        }

        .cta-button {
            background: var(--primary);
            color: white;
            border: none;
            padding: 10px 24px;
            border-radius: 50px;
            font-weight: 600;
            cursor: pointer;
            transition: var(--transition);
            box-shadow: 0 4px 12px rgba(67, 97, 238, 0.3);
        }

        .cta-button:hover {
            background: var(--primary-dark);
            transform: translateY(-2px);
            box-shadow: 0 6px 16px rgba(67, 97, 238, 0.4);
        }

        /* Hero Section */
        .hero {
            padding: 80px 0 60px;
            text-align: center;
            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -10%;
            width: 120%;
            height: 200%;
            background: radial-gradient(circle, rgba(67, 97, 238, 0.08) 0%, rgba(67, 97, 238, 0) 70%);
            z-index: -1;
        }

        .hero h1 {
            font-size: 3rem;
            margin-bottom: 20px;
            background: linear-gradient(to right, var(--primary), var(--primary-light));
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            line-height: 1.2;
        }

        .hero p {
            font-size: 1.2rem;
            color: var(--gray);
            max-width: 700px;
            margin: 0 auto 40px;
        }

        .hero-buttons {
            display: flex;
            gap: 16px;
            justify-content: center;
            margin-bottom: 40px;
        }

        .hero-image {
            max-width: 800px;
            margin: 0 auto;
            border-radius: var(--border-radius);
            box-shadow: var(--shadow-lg);
            overflow: hidden;
            border: 1px solid var(--light-gray);
        }

        .hero-image img {
            width: 100%;
            height: auto;
            display: block;
        }

        /* Tools Section */
        .section-title {
            text-align: center;
            margin-bottom: 40px;
        }

        .section-title h2 {
            font-size: 2.2rem;
            margin-bottom: 16px;
            color: var(--dark);
        }

        .section-title p {
            color: var(--gray);
            max-width: 700px;
            margin: 0 auto;
        }

        .tools-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
            gap: 24px;
            margin: 60px 0;
        }

        .tool-card {
            background: var(--card-bg);
            border-radius: var(--border-radius);
            padding: 30px;
            box-shadow: var(--shadow-md);
            transition: var(--transition);
            text-align: center;
            position: relative;
            overflow: hidden;
            border: 1px solid var(--light-gray);
        }

        .tool-card:hover {
            transform: translateY(-10px);
            box-shadow: var(--shadow-lg);
            border-color: var(--primary-light);
        }

        .tool-icon {
            width: 80px;
            height: 80px;
            background: rgba(67, 97, 238, 0.1);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 20px;
            color: var(--primary);
            font-size: 1.8rem;
            transition: var(--transition);
        }

        .tool-card:hover .tool-icon {
            background: var(--primary);
            color: white;
            transform: scale(1.1);
        }

        .tool-card h3 {
            font-size: 1.3rem;
            margin-bottom: 12px;
            color: var(--dark);
        }

        .tool-card p {
            color: var(--gray);
            font-size: 0.95rem;
            margin-bottom: 20px;
        }

        .tool-link {
            display: inline-flex;
            align-items: center;
            gap: 8px;
            color: var(--primary);
            font-weight: 500;
            text-decoration: none;
            transition: var(--transition);
        }

        .tool-link:hover {
            color: var(--primary-dark);
            gap: 12px;
        }

        /* Categories */
        .categories {
            margin: 80px 0;
        }

        .category-tabs {
            display: flex;
            justify-content: center;
            gap: 8px;
            margin-bottom: 40px;
            flex-wrap: wrap;
        }

        .category-tab {
            padding: 10px 24px;
            background: var(--light-gray);
            border-radius: 50px;
            cursor: pointer;
            transition: var(--transition);
            font-weight: 500;
        }

        .category-tab.active, .category-tab:hover {
            background: var(--primary);
            color: white;
        }

        /* Features */
        .features {
            background: var(--card-bg);
            padding: 80px 0;
            margin: 80px 0;
            position: relative;
        }

        .features::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(135deg, rgba(67, 97, 238, 0.03) 0%, rgba(0, 201, 167, 0.03) 100%);
            z-index: -1;
        }

        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 40px;
        }

        .feature-card {
            display: flex;
            gap: 20px;
        }

        .feature-icon {
            flex-shrink: 0;
            width: 60px;
            height: 60px;
            background: rgba(67, 97, 238, 0.1);
            border-radius: 16px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--primary);
            font-size: 1.5rem;
        }

        .feature-content h3 {
            font-size: 1.2rem;
            margin-bottom: 12px;
            color: var(--dark);
        }

        .feature-content p {
            color: var(--gray);
            font-size: 0.95rem;
        }

        /* CTA Section */
        .cta-section {
            text-align: center;
            padding: 80px 0;
            background: linear-gradient(135deg, var(--primary) 0%, var(--primary-light) 100%);
            color: white;
            border-radius: var(--border-radius);
            margin: 80px 0;
            position: relative;
            overflow: hidden;
        }

        .cta-section::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(255,255,255,0.1) 0%, rgba(255,255,255,0) 70%);
            z-index: 1;
        }

        .cta-content {
            position: relative;
            z-index: 2;
        }

        .cta-section h2 {
            font-size: 2.2rem;
            margin-bottom: 20px;
        }

        .cta-section p {
            max-width: 700px;
            margin: 0 auto 40px;
            opacity: 0.9;
        }

        /* Footer */
        footer {
            background: var(--dark);
            color: white;
            padding: 80px 0 30px;
        }

        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 40px;
            margin-bottom: 60px;
        }

        .footer-column h3 {
            font-size: 1.2rem;
            margin-bottom: 24px;
            position: relative;
            display: inline-block;
        }

        .footer-column h3::after {
            content: '';
            position: absolute;
            left: 0;
            bottom: -10px;
            width: 40px;
            height: 3px;
            background: var(--primary);
            border-radius: 3px;
        }

        .footer-links {
            list-style: none;
        }

        .footer-links li {
            margin-bottom: 12px;
        }

        .footer-links a {
            color: #CBD5E0;
            text-decoration: none;
            transition: var(--transition);
            display: inline-block;
            font-size: 0.95rem;
        }

        .footer-links a:hover {
            color: white;
            transform: translateX(5px);
        }

        .footer-about {
            max-width: 300px;
        }

        .footer-about p {
            color: #CBD5E0;
            font-size: 0.95rem;
            line-height: 1.6;
            margin-bottom: 20px;
        }

        .social-links {
            display: flex;
            gap: 16px;
            margin-top: 20px;
        }

        .social-links a {
            color: white;
            background: rgba(255, 255, 255, 0.1);
            width: 40px;
            height: 40px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: var(--transition);
        }

        .social-links a:hover {
            background: var(--primary);
            transform: translateY(-3px);
        }

        .copyright {
            text-align: center;
            padding-top: 30px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            color: #A0AEC0;
            font-size: 0.9rem;
        }

        /* Responsive Adjustments */
        @media (max-width: 1024px) {
            .hero h1 {
                font-size: 2.5rem;
            }
            
            .section-title h2 {
                font-size: 2rem;
            }
        }

        @media (max-width: 768px) {
            .header-content {
                flex-direction: column;
                gap: 16px;
            }

            nav ul {
                gap: 16px;
                flex-wrap: wrap;
                justify-content: center;
            }

            .hero {
                padding: 60px 0 40px;
            }

            .hero h1 {
                font-size: 2.2rem;
            }

            .hero-buttons {
                flex-direction: column;
                align-items: center;
            }

            .hero p {
                font-size: 1.1rem;
            }

            .tools-grid {
                grid-template-columns: repeat(auto-fill, minmax(240px, 1fr));
            }
        }

        @media (max-width: 480px) {
            .hero {
                padding: 40px 0 30px;
            }

            .hero h1 {
                font-size: 1.8rem;
            }

            .hero p {
                font-size: 1rem;
            }

            .section-title h2 {
                font-size: 1.8rem;
            }

            .tool-card {
                padding: 24px;
            }

            .feature-card {
                flex-direction: column;
            }

            .cta-section h2 {
                font-size: 1.8rem;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="container header-content">
            <a href="#" class="logo">
                <i class="fas fa-tools logo-icon"></i>
                <span>ToolKit Pro</span>
            </a>
            <nav>
                <ul>
                    <li><a href="#">Home</a></li>
                    <li><a href="#">Image Tools</a></li>
                    <li><a href="#">PDF Tools</a></li>
                    <li><a href="#">Features</a></li>
                    <li><a href="#">Pricing</a></li>
                </ul>
            </nav>
            <button class="cta-button">Get Started</button>
        </div>
    </header>

    <main>
        <section class="hero">
            <div class="container">
                <h1>Your Complete Online Toolkit for Images & PDFs</h1>
                <p>Free, powerful tools to optimize, convert, edit and enhance your files without compromising quality.</p>
                
                <div class="hero-buttons">
                    <button class="cta-button">
                        <i class="fas fa-image"></i> Explore Image Tools
                    </button>
                    <button class="cta-button" style="background: var(--secondary); box-shadow: 0 4px 12px rgba(255, 94, 125, 0.3);">
                        <i class="fas fa-file-pdf"></i> Discover PDF Tools
                    </button>
                </div>
                
                <div class="hero-image">
                    <img src="https://images.unsplash.com/photo-1551288049-bebda4e38f71?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80" alt="ToolKit Pro interface">
                </div>
            </div>
        </section>

        <section class="container">
            <div class="section-title">
                <h2>Popular Tools</h2>
                <p>Our most frequently used tools to make your workflow easier</p>
            </div>
            
            <div class="tools-grid">
                <!-- Image Tools -->
                <div class="tool-card">
                    <div class="tool-icon">
                        <i class="fas fa-compress-alt"></i>
                    </div>
                    <h3>Image Compressor</h3>
                    <p>Reduce image file size without losing quality for faster websites and apps</p>
                    <a href="#" class="tool-link">
                        Use Tool <i class="fas fa-arrow-right"></i>
                    </a>
                </div>
                
                <div class="tool-card">
                    <div class="tool-icon">
                        <i class="fas fa-exchange-alt"></i>
                    </div>
                    <h3>Image Converter</h3>
                    <p>Convert between JPG, PNG, WEBP, GIF and other popular formats</p>
                    <a href="#" class="tool-link">
                        Use Tool <i class="fas fa-arrow-right"></i>
                    </a>
                </div>
                
                <div class="tool-card">
                    <div class="tool-icon">
                        <i class="fas fa-crop"></i>
                    </div>
                    <h3>Image Cropper</h3>
                    <p>Crop and resize images to perfect dimensions for social media or websites</p>
                    <a href="#" class="tool-link">
                        Use Tool <i class="fas fa-arrow-right"></i>
                    </a>
                </div>
                
                <!-- PDF Tools -->
                <div class="tool-card">
                    <div class="tool-icon">
                        <i class="fas fa-file-pdf"></i>
                    </div>
                    <h3>PDF Compressor</h3>
                    <p>Reduce PDF file size while maintaining text and image quality</p>
                    <a href="#" class="tool-link">
                        Use Tool <i class="fas fa-arrow-right"></i>
                    </a>
                </div>
                
                <div class="tool-card">
                    <div class="tool-icon">
                        <i class="fas fa-file-word"></i>
                    </div>
                    <h3>PDF to Word</h3>
                    <p>Convert PDF files to editable Word documents with perfect formatting</p>
                    <a href="#" class="tool-link">
                        Use Tool <i class="fas fa-arrow-right"></i>
                    </a>
                </div>
                
                <div class="tool-card">
                    <div class="tool-icon">
                        <i class="fas fa-lock"></i>
                    </div>
                    <h3>PDF Protector</h3>
                    <p>Add passwords and permissions to secure your PDF documents</p>
                    <a href="#" class="tool-link">
                        Use Tool <i class="fas fa-arrow-right"></i>
                    </a>
                </div>
            </div>
        </section>

        <section class="categories container">
            <div class="section-title">
                <h2>Browse by Category</h2>
                <p>Find the perfect tool for your specific needs</p>
            </div>
            
            <div class="category-tabs">
                <div class="category-tab active">All Tools</div>
                <div class="category-tab">Image Tools</div>
                <div class="category-tab">PDF Tools</div>
                <div class="category-tab">Converters</div>
                <div class="category-tab">Optimizers</div>
                <div class="category-tab">Editors</div>
            </div>
            
            <!-- Tool cards would be filtered by JavaScript based on category selection -->
        </section>

        <section class="features">
            <div class="container">
                <div class="section-title">
                    <h2>Why Choose ToolKit Pro</h2>
                    <p>We provide the best experience for all your file processing needs</p>
                </div>
                
                <div class="features-grid">
                    <div class="feature-card">
                        <div class="feature-icon">
                            <i class="fas fa-bolt"></i>
                        </div>
                        <div class="feature-content">
                            <h3>Lightning Fast</h3>
                            <p>Our tools process files in seconds using advanced browser-based technology, no waiting in queues.</p>
                        </div>
                    </div>
                    
                    <div class="feature-card">
                        <div class="feature-icon">
                            <i class="fas fa-lock"></i>
                        </div>
                        <div class="feature-content">
                            <h3>100% Secure</h3>
                            <p>All processing happens in your browser. Your files never leave your computer unless you choose to save them.</p>
                        </div>
                    </div>
                    
                    <div class="feature-card">
                        <div class="feature-icon">
                            <i class="fas fa-trophy"></i>
                        </div>
                        <div class="feature-content">
                            <h3>Premium Quality</h3>
                            <p>Advanced algorithms ensure your files maintain maximum quality while achieving optimal compression.</p>
                        </div>
                    </div>
                    
                    <div class="feature-card">
                        <div class="feature-icon">
                            <i class="fas fa-dollar-sign"></i>
                        </div>
                        <div class="feature-content">
                            <h3>Free Forever</h3>
                            <p>All our basic tools are completely free with no hidden costs or watermarks on your files.</p>
                        </div>
                    </div>
                    
                    <div class="feature-card">
                        <div class="feature-icon">
                            <i class="fas fa-desktop"></i>
                        </div>
                        <div class="feature-content">
                            <h3>No Installation</h3>
                            <p>Works directly in your web browser on any device - no software to download or install.</p>
                        </div>
                    </div>
                    
                    <div class="feature-card">
                        <div class="feature-icon">
                            <i class="fas fa-infinity"></i>
                        </div>
                        <div class="feature-content">
                            <h3>Unlimited Use</h3>
                            <p>Process as many files as you need with no daily limits or restrictions.</p>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <section class="cta-section">
            <div class="container cta-content">
                <h2>Ready to Optimize Your Workflow?</h2>
                <p>Join thousands of professionals who use ToolKit Pro daily to save time and enhance their productivity</p>
                <button class="cta-button" style="background: white; color: var(--primary); box-shadow: 0 4px 12px rgba(0,0,0,0.15);">
                    <i class="fas fa-rocket"></i> Get Started Now
                </button>
            </div>
        </section>
    </main>

    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-column footer-about">
                    <h3>ToolKit Pro</h3>
                    <p>Your complete online toolkit for image and PDF processing. Free, fast, and secure tools for professionals and hobbyists alike.</p>
                    <div class="social-links">
                        <a href="#"><i class="fab fa-twitter"></i></a>
                        <a href="#"><i class="fab fa-facebook-f"></i></a>
                        <a href="#"><i class="fab fa-instagram"></i></a>
                        <a href="#"><i class="fab fa-github"></i></a>
                    </div>
                </div>
                
                <div class="footer-column">
                    <h3>Image Tools</h3>
                    <ul class="footer-links">
                        <li><a href="#">Compressor</a></li>
                        <li><a href="#">Converter</a></li>
                        <li><a href="#">Resizer</a></li>
                        <li><a href="#">Cropper</a></li>
                        <li><a href="#">Editor</a></li>
                    </ul>
                </div>
                
                <div class="footer-column">
                    <h3>PDF Tools</h3>
                    <ul class="footer-links">
                        <li><a href="#">Compressor</a></li>
                        <li><a href="#">Converter</a></li>
                        <li><a href="#">Merger</a></li>
                        <li><a href="#">Splitter</a></li>
                        <li><a href="#">Protector</a></li>
                    </ul>
                </div>
                
                <div class="footer-column">
                    <h3>Company</h3>
                    <ul class="footer-links">
                        <li><a href="#">About Us</a></li>
                        <li><a href="#">Blog</a></li>
                        <li><a href="#">Careers</a></li>
                        <li><a href="#">Contact</a></li>
                        <li><a href="#">Privacy Policy</a></li>
                    </ul>
                </div>
            </div>
            
            <div class="copyright">
                &copy; 2023 ToolKit Pro. All rights reserved.
            </div>
        </div>
    </footer>

    <script>
        // Simple JavaScript for interactive elements
        document.addEventListener('DOMContentLoaded', function() {
            // Category tabs functionality
            const tabs = document.querySelectorAll('.category-tab');
            tabs.forEach(tab => {
                tab.addEventListener('click', function() {
                    tabs.forEach(t => t.classList.remove('active'));
                    this.classList.add('active');
                    // Here you would add code to filter tools by category
                });
            });
            
            // Smooth scrolling for anchor links
            document.querySelectorAll('a[href^="#"]').forEach(anchor => {
                anchor.addEventListener('click', function(e) {
                    e.preventDefault();
                    document.querySelector(this.getAttribute('href')).scrollIntoView({
                        behavior: 'smooth'
                    });
                });
            });
        });
    </script>
</body>
</html># index.html.
