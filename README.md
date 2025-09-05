<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Black Swan Holdings is a diversified investment and holding company delivering excellence through specialized subsidiaries across multiple industries.">
    <title>Black Swan Holdings Pty Ltd</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Segoe+UI:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary: #1a1a1a;
            --secondary: #2c2c2c;
            --accent: #b38b6d;
            --accent-light: #d6a989;
            --text: #ffffff;
            --text-secondary: #cccccc;
            --transition: all 0.3s ease;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: var(--primary);
            color: var(--text);
            line-height: 1.6;
            overflow-x: hidden;
        }
        
        /* Skip link for accessibility */
        .skip-link {
            position: absolute;
            top: -40px;
            left: 0;
            background: var(--accent);
            color: var(--primary);
            padding: 8px;
            z-index: 1000;
            transition: var(--transition);
        }
        
        .skip-link:focus {
            top: 0;
        }
        
        header {
            background-color: var(--secondary);
            padding: 1rem 2rem;
            position: sticky;
            top: 0;
            z-index: 100;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.3);
        }
        
        .header-container {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            display: flex;
            align-items: center;
            text-decoration: none;
            color: var(--text);
        }
        
        .logo h1 {
            font-size: 1.8rem;
            margin-left: 10px;
            color: var(--accent);
        }
        
        .logo-icon {
            font-size: 2rem;
            color: var(--accent);
        }
        
        /* Mobile menu button */
        .menu-toggle {
            display: none;
            background: none;
            border: none;
            color: var(--text);
            font-size: 1.5rem;
            cursor: pointer;
        }
        
        nav ul {
            display: flex;
            list-style: none;
        }
        
        nav li {
            position: relative;
            margin-left: 1.5rem;
        }
        
        nav a {
            color: var(--text);
            text-decoration: none;
            font-weight: 500;
            padding: 0.5rem 0;
            transition: var(--transition);
            display: flex;
            align-items: center;
        }
        
        nav a:hover {
            color: var(--accent);
        }
        
        .dropdown {
            position: absolute;
            top: 100%;
            left: 0;
            background-color: var(--secondary);
            width: 200px;
            padding: 1rem;
            border-radius: 5px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
            opacity: 0;
            visibility: hidden;
            transition: var(--transition);
            z-index: 101;
        }
        
        nav li:hover .dropdown {
            opacity: 1;
            visibility: visible;
        }
        
        .dropdown a {
            display: block;
            padding: 0.5rem 0;
            color: var(--text-secondary);
            transition: var(--transition);
        }
        
        .dropdown a:hover {
            color: var(--accent);
            padding-left: 5px;
        }
        
        .hero {
            background: linear-gradient(rgba(0, 0, 0, 0.7), rgba(0, 0, 0, 0.7)), url('https://images.unsplash.com/photo-1593642632823-8f785ba67e45?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1200&q=80');
            background-size: cover;
            background-position: center;
            padding: 7rem 2rem;
            text-align: center;
            min-height: 80vh;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        
        .hero-content {
            max-width: 800px;
            margin: 0 auto;
            animation: fadeIn 1s ease;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        .hero h2 {
            font-size: 2.8rem;
            margin-bottom: 1.5rem;
            color: var(--accent);
        }
        
        .hero p {
            font-size: 1.2rem;
            margin-bottom: 2.5rem;
            color: var(--text-secondary);
        }
        
        .btn {
            display: inline-block;
            background-color: var(--accent);
            color: var(--primary);
            padding: 0.9rem 2rem;
            border-radius: 5px;
            text-decoration: none;
            font-weight: 600;
            transition: var(--transition);
            border: 2px solid transparent;
        }
        
        .btn:hover {
            background-color: transparent;
            border-color: var(--accent);
            color: var(--accent);
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(179, 139, 109, 0.3);
        }
        
        .subsidiaries {
            padding: 6rem 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }
        
        .section-title {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 3.5rem;
            color: var(--accent);
            position: relative;
            padding-bottom: 15px;
        }
        
        .section-title::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 3px;
            background-color: var(--accent);
        }
        
        .subsidiaries-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2.5rem;
        }
        
        .subsidiary-card {
            background-color: var(--secondary);
            border-radius: 10px;
            padding: 2.5rem 2rem;
            transition: var(--transition);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            height: 100%;
            display: flex;
            flex-direction: column;
            position: relative;
            overflow: hidden;
        }
        
        .subsidiary-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-size: cover;
            background-position: center;
            opacity: 0.15;
            z-index: 0;
        }
        
        .subsidiary-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.2);
        }
        
        .subsidiary-content {
            position: relative;
            z-index: 1;
        }
        
        .subsidiary-icon {
            font-size: 2.8rem;
            color: var(--accent);
            margin-bottom: 1.5rem;
        }
        
        .subsidiary-card h3 {
            font-size: 1.6rem;
            margin-bottom: 1.2rem;
            color: var(--accent);
        }
        
        .subsidiary-card p {
            color: var(--text-secondary);
            margin-bottom: 1.8rem;
            flex-grow: 1;
        }
        
        .services-list {
            list-style: none;
        }
        
        .services-list li {
            padding: 0.5rem 0;
            color: var(--text-secondary);
            transition: var(--transition);
            display: flex;
            align-items: center;
        }
        
        .services-list li:hover {
            color: var(--accent-light);
        }
        
        .services-list li:before {
            content: "•";
            color: var(--accent);
            font-weight: bold;
            display: inline-block;
            width: 1em;
            margin-right: 0.5rem;
        }
        
        /* Subsidiary-specific background images */
        #health::before {
            background-image: url('https://images.unsplash.com/photo-1559757148-5c350d0d3c56?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1000&q=80');
        }
        
        #oil::before {
            background-image: url('https://images.unsplash.com/photo-1633934458015-88a6f1c2bee1?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1000&q=80');
        }
        
        #logistics::before {
            background-image: url('https://images.unsplash.com/photo-1601056639633-7e8c2cbe1432?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1000&q=80');
        }
        
        #construction::before {
            background-image: url('https://images.unsplash.com/photo-1503387762-592deb58ef4e?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1000&q=80');
        }
        
        #farming::before {
            background-image: url('https://images.unsplash.com/photo-1625246335526-713ee0dd7b7f?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1000&q=80');
        }
        
        #beauty::before {
            background-image: url('https://images.unsplash.com/photo-1596462502278-27bfdc403348?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1000&q=80');
        }
        
        #leisure::before {
            background-image: url('https://images.unsplash.com/photo-1566073771259-6a8506099945?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1000&q=80');
        }
        
        #technologies::before {
            background-image: url('https://images.unsplash.com/photo-1534723328310-e82dad3ee43f?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1000&q=80');
        }
        
        .about {
            padding: 6rem 2rem;
            background-color: var(--secondary);
        }
        
        .about-container {
            max-width: 1200px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 4rem;
            align-items: center;
        }
        
        .about-content h2 {
            font-size: 2.5rem;
            margin-bottom: 2.5rem;
            color: var(--accent);
            position: relative;
            padding-bottom: 15px;
        }
        
        .about-content h2::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 80px;
            height: 3px;
            background-color: var(--accent);
        }
        
        .about-content > p {
            margin-bottom: 2rem;
            line-height: 1.8;
        }
        
        .about-details {
            list-style: none;
        }
        
        .about-details li {
            margin-bottom: 1.2rem;
            display: flex;
            align-items: center;
        }
        
        .about-details i {
            margin-right: 1.2rem;
            color: var(--accent);
            font-size: 1.3rem;
            width: 25px;
        }
        
        .mission-vision h3 {
            font-size: 1.5rem;
            margin: 2rem 0 1rem;
            color: var(--accent);
        }
        
        .mission-vision p {
            margin-bottom: 1.5rem;
            line-height: 1.7;
        }
        
        .chairman-bio {
            background-color: var(--primary);
            padding: 2rem;
            border-radius: 10px;
            margin-top: 2rem;
            border-left: 4px solid var(--accent);
        }
        
        .chairman-bio h3 {
            color: var(--accent);
            margin-bottom: 1rem;
        }
        
        .chairman-bio p {
            margin-bottom: 1rem;
            line-height: 1.7;
        }
        
        .contact {
            padding: 6rem 2rem;
        }
        
        .contact-container {
            max-width: 1200px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 4rem;
        }
        
        .contact-info h2 {
            font-size: 2.2rem;
            margin-bottom: 2.5rem;
            color: var(--accent);
            position: relative;
            padding-bottom: 15px;
        }
        
        .contact-info h2::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 80px;
            height: 3px;
            background-color: var(--accent);
        }
        
        .contact-details {
            list-style: none;
        }
        
        .contact-details li {
            margin-bottom: 1.5rem;
            display: flex;
            align-items: center;
            transition: var(--transition);
        }
        
        .contact-details li:hover {
            transform: translateX(5px);
        }
        
        .contact-details i {
            margin-right: 1.2rem;
            color: var(--accent);
            font-size: 1.3rem;
            width: 25px;
        }
        
        .contact-details a {
            color: var(--text);
            text-decoration: none;
            transition: var(--transition);
        }
        
        .contact-details a:hover {
            color: var(--accent);
        }
        
        .map {
            border-radius: 10px;
            overflow: hidden;
            height: 100%;
            min-height: 300px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }
        
        .map iframe {
            width: 100%;
            height: 100%;
            border: none;
        }
        
        footer {
            background-color: var(--primary);
            padding: 3rem 2rem;
            text-align: center;
            color: var(--text-secondary);
            font-size: 0.9rem;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        /* Back to top button */
        .back-to-top {
            position: fixed;
            bottom: 30px;
            right: 30px;
            background: var(--accent);
            color: var(--primary);
            width: 50px;
            height: 50px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            text-decoration: none;
            opacity: 0;
            visibility: hidden;
            transition: var(--transition);
            z-index: 99;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.2);
        }
        
        .back-to-top.visible {
            opacity: 1;
            visibility: visible;
        }
        
        .back-to-top:hover {
            background: var(--accent-light);
            transform: translateY(-5px);
        }
        
        /* Responsive styles */
        @media (max-width: 992px) {
            .hero h2 {
                font-size: 2.3rem;
            }
            
            .about-container {
                gap: 3rem;
            }
        }
        
        @media (max-width: 768px) {
            .menu-toggle {
                display: block;
            }
            
            nav {
                position: fixed;
                top: 0;
                right: -300px;
                width: 300px;
                height: 100vh;
                background: var(--secondary);
                padding: 2rem;
                transition: var(--transition);
                z-index: 999;
                overflow-y: auto;
            }
            
            nav.active {
                right: 0;
                box-shadow: -5px 0 15px rgba(0, 0, 0, 0.2);
            }
            
            nav ul {
                flex-direction: column;
                margin-top: 2rem;
            }
            
            nav li {
                margin: 1rem 0;
            }
            
            .dropdown {
                position: static;
                opacity: 1;
                visibility: visible;
                width: 100%;
                margin-top: 0.5rem;
                display: none;
                box-shadow: none;
                padding: 0.5rem 1rem;
            }
            
            nav li.active .dropdown {
                display: block;
            }
            
            .header-container {
                position: relative;
            }
            
            .hero {
                padding: 5rem 1.5rem;
                min-height: 60vh;
            }
            
            .hero h2 {
                font-size: 2rem;
            }
            
            .about-container {
                grid-template-columns: 1fr;
                gap: 2rem;
            }
            
            .subsidiaries, .about, .contact {
                padding: 4rem 1.5rem;
            }
            
            .section-title {
                font-size: 2rem;
                margin-bottom: 2.5rem;
            }
            
            .contact-container {
                gap: 2.5rem;
            }
            
            .back-to-top {
                bottom: 20px;
                right: 20px;
                width: 45px;
                height: 45px;
            }
        }
        
        @media (max-width: 480px) {
            .hero {
                padding: 4rem 1rem;
            }
            
            .hero h2 {
                font-size: 1.8rem;
            }
            
            .hero p {
                font-size: 1rem;
            }
            
            .btn {
                padding: 0.8rem 1.5rem;
            }
            
            .subsidiaries-grid {
                grid-template-columns: 1fr;
            }
            
            .subsidiary-card {
                padding: 2rem 1.5rem;
            }
        }
    </style>
</head>
<body>
    <a href="#main-content" class="skip-link">Skip to main content</a>
    
    <header>
        <div class="header-container">
            <a href="#" class="logo">
                <i class="fas fa-feather-alt logo-icon"></i>
                <h1>Black Swan Holdings</h1>
            </a>
            
            <button class="menu-toggle" id="menuToggle">
                <i class="fas fa-bars"></i>
            </button>
            
            <nav id="mainNav">
                <ul>
                    <li><a href="#">Home</a></li>
                    <li class="has-dropdown">
                        <a href="#subsidiaries">Subsidiaries <i class="fas fa-chevron-down"></i></a>
                        <div class="dropdown">
                            <a href="#health">Black Swan Health</a>
                            <a href="#oil">Black Swan Oil</a>
                            <a href="#logistics">Black Swan Logistics</a>
                            <a href="#construction">Black Swan Construction</a>
                            <a href="#farming">Black Swan Farming</a>
                            <a href="#beauty">Black Swan Beauty</a>
                            <a href="#leisure">Black Swan Leisure</a>
                            <a href="#technologies">Black Swan Technologies</a>
                        </div>
                    </li>
                    <li><a href="#about">About</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <main id="main-content">
        <section class="hero">
            <div class="hero-content">
                <h2>Exceptional Unmatched Service</h2>
                <p>Black Swan Holdings is a diversified investment and holding company delivering excellence through our specialized subsidiaries across multiple industries.</p>
                <a href="#subsidiaries" class="btn">Explore Our Subsidiaries</a>
            </div>
        </section>

        <section class="subsidiaries" id="subsidiaries">
            <h2 class="section-title">Our Subsidiaries</h2>
            <div class="subsidiaries-grid">
                <div class="subsidiary-card" id="health">
                    <div class="subsidiary-content">
                        <i class="fas fa-heartbeat subsidiary-icon"></i>
                        <h3>Black Swan Health</h3>
                        <p>Health Industry Revolutionaries. We integrate pharmaceuticals, advanced medical equipment, and specialized laboratory services with comprehensive training and maintenance.</p>
                        <ul class="services-list">
                            <li>Pharmaceuticals</li>
                            <li>Medical supplies</li>
                            <li>Hospital equipment and maintenance</li>
                            <li>Laboratory supplies</li>
                            <li>Laboratory equipment supplies and maintenance</li>
                            <li>Laboratory Staff Training</li>
                        </ul>
                    </div>
                </div>

                <div class="subsidiary-card" id="oil">
                    <div class="subsidiary-content">
                        <i class="fas fa-oil-well subsidiary-icon"></i>
                        <h3>Black Swan Oil</h3>
                        <p>Your integrated energy partner, managing the entire journey of crude oil from source to market through secure transportation, refining, and reliable supply.</p>
                        <ul class="services-list">
                            <li>Crude Oil supplies</li>
                            <li>Crude Oil refinery</li>
                            <li>Crude Oil Transportation</li>
                        </ul>
                    </div>
                </div>

                <div class="subsidiary-card" id="logistics">
                    <div class="subsidiary-content">
                        <i class="fas fa-truck-fast subsidiary-icon"></i>
                        <h3>Black Swan Logistics</h3>
                        <p>We optimize and streamline your supply chain, ensuring efficient, transparent, and resilient movement of goods across all your operations.</p>
                        <ul class="services-list">
                            <li>Supply Chain Management</li>
                        </ul>
                    </div>
                </div>

                <div class="subsidiary-card" id="construction">
                    <div class="subsidiary-content">
                        <i class="fas fa-hard-hat subsidiary-icon"></i>
                        <h3>Black Swan Construction</h3>
                        <p>We build modern communities, delivering quality and durability in everything from single-family homes to iconic high-rise developments.</p>
                        <ul class="services-list">
                            <li>Construction of homes and high rise buildings</li>
                        </ul>
                    </div>
                </div>

                <div class="subsidiary-card" id="farming">
                    <div class="subsidiary-content">
                        <i class="fas fa-tractor subsidiary-icon"></i>
                        <h3>Black Swan Farming</h3>
                        <p>A trusted source for fresh, sustainably farmed produce and livestock, supplying premium food from our fields to your table.</p>
                        <ul class="services-list">
                            <li>Commercial farming of livestock, fruits and vegetables</li>
                        </ul>
                    </div>
                </div>

                <div class="subsidiary-card" id="beauty">
                    <div class="subsidiary-content">
                        <i class="fas fa-spa subsidiary-icon"></i>
                        <h3>Black Swan Beauty</h3>
                        <p>A complete ecosystem of beauty, offering high-quality products and expert services through our own network of salons and barbershops.</p>
                        <ul class="services-list">
                            <li>Beauty products</li>
                            <li>Salons</li>
                            <li>Barbershops</li>
                        </ul>
                    </div>
                </div>

                <div class="subsidiary-card" id="leisure">
                    <div class="subsidiary-content">
                        <i class="fas fa-umbrella-beach subsidiary-icon"></i>
                        <h3>Black Swan Leisure</h3>
                        <p>We curate exceptional experiences, handling every detail of your escape—from luxury hotels and unique dining to seamless vacation bookings.</p>
                        <ul class="services-list">
                            <li>Booking of vacations</li>
                            <li>Restaurant services</li>
                            <li>Hotels, lodges, guest houses</li>
                        </ul>
                    </div>
                </div>

                <div class="subsidiary-card" id="technologies">
                    <div class="subsidiary-content">
                        <i class="fas fa-microchip subsidiary-icon"></i>
                        <h3>Black Swan Technologies</h3>
                        <p>We pioneer intelligent futures by developing cutting-edge AI solutions and platforms that solve complex challenges and drive innovation.</p>
                        <ul class="services-list">
                            <li>AI Development</li>
                            <li>AI Solutions</li>
                        </ul>
                    </div>
                </div>
            </div>
        </section>

        <section class="about" id="about">
            <div class="about-container">
                <div class="about-content">
                    <h2>About Black Swan Holdings</h2>
                    <p>We are an investment and holding company focused on delivering exceptional unmatched service through our diverse group of subsidiaries. Our vision is to revolutionize industries through innovation and excellence.</p>
                    <ul class="about-details">
                        <li><i class="fas fa-user"></i> Dr. Hübert M.T. Shitaleni (Chairman & Group Managing Director)</li>
                    </ul>
                    
                    <div class="chairman-bio">
                        <h3>About Our Chairman</h3>
                        <p>Dr. Hübert M.T. Shitaleni's career spans over a decade in Medical Laboratory Sciences, Laboratory Management, Academic Instruction, and Advancing Technologies.</p>
                        <p>Driven by core objectives to advance diverse industries in Namibia for the betterment of the Namibian society and SADC, Dr. Shitaleni brings a wealth of experience and visionary leadership to Black Swan Holdings.</p>
                    </div>
                </div>
                <div class="mission-vision">
                    <h3>Our Mission</h3>
                    <p>To provide exceptional, innovative services across diverse industries while maintaining the highest standards of quality and customer satisfaction.</p>
                    <h3>Our Vision</h3>
                    <p>To be the leading diversified holdings company in the region, known for revolutionizing each industry we operate in.</p>
                </div>
            </div>
        </section>

        <section class="contact" id="contact">
            <div class="contact-container">
                <div class="contact-info">
                    <h2>Contact Us</h2>
                    <ul class="contact-details">
                        <li><i class="fas fa-user"></i> Dr. Hübert M.T. Shitaleni (Chairman & Group Managing Director)</li>
                        <li><i class="fas fa-phone"></i> <a href="tel:+264812974355">+264 81 297 4355</a></li>
                        <li><i class="fas fa-envelope"></i> <a href="mailto:hshitaleni@gmx.com">hshitaleni@gmx.com</a></li>
                        <li><i class="fas fa-map-marker-alt"></i> Erf 209, Avis Road, Avis, Windhoek, Namibia</li>
                        <li><i class="fas fa-box"></i> P.O. Box 86462 Eros, Windhoek, Namibia</li>
                    </ul>
                </div>
                <div class="map">
                    <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d29902.41529532074!2d17.067659!3d-22.570583!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x1c0b1b0b0b0b0b0b%3A0x1b0b0b0b0b0b0b0b!2sAvis%2C%20Windhoek%2C%20Namibia!5e0!3m2!1sen!2sus!4v1631234567890!5m2!1sen!2sus" width="100%" height="100%" style="border:0;" allowfullscreen="" loading="lazy"></iframe>
                </div>
            </div>
        </section>
    </main>

    <a href="#" class="back-to-top" id="backToTop">
        <i class="fas fa-arrow-up"></i>
    </a>

    <footer>
        <p>&copy; 2023 Black Swan Holdings Pty Ltd. All rights reserved.</p>
    </footer>

    <script>
        // Mobile menu toggle
        const menuToggle = document.getElementById('menuToggle');
        const mainNav = document.getElementById('mainNav');
        
        menuToggle.addEventListener('click', function() {
            mainNav.classList.toggle('active');
            this.querySelector('i').classList.toggle('fa-bars');
            this.querySelector('i').classList.toggle('fa-times');
        });
        
        // Dropdown menu for mobile
        const dropdownParents = document.querySelectorAll('.has-dropdown');
        
        dropdownParents.forEach(parent => {
            parent.addEventListener('click', function(e) {
                if (window.innerWidth <= 768) {
                    e.preventDefault();
                    this.classList.toggle('active');
                }
            });
        });
        
        // Back to top button
        const backToTopButton = document.getElementById('backToTop');
        
        window.addEventListener('scroll', function() {
            if (window.pageYOffset > 300) {
                backToTopButton.classList.add('visible');
            } else {
                backToTopButton.classList.remove('visible');
            }
        });
        
        backToTopButton.addEventListener('click', function(e) {
            e.preventDefault();
            window.scrollTo({
                top: 0,
                behavior: 'smooth'
            });
        });
        
        // Smooth scrolling for anchor links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                if (this.getAttribute('href') !== '#') {
                    e.preventDefault();
                    
                    const targetId = this.getAttribute('href');
                    const targetElement = document.querySelector(targetId);
                    
                    if (targetElement) {
                        // Close mobile menu if open
                        if (mainNav.classList.contains('active')) {
                            mainNav.classList.remove('active');
                            menuToggle.querySelector('i').classList.add('fa-bars');
                            menuToggle.querySelector('i').classList.remove('fa-times');
                        }
                        
                        window.scrollTo({
                            top: targetElement.offsetTop - 80,
                            behavior: 'smooth'
                        });
                    }
                }
            });
        });
    </script>
</body>
</html>
