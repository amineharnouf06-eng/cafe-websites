# cafe-websites<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Café de Luxe | Premium Experience</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700&family=Montserrat:wght@300;400;500&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Montserrat', sans-serif;
            color: #3c2f2d;
            line-height: 1.6;
            background-color: #f9f6f3;
        }
        
        h1, h2, h3, h4 {
            font-family: 'Playfair Display', serif;
            font-weight: 700;
        }
        
        .container {
            width: 100%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        /* Header */
        header {
            background-color: #3c2f2d;
            color: #e0c9a6;
            padding: 20px 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
        }
        
        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            font-family: 'Playfair Display', serif;
            font-size: 28px;
            font-weight: 700;
        }
        
        .logo span {
            color: #c9a992;
        }
        
        nav ul {
            display: flex;
            list-style: none;
        }
        
        nav ul li {
            margin-left: 30px;
        }
        
        nav ul li a {
            color: #e0c9a6;
            text-decoration: none;
            font-size: 16px;
            transition: color 0.3s;
        }
        
        nav ul li a:hover {
            color: #ffffff;
        }
        
        /* Hero Section */
        .hero {
            height: 100vh;
            background: linear-gradient(rgba(60, 47, 45, 0.7), rgba(60, 47, 45, 0.7)), url('https://images.unsplash.com/photo-1445116572660-236099ec97a0?ixlib=rb-4.0.3&auto=format&fit=crop&w=1500&q=80') no-repeat center center/cover;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: #fff;
            padding-top: 80px;
        }
        
        .hero-content {
            max-width: 800px;
        }
        
        .hero h1 {
            font-size: 4rem;
            margin-bottom: 20px;
            color: #e0c9a6;
        }
        
        .hero p {
            font-size: 1.2rem;
            margin-bottom: 30px;
            font-weight: 300;
        }
        
        .btn {
            display: inline-block;
            background-color: #c9a992;
            color: #3c2f2d;
            padding: 12px 30px;
            text-decoration: none;
            border-radius: 30px;
            font-weight: 500;
            transition: all 0.3s;
        }
        
        .btn:hover {
            background-color: #e0c9a6;
            transform: translateY(-3px);
        }
        
        /* Sections */
        section {
            padding: 80px 0;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 50px;
        }
        
        .section-title h2 {
            font-size: 2.5rem;
            color: #3c2f2d;
            position: relative;
            display: inline-block;
            padding-bottom: 15px;
        }
        
        .section-title h2::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 3px;
            background-color: #c9a992;
        }
        
        /* About */
        .about-content {
            display: flex;
            align-items: center;
            gap: 50px;
        }
        
        .about-text {
            flex: 1;
        }
        
        .about-image {
            flex: 1;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }
        
        .about-image img {
            width: 100%;
            height: auto;
            display: block;
        }
        
        /* Menu */
        .menu {
            background-color: #f1ebe5;
        }
        
        .menu-items {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .menu-item {
            background-color: #fff;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            transition: transform 0.3s;
        }
        
        .menu-item:hover {
            transform: translateY(-10px);
        }
        
        .menu-item img {
            width: 100%;
            height: 200px;
            object-fit: cover;
        }
        
        .menu-item-content {
            padding: 20px;
        }
        
        .menu-item h3 {
            font-size: 1.5rem;
            margin-bottom: 10px;
        }
        
        .menu-item p {
            color: #7a6a65;
            margin-bottom: 15px;
        }
        
        .price {
            font-weight: 700;
            color: #c9a992;
            font-size: 1.2rem;
        }
        
        /* Gallery */
        .gallery-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
        }
        
        .gallery-item {
            height: 250px;
            border-radius: 10px;
            overflow: hidden;
            position: relative;
        }
        
        .gallery-item img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s;
        }
        
        .gallery-item:hover img {
            transform: scale(1.1);
        }
        
        /* Contact */
        .contact {
            background-color: #3c2f2d;
            color: #e0c9a6;
        }
        
        .contact-container {
            display: flex;
            gap: 50px;
        }
        
        .contact-info, .contact-form {
            flex: 1;
        }
        
        .contact-info h3 {
            font-size: 1.8rem;
            margin-bottom: 20px;
            color: #c9a992;
        }
        
        .contact-details {
            margin-bottom: 30px;
        }
        
        .contact-details p {
            margin-bottom: 10px;
            display: flex;
            align-items: center;
        }
        
        .contact-details i {
            margin-right: 10px;
            color: #c9a992;
        }
        
        .social-links {
            display: flex;
            gap: 15px;
        }
        
        .social-links a {
            display: inline-block;
            width: 40px;
            height: 40px;
            background-color: #c9a992;
            color: #3c2f2d;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: all 0.3s;
        }
        
        .social-links a:hover {
            background-color: #e0c9a6;
            transform: translateY(-3px);
        }
        
        .form-group {
            margin-bottom: 20px;
        }
        
        .form-group input, .form-group textarea {
            width: 100%;
            padding: 12px;
            border: none;
            border-radius: 5px;
            background-color: #f9f6f3;
            color: #3c2f2d;
        }
        
        .form-group textarea {
            height: 120px;
            resize: vertical;
        }
        
        /* Footer */
        footer {
            background-color: #2a211f;
            color: #e0c9a6;
            padding: 30px 0;
            text-align: center;
        }
        
        /* Responsive */
        @media (max-width: 768px) {
            .header-container {
                flex-direction: column;
            }
            
            nav ul {
                margin-top: 20px;
            }
            
            nav ul li {
                margin-left: 15px;
                margin-right: 15px;
            }
            
            .hero h1 {
                font-size: 2.5rem;
            }
            
            .about-content, .contact-container {
                flex-direction: column;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container header-container">
            <div class="logo">Café <span>de Luxe</span></div>
            <nav>
                <ul>
                    <li><a href="#home">Home</a></li>
                    <li><a href="#about">About</a></li>
                    <li><a href="#menu">Menu</a></li>
                    <li><a href="#gallery">Gallery</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section id="home" class="hero">
        <div class="container hero-content">
            <h1>Experience Luxury in Every Sip</h1>
            <p>Indulge in the finest coffee blends and exquisite pastries in an atmosphere of refined elegance.</p>
            <a href="#reservation" class="btn">Make a Reservation</a>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="about">
        <div class="container">
            <div class="section-title">
                <h2>Our Story</h2>
            </div>
            <div class="about-content">
                <div class="about-text">
                    <h3>Where Tradition Meets Luxury</h3>
                    <p>Founded in 2010, Café de Luxe began as a small passion project between two coffee enthusiasts with a vision to create a space where people could experience coffee as a luxury experience rather than just a daily ritual.</p>
                    <p>Today, we source our beans from the world's finest coffee plantations, roast them to perfection in-house, and craft each beverage with meticulous attention to detail. Our patisserie works with award-winning chefs to create desserts that are both visually stunning and delightfully delicious.</p>
                    <p>At Café de Luxe, we believe that the coffee experience should engage all the senses, from the rich aroma of freshly ground beans to the elegant presentation of each cup.</p>
                </div>
                <div class="about-image">
                    <img src="https://images.unsplash.com/photo-1554118811-1e0d58224f24?ixlib=rb-4.0.3&auto=format&fit=crop&w=1500&q=80" alt="Café Interior">
                </div>
            </div>
        </div>
    </section>

    <!-- Menu Section -->
    <section id="menu" class="menu">
        <div class="container">
            <div class="section-title">
                <h2>Signature Offerings</h2>
            </div>
            <div class="menu-items">
                <div class="menu-item">
                    <img src="https://images.unsplash.com/photo-1495474472287-4d71bcdd2085?ixlib=rb-4.0.3&auto=format&fit=crop&w=1500&q=80" alt="Luxe Latte">
                    <div class="menu-item-content">
                        <h3>Luxe Latte</h3>
                        <p>Our signature latte made with single-origin espresso and velvet-textured milk, finished with hand-crafted latte art.</p>
                        <span class="price">$8.50</span>
                    </div>
                </div>
                <div class="menu-item">
                    <img src="https://images.unsplash.com/photo-1564894809617-ef2e6c8fc041?ixlib=rb-4.0.3&auto=format&fit=crop&w=1500&q=80" alt="Gold Rush Mocha">
                    <div class="menu-item-content">
                        <h3>Gold Rush Mocha</h3>
                        <p>Premium dark chocolate, espresso, and a hint of gold dust, topped with whipped cream and edible gold leaf.</p>
                        <span class="price">$12.00</span>
                    </div>
                </div>
                <div class="menu-item">
                    <img src="https://images.unsplash.com/photo-1559715745-e1b33a271c8f?ixlib=rb-4.0.3&auto=format&fit=crop&w=1500&q=80" alt="Truffle Delight">
                    <div class="menu-item-content">
                        <h3>Truffle Delight</h3>
                        <p>Decadent dark chocolate truffle cake with layers of ganache and a delicate gold-dusted finish.</p>
                        <span class="price">$9.75</span>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Gallery Section -->
    <section id="gallery" class="gallery">
        <div class="container">
            <div class="section-title">
                <h2>Our Ambiance</h2>
            </div>
            <div class="gallery-grid">
                <div class="gallery-item">
                    <img src="https://images.unsplash.com/photo-1445116572660-236099ec97a0?ixlib=rb-4.0.3&auto=format&fit=crop&w=1500&q=80" alt="Café Interior">
                </div>
                <div class="gallery-item">
                    <img src="https://images.unsplash.com/photo-1578662996442-48f60103fc96?ixlib=rb-4.0.3&auto=format&fit=crop&w=1500&q=80" alt="Coffee Art">
                </div>
                <div class="gallery-item">
                    <img src="https://images.unsplash.com/photo-1481833761820-0509d3217039?ixlib=rb-4.0.3&auto=format&fit=crop&w=1500&q=80" alt="Pastries">
                </div>
                <div class="gallery-item">
                    <img src="https://images.unsplash.com/photo-1559925390-28a2d3b4b8e5?ixlib=rb-4.0.3&auto=format&fit=crop&w=1500&q=80" alt="Coffee Making">
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="contact">
        <div class="container">
            <div class="section-title">
                <h2>Visit Us</h2>
            </div>
            <div class="contact-container">
                <div class="contact-info">
                    <h3>Get in Touch</h3>
                    <div class="contact-details">
                        <p><i class="fas fa-map-marker-alt"></i> 123 Luxury Lane, Prestige District, Marrakech</p>
                        <p><i class="fas fa-phone"></i> +212 5 1234 5678</p>
                        <p><i class="fas fa-envelope"></i> info@cafedeluxe.com</p>
                        <p><i class="fas fa-clock"></i> Open daily: 7:00 AM - 11:00 PM</p>
                    </div>
                    <div class="social-links">
                        <a href="#"><i class="fab fa-facebook-f"></i></a>
                        <a href="#"><i class="fab fa-instagram"></i></a>
                        <a href="#"><i class="fab fa-twitter"></i></a>
                        <a href="#"><i class="fab fa-tripadvisor"></i></a>
                    </div>
                </div>
                <div class="contact-form">
                    <h3>Make a Reservation</h3>
                    <form>
                        <div class="form-group">
                            <input type="text" placeholder="Your Name" required>
                        </div>
                        <div class="form-group">
                            <input type="email" placeholder="Your Email" required>
                        </div>
                        <div class="form-group">
                            <input type="tel" placeholder="Your Phone" required>
                        </div>
                        <div class="form-group">
                            <input type="date" required>
                        </div>
                        <div class="form-group">
                            <input type="time" required>
                        </div>
                        <div class="form-group">
                            <textarea placeholder="Special Requests"></textarea>
                        </div>
                        <button type="submit" class="btn">Book Now</button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <p>&copy; 2023 Café de Luxe. All rights reserved.</p>
        </div>
    </footer>
</body>
</html>
