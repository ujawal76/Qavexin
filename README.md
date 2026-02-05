<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Qavexin | Digital Solutions & Technology</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        :root {
            --bg-deep: #05070a;
            --bg-card: #0f1218;
            --accent-cyan: #00d2ff;
            --accent-blue: #0072ff;
            --text-main: #e0e0e0;
            --glass: rgba(255, 255, 255, 0.03);
        }

        * { margin: 0; padding: 0; box-sizing: border-box; }

        body {
            font-family: 'Inter', sans-serif;
            background-color: var(--bg-deep);
            color: var(--text-main);
            overflow-x: hidden;
            scroll-behavior: smooth;
        }

        body::before {
            content: "";
            position: fixed;
            top: 0; left: 0; width: 100%; height: 100%;
            background: 
                radial-gradient(circle at 10% 20%, rgba(0, 210, 255, 0.05) 0%, transparent 40%),
                radial-gradient(circle at 90% 80%, rgba(0, 114, 255, 0.05) 0%, transparent 40%);
            z-index: -1;
        }

        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px 8%;
            background: rgba(5, 7, 10, 0.8);
            backdrop-filter: blur(10px);
            position: sticky;
            top: 0;
            z-index: 1000;
            border-bottom: 1px solid rgba(255,255,255,0.05);
        }

        .logo { font-size: 1.5rem; font-weight: 800; letter-spacing: 2px; }
        .logo span { color: var(--accent-cyan); }

        nav ul { display: flex; list-style: none; }
        nav ul li { margin-left: 30px; }
        nav ul li a { color: white; text-decoration: none; font-size: 0.9rem; transition: 0.3s; }
        nav ul li a:hover { color: var(--accent-cyan); }

        .hero {
            height: 80vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            padding: 0 20px;
        }

        .hero h1 { font-size: clamp(2.5rem, 6vw, 4rem); margin-bottom: 10px; }
        .hero p { font-size: 1.2rem; color: var(--accent-cyan); letter-spacing: 3px; margin-bottom: 30px; text-transform: uppercase;}

        .cta-btn {
            padding: 15px 35px;
            background: linear-gradient(45deg, var(--accent-blue), var(--accent-cyan));
            color: white;
            text-decoration: none;
            border-radius: 50px;
            font-weight: bold;
            box-shadow: 0 10px 20px rgba(0, 210, 255, 0.2);
            transition: 0.3s;
        }
        .cta-btn:hover { transform: scale(1.05); }

        /* Portfolio Section */
        .portfolio-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 25px;
            padding: 40px 8%;
        }

        .work-item {
            border-radius: 15px;
            overflow: hidden;
            background: var(--bg-card);
            border: 1px solid rgba(255,255,255,0.1);
            transition: 0.3s;
        }

        .work-item img { width: 100%; height: 200px; object-fit: cover; filter: grayscale(50%); transition: 0.5s; }
        .work-item:hover img { filter: grayscale(0%); transform: scale(1.1); }
        .work-info { padding: 20px; }
        .work-info h4 { margin-bottom: 5px; color: var(--accent-cyan); }

        .btn-center { text-align: center; margin-top: 30px; }

        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
            padding: 40px 8%;
        }

        .card {
            background: var(--bg-card);
            border: 1px solid rgba(255,255,255,0.05);
            padding: 40px;
            border-radius: 20px;
            transition: 0.4s;
        }

        .card:hover { border-color: var(--accent-cyan); transform: translateY(-5px); }
        .card i { font-size: 2.5rem; color: var(--accent-cyan); margin-bottom: 20px; }

        .contact { padding: 80px 8%; }
        .contact-container {
            max-width: 600px;
            margin: 0 auto;
            background: var(--bg-card);
            padding: 40px;
            border-radius: 20px;
        }

        input, textarea {
            width: 100%; padding: 15px; margin-bottom: 20px;
            background: #1a1e26; border: 1px solid rgba(255,255,255,0.1);
            color: white; border-radius: 8px;
        }

        button {
            width: 100%; padding: 15px; background: var(--accent-cyan);
            border: none; color: black; font-weight: bold;
            border-radius: 8px; cursor: pointer; transition: 0.3s;
        }
        button:hover { background: white; }

        .social-links { margin: 20px 0; }
        .social-links a {
            color: var(--text-main); font-size: 1.5rem; margin: 0 15px;
            transition: 0.3s; text-decoration: none;
        }
        .social-links a:hover { color: var(--accent-cyan); }

        footer {
            padding: 60px 40px; text-align: center;
            border-top: 1px solid rgba(255,255,255,0.05);
            font-size: 0.9rem; color: #666;
        }

        @media (max-width: 768px) { nav ul { display: none; } }
    </style>
</head>
<body>

    <nav>
        <div class="logo">QAVE<span>XIN</span></div>
        <ul>
            <li><a href="#home">Home</a></li>
            <li><a href="#work">Our Work</a></li>
            <li><a href="#services">Services</a></li>
            <li><a href="#contact">Contact</a></li>
        </ul>
    </nav>

    <section class="hero" id="home">
        <h1>We Build. We Design. We Scale.</h1>
        <p>Digital Solutions & Technology</p>
        <a href="#work" class="cta-btn">View My Portfolio</a>
    </section>

    <h2 class="section-title" id="work" style="text-align:center; padding-top: 60px;">Our <span>Recent</span> Work</h2>
    <section class="portfolio-grid">
        <div class="work-item">
            <img src="https://images.unsplash.com/photo-1460925895917-afdab827c52f?auto=format&fit=crop&w=500" alt="Work 1">
            <div class="work-info">
                <h4>E-commerce Website</h4>
                <p>Clean and modern shopping experience.</p>
            </div>
        </div>
        <div class="work-item">
            <img src="https://images.unsplash.com/photo-1626785774573-4b799315345d?auto=format&fit=crop&w=500" alt="Work 2">
            <div class="work-info">
                <h4>Logo Branding</h4>
                <p>Corporate identity for tech startups.</p>
            </div>
        </div>
        <div class="work-item">
            <img src="https://images.unsplash.com/photo-1611162617474-5b21e879e113?auto=format&fit=crop&w=500" alt="Work 3">
            <div class="work-info">
                <h4>YT Graphics</h4>
                <p>High CTR Thumbnails and Banners.</p>
            </div>
        </div>
    </section>
    <div class="btn-center">
        <a href="https://drive.google.com/drive/folders/1dWV40cF5xyTXVB8TChyRe8qlNmcILtmB?usp=gmail" target="_blank" class="cta-btn" style="background: transparent; border: 1px solid var(--accent-cyan);">View More Projects</a>
    </div>

    <h2 class="section-title" id="services" style="text-align:center; padding-top: 80px;">Our <span>Specialized</span> Services</h2>
    <section class="services-grid">
        <div class="card">
            <i class="fas fa-code"></i>
            <h3>Website Making</h3>
            <p>Modern, responsive, and blazing fast websites including SEO and UI/UX Designing.</p>
        </div>
        <div class="card">
            <i class="fas fa-pen-nib"></i>
            <h3>Logo & Branding</h3>
            <p>We create iconic logos and business profiles that make your brand stand out from the crowd.</p>
        </div>
        <div class="card">
            <i class="fas fa-id-card"></i>
            <h3>Business Cards</h3>
            <p>Professional business card making and complete digital business profile creation.</p>
        </div>
        <div class="card">
            <i class="fab fa-youtube"></i>
            <h3>YouTube Graphics</h3>
            <p>Professional YouTube banner making and viral thumbnail designing to grow your channel.</p>
        </div>
        <div class="card">
            <i class="fas fa-layer-group"></i>
            <h3>Banner Making</h3>
            <p>High-quality digital and print banners for events, social media, and advertising.</p>
        </div>
        <div class="card">
            <i class="fas fa-lightbulb"></i>
            <h3>Digital Solutions</h3>
            <p>Complete tech support, from concept to execution. We bring your digital ideas to life.</p>
        </div>
    </section>

    <section class="contact" id="contact">
        <h2 class="section-title" style="text-align:center; margin-bottom: 30px;">Get In <span>Touch</span></h2>
        <div class="contact-container">
            <form action="https://formsubmit.co/ujawalsharma999@gmail.com" method="POST">
                <input type="text" name="name" placeholder="Your Name" required>
                <input type="email" name="email" placeholder="Your Email" required>
                <textarea name="message" rows="5" placeholder="Project Details (e.g. Logo, Website, Banner)" required></textarea>
                 
                <input type="hidden" name="_next" value="https://Qavexin.in">
                <button type="submit">Send Message</button>
            </form>
        </div>
    </section>

    <footer>
        <div class="logo">QAVE<span>XIN</span></div>
        <div class="social-links">
            <a href="https://instagram.com/Qavexin" target="_blank"><i class="fab fa-instagram"></i></a>
            <a href="https://linkedin.com" target="_blank"><i class="fab fa-linkedin"></i></a>
            <a href="https://twitter.com" target="_blank"><i class="fab fa-twitter"></i></a>
        </div>
        <p>&copy; 2026 Qavexin India | Founder: Ujjwal Sharma</p>
        <p>hello@Qavexin.in | +91 98765 43210</p>
    </footer>

</body>
</html>
