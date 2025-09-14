# koraykanbur.github.io
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Streamline | Premium Custom Swim Caps</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --color-black: #000000;
            --color-white: #FFFFFF;
            --color-navy: #0A1D37;
            --color-accent: #1E4A76;
            --spacing-xs: 0.5rem;
            --spacing-sm: 1rem;
            --spacing-md: 2rem;
            --spacing-lg: 4rem;
            --spacing-xl: 8rem;
            --border-radius: 4px;
            --transition: all 0.3s ease;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Inter', sans-serif;
            color: var(--color-black);
            background-color: var(--color-white);
            line-height: 1.6;
            overflow-x: hidden;
        }

        a {
            text-decoration: none;
            color: inherit;
            transition: var(--transition);
        }

        ul {
            list-style: none;
        }

        img {
            max-width: 100%;
            height: auto;
            display: block;
        }

        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
        }

        /* Header */
        header {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            background-color: var(--color-white);
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.05);
            z-index: 1000;
            padding: var(--spacing-sm) 0;
        }

        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 1.8rem;
            font-weight: 700;
            color: var(--color-navy);
        }

        .nav-menu {
            display: flex;
            gap: var(--spacing-md);
        }

        .nav-link {
            font-weight: 500;
            position: relative;
        }

        .nav-link::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 2px;
            background-color: var(--color-navy);
            transition: var(--transition);
        }

        .nav-link:hover::after {
            width: 100%;
        }

        .cta-button {
            background-color: var(--color-navy);
            color: var(--color-white);
            padding: 0.6rem 1.5rem;
            border-radius: var(--border-radius);
            font-weight: 500;
            transition: var(--transition);
        }

        .cta-button:hover {
            background-color: var(--color-accent);
            transform: translateY(-2px);
        }

        /* Hero Section */
        .hero {
            padding-top: var(--spacing-xl);
            padding-bottom: var(--spacing-lg);
            min-height: 100vh;
            display: flex;
            align-items: center;
            background: linear-gradient(135deg, rgba(255,255,255,1) 0%, rgba(245,248,255,1) 100%);
        }

        .hero-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: var(--spacing-lg);
            align-items: center;
        }

        .hero-text {
            opacity: 0;
            transform: translateY(20px);
            animation: fadeInUp 1s ease forwards 0.5s;
        }

        .hero-title {
            font-size: 3.5rem;
            font-weight: 700;
            line-height: 1.2;
            margin-bottom: var(--spacing-md);
            color: var(--color-navy);
        }

        .hero-subtitle {
            font-size: 1.2rem;
            font-weight: 400;
            margin-bottom: var(--spacing-md);
            color: var(--color-black);
        }

        .hero-image {
            opacity: 0;
            transform: translateY(20px);
            animation: fadeInUp 1s ease forwards 0.8s;
            position: relative;
        }

        .hero-image::before {
            content: '';
            position: absolute;
            top: -20px;
            right: -20px;
            width: 100%;
            height: 100%;
            border: 2px solid var(--color-navy);
            border-radius: var(--border-radius);
            z-index: -1;
        }

        /* Features Section */
        .features {
            padding: var(--spacing-xl) 0;
            background-color: var(--color-white);
        }

        .section-title {
            text-align: center;
            font-size: 2.5rem;
            font-weight: 700;
            margin-bottom: var(--spacing-lg);
            color: var(--color-navy);
        }

        .features-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: var(--spacing-md);
        }

        .feature-card {
            text-align: center;
            padding: var(--spacing-md);
            border-radius: var(--border-radius);
            transition: var(--transition);
            opacity: 0;
            transform: translateY(20px);
        }

        .feature-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
        }

        .feature-icon {
            width: 60px;
            height: 60px;
            margin: 0 auto var(--spacing-sm);
            background-color: var(--color-navy);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--color-white);
            font-size: 1.5rem;
        }

        .feature-title {
            font-size: 1.3rem;
            font-weight: 600;
            margin-bottom: var(--spacing-xs);
            color: var(--color-navy);
        }

        /* Products Section */
        .products {
            padding: var(--spacing-xl) 0;
            background-color: #f8f9fa;
        }

        .products-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: var(--spacing-md);
        }

        .product-card {
            background-color: var(--color-white);
            border-radius: var(--border-radius);
            overflow: hidden;
            transition: var(--transition);
            opacity: 0;
            transform: translateY(20px);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
        }

        .product-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.1);
        }

        .product-image {
            height: 250px;
            background-color: #f1f5f9;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .product-content {
            padding: var(--spacing-md);
        }

        .product-title {
            font-size: 1.2rem;
            font-weight: 600;
            margin-bottom: var(--spacing-xs);
            color: var(--color-navy);
        }

        /* CTA Section */
        .cta-section {
            padding: var(--spacing-xl) 0;
            background-color: var(--color-navy);
            color: var(--color-white);
            text-align: center;
        }

        .cta-title {
            font-size: 2.5rem;
            font-weight: 700;
            margin-bottom: var(--spacing-md);
        }

        .cta-subtitle {
            font-size: 1.2rem;
            margin-bottom: var(--spacing-md);
            max-width: 600px;
            margin-left: auto;
            margin-right: auto;
        }

        /* Footer */
        footer {
            padding: var(--spacing-lg) 0;
            background-color: var(--color-black);
            color: var(--color-white);
        }

        .footer-container {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: var(--spacing-md);
        }

        .footer-logo {
            font-size: 1.8rem;
            font-weight: 700;
            margin-bottom: var(--spacing-sm);
        }

        .footer-heading {
            font-size: 1.2rem;
            font-weight: 600;
            margin-bottom: var(--spacing-sm);
        }

        .footer-links li {
            margin-bottom: var(--spacing-xs);
        }

        .footer-links a:hover {
            color: rgba(255, 255, 255, 0.7);
        }

        .social-links {
            display: flex;
            gap: var(--spacing-sm);
            margin-top: var(--spacing-sm);
        }

        .social-link {
            width: 40px;
            height: 40px;
            border-radius: 50%;
            background-color: rgba(255, 255, 255, 0.1);
            display: flex;
            align-items: center;
            justify-content: center;
            transition: var(--transition);
        }

        .social-link:hover {
            background-color: var(--color-navy);
            transform: translateY(-3px);
        }

        .copyright {
            text-align: center;
            margin-top: var(--spacing-lg);
            padding-top: var(--spacing-md);
            border-top: 1px solid rgba(255, 255, 255, 0.1);
        }

        /* Animations */
        @keyframes fadeInUp {
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        /* Responsive Design */
        @media (max-width: 992px) {
            .hero-content {
                grid-template-columns: 1fr;
                text-align: center;
            }
            
            .features-grid,
            .products-grid {
                grid-template-columns: repeat(2, 1fr);
            }
            
            .footer-container {
                grid-template-columns: repeat(2, 1fr);
            }
        }

        @media (max-width: 576px) {
            .features-grid,
            .products-grid {
                grid-template-columns: 1fr;
            }
            
            .footer-container {
                grid-template-columns: 1fr;
            }
            
            .hero-title {
                font-size: 2.5rem;
            }
            
            .nav-menu {
                display: none;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container header-container">
            <a href="#" class="logo">Streamline</a>
            <nav>
                <ul class="nav-menu">
                    <li><a href="#" class="nav-link">Home</a></li>
                    <li><a href="#" class="nav-link">Products</a></li>
                    <li><a href="#" class="nav-link">Customization</a></li>
                    <li><a href="#" class="nav-link">Teams</a></li>
                    <li><a href="#" class="nav-link">About</a></li>
                    <li><a href="#" class="nav-link">Contact</a></li>
                </ul>
            </nav>
            <a href="#" class="cta-button">Order Now</a>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero">
        <div class="container hero-content">
            <div class="hero-text">
                <h1 class="hero-title">Elevate Your Swim Experience with Custom Caps</h1>
                <p class="hero-subtitle">Premium quality, fully customizable swim caps for teams and individuals across the UAE.</p>
                <a href="#" class="cta-button">Explore Collections</a>
            </div>
            <div class="hero-image">
                <img src="data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iNjAwIiBoZWlnaHQ9IjUwMCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj48cmVjdCB3aWR0aD0iMTAwJSIgaGVpZ2h0PSIxMDAlIiBmaWxsPSIjZjFmNWY5Ii8+PGNpcmNsZSBjeD0iMzAwIiBjeT0iMjUwIiByPSIxMDAiIGZpbGw9IiMwQTFEMzciLz48dGV4dCB4PSIzMDAiIHk9IjI1MCIgZm9udC1mYW1pbHk9IkFyaWFsIiBmb250LXNpemU9IjE4IiBmaWxsPSIjRkZGRkZGIiB0ZXh0LWFuY2hvcj0ibWlkZGxlIiBkeT0iLjNlbSI+U1RSRUFNTElORTwvdGV4dD48L3N2Zz4=" alt="Streamline Custom Swim Cap">
            </div>
        </div>
    </section>

    <!-- Features Section -->
    <section class="features">
        <div class="container">
            <h2 class="section-title">Why Choose Streamline</h2>
            <div class="features-grid">
                <div class="feature-card">
                    <div class="feature-icon">✓</div>
                    <h3 class="feature-title">Premium Materials</h3>
                    <p>Made from high-quality silicone for durability and comfort.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">🎨</div>
                    <h3 class="feature-title">Fully Customizable</h3>
                    <p>Design your own caps with logos, colors, and text.</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">🚀</div>
                    <h3 class="feature-title">Fast Turnaround</h3>
                    <p>Quick production and delivery across the UAE.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Products Section -->
    <section class="products">
        <div class="container">
            <h2 class="section-title">Our Collections</h2>
            <div class="products-grid">
                <div class="product-card">
                    <div class="product-image">
                        <img src="data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMzAwIiBoZWlnaHQ9IjMwMCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj48cmVjdCB3aWR0aD0iMTAwJSIgaGVpZ2h0PSIxMDAlIiBmaWxsPSIjMUI0QTc2Ii8+PGNpcmNsZSBjeD0iMTUwIiBjeT0iMTUwIiByPSI3MCIgZmlsbD0iI0ZGRkZGRiIvPjwvc3ZnPg==" alt="Team Swim Caps">
                    </div>
                    <div class="product-content">
                        <h3 class="product-title">Team Caps</h3>
                        <p>Custom designs for swim teams and clubs.</p>
                    </div>
                </div>
                <div class="product-card">
                    <div class="product-image">
                        <img src="data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMzAwIiBoZWlnaHQ9IjMwMCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj48cmVjdCB3aWR0aD0iMTAwJSIgaGVpZ2h0PSIxMDAlIiBmaWxsPSIjRkZGRkZGIi8+PGNpcmNsZSBjeD0iMTUwIiBjeT0iMTUwIiByPSI3MCIgZmlsbD0iIzBCMUQzNyIvPjwvc3ZnPg==" alt="Competition Swim Caps">
                    </div>
                    <div class="product-content">
                        <h3 class="product-title">Competition Caps</h3>
                        <p>High-performance caps for serious swimmers.</p>
                    </div>
                </div>
                <div class="product-card">
                    <div class="product-image">
                        <img src="data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMzAwIiBoZWlnaHQ9IjMwMCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj48cmVjdCB3aWR0aD0iMTAwJSIgaGVpZ2h0PSIxMDAlIiBmaWxsPSIjMUI0QTc2Ii8+PHBvbHlnb24gcG9pbnRzPSIxNTAsODAgMjIwLDIyMCA4MCwyMjAiIGZpbGw9IiNGRkZGRkYiLz48L3N2Zz4=" alt="Custom Design Caps">
                    </div>
                    <div class="product-content">
                        <h3 class="product-title">Custom Designs</h3>
                        <p>Unique patterns and personalized swim caps.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- CTA Section -->
    <section class="cta-section">
        <div class="container">
            <h2 class="cta-title">Ready to Design Your Swim Caps?</h2>
            <p class="cta-subtitle">Get in touch with our team to create custom swim caps that represent your brand or team identity.</p>
            <a href="#" class="cta-button">Start Your Order</a>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container footer-container">
            <div class="footer-info">
                <div class="footer-logo">Streamline</div>
                <p>Premium custom swim caps for teams and individuals across the UAE.</p>
                <div class="social-links">
                    <a href="https://instagram.com/streamline.ae" class="social-link">IG</a>
                    <a href="#" class="social-link">FB</a>
                    <a href="#" class="social-link">TW</a>
                </div>
            </div>
            <div class="footer-links">
                <h3 class="footer-heading">Products</h3>
                <ul>
                    <li><a href="#">Team Caps</a></li>
                    <li><a href="#">Competition Caps</a></li>
                    <li><a href="#">Custom Designs</a></li>
                    <li><a href="#">Accessories</a></li>
                </ul>
            </div>
            <div class="footer-links">
                <h3 class="footer-heading">Company</h3>
                <ul>
                    <li><a href="#">About Us</a></li>
                    <li><a href="#">Contact</a></li>
                    <li><a href="#">Shipping</a></li>
                    <li><a href="#">Returns</a></li>
                </ul>
            </div>
            <div class="footer-links">
                <h3 class="footer-heading">Contact</h3>
                <ul>
                    <li>Dubai, UAE</li>
                    <li>info@streamline.ae</li>
                    <li>+971 4 123 4567</li>
                </ul>
            </div>
        </div>
        <div class="container copyright">
            <p>&copy; 2023 Streamline. All rights reserved.</p>
        </div>
    </footer>

    <script>
        // Simple animation for elements when they come into view
        document.addEventListener('DOMContentLoaded', function() {
            const animatedElements = document.querySelectorAll('.feature-card, .product-card');
            
            const observer = new IntersectionObserver((entries) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        entry.target.style.animation = `fadeInUp 1s ease forwards ${entry.target.dataset.delay || '0s'}`;
                        observer.unobserve(entry.target);
                    }
                });
            }, { threshold: 0.1 });
            
            animatedElements.forEach((el, index) => {
                el.style.opacity = '0';
                el.style.transform = 'translateY(20px)';
                el.dataset.delay = `${index * 0.2}s`;
                observer.observe(el);
            });
        });
    </script>
</body>
</html>
