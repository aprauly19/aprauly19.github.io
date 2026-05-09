<!DOCTYPE html>
<html lang="en-GB">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Cakes by the Lakes Wirral | Homemade Café in Upton, Wirral</title>
    <meta name="description" content="Wirral's cosiest little café in Upton. Freshly made cakes, artisan sandwiches, and speciality coffee. Family-run, dog-friendly, and warm atmosphere.">
    
    <!-- Open Graph Tags -->
    <meta property="og:title" content="Cakes by the Lakes Wirral | Homemade Café">
    <meta property="og:description" content="Artisan cakes, sandwiches & coffee in the heart of Upton. Freshly made every day with heart.">
    <meta property="og:type" content="website">
    <meta property="og:url" content="https://cakesbythelakeswirral.co.uk">

    <!-- Google Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Lato:wght@400;700&family=Playfair+Display:ital,wght@0,700;1,700&display=swap" rel="stylesheet">

    <style>
        :root {
            --cream: #FDF6EC;
            --rose: #E8A598;
            --sage: #8FAF8C;
            --brown: #4A2C2A;
            --white: #ffffff;
            --transition: all 0.4s cubic-bezier(0.165, 0.84, 0.44, 1);
        }

        * { margin: 0; padding: 0; box-sizing: border-box; }

        body {
            font-family: 'Lato', sans-serif;
            background-color: var(--cream);
            color: var(--brown);
            line-height: 1.6;
            overflow-x: hidden;
        }

        h1, h2, h3, h4 {
            font-family: 'Playfair Display', serif;
            font-weight: 700;
        }

        /* --- Global Animations --- */
        .reveal {
            opacity: 0;
            transform: translateY(30px);
            transition: var(--transition);
        }

        .reveal.active {
            opacity: 1;
            transform: translateY(0);
        }

        /* --- Hero Section --- */
        .hero {
            position: relative;
            min-height: 90vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            padding: 2rem;
            background: linear-gradient(135deg, var(--cream) 0%, var(--rose) 100%);
            overflow: hidden;
        }

        .hero-content {
            z-index: 2;
            max-width: 800px;
        }

        .hero h1 {
            font-size: clamp(2.5rem, 8vw, 4.5rem);
            line-height: 1.1;
            margin-bottom: 1.5rem;
        }

        .hero p {
            font-size: clamp(1.1rem, 3vw, 1.4rem);
            margin-bottom: 2.5rem;
            opacity: 0.9;
        }

        .btn-group {
            display: flex;
            gap: 1rem;
            justify-content: center;
            flex-wrap: wrap;
        }

        .btn {
            padding: 1rem 2.5rem;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 700;
            transition: var(--transition);
            display: inline-block;
            cursor: pointer;
        }

        .btn-primary {
            background-color: var(--brown);
            color: var(--white);
        }

        .btn-primary:hover {
            transform: scale(1.05);
            box-shadow: 0 10px 20px rgba(74, 44, 42, 0.2);
        }

        .btn-outline {
            border: 2px solid var(--brown);
            color: var(--brown);
        }

        .btn-outline:hover {
            background-color: var(--brown);
            color: var(--white);
        }

        .badge {
            display: inline-block;
            background: rgba(255, 255, 255, 0.6);
            padding: 0.5rem 1.2rem;
            border-radius: 50px;
            margin-bottom: 2rem;
            font-weight: 700;
            backdrop-filter: blur(5px);
            border: 1px solid rgba(74, 44, 42, 0.1);
        }

        /* Floating Icons */
        .floating-icon {
            position: absolute;
            opacity: 0.15;
            z-index: 1;
            animation: float 6s ease-in-out infinite;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0) rotate(0deg); }
            50% { transform: translateY(-20px) rotate(10deg); }
        }

        /* --- Trust Bar --- */
        .trust-bar {
            background: var(--brown);
            color: var(--white);
            padding: 0.8rem 0;
            overflow: hidden;
            white-space: nowrap;
        }

        .ticker {
            display: inline-block;
            animation: marquee 30s linear infinite;
        }

        .ticker span {
            display: inline-block;
            padding-right: 3rem;
            font-weight: 700;
            text-transform: uppercase;
            font-size: 0.9rem;
            letter-spacing: 1px;
        }

        @keyframes marquee {
            0% { transform: translateX(0); }
            100% { transform: translateX(-50%); }
        }

        /* --- About Section --- */
        .section-padding { padding: 5rem 10%; }

        .about-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 4rem;
            align-items: center;
        }

        .about-img {
            width: 100%;
            height: 500px;
            border-radius: 20px;
            object-fit: cover;
            box-shadow: 20px 20px 0 var(--sage);
        }

        .feature-pills {
            display: flex;
            gap: 1rem;
            margin-top: 2rem;
            flex-wrap: wrap;
        }

        .pill {
            background: var(--rose);
            padding: 0.5rem 1rem;
            border-radius: 50px;
            color: var(--white);
            font-weight: 700;
            font-size: 0.9rem;
        }

        /* --- Menu Section --- */
        .menu-section { background-color: var(--white); text-align: center; }

        .menu-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 2rem;
            margin-top: 3rem;
        }

        .menu-card {
            background: var(--cream);
            padding: 2.5rem;
            border-radius: 20px;
            text-align: left;
            transition: var(--transition);
            border: 1px solid rgba(143, 175, 140, 0.2);
        }

        .menu-card:hover { transform: translateY(-10px); box-shadow: 0 15px 30px rgba(0,0,0,0.05); }

        .menu-card h3 { color: var(--rose); margin-bottom: 1rem; font-size: 1.8rem; }
        
        .menu-card ul { list-style: none; }
        .menu-card li { margin-bottom: 0.5rem; position: relative; padding-left: 1.5rem; }
        .menu-card li::before { content: '•'; position: absolute; left: 0; color: var(--sage); font-weight: bold; }

        .meal-deal {
            background: var(--rose);
            color: var(--brown);
            padding: 1.5rem;
            border-radius: 15px;
            margin-top: 3rem;
            font-weight: 700;
            font-size: 1.2rem;
            display: inline-block;
        }

        /* --- Info Section --- */
        .info-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 3rem;
        }

        .status-badge {
            padding: 0.3rem 0.8rem;
            border-radius: 5px;
            font-weight: 700;
            font-size: 0.8rem;
            margin-left: 10px;
        }
        .status-open { background: #d4edda; color: #155724; }
        .status-closed { background: #f8d7da; color: #721c24; }

        .map-container {
            width: 100%;
            height: 300px;
            border-radius: 15px;
            overflow: hidden;
            margin-top: 1.5rem;
        }

        .info-icons {
            display: flex;
            gap: 1.5rem;
            margin-top: 1.5rem;
            font-size: 0.85rem;
            font-weight: 700;
            flex-wrap: wrap;
        }

        /* --- Review Carousel --- */
        .reviews-section { background: var(--cream); overflow: hidden; }
        
        .review-viewport {
            width: 100%;
            overflow: hidden;
            margin-top: 3rem;
            cursor: grab;
        }

        .review-track {
            display: flex;
            transition: transform 0.5s ease-out;
            gap: 2rem;
        }

        .review-card {
            min-width: 350px;
            background: var(--white);
            padding: 2rem;
            border-radius: 15px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.03);
        }

        .stars { color: #FFD700; margin-bottom: 0.5rem; }
        .reviewer { font-weight: 700; display: block; margin-bottom: 0.2rem; }
        .review-date { font-size: 0.8rem; color: #888; margin-bottom: 1rem; display: block; }
        
        .review-text {
            font-size: 0.95rem;
            display: -webkit-box;
            -webkit-line-clamp: 3;
            -webkit-box-orient: vertical;
            overflow: hidden;
        }

        .review-text.expanded {
            -webkit-line-clamp: unset;
        }

        .read-more {
            color: var(--sage);
            font-weight: 700;
            cursor: pointer;
            font-size: 0.85rem;
            display: block;
            margin-top: 0.5rem;
        }

        /* --- Footer Section --- */
        .final-cta {
            background: var(--brown);
            color: var(--white);
            text-align: center;
            padding: 5rem 10%;
        }

        .final-cta h2 { font-size: 2.5rem; margin-bottom: 1rem; }
        
        footer {
            background: #361f1e;
            color: rgba(255,255,255,0.7);
            padding: 2rem 10%;
            text-align: center;
            font-size: 0.9rem;
        }

        .social-link {
            color: var(--white);
            font-size: 1.5rem;
            margin-top: 1rem;
            display: inline-block;
            text-decoration: none;
        }

        /* --- Responsive --- */
        @media (max-width: 900px) {
            .about-grid, .info-grid { grid-template-columns: 1fr; }
            .about-img { height: 350px; order: -1; }
            .menu-grid { grid-template-columns: 1fr; }
            .section-padding { padding: 4rem 5%; }
        }

        @media (max-width: 600px) {
            .hero h1 { font-size: 2.5rem; }
            .review-card { min-width: 280px; }
        }
    </style>
</head>
<body>

    <!-- Section 1: Hero -->
    <header class="hero">
        <!-- Floating SVGs -->
        <svg class="floating-icon" style="top: 15%; left: 10%; width: 60px;" viewBox="0 0 24 24" fill="currentColor"><path d="M11 2c.047 0 .092.006.137.017a2.502 2.502 0 0 1 4.726 0c.045-.011.09-.017.137-.017 1.38 0 2.5 1.12 2.5 2.5 0 .597-.216 1.138-.567 1.56.35.423.567.964.567 1.561 0 1.38-1.12 2.5-2.5 2.5-.047 0-.092-.006-.137-.017a2.502 2.502 0 0 1-4.726 0c-.045.011-.09.017-.137.017-1.38 0-2.5-1.12-2.5-2.5 0-.597.216-1.138.567-1.56a2.506 2.506 0 0 1-.567-1.561c0-1.38 1.12-2.5 2.5-2.5zm0 14h2v2h-2v-2zm-6-2h14v1h-14v-1zm0 2h14v1h-14v-1zm-1 3h16v1h-16v-1z"/></svg>
        <svg class="floating-icon" style="bottom: 20%; right: 10%; width: 50px;" viewBox="0 0 24 24" fill="currentColor"><path d="M2 21h18v-2H2v2zM20 8h-2V5h2v3zm2-3h-4a2 2 0 0 0-2 2v3a2 2 0 0 0 2 2h4a2 2 0 0 0 2-2V7a2 2 0 0 0-2-2zM4 19h14v-9H4v9zM14 5c0-1.1-.9-2-2-2s-2 .9-2 2h4z"/></svg>
        
        <div class="hero-content reveal">
            <span class="badge">⭐ 4.9/5 on Google · 100% Recommend on Facebook</span>
            <h1>Homemade with Heart. <br>Fresh Every Day.</h1>
            <p>Wirral's cosiest little café — cakes, sandwiches & speciality coffee in the heart of Upton</p>
            <div class="btn-group">
                <a href="#menu" class="btn btn-primary">See Our Menu ↓</a>
                <a href="#visit" class="btn btn-outline">Find Us</a>
            </div>
        </div>
    </header>

    <!-- Section 2: Trust Bar -->
    <div class="trust-bar">
        <div class="ticker">
            <span>🍰 100% Recommend on Facebook</span>
            <span>⭐ 4.9 Google Rating</span>
            <span>☕ Fresh Made Daily</span>
            <span>🐾 Dog Friendly</span>
            <span>📶 Free Wi-Fi</span>
            <span>👨‍👩‍👧 Family Friendly</span>
            <span>🅿️ Free Nearby Parking</span>
            <!-- Duplicate for infinite effect -->
            <span>🍰 100% Recommend on Facebook</span>
            <span>⭐ 4.9 Google Rating</span>
            <span>☕ Fresh Made Daily</span>
            <span>🐾 Dog Friendly</span>
            <span>📶 Free Wi-Fi</span>
            <span>👨‍👩‍👧 Family Friendly</span>
            <span>🅿️ Free Nearby Parking</span>
        </div>
    </div>

    <!-- Section 3: About -->
    <section class="section-padding reveal">
        <div class="about-grid">
            <img src="https://images.unsplash.com/photo-1559339352-11d035aa65de?q=80&w=1000" alt="Delicious Cakes" class="about-img">
            <div>
                <h2>A Little Café With a Big Heart</h2>
                <p style="margin: 1.5rem 0;">Cakes by the Lakes is Wirral's best-kept secret — a homemade, traditional café tucked away at 397 Upton Road, Noctorum. Everything is freshly made, the counter changes daily, and you'll always leave with a smile. Whether you're after a hearty sandwich, a stunning celebration cake, or just a slice of school cake and a latte — you've found your place.</p>
                <div class="feature-pills">
                    <span class="pill">🏠 Family Run</span>
                    <span class="pill">🌿 Fresh Daily</span>
                    <span class="pill">💛 Affordable Prices</span>
                </div>
            </div>
        </div>
    </section>

    <!-- Section 4: Menu -->
    <section id="menu" class="section-padding menu-section reveal">
        <h2>What's On the Counter Today</h2>
        <p>Our menu rotates daily — here's a taste of what to expect</p>
        
        <div class="menu-grid">
            <div class="menu-card reveal">
                <h3>🍰 Sweet Treats</h3>
                <ul>
                    <li>Victoria Sponge</li>
                    <li>Biscoff Cream Buns</li>
                    <li>Lemon Drizzle & Coffee & Walnut</li>
                    <li>Brownies & Kinder Brownies</li>
                    <li>Custard Tarts & School Cake</li>
                    <li>Milkybar Cheesecake & Caramel Cakes</li>
                </ul>
            </div>
            <div class="menu-card reveal">
                <h3>🥪 Savoury & Lunch</h3>
                <ul>
                    <li>Salt & Pepper Sausage Rolls</li>
                    <li>Nudger Sandwiches</li>
                    <li>Freshly Made Bagels & Toasties</li>
                    <li>Jacket Potatoes</li>
                    <li>Healthy Wraps</li>
                </ul>
            </div>
            <div class="menu-card reveal">
                <h3>🥗 Boxes & Salads</h3>
                <ul>
                    <li>Pasta Boxes (Pesto / Tomato / Chinese Chicken)</li>
                    <li>Salad Boxes (Chicken Bacon Mayo, Tuna Mayo)</li>
                    <li>Gluten-Free Options Available</li>
                </ul>
            </div>
            <div class="menu-card reveal">
                <h3>☕ Drinks</h3>
                <ul>
                    <li>Specialty Coffees</li>
                    <li>Iced Frappes & Milkshakes</li>
                    <li>Hot Chocolate & Fresh Smoothies</li>
                </ul>
            </div>
        </div>
        
        <div class="meal-deal reveal">
            🎉 Meal Deal — Main + Cake + Hot Drink from just £7.50!
        </div>
    </section>

    <!-- Section 5: Visit & Hours -->
    <section id="visit" class="section-padding reveal">
        <div class="info-grid">
            <div>
                <h2>Visit Us</h2>
                <div style="margin-top:1.5rem">
                    <p><strong>Opening Hours:</strong></p>
                    <p>Mon – Fri: 10:00 AM – 2:30 PM <span id="open-status" class="status-badge">Checking...</span></p>
                    <p>Sat – Sun: Closed</p>
                </div>
                
                <div style="margin-top:2rem">
                    <p>📍 397 Upton Road, Noctorum, CH43 9SE</p>
                    <p>📞 +44 7548 880879</p>
                    <p>📧 cakesbythelakes.wirral@gmail.com</p>
                </div>

                <div class="info-icons">
                    <span>🐾 Dog Friendly</span>
                    <span>👶 High Chairs</span>
                    <span>📶 Free Wi-Fi</span>
                    <span>🅿️ Free Parking</span>
                </div>
            </div>
            <div>
                <div class="map-container">
                    <iframe 
                        src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2389.576822557106!2d-3.0768417232815127!3d53.383049172304!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x487b270726715f33%3A0x6420556f8f7813a4!2s397%20Upton%20Rd%2C%20Noctorum%2C%20Birkenhead%20CH43%209SE!5e0!3m2!1sen!2suk!4v1710000000000" 
                        width="100%" height="100%" style="border:0;" allowfullscreen="" loading="lazy"></iframe>
                </div>
            </div>
        </div>
    </section>

    <!-- Section 6: Reviews Carousel -->
    <section class="section-padding reviews-section">
        <h2 style="text-align: center;">What Our Guests Say</h2>
        <div class="review-viewport">
            <div class="review-track" id="review-track">
                <!-- Review 1 -->
                <div class="review-card">
                    <div class="stars">★★★★★</div>
                    <span class="reviewer">Hughes Louise Emma</span>
                    <span class="review-date">19 Feb 2025</span>
                    <p class="review-text">Been here a few times and what can I say — every cake I've tried have been beautiful. I tried the huge nudger sandwich too the other day and it was amazing so fresh and the coleslaw was amazing. Highly recommend.</p>
                    <span class="read-more" onclick="toggleReview(this)">Read more</span>
                </div>
                <!-- Review 2 -->
                <div class="review-card">
                    <div class="stars">★★★★★</div>
                    <span class="reviewer">Louise Forster-Kerr</span>
                    <span class="review-date">25 Jan 2025</span>
                    <p class="review-text">Such a gorgeous little local spot! Lovely sandwiches, bagels and toasties...and the cakes wow! The staff are so friendly. My mum really fancied a meringue and there were none left, so the lovely lady went in the back and made her one! 10/10 customer service ✨</p>
                    <span class="read-more" onclick="toggleReview(this)">Read more</span>
                </div>
                <!-- Review 3 -->
                <div class="review-card">
                    <div class="stars">★★★★★</div>
                    <span class="reviewer">Tina Denise</span>
                    <span class="review-date">30 Nov 2024</span>
                    <p class="review-text">Love this place. It's warm and inviting. The bread is delicious, amazing salad boxes and the cakes — well I have no words. They are just delicious and all at affordable prices. I definitely recommend.</p>
                    <span class="read-more" onclick="toggleReview(this)">Read more</span>
                </div>
                <!-- Review 4 -->
                <div class="review-card">
                    <div class="stars">★★★★★</div>
                    <span class="reviewer">Valerie Jones</span>
                    <span class="review-date">3 May 2025</span>
                    <p class="review-text">My husband and I had lunch here a few w<!DOCTYPE html>
<html lang="en-GB">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Cakes by the Lakes Wirral | Homemade Café in Upton, Wirral</title>
    <meta name="description" content="Wirral's cosiest little café in Upton. Freshly made cakes, artisan sandwiches, and speciality coffee. Family-run, dog-friendly, and warm atmosphere.">
    
    <!-- Open Graph Tags -->
    <meta property="og:title" content="Cakes by the Lakes Wirral | Homemade Café">
    <meta property="og:description" content="Artisan cakes, sandwiches & coffee in the heart of Upton. Freshly made every day with heart.">
    <meta property="og:type" content="website">
    <meta property="og:url" content="https://cakesbythelakeswirral.co.uk">

    <!-- Google Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Lato:wght@400;700&family=Playfair+Display:ital,wght@0,700;1,700&display=swap" rel="stylesheet">

    <style>
        :root {
            --cream: #FDF6EC;
            --rose: #E8A598;
            --sage: #8FAF8C;
            --brown: #4A2C2A;
            --white: #ffffff;
            --transition: all 0.4s cubic-bezier(0.165, 0.84, 0.44, 1);
        }

        * { margin: 0; padding: 0; box-sizing: border-box; }

        body {
            font-family: 'Lato', sans-serif;
            background-color: var(--cream);
            color: var(--brown);
            line-height: 1.6;
            overflow-x: hidden;
        }

        h1, h2, h3, h4 {
            font-family: 'Playfair Display', serif;
            font-weight: 700;
        }

        /* --- Global Animations --- */
        .reveal {
            opacity: 0;
            transform: translateY(30px);
            transition: var(--transition);
        }

        .reveal.active {
            opacity: 1;
            transform: translateY(0);
        }

        /* --- Hero Section --- */
        .hero {
            position: relative;
            min-height: 90vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            padding: 2rem;
            background: linear-gradient(135deg, var(--cream) 0%, var(--rose) 100%);
            overflow: hidden;
        }

        .hero-content {
            z-index: 2;
            max-width: 800px;
        }

        .hero h1 {
            font-size: clamp(2.5rem, 8vw, 4.5rem);
            line-height: 1.1;
            margin-bottom: 1.5rem;
        }

        .hero p {
            font-size: clamp(1.1rem, 3vw, 1.4rem);
            margin-bottom: 2.5rem;
            opacity: 0.9;
        }

        .btn-group {
            display: flex;
            gap: 1rem;
            justify-content: center;
            flex-wrap: wrap;
        }

        .btn {
            padding: 1rem 2.5rem;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 700;
            transition: var(--transition);
            display: inline-block;
            cursor: pointer;
        }

        .btn-primary {
            background-color: var(--brown);
            color: var(--white);
        }

        .btn-primary:hover {
            transform: scale(1.05);
            box-shadow: 0 10px 20px rgba(74, 44, 42, 0.2);
        }

        .btn-outline {
            border: 2px solid var(--brown);
            color: var(--brown);
        }

        .btn-outline:hover {
            background-color: var(--brown);
            color: var(--white);
        }

        .badge {
            display: inline-block;
            background: rgba(255, 255, 255, 0.6);
            padding: 0.5rem 1.2rem;
            border-radius: 50px;
            margin-bottom: 2rem;
            font-weight: 700;
            backdrop-filter: blur(5px);
            border: 1px solid rgba(74, 44, 42, 0.1);
        }

        /* Floating Icons */
        .floating-icon {
            position: absolute;
            opacity: 0.15;
            z-index: 1;
            animation: float 6s ease-in-out infinite;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0) rotate(0deg); }
            50% { transform: translateY(-20px) rotate(10deg); }
        }

        /* --- Trust Bar --- */
        .trust-bar {
            background: var(--brown);
            color: var(--white);
            padding: 0.8rem 0;
            overflow: hidden;
            white-space: nowrap;
        }

        .ticker {
            display: inline-block;
            animation: marquee 30s linear infinite;
        }

        .ticker span {
            display: inline-block;
            padding-right: 3rem;
            font-weight: 700;
            text-transform: uppercase;
            font-size: 0.9rem;
            letter-spacing: 1px;
        }

        @keyframes marquee {
            0% { transform: translateX(0); }
            100% { transform: translateX(-50%); }
        }

        /* --- About Section --- */
        .section-padding { padding: 5rem 10%; }

        .about-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 4rem;
            align-items: center;
        }

        .about-img {
            width: 100%;
            height: 500px;
            border-radius: 20px;
            object-fit: cover;
            box-shadow: 20px 20px 0 var(--sage);
        }

        .feature-pills {
            display: flex;
            gap: 1rem;
            margin-top: 2rem;
            flex-wrap: wrap;
        }

        .pill {
            background: var(--rose);
            padding: 0.5rem 1rem;
            border-radius: 50px;
            color: var(--white);
            font-weight: 700;
            font-size: 0.9rem;
        }

        /* --- Menu Section --- */
        .menu-section { background-color: var(--white); text-align: center; }

        .menu-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 2rem;
            margin-top: 3rem;
        }

        .menu-card {
            background: var(--cream);
            padding: 2.5rem;
            border-radius: 20px;
            text-align: left;
            transition: var(--transition);
            border: 1px solid rgba(143, 175, 140, 0.2);
        }

        .menu-card:hover { transform: translateY(-10px); box-shadow: 0 15px 30px rgba(0,0,0,0.05); }

        .menu-card h3 { color: var(--rose); margin-bottom: 1rem; font-size: 1.8rem; }
        
        .menu-card ul { list-style: none; }
        .menu-card li { margin-bottom: 0.5rem; position: relative; padding-left: 1.5rem; }
        .menu-card li::before { content: '•'; position: absolute; left: 0; color: var(--sage); font-weight: bold; }

        .meal-deal {
            background: var(--rose);
            color: var(--brown);
            padding: 1.5rem;
            border-radius: 15px;
            margin-top: 3rem;
            font-weight: 700;
            font-size: 1.2rem;
            display: inline-block;
        }

        /* --- Info Section --- */
        .info-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 3rem;
        }

        .status-badge {
            padding: 0.3rem 0.8rem;
            border-radius: 5px;
            font-weight: 700;
            font-size: 0.8rem;
            margin-left: 10px;
        }
        .status-open { background: #d4edda; color: #155724; }
        .status-closed { background: #f8d7da; color: #721c24; }

        .map-container {
            width: 100%;
            height: 300px;
            border-radius: 15px;
            overflow: hidden;
            margin-top: 1.5rem;
        }

        .info-icons {
            display: flex;
            gap: 1.5rem;
            margin-top: 1.5rem;
            font-size: 0.85rem;
            font-weight: 700;
            flex-wrap: wrap;
        }

        /* --- Review Carousel --- */
        .reviews-section { background: var(--cream); overflow: hidden; }
        
        .review-viewport {
            width: 100%;
            overflow: hidden;
            margin-top: 3rem;
            cursor: grab;
        }

        .review-track {
            display: flex;
            transition: transform 0.5s ease-out;
            gap: 2rem;
        }

        .review-card {
            min-width: 350px;
            background: var(--white);
            padding: 2rem;
            border-radius: 15px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.03);
        }

        .stars { color: #FFD700; margin-bottom: 0.5rem; }
        .reviewer { font-weight: 700; display: block; margin-bottom: 0.2rem; }
        .review-date { font-size: 0.8rem; color: #888; margin-bottom: 1rem; display: block; }
        
        .review-text {
            font-size: 0.95rem;
            display: -webkit-box;
            -webkit-line-clamp: 3;
            -webkit-box-orient: vertical;
            overflow: hidden;
        }

        .review-text.expanded {
            -webkit-line-clamp: unset;
        }

        .read-more {
            color: var(--sage);
            font-weight: 700;
            cursor: pointer;
            font-size: 0.85rem;
            display: block;
            margin-top: 0.5rem;
        }

        /* --- Footer Section --- */
        .final-cta {
            background: var(--brown);
            color: var(--white);
            text-align: center;
            padding: 5rem 10%;
        }

        .final-cta h2 { font-size: 2.5rem; margin-bottom: 1rem; }
        
        footer {
            background: #361f1e;
            color: rgba(255,255,255,0.7);
            padding: 2rem 10%;
            text-align: center;
            font-size: 0.9rem;
        }

        .social-link {
            color: var(--white);
            font-size: 1.5rem;
            margin-top: 1rem;
            display: inline-block;
            text-decoration: none;
        }

        /* --- Responsive --- */
        @media (max-width: 900px) {
            .about-grid, .info-grid { grid-template-columns: 1fr; }
            .about-img { height: 350px; order: -1; }
            .menu-grid { grid-template-columns: 1fr; }
            .section-padding { padding: 4rem 5%; }
        }

        @media (max-width: 600px) {
            .hero h1 { font-size: 2.5rem; }
            .review-card { min-width: 280px; }
        }
    </style>
</head>
<body>

    <!-- Section 1: Hero -->
    <header class="hero">
        <!-- Floating SVGs -->
        <svg class="floating-icon" style="top: 15%; left: 10%; width: 60px;" viewBox="0 0 24 24" fill="currentColor"><path d="M11 2c.047 0 .092.006.137.017a2.502 2.502 0 0 1 4.726 0c.045-.011.09-.017.137-.017 1.38 0 2.5 1.12 2.5 2.5 0 .597-.216 1.138-.567 1.56.35.423.567.964.567 1.561 0 1.38-1.12 2.5-2.5 2.5-.047 0-.092-.006-.137-.017a2.502 2.502 0 0 1-4.726 0c-.045.011-.09.017-.137.017-1.38 0-2.5-1.12-2.5-2.5 0-.597.216-1.138.567-1.56a2.506 2.506 0 0 1-.567-1.561c0-1.38 1.12-2.5 2.5-2.5zm0 14h2v2h-2v-2zm-6-2h14v1h-14v-1zm0 2h14v1h-14v-1zm-1 3h16v1h-16v-1z"/></svg>
        <svg class="floating-icon" style="bottom: 20%; right: 10%; width: 50px;" viewBox="0 0 24 24" fill="currentColor"><path d="M2 21h18v-2H2v2zM20 8h-2V5h2v3zm2-3h-4a2 2 0 0 0-2 2v3a2 2 0 0 0 2 2h4a2 2 0 0 0 2-2V7a2 2 0 0 0-2-2zM4 19h14v-9H4v9zM14 5c0-1.1-.9-2-2-2s-2 .9-2 2h4z"/></svg>
        
        <div class="hero-content reveal">
            <span class="badge">⭐ 4.9/5 on Google · 100% Recommend on Facebook</span>
            <h1>Homemade with Heart. <br>Fresh Every Day.</h1>
            <p>Wirral's cosiest little café — cakes, sandwiches & speciality coffee in the heart of Upton</p>
            <div class="btn-group">
                <a href="#menu" class="btn btn-primary">See Our Menu ↓</a>
                <a href="#visit" class="btn btn-outline">Find Us</a>
            </div>
        </div>
    </header>

    <!-- Section 2: Trust Bar -->
    <div class="trust-bar">
        <div class="ticker">
            <span>🍰 100% Recommend on Facebook</span>
            <span>⭐ 4.9 Google Rating</span>
            <span>☕ Fresh Made Daily</span>
            <span>🐾 Dog Friendly</span>
            <span>📶 Free Wi-Fi</span>
            <span>👨‍👩‍👧 Family Friendly</span>
            <span>🅿️ Free Nearby Parking</span>
            <!-- Duplicate for infinite effect -->
            <span>🍰 100% Recommend on Facebook</span>
            <span>⭐ 4.9 Google Rating</span>
            <span>☕ Fresh Made Daily</span>
            <span>🐾 Dog Friendly</span>
            <span>📶 Free Wi-Fi</span>
            <span>👨‍👩‍👧 Family Friendly</span>
            <span>🅿️ Free Nearby Parking</span>
        </div>
    </div>

    <!-- Section 3: About -->
    <section class="section-padding reveal">
        <div class="about-grid">
            <img src="https://images.unsplash.com/photo-1559339352-11d035aa65de?q=80&w=1000" alt="Delicious Cakes" class="about-img">
            <div>
                <h2>A Little Café With a Big Heart</h2>
                <p style="margin: 1.5rem 0;">Cakes by the Lakes is Wirral's best-kept secret — a homemade, traditional café tucked away at 397 Upton Road, Noctorum. Everything is freshly made, the counter changes daily, and you'll always leave with a smile. Whether you're after a hearty sandwich, a stunning celebration cake, or just a slice of school cake and a latte — you've found your place.</p>
                <div class="feature-pills">
                    <span class="pill">🏠 Family Run</span>
                    <span class="pill">🌿 Fresh Daily</span>
                    <span class="pill">💛 Affordable Prices</span>
                </div>
            </div>
        </div>
    </section>

    <!-- Section 4: Menu -->
    <section id="menu" class="section-padding menu-section reveal">
        <h2>What's On the Counter Today</h2>
        <p>Our menu rotates daily — here's a taste of what to expect</p>
        
        <div class="menu-grid">
            <div class="menu-card reveal">
                <h3>🍰 Sweet Treats</h3>
                <ul>
                    <li>Victoria Sponge</li>
                    <li>Biscoff Cream Buns</li>
                    <li>Lemon Drizzle & Coffee & Walnut</li>
                    <li>Brownies & Kinder Brownies</li>
                    <li>Custard Tarts & School Cake</li>
                    <li>Milkybar Cheesecake & Caramel Cakes</li>
                </ul>
            </div>
            <div class="menu-card reveal">
                <h3>🥪 Savoury & Lunch</h3>
                <ul>
                    <li>Salt & Pepper Sausage Rolls</li>
                    <li>Nudger Sandwiches</li>
                    <li>Freshly Made Bagels & Toasties</li>
                    <li>Jacket Potatoes</li>
                    <li>Healthy Wraps</li>
                </ul>
            </div>
            <div class="menu-card reveal">
                <h3>🥗 Boxes & Salads</h3>
                <ul>
                    <li>Pasta Boxes (Pesto / Tomato / Chinese Chicken)</li>
                    <li>Salad Boxes (Chicken Bacon Mayo, Tuna Mayo)</li>
                    <li>Gluten-Free Options Available</li>
                </ul>
            </div>
            <div class="menu-card reveal">
                <h3>☕ Drinks</h3>
                <ul>
                    <li>Specialty Coffees</li>
                    <li>Iced Frappes & Milkshakes</li>
                    <li>Hot Chocolate & Fresh Smoothies</li>
                </ul>
            </div>
        </div>
        
        <div class="meal-deal reveal">
            🎉 Meal Deal — Main + Cake + Hot Drink from just £7.50!
        </div>
    </section>

    <!-- Section 5: Visit & Hours -->
    <section id="visit" class="section-padding reveal">
        <div class="info-grid">
            <div>
                <h2>Visit Us</h2>
                <div style="margin-top:1.5rem">
                    <p><strong>Opening Hours:</strong></p>
                    <p>Mon – Fri: 10:00 AM – 2:30 PM <span id="open-status" class="status-badge">Checking...</span></p>
                    <p>Sat – Sun: Closed</p>
                </div>
                
                <div style="margin-top:2rem">
                    <p>📍 397 Upton Road, Noctorum, CH43 9SE</p>
                    <p>📞 +44 7548 880879</p>
                    <p>📧 cakesbythelakes.wirral@gmail.com</p>
                </div>

                <div class="info-icons">
                    <span>🐾 Dog Friendly</span>
                    <span>👶 High Chairs</span>
                    <span>📶 Free Wi-Fi</span>
                    <span>🅿️ Free Parking</span>
                </div>
            </div>
            <div>
                <div class="map-container">
                    <iframe 
                        src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2389.576822557106!2d-3.0768417232815127!3d53.383049172304!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x487b270726715f33%3A0x6420556f8f7813a4!2s397%20Upton%20Rd%2C%20Noctorum%2C%20Birkenhead%20CH43%209SE!5e0!3m2!1sen!2suk!4v1710000000000" 
                        width="100%" height="100%" style="border:0;" allowfullscreen="" loading="lazy"></iframe>
                </div>
            </div>
        </div>
    </section>

    <!-- Section 6: Reviews Carousel -->
    <section class="section-padding reviews-section">
        <h2 style="text-align: center;">What Our Guests Say</h2>
        <div class="review-viewport">
            <div class="review-track" id="review-track">
                <!-- Review 1 -->
                <div class="review-card">
                    <div class="stars">★★★★★</div>
                    <span class="reviewer">Hughes Louise Emma</span>
                    <span class="review-date">19 Feb 2025</span>
                    <p class="review-text">Been here a few times and what can I say — every cake I've tried have been beautiful. I tried the huge nudger sandwich too the other day and it was amazing so fresh and the coleslaw was amazing. Highly recommend.</p>
                    <span class="read-more" onclick="toggleReview(this)">Read more</span>
                </div>
                <!-- Review 2 -->
                <div class="review-card">
                    <div class="stars">★★★★★</div>
                    <span class="reviewer">Louise Forster-Kerr</span>
                    <span class="review-date">25 Jan 2025</span>
                    <p class="review-text">Such a gorgeous little local spot! Lovely sandwiches, bagels and toasties...and the cakes wow! The staff are so friendly. My mum really fancied a meringue and there were none left, so the lovely lady went in the back and made her one! 10/10 customer service ✨</p>
                    <span class="read-more" onclick="toggleReview(this)">Read more</span>
                </div>
                <!-- Review 3 -->
                <div class="review-card">
                    <div class="stars">★★★★★</div>
                    <span class="reviewer">Tina Denise</span>
                    <span class="review-date">30 Nov 2024</span>
                    <p class="review-text">Love this place. It's warm and inviting. The bread is delicious, amazing salad boxes and the cakes — well I have no words. They are just delicious and all at affordable prices. I definitely recommend.</p>
                    <span class="read-more" onclick="toggleReview(this)">Read more</span>
                </div>
                <!-- Review 4 -->
                <div class="review-card">
                    <div class="stars">★★★★★</div>
                    <span class="reviewer">Valerie Jones</span>
                    <span class="review-date">3 May 2025</span>
                    <p class="review<!DOCTYPE html>
<html lang="en-GB">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Cakes by the Lakes Wirral | Homemade Café in Upton, Wirral</title>
    <meta name="description" content="Wirral's cosiest little café in Upton. Freshly made cakes, artisan sandwiches, and speciality coffee. Family-run, dog-friendly, and warm atmosphere.">
    
    <!-- Open Graph Tags -->
    <meta property="og:title" content="Cakes by the Lakes Wirral | Homemade Café">
    <meta property="og:description" content="Artisan cakes, sandwiches & coffee in the heart of Upton. Freshly made every day with heart.">
    <meta property="og:type" content="website">
    <meta property="og:url" content="https://cakesbythelakeswirral.co.uk">

    <!-- Google Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Lato:wght@400;700&family=Playfair+Display:ital,wght@0,700;1,700&display=swap" rel="stylesheet">

    <style>
        :root {
            --cream: #FDF6EC;
            --rose: #E8A598;
            --sage: #8FAF8C;
            --brown: #4A2C2A;
            --white: #ffffff;
            --transition: all 0.4s cubic-bezier(0.165, 0.84, 0.44, 1);
        }

        * { margin: 0; padding: 0; box-sizing: border-box; }

        body {
            font-family: 'Lato', sans-serif;
            background-color: var(--cream);
            color: var(--brown);
            line-height: 1.6;
            overflow-x: hidden;
        }

        h1, h2, h3, h4 {
            font-family: 'Playfair Display', serif;
            font-weight: 700;
        }

        /* --- Global Animations --- */
        .reveal {
            opacity: 0;
            transform: translateY(30px);
            transition: var(--transition);
        }

        .reveal.active {
            opacity: 1;
            transform: translateY(0);
        }

        /* --- Hero Section --- */
        .hero {
            position: relative;
            min-height: 90vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            padding: 2rem;
            background: linear-gradient(135deg, var(--cream) 0%, var(--rose) 100%);
            overflow: hidden;
        }

        .hero-content {
            z-index: 2;
            max-width: 800px;
        }

        .hero h1 {
            font-size: clamp(2.5rem, 8vw, 4.5rem);
            line-height: 1.1;
            margin-bottom: 1.5rem;
        }

        .hero p {
            font-size: clamp(1.1rem, 3vw, 1.4rem);
            margin-bottom: 2.5rem;
            opacity: 0.9;
        }

        .btn-group {
            display: flex;
            gap: 1rem;
            justify-content: center;
            flex-wrap: wrap;
        }

        .btn {
            padding: 1rem 2.5rem;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 700;
            transition: var(--transition);
            display: inline-block;
            cursor: pointer;
        }

        .btn-primary {
            background-color: var(--brown);
            color: var(--white);
        }

        .btn-primary:hover {
            transform: scale(1.05);
            box-shadow: 0 10px 20px rgba(74, 44, 42, 0.2);
        }

        .btn-outline {
            border: 2px solid var(--brown);
            color: var(--brown);
        }

        .btn-outline:hover {
            background-color: var(--brown);
            color: var(--white);
        }

        .badge {
            display: inline-block;
            background: rgba(255, 255, 255, 0.6);
            padding: 0.5rem 1.2rem;
            border-radius: 50px;
            margin-bottom: 2rem;
            font-weight: 700;
            backdrop-filter: blur(5px);
            border: 1px solid rgba(74, 44, 42, 0.1);
        }

        /* Floating Icons */
        .floating-icon {
            position: absolute;
            opacity: 0.15;
            z-index: 1;
            animation: float 6s ease-in-out infinite;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0) rotate(0deg); }
            50% { transform: translateY(-20px) rotate(10deg); }
        }

        /* --- Trust Bar --- */
        .trust-bar {
            background: var(--brown);
            color: var(--white);
            padding: 0.8rem 0;
            overflow: hidden;
            white-space: nowrap;
        }

        .ticker {
            display: inline-block;
            animation: marquee 30s linear infinite;
        }

        .ticker span {
            display: inline-block;
            padding-right: 3rem;
            font-weight: 700;
            text-transform: uppercase;
            font-size: 0.9rem;
            letter-spacing: 1px;
        }

        @keyframes marquee {
            0% { transform: translateX(0); }
            100% { transform: translateX(-50%); }
        }

        /* --- About Section --- */
        .section-padding { padding: 5rem 10%; }

        .about-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 4rem;
            align-items: center;
        }

        .about-img {
            width: 100%;
            height: 500px;
            border-radius: 20px;
            object-fit: cover;
            box-shadow: 20px 20px 0 var(--sage);
        }

        .feature-pills {
            display: flex;
            gap: 1rem;
            margin-top: 2rem;
            flex-wrap: wrap;
        }

        .pill {
            background: var(--rose);
            padding: 0.5rem 1rem;
            border-radius: 50px;
            color: var(--white);
            font-weight: 700;
            font-size: 0.9rem;
        }

        /* --- Menu Section --- */
        .menu-section { background-color: var(--white); text-align: center; }

        .menu-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 2rem;
            margin-top: 3rem;
        }

        .menu-card {
            background: var(--cream);
            padding: 2.5rem;
            border-radius: 20px;
            text-align: left;
            transition: var(--transition);
            border: 1px solid rgba(143, 175, 140, 0.2);
        }

        .menu-card:hover { transform: translateY(-10px); box-shadow: 0 15px 30px rgba(0,0,0,0.05); }

        .menu-card h3 { color: var(--rose); margin-bottom: 1rem; font-size: 1.8rem; }
        
        .menu-card ul { list-style: none; }
        .menu-card li { margin-bottom: 0.5rem; position: relative; padding-left: 1.5rem; }
        .menu-card li::before { content: '•'; position: absolute; left: 0; color: var(--sage); font-weight: bold; }

        .meal-deal {
            background: var(--rose);
            color: var(--brown);
            padding: 1.5rem;
            border-radius: 15px;
            margin-top: 3rem;
            font-weight: 700;
            font-size: 1.2rem;
            display: inline-block;
        }

        /* --- Info Section --- */
        .info-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 3rem;
        }

        .status-badge {
            padding: 0.3rem 0.8rem;
            border-radius: 5px;
            font-weight: 700;
            font-size: 0.8rem;
            margin-left: 10px;
        }
        .status-open { background: #d4edda; color: #155724; }
        .status-closed { background: #f8d7da; color: #721c24; }

        .map-container {
            width: 100%;
            height: 300px;
            border-radius: 15px;
            overflow: hidden;
            margin-top: 1.5rem;
        }

        .info-icons {
            display: flex;
            gap: 1.5rem;
            margin-top: 1.5rem;
            font-size: 0.85rem;
            font-weight: 700;
            flex-wrap: wrap;
        }

        /* --- Review Carousel --- */
        .reviews-section { background: var(--cream); overflow: hidden; }
        
        .review-viewport {
            width: 100%;
            overflow: hidden;
            margin-top: 3rem;
            cursor: grab;
        }

        .review-track {
            display: flex;
            transition: transform 0.5s ease-out;
            gap: 2rem;
        }

        .review-card {
            min-width: 350px;
            background: var(--white);
            padding: 2rem;
            border-radius: 15px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.03);
        }

        .stars { color: #FFD700; margin-bottom: 0.5rem; }
        .reviewer { font-weight: 700; display: block; margin-bottom: 0.2rem; }
        .review-date { font-size: 0.8rem; color: #888; margin-bottom: 1rem; display: block; }
        
        .review-text {
            font-size: 0.95rem;
            display: -webkit-box;
            -webkit-line-clamp: 3;
            -webkit-box-orient: vertical;
            overflow: hidden;
        }

        .review-text.expanded {
            -webkit-line-clamp: unset;
        }

        .read-more {
            color: var(--sage);
            font-weight: 700;
            cursor: pointer;
            font-size: 0.85rem;
            display: block;
            margin-top: 0.5rem;
        }

        /* --- Footer Section --- */
        .final-cta {
            background: var(--brown);
            color: var(--white);
            text-align: center;
            padding: 5rem 10%;
        }

        .final-cta h2 { font-size: 2.5rem; margin-bottom: 1rem; }
        
        footer {
            background: #361f1e;
            color: rgba(255,255,255,0.7);
            padding: 2rem 10%;
            text-align: center;
            font-size: 0.9rem;
        }

        .social-link {
            color: var(--white);
            font-size: 1.5rem;
            margin-top: 1rem;
            display: inline-block;
            text-decoration: none;
        }

        /* --- Responsive --- */
        @media (max-width: 900px) {
            .about-grid, .info-grid { grid-template-columns: 1fr; }
            .about-img { height: 350px; order: -1; }
            .menu-grid { grid-template-columns: 1fr; }
            .section-padding { padding: 4rem 5%; }
        }

        @media (max-width: 600px) {
            .hero h1 { font-size: 2.5rem; }
            .review-card { min-width: 280px; }
        }
    </style>
</head>
<body>

    <!-- Section 1: Hero -->
    <header class="hero">
        <!-- Floating SVGs -->
        <svg class="floating-icon" style="top: 15%; left: 10%; width: 60px;" viewBox="0 0 24 24" fill="currentColor"><path d="M11 2c.047 0 .092.006.137.017a2.502 2.502 0 0 1 4.726 0c.045-.011.09-.017.137-.017 1.38 0 2.5 1.12 2.5 2.5 0 .597-.216 1.138-.567 1.56.35.423.567.964.567 1.561 0 1.38-1.12 2.5-2.5 2.5-.047 0-.092-.006-.137-.017a2.502 2.502 0 0 1-4.726 0c-.045.011-.09.017-.137.017-1.38 0-2.5-1.12-2.5-2.5 0-.597.216-1.138.567-1.56a2.506 2.506 0 0 1-.567-1.561c0-1.38 1.12-2.5 2.5-2.5zm0 14h2v2h-2v-2zm-6-2h14v1h-14v-1zm0 2h14v1h-14v-1zm-1 3h16v1h-16v-1z"/></svg>
        <svg class="floating-icon" style="bottom: 20%; right: 10%; width: 50px;" viewBox="0 0 24 24" fill="currentColor"><path d="M2 21h18v-2H2v2zM20 8h-2V5h2v3zm2-3h-4a2 2 0 0 0-2 2v3a2 2 0 0 0 2 2h4a2 2 0 0 0 2-2V7a2 2 0 0 0-2-2zM4 19h14v-9H4v9zM14 5c0-1.1-.9-2-2-2s-2 .9-2 2h4z"/></svg>
        
        <div class="hero-content reveal">
            <span class="badge">⭐ 4.9/5 on Google · 100% Recommend on Facebook</span>
            <h1>Homemade with Heart. <br>Fresh Every Day.</h1>
            <p>Wirral's cosiest little café — cakes, sandwiches & speciality coffee in the heart of Upton</p>
            <div class="btn-group">
                <a href="#menu" class="btn btn-primary">See Our Menu ↓</a>
                <a href="#visit" class="btn btn-outline">Find Us</a>
            </div>
        </div>
    </header>

    <!-- Section 2: Trust Bar -->
    <div class="trust-bar">
        <div class="ticker">
            <span>🍰 100% Recommend on Facebook</span>
            <span>⭐ 4.9 Google Rating</span>
            <span>☕ Fresh Made Daily</span>
            <span>🐾 Dog Friendly</span>
            <span>📶 Free Wi-Fi</span>
            <span>👨‍👩‍👧 Family Friendly</span>
            <span>🅿️ Free Nearby Parking</span>
            <!-- Duplicate for infinite effect -->
            <span>🍰 100% Recommend on Facebook</span>
            <span>⭐ 4.9 Google Rating</span>
            <span>☕ Fresh Made Daily</span>
            <span>🐾 Dog Friendly</span>
            <span>📶 Free Wi-Fi</span>
            <span>👨‍👩‍👧 Family Friendly</span>
            <span>🅿️ Free Nearby Parking</span>
        </div>
    </div>

    <!-- Section 3: About -->
    <section class="section-padding reveal">
        <div class="about-grid">
            <img src="https://images.unsplash.com/photo-1559339352-11d035aa65de?q=80&w=1000" alt="Delicious Cakes" class="about-img">
            <div>
                <h2>A Little Café With a Big Heart</h2>
                <p style="margin: 1.5rem 0;">Cakes by the Lakes is Wirral's best-kept secret — a homemade, traditional café tucked away at 397 Upton Road, Noctorum. Everything is freshly made, the counter changes daily, and you'll always leave with a smile. Whether you're after a hearty sandwich, a stunning celebration cake, or just a slice of school cake and a latte — you've found your place.</p>
                <div class="feature-pills">
                    <span class="pill">🏠 Family Run</span>
                    <span class="pill">🌿 Fresh Daily</span>
                    <span class="pill">💛 Affordable Prices</span>
                </div>
            </div>
        </div>
    </section>

    <!-- Section 4: Menu -->
    <section id="menu" class="section-padding menu-section reveal">
        <h2>What's On the Counter Today</h2>
        <p>Our menu rotates daily — here's a taste of what to expect</p>
        
        <div class="menu-grid">
            <div class="menu-card reveal">
                <h3>🍰 Sweet Treats</h3>
                <ul>
                    <li>Victoria Sponge</li>
                    <li>Biscoff Cream Buns</li>
                    <li>Lemon Drizzle & Coffee & Walnut</li>
                    <li>Brownies & Kinder Brownies</li>
                    <li>Custard Tarts & School Cake</li>
                    <li>Milkybar Cheesecake & Caramel Cakes</li>
                </ul>
            </div>
            <div class="menu-card reveal">
                <h3>🥪 Savoury & Lunch</h3>
                <ul>
                    <li>Salt & Pepper Sausage Rolls</li>
                    <li>Nudger Sandwiches</li>
                    <li>Freshly Made Bagels & Toasties</li>
                    <li>Jacket Potatoes</li>
                    <li>Healthy Wraps</li>
                </ul>
            </div>
            <div class="menu-card reveal">
                <h3>🥗 Boxes & Salads</h3>
                <ul>
                    <li>Pasta Boxes (Pesto / Tomato / Chinese Chicken)</li>
                    <li>Salad Boxes (Chicken Bacon Mayo, Tuna Mayo)</li>
                    <li>Gluten-Free Options Available</li>
                </ul>
            </div>
            <div class="menu-card reveal">
                <h3>☕ Drinks</h3>
                <ul>
                    <li>Specialty Coffees</li>
                    <li>Iced Frappes & Milkshakes</li>
                    <li>Hot Chocolate & Fresh Smoothies</li>
                </ul>
            </div>
        </div>
        
        <div class="meal-deal reveal">
            🎉 Meal Deal — Main + Cake + Hot Drink from just £7.50!
        </div>
    </section>

    <!-- Section 5: Visit & Hours -->
    <section id="visit" class="section-padding reveal">
        <div class="info-grid">
            <div>
                <h2>Visit Us</h2>
                <div style="margin-top:1.5rem">
                    <p><strong>Opening Hours:</strong></p>
                    <p>Mon – Fri: 10:00 AM – 2:30 PM <span id="open-status" class="status-badge">Checking...</span></p>
                    <p>Sat – Sun: Closed</p>
                </div>
                
                <div style="margin-top:2rem">
                    <p>📍 397 Upton Road, Noctorum, CH43 9SE</p>
                    <p>📞 +44 7548 880879</p>
                    <p>📧 cakesbythelakes.wirral@gmail.com</p>
                </div>

                <div class="info-icons">
                    <span>🐾 Dog Friendly</span>
                    <span>👶 High Chairs</span>
                    <span>📶 Free Wi-Fi</span>
                    <span>🅿️ Free Parking</span>
                </div>
            </div>
            <div>
                <div class="map-container">
                    <iframe 
                        src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2389.576822557106!2d-3.0768417232815127!3d53.383049172304!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x487b270726715f33%3A0x6420556f8f7813a4!2s397%20Upton%20Rd%2C%20Noctorum%2C%20Birkenhead%20CH43%209SE!5e0!3m2!1sen!2suk!4v1710000000000" 
                        width="100%" height="100%" style="border:0;" allowfullscreen="" loading="lazy"></iframe>
                </div>
            </div>
        </div>
    </section>

    <!-- Section 6: Reviews Carousel -->
    <section class="section-padding reviews-section">
        <h2 style="text-align: center;">What Our Guests Say</h2>
        <div class="review-viewport">
            <div class="review-track" id="review-track">
                <!-- Review 1 -->
                <div class="review-card">
                    <div class="stars">★★★★★</div>
                    <span class="reviewer">Hughes Louise Emma</span>
                    <span class="review-date">19 Feb 2025</span>
                    <p class="review-text">Been here a few times and what can I say — every cake I've tried have been beautiful. I tried the huge nudger sandwich too the other day and it was amazing so fresh and the coleslaw was amazing. Highly recommend.</p>
                    <span class="read-more" onclick="toggleReview(this)">Read more</span>
                </div>
                <!-- Review 2 -->
                <div class="review-card">
                    <div class="stars">★★★★★</div>
                    <span class="reviewer">Louise Forster-Kerr</span>
                    <span class="review-date">25 Jan 2025</span>
                    <p class="review-text">Such a gorgeous little local spot! Lovely sandwiches, bagels and toasties...and the cakes wow! The staff are so friendly. My mum really fancied a meringue and there were none left, so the lovely lady went in the back and made her one! 10/10 customer service ✨</p>
                    <span class="read-more" onclick="toggleReview(this)">Read more</span>
                </div>
                <!-- Review 3 -->
                <div class="review-card">
                    <div class="stars">★★★★★</div>
                    <span class="reviewer">Tina Denise</span>
                    <span class="review-date">30 Nov 2024</span>
                    <p class="review-text">Love this place. It's warm and inviting. The bread is delicious, amazing salad boxes and the cakes — well I have no words. They are just delicious and all at affordable prices. I definitely recommend.</p>
                    <span class="read-more" onclick="toggleReview(this)">Read more</span>
                </div>
                <!-- Review 4 -->
                <div class="review-card">
                    <div class="stars">★★★★★</div>
                    <span class="reviewer">Valerie Jones</span>
                    <span class="review-date">3 May 2025</span>
                    <p class="review-text">My husband and I had lunch here a few w<!DOCTYPE html>
<html lang="en-GB">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Cakes by the Lakes Wirral | Homemade Café in Upton, Wirral</title>
    <meta name="description" content="Wirral's cosiest little café in Upton. Freshly made cakes, artisan sandwiches, and speciality coffee. Family-run, dog-friendly, and warm atmosphere.">
    
    <!-- Open Graph Tags -->
    <meta property="og:title" content="Cakes by the Lakes Wirral | Homemade Café">
    <meta property="og:description" content="Artisan cakes, sandwiches & coffee in the heart of Upton. Freshly made every day with heart.">
    <meta property="og:type" content="website">
    <meta property="og:url" content="https://cakesbythelakeswirral.co.uk">

    <!-- Google Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Lato:wght@400;700&family=Playfair+Display:ital,wght@0,700;1,700&display=swap" rel="stylesheet">

    <style>
        :root {
            --cream: #FDF6EC;
            --rose: #E8A598;
            --sage: #8FAF8C;
            --brown: #4A2C2A;
            --white: #ffffff;
            --transition: all 0.4s cubic-bezier(0.165, 0.84, 0.44, 1);
        }

        * { margin: 0; padding: 0; box-sizing: border-box; }

        body {
            font-family: 'Lato', sans-serif;
            background-color: var(--cream);
            color: var(--brown);
            line-height: 1.6;
            overflow-x: hidden;
        }

        h1, h2, h3, h4 {
            font-family: 'Playfair Display', serif;
            font-weight: 700;
        }

        /* --- Global Animations --- */
        .reveal {
            opacity: 0;
            transform: translateY(30px);
            transition: var(--transition);
        }

        .reveal.active {
            opacity: 1;
            transform: translateY(0);
        }

        /* --- Hero Section --- */
        .hero {
            position: relative;
            min-height: 90vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            padding: 2rem;
            background: linear-gradient(135deg, var(--cream) 0%, var(--rose) 100%);
            overflow: hidden;
        }

        .hero-content {
            z-index: 2;
            max-width: 800px;
        }

        .hero h1 {
            font-size: clamp(2.5rem, 8vw, 4.5rem);
            line-height: 1.1;
            margin-bottom: 1.5rem;
        }

        .hero p {
            font-size: clamp(1.1rem, 3vw, 1.4rem);
            margin-bottom: 2.5rem;
            opacity: 0.9;
        }

        .btn-group {
            display: flex;
            gap: 1rem;
            justify-content: center;
            flex-wrap: wrap;
        }

        .btn {
            padding: 1rem 2.5rem;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 700;
            transition: var(--transition);
            display: inline-block;
            cursor: pointer;
        }

        .btn-primary {
            background-color: var(--brown);
            color: var(--white);
        }

        .btn-primary:hover {
            transform: scale(1.05);
            box-shadow: 0 10px 20px rgba(74, 44, 42, 0.2);
        }

        .btn-outline {
            border: 2px solid var(--brown);
            color: var(--brown);
        }

        .btn-outline:hover {
            background-color: var(--brown);
            color: var(--white);
        }

        .badge {
            display: inline-block;
            background: rgba(255, 255, 255, 0.6);
            padding: 0.5rem 1.2rem;
            border-radius: 50px;
            margin-bottom: 2rem;
            font-weight: 700;
            backdrop-filter: blur(5px);
            border: 1px solid rgba(74, 44, 42, 0.1);
        }

        /* Floating Icons */
        .floating-icon {
            position: absolute;
            opacity: 0.15;
            z-index: 1;
            animation: float 6s ease-in-out infinite;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0) rotate(0deg); }
            50% { transform: translateY(-20px) rotate(10deg); }
        }

        /* --- Trust Bar --- */
        .trust-bar {
            background: var(--brown);
            color: var(--white);
            padding: 0.8rem 0;
            overflow: hidden;
            white-space: nowrap;
        }

        .ticker {
            display: inline-block;
            animation: marquee 30s linear infinite;
        }

        .ticker span {
            display: inline-block;
            padding-right: 3rem;
            font-weight: 700;
            text-transform: uppercase;
            font-size: 0.9rem;
            letter-spacing: 1px;
        }

        @keyframes marquee {
            0% { transform: translateX(0); }
            100% { transform: translateX(-50%); }
        }

        /* --- About Section --- */
        .section-padding { padding: 5rem 10%; }

        .about-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 4rem;
            align-items: center;
        }

        .about-img {
            width: 100%;
            height: 500px;
            border-radius: 20px;
            object-fit: cover;
            box-shadow: 20px 20px 0 var(--sage);
        }

        .feature-pills {
            display: flex;
            gap: 1rem;
            margin-top: 2rem;
            flex-wrap: wrap;
        }

        .pill {
            background: var(--rose);
            padding: 0.5rem 1rem;
            border-radius: 50px;
            color: var(--white);
            font-weight: 700;
            font-size: 0.9rem;
        }

        /* --- Menu Section --- */
        .menu-section { background-color: var(--white); text-align: center; }

        .menu-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 2rem;
            margin-top: 3rem;
        }

        .menu-card {
            background: var(--cream);
            padding: 2.5rem;
            border-radius: 20px;
            text-align: left;
            transition: var(--transition);
            border: 1px solid rgba(143, 175, 140, 0.2);
        }

        .menu-card:hover { transform: translateY(-10px); box-shadow: 0 15px 30px rgba(0,0,0,0.05); }

        .menu-card h3 { color: var(--rose); margin-bottom: 1rem; font-size: 1.8rem; }
        
        .menu-card ul { list-style: none; }
        .menu-card li { margin-bottom: 0.5rem; position: relative; padding-left: 1.5rem; }
        .menu-card li::before { content: '•'; position: absolute; left: 0; color: var(--sage); font-weight: bold; }

        .meal-deal {
            background: var(--rose);
            color: var(--brown);
            padding: 1.5rem;
            border-radius: 15px;
            margin-top: 3rem;
            font-weight: 700;
            font-size: 1.2rem;
            display: inline-block;
        }

        /* --- Info Section --- */
        .info-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 3rem;
        }

        .status-badge {
            padding: 0.3rem 0.8rem;
            border-radius: 5px;
            font-weight: 700;
            font-size: 0.8rem;
            margin-left: 10px;
        }
        .status-open { background: #d4edda; color: #155724; }
        .status-closed { background: #f8d7da; color: #721c24; }

        .map-container {
            width: 100%;
            height: 300px;
            border-radius: 15px;
            overflow: hidden;
            margin-top: 1.5rem;
        }

        .info-icons {
            display: flex;
            gap: 1.5rem;
            margin-top: 1.5rem;
            font-size: 0.85rem;
            font-weight: 700;
            flex-wrap: wrap;
        }

        /* --- Review Carousel --- */
        .reviews-section { background: var(--cream); overflow: hidden; }
        
        .review-viewport {
            width: 100%;
            overflow: hidden;
            margin-top: 3rem;
            cursor: grab;
        }

        .review-track {
            display: flex;
            transition: transform 0.5s ease-out;
            gap: 2rem;
        }

        .review-card {
            min-width: 350px;
            background: var(--white);
            padding: 2rem;
            border-radius: 15px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.03);
        }

        .stars { color: #FFD700; margin-bottom: 0.5rem; }
        .reviewer { font-weight: 700; display: block; margin-bottom: 0.2rem; }
        .review-date { font-size: 0.8rem; color: #888; margin-bottom: 1rem; display: block; }
        
        .review-text {
            font-size: 0.95rem;
            display: -webkit-box;
            -webkit-line-clamp: 3;
            -webkit-box-orient: vertical;
            overflow: hidden;
        }

        .review-text.expanded {
            -webkit-line-clamp: unset;
        }

        .read-more {
            color: var(--sage);
            font-weight: 700;
            cursor: pointer;
            font-size: 0.85rem;
            display: block;
            margin-top: 0.5rem;
        }

        /* --- Footer Section --- */
        .final-cta {
            background: var(--brown);
            color: var(--white);
            text-align: center;
            padding: 5rem 10%;
        }

        .final-cta h2 { font-size: 2.5rem; margin-bottom: 1rem; }
        
        footer {
            background: #361f1e;
            color: rgba(255,255,255,0.7);
            padding: 2rem 10%;
            text-align: center;
            font-size: 0.9rem;
        }

        .social-link {
            color: var(--white);
            font-size: 1.5rem;
            margin-top: 1rem;
            display: inline-block;
            text-decoration: none;
        }

        /* --- Responsive --- */
        @media (max-width: 900px) {
            .about-grid, .info-grid { grid-template-columns: 1fr; }
            .about-img { height: 350px; order: -1; }
            .menu-grid { grid-template-columns: 1fr; }
            .section-padding { padding: 4rem 5%; }
        }

        @media (max-width: 600px) {
            .hero h1 { font-size: 2.5rem; }
            .review-card { min-width: 280px; }
        }
    </style>
</head>
<body>

    <!-- Section 1: Hero -->
    <header class="hero">
        <!-- Floating SVGs -->
        <svg class="floating-icon" style="top: 15%; left: 10%; width: 60px;" viewBox="0 0 24 24" fill="currentColor"><path d="M11 2c.047 0 .092.006.137.017a2.502 2.502 0 0 1 4.726 0c.045-.011.09-.017.137-.017 1.38 0 2.5 1.12 2.5 2.5 0 .597-.216 1.138-.567 1.56.35.423.567.964.567 1.561 0 1.38-1.12 2.5-2.5 2.5-.047 0-.092-.006-.137-.017a2.502 2.502 0 0 1-4.726 0c-.045.011-.09.017-.137.017-1.38 0-2.5-1.12-2.5-2.5 0-.597.216-1.138.567-1.56a2.506 2.506 0 0 1-.567-1.561c0-1.38 1.12-2.5 2.5-2.5zm0 14h2v2h-2v-2zm-6-2h14v1h-14v-1zm0 2h14v1h-14v-1zm-1 3h16v1h-16v-1z"/></svg>
        <svg class="floating-icon" style="bottom: 20%; right: 10%; width: 50px;" viewBox="0 0 24 24" fill="currentColor"><path d="M2 21h18v-2H2v2zM20 8h-2V5h2v3zm2-3h-4a2 2 0 0 0-2 2v3a2 2 0 0 0 2 2h4a2 2 0 0 0 2-2V7a2 2 0 0 0-2-2zM4 19h14v-9H4v9zM14 5c0-1.1-.9-2-2-2s-2 .9-2 2h4z"/></svg>
        
        <div class="hero-content reveal">
            <span class="badge">⭐ 4.9/5 on Google · 100% Recommend on Facebook</span>
            <h1>Homemade with Heart. <br>Fresh Every Day.</h1>
            <p>Wirral's cosiest little café — cakes, sandwiches & speciality coffee in the heart of Upton</p>
            <div class="btn-group">
                <a href="#menu" class="btn btn-primary">See Our Menu ↓</a>
                <a href="#visit" class="btn btn-outline">Find Us</a>
            </div>
        </div>
    </header>

    <!-- Section 2: Trust Bar -->
    <div class="trust-bar">
        <div class="ticker">
            <span>🍰 100% Recommend on Facebook</span>
            <span>⭐ 4.9 Google Rating</span>
            <span>☕ Fresh Made Daily</span>
            <span>🐾 Dog Friendly</span>
            <span>📶 Free Wi-Fi</span>
            <span>👨‍👩‍👧 Family Friendly</span>
            <span>🅿️ Free Nearby Parking</span>
            <!-- Duplicate for infinite effect -->
            <span>🍰 100% Recommend on Facebook</span>
            <span>⭐ 4.9 Google Rating</span>
            <span>☕ Fresh Made Daily</span>
            <span>🐾 Dog Friendly</span>
            <span>📶 Free Wi-Fi</span>
            <span>👨‍👩‍👧 Family Friendly</span>
            <span>🅿️ Free Nearby Parking</span>
        </div>
    </div>

    <!-- Section 3: About -->
    <section class="section-padding reveal">
        <div class="about-grid">
            <img src="https://images.unsplash.com/photo-1559339352-11d035aa65de?q=80&w=1000" alt="Delicious Cakes" class="about-img">
            <div>
                <h2>A Little Café With a Big Heart</h2>
                <p style="margin: 1.5rem 0;">Cakes by the Lakes is Wirral's best-kept secret — a homemade, traditional café tucked away at 397 Upton Road, Noctorum. Everything is freshly made, the counter changes daily, and you'll always leave with a smile. Whether you're after a hearty sandwich, a stunning celebration cake, or just a slice of school cake and a latte — you've found your place.</p>
                <div class="feature-pills">
                    <span class="pill">🏠 Family Run</span>
                    <span class="pill">🌿 Fresh Daily</span>
                    <span class="pill">💛 Affordable Prices</span>
                </div>
            </div>
        </div>
    </section>

    <!-- Section 4: Menu -->
    <section id="menu" class="section-padding menu-section reveal">
        <h2>What's On the Counter Today</h2>
        <p>Our menu rotates daily — here's a taste of what to expect</p>
        
        <div class="menu-grid">
            <div class="menu-card reveal">
                <h3>🍰 Sweet Treats</h3>
                <ul>
                    <li>Victoria Sponge</li>
                    <li>Biscoff Cream Buns</li>
                    <li>Lemon Drizzle & Coffee & Walnut</li>
                    <li>Brownies & Kinder Brownies</li>
                    <li>Custard Tarts & School Cake</li>
                    <li>Milkybar Cheesecake & Caramel Cakes</li>
                </ul>
            </div>
            <div class="menu-card reveal">
                <h3>🥪 Savoury & Lunch</h3>
                <ul>
                    <li>Salt & Pepper Sausage Rolls</li>
                    <li>Nudger Sandwiches</li>
                    <li>Freshly Made Bagels & Toasties</li>
                    <li>Jacket Potatoes</li>
                    <li>Healthy Wraps</li>
                </ul>
            </div>
            <div class="menu-card reveal">
                <h3>🥗 Boxes & Salads</h3>
                <ul>
                    <li>Pasta Boxes (Pesto / Tomato / Chinese Chicken)</li>
                    <li>Salad Boxes (Chicken Bacon Mayo, Tuna Mayo)</li>
                    <li>Gluten-Free Options Available</li>
                </ul>
            </div>
            <div class="menu-card reveal">
                <h3>☕ Drinks</h3>
                <ul>
                    <li>Specialty Coffees</li>
                    <li>Iced Frappes & Milkshakes</li>
                    <li>Hot Chocolate & Fresh Smoothies</li>
                </ul>
            </div>
        </div>
        
        <div class="meal-deal reveal">
            🎉 Meal Deal — Main + Cake + Hot Drink from just £7.50!
        </div>
    </section>

    <!-- Section 5: Visit & Hours -->
    <section id="visit" class="section-padding reveal">
        <div class="info-grid">
            <div>
                <h2>Visit Us</h2>
                <div style="margin-top:1.5rem">
                    <p><strong>Opening Hours:</strong></p>
                    <p>Mon – Fri: 10:00 AM – 2:30 PM <span id="open-status" class="status-badge">Checking...</span></p>
                    <p>Sat – Sun: Closed</p>
                </div>
                
                <div style="margin-top:2rem">
                    <p>📍 397 Upton Road, Noctorum, CH43 9SE</p>
                    <p>📞 +44 7548 880879</p>
                    <p>📧 cakesbythelakes.wirral@gmail.com</p>
                </div>

                <div class="info-icons">
                    <span>🐾 Dog Friendly</span>
                    <span>👶 High Chairs</span>
                    <span>📶 Free Wi-Fi</span>
                    <span>🅿️ Free Parking</span>
                </div>
            </div>
            <div>
                <div class="map-container">
                    <iframe 
                        src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2389.576822557106!2d-3.0768417232815127!3d53.383049172304!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x487b270726715f33%3A0x6420556f8f7813a4!2s397%20Upton%20Rd%2C%20Noctorum%2C%20Birkenhead%20CH43%209SE!5e0!3m2!1sen!2suk!4v1710000000000" 
                        width="100%" height="100%" style="border:0;" allowfullscreen="" loading="lazy"></iframe>
                </div>
            </div>
        </div>
    </section>

    <!-- Section 6: Reviews Carousel -->
    <section class="section-padding reviews-section">
        <h2 style="text-align: center;">What Our Guests Say</h2>
        <div class="review-viewport">
            <div class="review-track" id="review-track">
                <!-- Review 1 -->
                <div class="review-card">
                    <div class="stars">★★★★★</div>
                    <span class="reviewer">Hughes Louise Emma</span>
                    <span class="review-date">19 Feb 2025</span>
                    <p class="review-text">Been here a few times and what can I say — every cake I've tried have been beautiful. I tried the huge nudger sandwich too the other day and it was amazing so fresh and the coleslaw was amazing. Highly recommend.</p>
                    <span class="read-more" onclick="toggleReview(this)">Read more</span>
                </div>
                <!-- Review 2 -->
                <div class="review-card">
                    <div class="stars">★★★★★</div>
                    <span class="reviewer">Louise Forster-Kerr</span>
                    <span class="review-date">25 Jan 2025</span>
                    <p class="review-text">Such a gorgeous little local spot! Lovely sandwiches, bagels and toasties...and the cakes wow! The staff are so friendly. My mum really fancied a meringue and there were none left, so the lovely lady went in the back and made her one! 10/10 customer service ✨</p>
                    <span class="read-more" onclick="toggleReview(this)">Read more</span>
                </div>
                <!-- Review 3 -->
                <div class="review-card">
                    <div class="stars">★★★★★</div>
                    <span class="reviewer">Tina Denise</span>
                    <span class="review-date">30 Nov 2024</span>
                    <p class="review-text">Love this place. It's warm and inviting. The bread is delicious, amazing salad boxes and the cakes — well I have no words. They are just delicious and all at affordable prices. I definitely recommend.</p>
                    <span class="read-more" onclick="toggleReview(this)">Read more</span>
                </div>
                <!-- Review 4 -->
                <div class="review-card">
                    <div class="stars">★★★★★</div>
                    <span class="reviewer">Valerie Jones</span>
                    <span class="review-date">3 May 2025</span>
                    <p class="review-text">My husband and I had lunch here a few w<!DOCTYPE html>
<html lang="en-GB">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Cakes by the Lakes Wirral | Homemade Café in Upton, Wirral</title>
    <meta name="description" content="Wirral's cosiest little café in Upton. Freshly made cakes, artisan sandwiches, and speciality coffee. Family-run, dog-friendly, and warm atmosphere.">
    
    <!-- Open Graph Tags -->
    <meta property="og:title" content="Cakes by the Lakes Wirral | Homemade Café">
    <meta property="og:description" content="Artisan cakes, sandwiches & coffee in the heart of Upton. Freshly made every day with heart.">
    <meta property="og:type" content="website">
    <meta property="og:url" content="https://cakesbythelakeswirral.co.uk">

    <!-- Google Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Lato:wght@400;700&family=Playfair+Display:ital,wght@0,700;1,700&display=swap" rel="stylesheet">

    <style>
        :root {
            --cream: #FDF6EC;
            --rose: #E8A598;
            --sage: #8FAF8C;
            --brown: #4A2C2A;
            --white: #ffffff;
            --transition: all 0.4s cubic-bezier(0.165, 0.84, 0.44, 1);
        }

        * { margin: 0; padding: 0; box-sizing: border-box; }

        body {
            font-family: 'Lato', sans-serif;
            background-color: var(--cream);
            color: var(--brown);
            line-height: 1.6;
            overflow-x: hidden;
        }

        h1, h2, h3, h4 {
            font-family: 'Playfair Display', serif;
            font-weight: 700;
        }

        /* --- Global Animations --- */
        .reveal {
            opacity: 0;
            transform: translateY(30px);
            transition: var(--transition);
        }

        .reveal.active {
            opacity: 1;
            transform: translateY(0);
        }

        /* --- Hero Section --- */
        .hero {
            position: relative;
            min-height: 90vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            padding: 2rem;
            background: linear-gradient(135deg, var(--cream) 0%, var(--rose) 100%);
            overflow: hidden;
        }

        .hero-content {
            z-index: 2;
            max-width: 800px;
        }

        .hero h1 {
            font-size: clamp(2.5rem, 8vw, 4.5rem);
            line-height: 1.1;
            margin-bottom: 1.5rem;
        }

        .hero p {
            font-size: clamp(1.1rem, 3vw, 1.4rem);
            margin-bottom: 2.5rem;
            opacity: 0.9;
        }

        .btn-group {
            display: flex;
            gap: 1rem;
            justify-content: center;
            flex-wrap: wrap;
        }

        .btn {
            padding: 1rem 2.5rem;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 700;
            transition: var(--transition);
            display: inline-block;
            cursor: pointer;
        }

        .btn-primary {
            background-color: var(--brown);
            color: var(--white);
        }

        .btn-primary:hover {
            transform: scale(1.05);
            box-shadow: 0 10px 20px rgba(74, 44, 42, 0.2);
        }

        .btn-outline {
            border: 2px solid var(--brown);
            color: var(--brown);
        }

        .btn-outline:hover {
            background-color: var(--brown);
            color: var(--white);
        }

        .badge {
            display: inline-block;
            background: rgba(255, 255, 255, 0.6);
            padding: 0.5rem 1.2rem;
            border-radius: 50px;
            margin-bottom: 2rem;
            font-weight: 700;
            backdrop-filter: blur(5px);
            border: 1px solid rgba(74, 44, 42, 0.1);
        }

        /* Floating Icons */
        .floating-icon {
            position: absolute;
            opacity: 0.15;
            z-index: 1;
            animation: float 6s ease-in-out infinite;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0) rotate(0deg); }
            50% { transform: translateY(-20px) rotate(10deg); }
        }

        /* --- Trust Bar --- */
        .trust-bar {
            background: var(--brown);
            color: var(--white);
            padding: 0.8rem 0;
            overflow: hidden;
            white-space: nowrap;
        }

        .ticker {
            display: inline-block;
            animation: marquee 30s linear infinite;
        }

        .ticker span {
            display: inline-block;
            padding-right: 3rem;
            font-weight: 700;
            text-transform: uppercase;
            font-size: 0.9rem;
            letter-spacing: 1px;
        }

        @keyframes marquee {
            0% { transform: translateX(0); }
            100% { transform: translateX(-50%); }
        }

        /* --- About Section --- */
        .section-padding { padding: 5rem 10%; }

        .about-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 4rem;
            align-items: center;
        }

        .about-img {
            width: 100%;
            height: 500px;
            border-radius: 20px;
            object-fit: cover;
            box-shadow: 20px 20px 0 var(--sage);
        }

        .feature-pills {
            display: flex;
            gap: 1rem;
            margin-top: 2rem;
            flex-wrap: wrap;
        }

        .pill {
            background: var(--rose);
            padding: 0.5rem 1rem;
            border-radius: 50px;
            color: var(--white);
            font-weight: 700;
            font-size: 0.9rem;
        }

        /* --- Menu Section --- */
        .menu-section { background-color: var(--white); text-align: center; }

        .menu-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 2rem;
            margin-top: 3rem;
        }

        .menu-card {
            background: var(--cream);
            padding: 2.5rem;
            border-radius: 20px;
            text-align: left;
            transition: var(--transition);
            border: 1px solid rgba(143, 175, 140, 0.2);
        }

        .menu-card:hover { transform: translateY(-10px); box-shadow: 0 15px 30px rgba(0,0,0,0.05); }

        .menu-card h3 { color: var(--rose); margin-bottom: 1rem; font-size: 1.8rem; }
        
        .menu-card ul { list-style: none; }
        .menu-card li { margin-bottom: 0.5rem; position: relative; padding-left: 1.5rem; }
        .menu-card li::before { content: '•'; position: absolute; left: 0; color: var(--sage); font-weight: bold; }

        .meal-deal {
            background: var(--rose);
            color: var(--brown);
            padding: 1.5rem;
            border-radius: 15px;
            margin-top: 3rem;
            font-weight: 700;
            font-size: 1.2rem;
            display: inline-block;
        }

        /* --- Info Section --- */
        .info-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 3rem;
        }

        .status-badge {
            padding: 0.3rem 0.8rem;
            border-radius: 5px;
            font-weight: 700;
            font-size: 0.8rem;
            margin-left: 10px;
        }
        .status-open { background: #d4edda; color: #155724; }
        .status-closed { background: #f8d7da; color: #721c24; }

        .map-container {
            width: 100%;
            height: 300px;
            border-radius: 15px;
            overflow: hidden;
            margin-top: 1.5rem;
        }

        .info-icons {
            display: flex;
            gap: 1.5rem;
            margin-top: 1.5rem;
            font-size: 0.85rem;
            font-weight: 700;
            flex-wrap: wrap;
        }

        /* --- Review Carousel --- */
        .reviews-section { background: var(--cream); overflow: hidden; }
        
        .review-viewport {
            width: 100%;
            overflow: hidden;
            margin-top: 3rem;
            cursor: grab;
        }

        .review-track {
            display: flex;
            transition: transform 0.5s ease-out;
            gap: 2rem;
        }

        .review-card {
            min-width: 350px;
            background: var(--white);
            padding: 2rem;
            border-radius: 15px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.03);
        }

        .stars { color: #FFD700; margin-bottom: 0.5rem; }
        .reviewer { font-weight: 700; display: block; margin-bottom: 0.2rem; }
        .review-date { font-size: 0.8rem; color: #888; margin-bottom: 1rem; display: block; }
        
        .review-text {
            font-size: 0.95rem;
            display: -webkit-box;
            -webkit-line-clamp: 3;
            -webkit-box-orient: vertical;
            overflow: hidden;
        }

        .review-text.expanded {
            -webkit-line-clamp: unset;
        }

        .read-more {
            color: var(--sage);
            font-weight: 700;
            cursor: pointer;
            font-size: 0.85rem;
            display: block;
            margin-top: 0.5rem;
        }

        /* --- Footer Section --- */
        .final-cta {
            background: var(--brown);
            color: var(--white);
            text-align: center;
            padding: 5rem 10%;
        }

        .final-cta h2 { font-size: 2.5rem; margin-bottom: 1rem; }
        
        footer {
            background: #361f1e;
            color: rgba(255,255,255,0.7);
            padding: 2rem 10%;
            text-align: center;
            font-size: 0.9rem;
        }

        .social-link {
            color: var(--white);
            font-size: 1.5rem;
            margin-top: 1rem;
            display: inline-block;
            text-decoration: none;
        }

        /* --- Responsive --- */
        @media (max-width: 900px) {
            .about-grid, .info-grid { grid-template-columns: 1fr; }
            .about-img { height: 350px; order: -1; }
            .menu-grid { grid-template-columns: 1fr; }
            .section-padding { padding: 4rem 5%; }
        }

        @media (max-width: 600px) {
            .hero h1 { font-size: 2.5rem; }
            .review-card { min-width: 280px; }
        }
    </style>
</head>
<body>

    <!-- Section 1: Hero -->
    <header class="hero">
        <!-- Floating SVGs -->
        <svg class="floating-icon" style="top: 15%; left: 10%; width: 60px;" viewBox="0 0 24 24" fill="currentColor"><path d="M11 2c.047 0 .092.006.137.017a2.502 2.502 0 0 1 4.726 0c.045-.011.09-.017.137-.017 1.38 0 2.5 1.12 2.5 2.5 0 .597-.216 1.138-.567 1.56.35.423.567.964.567 1.561 0 1.38-1.12 2.5-2.5 2.5-.047 0-.092-.006-.137-.017a2.502 2.502 0 0 1-4.726 0c-.045.011-.09.017-.137.017-1.38 0-2.5-1.12-2.5-2.5 0-.597.216-1.138.567-1.56a2.506 2.506 0 0 1-.567-1.561c0-1.38 1.12-2.5 2.5-2.5zm0 14h2v2h-2v-2zm-6-2h14v1h-14v-1zm0 2h14v1h-14v-1zm-1 3h16v1h-16v-1z"/></svg>
        <svg class="floating-icon" style="bottom: 20%; right: 10%; width: 50px;" viewBox="0 0 24 24" fill="currentColor"><path d="M2 21h18v-2H2v2zM20 8h-2V5h2v3zm2-3h-4a2 2 0 0 0-2 2v3a2 2 0 0 0 2 2h4a2 2 0 0 0 2-2V7a2 2 0 0 0-2-2zM4 19h14v-9H4v9zM14 5c0-1.1-.9-2-2-2s-2 .9-2 2h4z"/></svg>
        
        <div class="hero-content reveal">
            <span class="badge">⭐ 4.9/5 on Google · 100% Recommend on Facebook</span>
            <h1>Homemade with Heart. <br>Fresh Every Day.</h1>
            <p>Wirral's cosiest little café — cakes, sandwiches & speciality coffee in the heart of Upton</p>
            <div class="btn-group">
                <a href="#menu" class="btn btn-primary">See Our Menu ↓</a>
                <a href="#visit" class="btn btn-outline">Find Us</a>
            </div>
        </div>
    </header>

    <!-- Section 2: Trust Bar -->
    <div class="trust-bar">
        <div class="ticker">
            <span>🍰 100% Recommend on Facebook</span>
            <span>⭐ 4.9 Google Rating</span>
            <span>☕ Fresh Made Daily</span>
            <span>🐾 Dog Friendly</span>
            <span>📶 Free Wi-Fi</span>
            <span>👨‍👩‍👧 Family Friendly</span>
            <span>🅿️ Free Nearby Parking</span>
            <!-- Duplicate for infinite effect -->
            <span>🍰 100% Recommend on Facebook</span>
            <span>⭐ 4.9 Google Rating</span>
            <span>☕ Fresh Made Daily</span>
            <span>🐾 Dog Friendly</span>
            <span>📶 Free Wi-Fi</span>
            <span>👨‍👩‍👧 Family Friendly</span>
            <span>🅿️ Free Nearby Parking</span>
        </div>
    </div>

    <!-- Section 3: About -->
    <section class="section-padding reveal">
        <div class="about-grid">
            <img src="https://images.unsplash.com/photo-1559339352-11d035aa65de?q=80&w=1000" alt="Delicious Cakes" class="about-img">
            <div>
                <h2>A Little Café With a Big Heart</h2>
                <p style="margin: 1.5rem 0;">Cakes by the Lakes is Wirral's best-kept secret — a homemade, traditional café tucked away at 397 Upton Road, Noctorum. Everything is freshly made, the counter changes daily, and you'll always leave with a smile. Whether you're after a hearty sandwich, a stunning celebration cake, or just a slice of school cake and a latte — you've found your place.</p>
                <div class="feature-pills">
                    <span class="pill">🏠 Family Run</span>
                    <span class="pill">🌿 Fresh Daily</span>
                    <span class="pill">💛 Affordable Prices</span>
                </div>
            </div>
        </div>
    </section>

    <!-- Section 4: Menu -->
    <section id="menu" class="section-padding menu-section reveal">
        <h2>What's On the Counter Today</h2>
        <p>Our menu rotates daily — here's a taste of what to expect</p>
        
        <div class="menu-grid">
            <div class="menu-card reveal">
                <h3>🍰 Sweet Treats</h3>
                <ul>
                    <li>Victoria Sponge</li>
                    <li>Biscoff Cream Buns</li>
                    <li>Lemon Drizzle & Coffee & Walnut</li>
                    <li>Brownies & Kinder Brownies</li>
                    <li>Custard Tarts & School Cake</li>
                    <li>Milkybar Cheesecake & Caramel Cakes</li>
                </ul>
            </div>
            <div class="menu-card reveal">
                <h3>🥪 Savoury & Lunch</h3>
                <ul>
                    <li>Salt & Pepper Sausage Rolls</li>
                    <li>Nudger Sandwiches</li>
                    <li>Freshly Made Bagels & Toasties</li>
                    <li>Jacket Potatoes</li>
                    <li>Healthy Wraps</li>
                </ul>
            </div>
            <div class="menu-card reveal">
                <h3>🥗 Boxes & Salads</h3>
                <ul>
                    <li>Pasta Boxes (Pesto / Tomato / Chinese Chicken)</li>
                    <li>Salad Boxes (Chicken Bacon Mayo, Tuna Mayo)</li>
                    <li>Gluten-Free Options Available</li>
                </ul>
            </div>
            <div class="menu-card reveal">
                <h3>☕ Drinks</h3>
                <ul>
                    <li>Specialty Coffees</li>
                    <li>Iced Frappes & Milkshakes</li>
                    <li>Hot Chocolate & Fresh Smoothies</li>
                </ul>
            </div>
        </div>
        
        <div class="meal-deal reveal">
            🎉 Meal Deal — Main + Cake + Hot Drink from just £7.50!
        </div>
    </section>

    <!-- Section 5: Visit & Hours -->
    <section id="visit" class="section-padding reveal">
        <div class="info-grid">
            <div>
                <h2>Visit Us</h2>
                <div style="margin-top:1.5rem">
                    <p><strong>Opening Hours:</strong></p>
                    <p>Mon – Fri: 10:00 AM – 2:30 PM <span id="open-status" class="status-badge">Checking...</span></p>
                    <p>Sat – Sun: Closed</p>
                </div>
                
                <div style="margin-top:2rem">
                    <p>📍 397 Upton Road, Noctorum, CH43 9SE</p>
                    <p>📞 +44 7548 880879</p>
                    <p>📧 cakesbythelakes.wirral@gmail.com</p>
                </div>

                <div class="info-icons">
                    <span>🐾 Dog Friendly</span>
                    <span>👶 High Chairs</span>
                    <span>📶 Free Wi-Fi</span>
                    <span>🅿️ Free Parking</span>
                </div>
            </div>
            <div>
                <div class="map-container">
                    <iframe 
                        src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2389.576822557106!2d-3.0768417232815127!3d53.383049172304!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x487b270726715f33%3A0x6420556f8f7813a4!2s397%20Upton%20Rd%2C%20Noctorum%2C%20Birkenhead%20CH43%209SE!5e0!3m2!1sen!2suk!4v1710000000000" 
                        width="100%" height="100%" style="border:0;" allowfullscreen="" loading="lazy"></iframe>
                </div>
            </div>
        </div>
    </section>

    <!-- Section 6: Reviews Carousel -->
    <section class="section-padding reviews-section">
        <h2 style="text-align: center;">What Our Guests Say</h2>
        <div class="review-viewport">
            <div class="review-track" id="review-track">
                <!-- Review 1 -->
                <div class="review-card">
                    <div class="stars">★★★★★</div>
                    <span class="reviewer">Hughes Louise Emma</span>
                    <span class="review-date">19 Feb 2025</span>
                    <p class="review-text">Been here a few times and what can I say — every cake I've tried have been beautiful. I tried the huge nudger sandwich too the other day and it was amazing so fresh and the coleslaw was amazing. Highly recommend.</p>
                    <span class="read-more" onclick="toggleReview(this)">Read more</span>
                </div>
                <!-- Review 2 -->
                <div class="review-card">
                    <div class="stars">★★★★★</div>
                    <span class="reviewer">Louise Forster-Kerr</span>
                    <span class="review-date">25 Jan 2025</span>
                    <p class="review-text">Such a gorgeous little local spot! Lovely sandwiches, bagels and toasties...and the cakes wow! The staff are so friendly. My mum really fancied a meringue and there were none left, so the lovely lady went in the back and made her one! 10/10 customer service ✨</p>
                    <span class="read-more" onclick="toggleReview(this)">Read more</span>
                </div>
                <!-- Review 3 -->
                <div class="review-card">
                    <div class="stars">★★★★★</div>
                    <span class="reviewer">Tina Denise</span>
                    <span class="review-date">30 Nov 2024</span>
                    <p class="review-text">Love this place. It's warm and inviting. The bread is delicious, amazing salad boxes and the cakes — well I have no words. They are just delicious and all at affordable prices. I definitely recommend.</p>
                    <span class="read-more" onclick="toggleReview(this)">Read more</span>
                </div>
                <!-- Review 4 -->
                <div class="review-card">
                    <div class="stars">★★★★★</div>
                    <span class="reviewer">Valerie Jones</span>
                    <span class="review-date">3 May 2025</span>
                    <p class="review-text">My husband and I had lunch here a few w<!DOCTYPE html>
<html lang="en-GB">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Cakes by the Lakes Wirral | Homemade Café in Upton, Wirral</title>
    <meta name="description" content="Wirral's cosiest little café in Upton. Freshly made cakes, artisan sandwiches, and speciality coffee. Family-run, dog-friendly, and warm atmosphere.">
    
    <!-- Open Graph Tags -->
    <meta property="og:title" content="Cakes by the Lakes Wirral | Homemade Café">
    <meta property="og:description" content="Artisan cakes, sandwiches & coffee in the heart of Upton. Freshly made every day with heart.">
    <meta property="og:type" content="website">
    <meta property="og:url" content="https://cakesbythelakeswirral.co.uk">

    <!-- Google Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Lato:wght@400;700&family=Playfair+Display:ital,wght@0,700;1,700&display=swap" rel="stylesheet">

    <style>
        :root {
            --cream: #FDF6EC;
            --rose: #E8A598;
            --sage: #8FAF8C;
            --brown: #4A2C2A;
            --white: #ffffff;
            --transition: all 0.4s cubic-bezier(0.165, 0.84, 0.44, 1);
        }

        * { margin: 0; padding: 0; box-sizing: border-box; }

        body {
            font-family: 'Lato', sans-serif;
            background-color: var(--cream);
            color: var(--brown);
            line-height: 1.6;
            overflow-x: hidden;
        }

        h1, h2, h3, h4 {
            font-family: 'Playfair Display', serif;
            font-weight: 700;
        }

        /* --- Global Animations --- */
        .reveal {
            opacity: 0;
            transform: translateY(30px);
            transition: var(--transition);
        }

        .reveal.active {
            opacity: 1;
            transform: translateY(0);
        }

        /* --- Hero Section --- */
        .hero {
            position: relative;
            min-height: 90vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            padding: 2rem;
            background: linear-gradient(135deg, var(--cream) 0%, var(--rose) 100%);
            overflow: hidden;
        }

        .hero-content {
            z-index: 2;
            max-width: 800px;
        }

        .hero h1 {
            font-size: clamp(2.5rem, 8vw, 4.5rem);
            line-height: 1.1;
            margin-bottom: 1.5rem;
        }

        .hero p {
            font-size: clamp(1.1rem, 3vw, 1.4rem);
            margin-bottom: 2.5rem;
            opacity: 0.9;
        }

        .btn-group {
            display: flex;
            gap: 1rem;
            justify-content: center;
            flex-wrap: wrap;
        }

        .btn {
            padding: 1rem 2.5rem;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 700;
            transition: var(--transition);
            display: inline-block;
            cursor: pointer;
        }

        .btn-primary {
            background-color: var(--brown);
            color: var(--white);
        }

        .btn-primary:hover {
            transform: scale(1.05);
            box-shadow: 0 10px 20px rgba(74, 44, 42, 0.2);
        }

        .btn-outline {
            border: 2px solid var(--brown);
            color: var(--brown);
        }

        .btn-outline:hover {
            background-color: var(--brown);
            color: var(--white);
        }

        .badge {
            display: inline-block;
            background: rgba(255, 255, 255, 0.6);
            padding: 0.5rem 1.2rem;
            border-radius: 50px;
            margin-bottom: 2rem;
            font-weight: 700;
            backdrop-filter: blur(5px);
            border: 1px solid rgba(74, 44, 42, 0.1);
        }

        /* Floating Icons */
        .floating-icon {
            position: absolute;
            opacity: 0.15;
            z-index: 1;
            animation: float 6s ease-in-out infinite;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0) rotate(0deg); }
            50% { transform: translateY(-20px) rotate(10deg); }
        }

        /* --- Trust Bar --- */
        .trust-bar {
            background: var(--brown);
            color: var(--white);
            padding: 0.8rem 0;
            overflow: hidden;
            white-space: nowrap;
        }

        .ticker {
            display: inline-block;
            animation: marquee 30s linear infinite;
        }

        .ticker span {
            display: inline-block;
            padding-right: 3rem;
            font-weight: 700;
            text-transform: uppercase;
            font-size: 0.9rem;
            letter-spacing: 1px;
        }

        @keyframes marquee {
            0% { transform: translateX(0); }
            100% { transform: translateX(-50%); }
        }

        /* --- About Section --- */
        .section-padding { padding: 5rem 10%; }

        .about-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 4rem;
            align-items: center;
        }

        .about-img {
            width: 100%;
            height: 500px;
            border-radius: 20px;
            object-fit: cover;
            box-shadow: 20px 20px 0 var(--sage);
        }

        .feature-pills {
            display: flex;
            gap: 1rem;
            margin-top: 2rem;
            flex-wrap: wrap;
        }

        .pill {
            background: var(--rose);
            padding: 0.5rem 1rem;
            border-radius: 50px;
            color: var(--white);
            font-weight: 700;
            font-size: 0.9rem;
        }

        /* --- Menu Section --- */
        .menu-section { background-color: var(--white); text-align: center; }

        .menu-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 2rem;
            margin-top: 3rem;
        }

        .menu-card {
            background: var(--cream);
            padding: 2.5rem;
            border-radius: 20px;
            text-align: left;
            transition: var(--transition);
            border: 1px solid rgba(143, 175, 140, 0.2);
        }

        .menu-card:hover { transform: translateY(-10px); box-shadow: 0 15px 30px rgba(0,0,0,0.05); }

        .menu-card h3 { color: var(--rose); margin-bottom: 1rem; font-size: 1.8rem; }
        
        .menu-card ul { list-style: none; }
        .menu-card li { margin-bottom: 0.5rem; position: relative; padding-left: 1.5rem; }
        .menu-card li::before { content: '•'; position: absolute; left: 0; color: var(--sage); font-weight: bold; }

        .meal-deal {
            background: var(--rose);
            color: var(--brown);
            padding: 1.5rem;
            border-radius: 15px;
            margin-top: 3rem;
            font-weight: 700;
            font-size: 1.2rem;
            display: inline-block;
        }

        /* --- Info Section --- */
        .info-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 3rem;
        }

        .status-badge {
            padding: 0.3rem 0.8rem;
            border-radius: 5px;
            font-weight: 700;
            font-size: 0.8rem;
            margin-left: 10px;
        }
        .status-open { background: #d4edda; color: #155724; }
        .status-closed { background: #f8d7da; color: #721c24; }

        .map-container {
            width: 100%;
            height: 300px;
            border-radius: 15px;
            overflow: hidden;
            margin-top: 1.5rem;
        }

        .info-icons {
            display: flex;
            gap: 1.5rem;
            margin-top: 1.5rem;
            font-size: 0.85rem;
            font-weight: 700;
            flex-wrap: wrap;
        }

        /* --- Review Carousel --- */
        .reviews-section { background: var(--cream); overflow: hidden; }
        
        .review-viewport {
            width: 100%;
            overflow: hidden;
            margin-top: 3rem;
            cursor: grab;
        }

        .review-track {
            display: flex;
            transition: transform 0.5s ease-out;
            gap: 2rem;
        }

        .review-card {
            min-width: 350px;
            background: var(--white);
            padding: 2rem;
            border-radius: 15px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.03);
        }

        .stars { color: #FFD700; margin-bottom: 0.5rem; }
        .reviewer { font-weight: 700; display: block; margin-bottom: 0.2rem; }
        .review-date { font-size: 0.8rem; color: #888; margin-bottom: 1rem; display: block; }
        
        .review-text {
            font-size: 0.95rem;
            display: -webkit-box;
            -webkit-line-clamp: 3;
            -webkit-box-orient: vertical;
            overflow: hidden;
        }

        .review-text.expanded {
            -webkit-line-clamp: unset;
        }

        .read-more {
            color: var(--sage);
            font-weight: 700;
            cursor: pointer;
            font-size: 0.85rem;
            display: block;
            margin-top: 0.5rem;
        }

        /* --- Footer Section --- */
        .final-cta {
            background: var(--brown);
            color: var(--white);
            text-align: center;
            padding: 5rem 10%;
        }

        .final-cta h2 { font-size: 2.5rem; margin-bottom: 1rem; }
        
        footer {
            background: #361f1e;
            color: rgba(255,255,255,0.7);
            padding: 2rem 10%;
            text-align: center;
            font-size: 0.9rem;
        }

        .social-link {
            color: var(--white);
            font-size: 1.5rem;
            margin-top: 1rem;
            display: inline-block;
            text-decoration: none;
        }

        /* --- Responsive --- */
        @media (max-width: 900px) {
            .about-grid, .info-grid { grid-template-columns: 1fr; }
            .about-img { height: 350px; order: -1; }
            .menu-grid { grid-template-columns: 1fr; }
            .section-padding { padding: 4rem 5%; }
        }

        @media (max-width: 600px) {
            .hero h1 { font-size: 2.5rem; }
            .review-card { min-width: 280px; }
        }
    </style>
</head>
<body>

    <!-- Section 1: Hero -->
    <header class="hero">
        <!-- Floating SVGs -->
        <svg class="floating-icon" style="top: 15%; left: 10%; width: 60px;" viewBox="0 0 24 24" fill="currentColor"><path d="M11 2c.047 0 .092.006.137.017a2.502 2.502 0 0 1 4.726 0c.045-.011.09-.017.137-.017 1.38 0 2.5 1.12 2.5 2.5 0 .597-.216 1.138-.567 1.56.35.423.567.964.567 1.561 0 1.38-1.12 2.5-2.5 2.5-.047 0-.092-.006-.137-.017a2.502 2.502 0 0 1-4.726 0c-.045.011-.09.017-.137.017-1.38 0-2.5-1.12-2.5-2.5 0-.597.216-1.138.567-1.56a2.506 2.506 0 0 1-.567-1.561c0-1.38 1.12-2.5 2.5-2.5zm0 14h2v2h-2v-2zm-6-2h14v1h-14v-1zm0 2h14v1h-14v-1zm-1 3h16v1h-16v-1z"/></svg>
        <svg class="floating-icon" style="bottom: 20%; right: 10%; width: 50px;" viewBox="0 0 24 24" fill="currentColor"><path d="M2 21h18v-2H2v2zM20 8h-2V5h2v3zm2-3h-4a2 2 0 0 0-2 2v3a2 2 0 0 0 2 2h4a2 2 0 0 0 2-2V7a2 2 0 0 0-2-2zM4 19h14v-9H4v9zM14 5c0-1.1-.9-2-2-2s-2 .9-2 2h4z"/></svg>
        
        <div class="hero-content reveal">
            <span class="badge">⭐ 4.9/5 on Google · 100% Recommend on Facebook</span>
            <h1>Homemade with Heart. <br>Fresh Every Day.</h1>
            <p>Wirral's cosiest little café — cakes, sandwiches & speciality coffee in the heart of Upton</p>
            <div class="btn-group">
                <a href="#menu" class="btn btn-primary">See Our Menu ↓</a>
                <a href="#visit" class="btn btn-outline">Find Us</a>
            </div>
        </div>
    </header>

    <!-- Section 2: Trust Bar -->
    <div class="trust-bar">
        <div class="ticker">
            <span>🍰 100% Recommend on Facebook</span>
            <span>⭐ 4.9 Google Rating</span>
            <span>☕ Fresh Made Daily</span>
            <span>🐾 Dog Friendly</span>
            <span>📶 Free Wi-Fi</span>
            <span>👨‍👩‍👧 Family Friendly</span>
            <span>🅿️ Free Nearby Parking</span>
            <!-- Duplicate for infinite effect -->
            <span>🍰 100% Recommend on Facebook</span>
            <span>⭐ 4.9 Google Rating</span>
            <span>☕ Fresh Made Daily</span>
            <span>🐾 Dog Friendly</span>
            <span>📶 Free Wi-Fi</span>
            <span>👨‍👩‍👧 Family Friendly</span>
            <span>🅿️ Free Nearby Parking</span>
        </div>
    </div>

    <!-- Section 3: About -->
    <section class="section-padding reveal">
        <div class="about-grid">
            <img src="https://images.unsplash.com/photo-1559339352-11d035aa65de?q=80&w=1000" alt="Delicious Cakes" class="about-img">
            <div>
                <h2>A Little Café With a Big Heart</h2>
                <p style="margin: 1.5rem 0;">Cakes by the Lakes is Wirral's best-kept secret — a homemade, traditional café tucked away at 397 Upton Road, Noctorum. Everything is freshly made, the counter changes daily, and you'll always leave with a smile. Whether you're after a hearty sandwich, a stunning celebration cake, or just a slice of school cake and a latte — you've found your place.</p>
                <div class="feature-pills">
                    <span class="pill">🏠 Family Run</span>
                    <span class="pill">🌿 Fresh Daily</span>
                    <span class="pill">💛 Affordable Prices</span>
                </div>
            </div>
        </div>
    </section>

    <!-- Section 4: Menu -->
    <section id="menu" class="section-padding menu-section reveal">
        <h2>What's On the Counter Today</h2>
        <p>Our menu rotates daily — here's a taste of what to expect</p>
        
        <div class="menu-grid">
            <div class="menu-card reveal">
                <h3>🍰 Sweet Treats</h3>
                <ul>
                    <li>Victoria Sponge</li>
                    <li>Biscoff Cream Buns</li>
                    <li>Lemon Drizzle & Coffee & Walnut</li>
                    <li>Brownies & Kinder Brownies</li>
                    <li>Custard Tarts & School Cake</li>
                    <li>Milkybar Cheesecake & Caramel Cakes</li>
                </ul>
            </div>
            <div class="menu-card reveal">
                <h3>🥪 Savoury & Lunch</h3>
                <ul>
                    <li>Salt & Pepper Sausage Rolls</li>
                    <li>Nudger Sandwiches</li>
                    <li>Freshly Made Bagels & Toasties</li>
                    <li>Jacket Potatoes</li>
                    <li>Healthy Wraps</li>
                </ul>
            </div>
            <div class="menu-card reveal">
                <h3>🥗 Boxes & Salads</h3>
                <ul>
                    <li>Pasta Boxes (Pesto / Tomato / Chinese Chicken)</li>
                    <li>Salad Boxes (Chicken Bacon Mayo, Tuna Mayo)</li>
                    <li>Gluten-Free Options Available</li>
                </ul>
            </div>
            <div class="menu-card reveal">
                <h3>☕ Drinks</h3>
                <ul>
                    <li>Specialty Coffees</li>
                    <li>Iced Frappes & Milkshakes</li>
                    <li>Hot Chocolate & Fresh Smoothies</li>
                </ul>
            </div>
        </div>
        
        <div class="meal-deal reveal">
            🎉 Meal Deal — Main + Cake + Hot Drink from just £7.50!
        </div>
    </section>

    <!-- Section 5: Visit & Hours -->
    <section id="visit" class="section-padding reveal">
        <div class="info-grid">
            <div>
                <h2>Visit Us</h2>
                <div style="margin-top:1.5rem">
                    <p><strong>Opening Hours:</strong></p>
                    <p>Mon – Fri: 10:00 AM – 2:30 PM <span id="open-status" class="status-badge">Checking...</span></p>
                    <p>Sat – Sun: Closed</p>
                </div>
                
                <div style="margin-top:2rem">
                    <p>📍 397 Upton Road, Noctorum, CH43 9SE</p>
                    <p>📞 +44 7548 880879</p>
                    <p>📧 cakesbythelakes.wirral@gmail.com</p>
                </div>

                <div class="info-icons">
                    <span>🐾 Dog Friendly</span>
                    <span>👶 High Chairs</span>
                    <span>📶 Free Wi-Fi</span>
                    <span>🅿️ Free Parking</span>
                </div>
            </div>
            <div>
                <div class="map-container">
                    <iframe 
                        src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2389.576822557106!2d-3.0768417232815127!3d53.383049172304!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x487b270726715f33%3A0x6420556f8f7813a4!2s397%20Upton%20Rd%2C%20Noctorum%2C%20Birkenhead%20CH43%209SE!5e0!3m2!1sen!2suk!4v1710000000000" 
                        width="100%" height="100%" style="border:0;" allowfullscreen="" loading="lazy"></iframe>
                </div>
            </div>
        </div>
    </section>

    <!-- Section 6: Reviews Carousel -->
    <section class="section-padding reviews-section">
        <h2 style="text-align: center;">What Our Guests Say</h2>
        <div class="review-viewport">
            <div class="review-track" id="review-track">
                <!-- Review 1 -->
                <div class="review-card">
                    <div class="stars">★★★★★</div>
                    <span class="reviewer">Hughes Louise Emma</span>
                    <span class="review-date">19 Feb 2025</span>
                    <p class="review-text">Been here a few times and what can I say — every cake I've tried have been beautiful. I tried the huge nudger sandwich too the other day and it was amazing so fresh and the coleslaw was amazing. Highly recommend.</p>
                    <span class="read-more" onclick="toggleReview(this)">Read more</span>
                </div>
                <!-- Review 2 -->
                <div class="review-card">
                    <div class="stars">★★★★★</div>
                    <span class="reviewer">Louise Forster-Kerr</span>
                    <span class="review-date">25 Jan 2025</span>
                    <p class="review-text">Such a gorgeous little local spot! Lovely sandwiches, bagels and toasties...and the cakes wow! The staff are so friendly. My mum really fancied a meringue and there were none left, so the lovely lady went in the back and made her one! 10/10 customer service ✨</p>
                    <span class="read-more" onclick="toggleReview(this)">Read more</span>
                </div>
                <!-- Review 3 -->
                <div class="review-card">
                    <div class="stars">★★★★★</div>
                    <span class="reviewer">Tina Denise</span>
                    <span class="review-date">30 Nov 2024</span>
                    <p class="review-text">Love this place. It's warm and inviting. The bread is delicious, amazing salad boxes and the cakes — well I have no words. They are just delicious and all at affordable prices. I definitely recommend.</p>
                    <span class="read-more" onclick="toggleReview(this)">Read more</span>
                </div>
                <!-- Review 4 -->
                <div class="review-card">
                    <div class="stars">★★★★★</div>
                    <span class="reviewer">Valerie Jones</span>
                    <span class="review-date">3 May 2025</span>
                    <p class="review-text">My husband and I had lunch here a few w<!DOCTYPE html>
<html lang="en-GB">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Cakes by the Lakes Wirral | Homemade Café in Upton, Wirral</title>
    <meta name="description" content="Wirral's cosiest little café in Upton. Freshly made cakes, artisan sandwiches, and speciality coffee. Family-run, dog-friendly, and warm atmosphere.">
    
    <!-- Open Graph Tags -->
    <meta property="og:title" content="Cakes by the Lakes Wirral | Homemade Café">
    <meta property="og:description" content="Artisan cakes, sandwiches & coffee in the heart of Upton. Freshly made every day with heart.">
    <meta property="og:type" content="website">
    <meta property="og:url" content="https://cakesbythelakeswirral.co.uk">

    <!-- Google Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Lato:wght@400;700&family=Playfair+Display:ital,wght@0,700;1,700&display=swap" rel="stylesheet">

    <style>
        :root {
            --cream: #FDF6EC;
            --rose: #E8A598;
            --sage: #8FAF8C;
            --brown: #4A2C2A;
            --white: #ffffff;
            --transition: all 0.4s cubic-bezier(0.165, 0.84, 0.44, 1);
        }

        * { margin: 0; padding: 0; box-sizing: border-box; }

        body {
            font-family: 'Lato', sans-serif;
            background-color: var(--cream);
            color: var(--brown);
            line-height: 1.6;
            overflow-x: hidden;
        }

        h1, h2, h3, h4 {
            font-family: 'Playfair Display', serif;
            font-weight: 700;
        }

        /* --- Global Animations --- */
        .reveal {
            opacity: 0;
            transform: translateY(30px);
            transition: var(--transition);
        }

        .reveal.active {
            opacity: 1;
            transform: translateY(0);
        }

        /* --- Hero Section --- */
        .hero {
            position: relative;
            min-height: 90vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            padding: 2rem;
            background: linear-gradient(135deg, var(--cream) 0%, var(--rose) 100%);
            overflow: hidden;
        }

        .hero-content {
            z-index: 2;
            max-width: 800px;
        }

        .hero h1 {
            font-size: clamp(2.5rem, 8vw, 4.5rem);
            line-height: 1.1;
            margin-bottom: 1.5rem;
        }

        .hero p {
            font-size: clamp(1.1rem, 3vw, 1.4rem);
            margin-bottom: 2.5rem;
            opacity: 0.9;
        }

        .btn-group {
            display: flex;
            gap: 1rem;
            justify-content: center;
            flex-wrap: wrap;
        }

        .btn {
            padding: 1rem 2.5rem;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 700;
            transition: var(--transition);
            display: inline-block;
            cursor: pointer;
        }

        .btn-primary {
            background-color: var(--brown);
            color: var(--white);
        }

        .btn-primary:hover {
            transform: scale(1.05);
            box-shadow: 0 10px 20px rgba(74, 44, 42, 0.2);
        }

        .btn-outline {
            border: 2px solid var(--brown);
            color: var(--brown);
        }

        .btn-outline:hover {
            background-color: var(--brown);
            color: var(--white);
        }

        .badge {
            display: inline-block;
            background: rgba(255, 255, 255, 0.6);
            padding: 0.5rem 1.2rem;
            border-radius: 50px;
            margin-bottom: 2rem;
            font-weight: 700;
            backdrop-filter: blur(5px);
            border: 1px solid rgba(74, 44, 42, 0.1);
        }

        /* Floating Icons */
        .floating-icon {
            position: absolute;
            opacity: 0.15;
            z-index: 1;
            animation: float 6s ease-in-out infinite;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0) rotate(0deg); }
            50% { transform: translateY(-20px) rotate(10deg); }
        }

        /* --- Trust Bar --- */
        .trust-bar {
            background: var(--brown);
            color: var(--white);
            padding: 0.8rem 0;
            overflow: hidden;
            white-space: nowrap;
        }

        .ticker {
            display: inline-block;
            animation: marquee 30s linear infinite;
        }

        .ticker span {
            display: inline-block;
            padding-right: 3rem;
            font-weight: 700;
            text-transform: uppercase;
            font-size: 0.9rem;
            letter-spacing: 1px;
        }

        @keyframes marquee {
            0% { transform: translateX(0); }
            100% { transform: translateX(-50%); }
        }

        /* --- About Section --- */
        .section-padding { padding: 5rem 10%; }

        .about-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 4rem;
            align-items: center;
        }

        .about-img {
            width: 100%;
            height: 500px;
            border-radius: 20px;
            object-fit: cover;
            box-shadow: 20px 20px 0 var(--sage);
        }

        .feature-pills {
            display: flex;
            gap: 1rem;
            margin-top: 2rem;
            flex-wrap: wrap;
        }

        .pill {
            background: var(--rose);
            padding: 0.5rem 1rem;
            border-radius: 50px;
            color: var(--white);
            font-weight: 700;
            font-size: 0.9rem;
        }

        /* --- Menu Section --- */
        .menu-section { background-color: var(--white); text-align: center; }

        .menu-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 2rem;
            margin-top: 3rem;
        }

        .menu-card {
            background: var(--cream);
            padding: 2.5rem;
            border-radius: 20px;
            text-align: left;
            transition: var(--transition);
            border: 1px solid rgba(143, 175, 140, 0.2);
        }

        .menu-card:hover { transform: translateY(-10px); box-shadow: 0 15px 30px rgba(0,0,0,0.05); }

        .menu-card h3 { color: var(--rose); margin-bottom: 1rem; font-size: 1.8rem; }
        
        .menu-card ul { list-style: none; }
        .menu-card li { margin-bottom: 0.5rem; position: relative; padding-left: 1.5rem; }
        .menu-card li::before { content: '•'; position: absolute; left: 0; color: var(--sage); font-weight: bold; }

        .meal-deal {
            background: var(--rose);
            color: var(--brown);
            padding: 1.5rem;
            border-radius: 15px;
            margin-top: 3rem;
            font-weight: 700;
            font-size: 1.2rem;
            display: inline-block;
        }

        /* --- Info Section --- */
        .info-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 3rem;
        }

        .status-badge {
            padding: 0.3rem 0.8rem;
            border-radius: 5px;
            font-weight: 700;
            font-size: 0.8rem;
            margin-left: 10px;
        }
        .status-open { background: #d4edda; color: #155724; }
        .status-closed { background: #f8d7da; color: #721c24; }

        .map-container {
            width: 100%;
            height: 300px;
            border-radius: 15px;
            overflow: hidden;
            margin-top: 1.5rem;
        }

        .info-icons {
            display: flex;
            gap: 1.5rem;
            margin-top: 1.5rem;
            font-size: 0.85rem;
            font-weight: 700;
            flex-wrap: wrap;
        }

        /* --- Review Carousel --- */
        .reviews-section { background: var(--cream); overflow: hidden; }
        
        .review-viewport {
            width: 100%;
            overflow: hidden;
            margin-top: 3rem;
            cursor: grab;
        }

        .review-track {
            display: flex;
            transition: transform 0.5s ease-out;
            gap: 2rem;
        }

        .review-card {
            min-width: 350px;
            background: var(--white);
            padding: 2rem;
            border-radius: 15px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.03);
        }

        .stars { color: #FFD700; margin-bottom: 0.5rem; }
        .reviewer { font-weight: 700; display: block; margin-bottom: 0.2rem; }
        .review-date { font-size: 0.8rem; color: #888; margin-bottom: 1rem; display: block; }
        
        .review-text {
            font-size: 0.95rem;
            display: -webkit-box;
            -webkit-line-clamp: 3;
            -webkit-box-orient: vertical;
            overflow: hidden;
        }

        .review-text.expanded {
            -webkit-line-clamp: unset;
        }

        .read-more {
            color: var(--sage);
            font-weight: 700;
            cursor: pointer;
            font-size: 0.85rem;
            display: block;
            margin-top: 0.5rem;
        }

        /* --- Footer Section --- */
        .final-cta {
            background: var(--brown);
            color: var(--white);
            text-align: center;
            padding: 5rem 10%;
        }

        .final-cta h2 { font-size: 2.5rem; margin-bottom: 1rem; }
        
        footer {
            background: #361f1e;
            color: rgba(255,255,255,0.7);
            padding: 2rem 10%;
            text-align: center;
            font-size: 0.9rem;
        }

        .social-link {
            color: var(--white);
            font-size: 1.5rem;
            margin-top: 1rem;
            display: inline-block;
            text-decoration: none;
        }

        /* --- Responsive --- */
        @media (max-width: 900px) {
            .about-grid, .info-grid { grid-template-columns: 1fr; }
            .about-img { height: 350px; order: -1; }
            .menu-grid { grid-template-columns: 1fr; }
            .section-padding { padding: 4rem 5%; }
        }

        @media (max-width: 600px) {
            .hero h1 { font-size: 2.5rem; }
            .review-card { min-width: 280px; }
        }
    </style>
</head>
<body>

    <!-- Section 1: Hero -->
    <header class="hero">
        <!-- Floating SVGs -->
        <svg class="floating-icon" style="top: 15%; left: 10%; width: 60px;" viewBox="0 0 24 24" fill="currentColor"><path d="M11 2c.047 0 .092.006.137.017a2.502 2.502 0 0 1 4.726 0c.045-.011.09-.017.137-.017 1.38 0 2.5 1.12 2.5 2.5 0 .597-.216 1.138-.567 1.56.35.423.567.964.567 1.561 0 1.38-1.12 2.5-2.5 2.5-.047 0-.092-.006-.137-.017a2.502 2.502 0 0 1-4.726 0c-.045.011-.09.017-.137.017-1.38 0-2.5-1.12-2.5-2.5 0-.597.216-1.138.567-1.56a2.506 2.506 0 0 1-.567-1.561c0-1.38 1.12-2.5 2.5-2.5zm0 14h2v2h-2v-2zm-6-2h14v1h-14v-1zm0 2h14v1h-14v-1zm-1 3h16v1h-16v-1z"/></svg>
        <svg class="floating-icon" style="bottom: 20%; right: 10%; width: 50px;" viewBox="0 0 24 24" fill="currentColor"><path d="M2 21h18v-2H2v2zM20 8h-2V5h2v3zm2-3h-4a2 2 0 0 0-2 2v3a2 2 0 0 0 2 2h4a2 2 0 0 0 2-2V7a2 2 0 0 0-2-2zM4 19h14v-9H4v9zM14 5c0-1.1-.9-2-2-2s-2 .9-2 2h4z"/></svg>
        
        <div class="hero-content reveal">
            <span class="badge">⭐ 4.9/5 on Google · 100% Recommend on Facebook</span>
            <h1>Homemade with Heart. <br>Fresh Every Day.</h1>
            <p>Wirral's cosiest little café — cakes, sandwiches & speciality coffee in the heart of Upton</p>
            <div class="btn-group">
                <a href="#menu" class="btn btn-primary">See Our Menu ↓</a>
                <a href="#visit" class="btn btn-outline">Find Us</a>
            </div>
        </div>
    </header>

    <!-- Section 2: Trust Bar -->
    <div class="trust-bar">
        <div class="ticker">
            <span>🍰 100% Recommend on Facebook</span>
            <span>⭐ 4.9 Google Rating</span>
            <span>☕ Fresh Made Daily</span>
            <span>🐾 Dog Friendly</span>
            <span>📶 Free Wi-Fi</span>
            <span>👨‍👩‍👧 Family Friendly</span>
            <span>🅿️ Free Nearby Parking</span>
            <!-- Duplicate for infinite effect -->
            <span>🍰 100% Recommend on Facebook</span>
            <span>⭐ 4.9 Google Rating</span>
            <span>☕ Fresh Made Daily</span>
            <span>🐾 Dog Friendly</span>
            <span>📶 Free Wi-Fi</span>
            <span>👨‍👩‍👧 Family Friendly</span>
            <span>🅿️ Free Nearby Parking</span>
        </div>
    </div>

    <!-- Section 3: About -->
    <section class="section-padding reveal">
        <div class="about-grid">
            <img src="https://images.unsplash.com/photo-1559339352-11d035aa65de?q=80&w=1000" alt="Delicious Cakes" class="about-img">
            <div>
                <h2>A Little Café With a Big Heart</h2>
                <p style="margin: 1.5rem 0;">Cakes by the Lakes is Wirral's best-kept secret — a homemade, traditional café tucked away at 397 Upton Road, Noctorum. Everything is freshly made, the counter changes daily, and you'll always leave with a smile. Whether you're after a hearty sandwich, a stunning celebration cake, or just a slice of school cake and a latte — you've found your place.</p>
                <div class="feature-pills">
                    <span class="pill">🏠 Family Run</span>
                    <span class="pill">🌿 Fresh Daily</span>
                    <span class="pill">💛 Affordable Prices</span>
                </div>
            </div>
        </div>
    </section>

    <!-- Section 4: Menu -->
    <section id="menu" class="section-padding menu-section reveal">
        <h2>What's On the Counter Today</h2>
        <p>Our menu rotates daily — here's a taste of what to expect</p>
        
        <div class="menu-grid">
            <div class="menu-card reveal">
                <h3>🍰 Sweet Treats</h3>
                <ul>
                    <li>Victoria Sponge</li>
                    <li>Biscoff Cream Buns</li>
                    <li>Lemon Drizzle & Coffee & Walnut</li>
                    <li>Brownies & Kinder Brownies</li>
                    <li>Custard Tarts & School Cake</li>
                    <li>Milkybar Cheesecake & Caramel Cakes</li>
                </ul>
            </div>
            <div class="menu-card reveal">
                <h3>🥪 Savoury & Lunch</h3>
                <ul>
                    <li>Salt & Pepper Sausage Rolls</li>
                    <li>Nudger Sandwiches</li>
                    <li>Freshly Made Bagels & Toasties</li>
                    <li>Jacket Potatoes</li>
                    <li>Healthy Wraps</li>
                </ul>
            </div>
            <div class="menu-card reveal">
                <h3>🥗 Boxes & Salads</h3>
                <ul>
                    <li>Pasta Boxes (Pesto / Tomato / Chinese Chicken)</li>
                    <li>Salad Boxes (Chicken Bacon Mayo, Tuna Mayo)</li>
                    <li>Gluten-Free Options Available</li>
                </ul>
            </div>
            <div class="menu-card reveal">
                <h3>☕ Drinks</h3>
                <ul>
                    <li>Specialty Coffees</li>
                    <li>Iced Frappes & Milkshakes</li>
                    <li>Hot Chocolate & Fresh Smoothies</li>
                </ul>
            </div>
        </div>
        
        <div class="meal-deal reveal">
            🎉 Meal Deal — Main + Cake + Hot Drink from just £7.50!
        </div>
    </section>

    <!-- Section 5: Visit & Hours -->
    <section id="visit" class="section-padding reveal">
        <div class="info-grid">
            <div>
                <h2>Visit Us</h2>
                <div style="margin-top:1.5rem">
                    <p><strong>Opening Hours:</strong></p>
                    <p>Mon – Fri: 10:00 AM – 2:30 PM <span id="open-status" class="status-badge">Checking...</span></p>
                    <p>Sat – Sun: Closed</p>
                </div>
                
                <div style="margin-top:2rem">
                    <p>📍 397 Upton Road, Noctorum, CH43 9SE</p>
                    <p>📞 +44 7548 880879</p>
                    <p>📧 cakesbythelakes.wirral@gmail.com</p>
                </div>

                <div class="info-icons">
                    <span>🐾 Dog Friendly</span>
                    <span>👶 High Chairs</span>
                    <span>📶 Free Wi-Fi</span>
                    <span>🅿️ Free Parking</span>
                </div>
            </div>
            <div>
                <div class="map-container">
                    <iframe 
                        src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2389.576822557106!2d-3.0768417232815127!3d53.383049172304!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x487b270726715f33%3A0x6420556f8f7813a4!2s397%20Upton%20Rd%2C%20Noctorum%2C%20Birkenhead%20CH43%209SE!5e0!3m2!1sen!2suk!4v1710000000000" 
                        width="100%" height="100%" style="border:0;" allowfullscreen="" loading="lazy"></iframe>
                </div>
            </div>
        </div>
    </section>

    <!-- Section 6: Reviews Carousel -->
    <section class="section-padding reviews-section">
        <h2 style="text-align: center;">What Our Guests Say</h2>
        <div class="review-viewport">
            <div class="review-track" id="review-track">
                <!-- Review 1 -->
                <div class="review-card">
                    <div class="stars">★★★★★</div>
                    <span class="reviewer">Hughes Louise Emma</span>
                    <span class="review-date">19 Feb 2025</span>
                    <p class="review-text">Been here a few times and what can I say — every cake I've tried have been beautiful. I tried the huge nudger sandwich too the other day and it was amazing so fresh and the coleslaw was amazing. Highly recommend.</p>
                    <span class="read-more" onclick="toggleReview(this)">Read more</span>
                </div>
                <!-- Review 2 -->
                <div class="review-card">
                    <div class="stars">★★★★★</div>
                    <span class="reviewer">Louise Forster-Kerr</span>
                    <span class="review-date">25 Jan 2025</span>
                    <p class="review-text">Such a gorgeous little local spot! Lovely sandwiches, bagels and toasties...and the cakes wow! The staff are so friendly. My mum really fancied a meringue and there were none left, so the lovely lady went in the back and made her one! 10/10 customer service ✨</p>
                    <span class="read-more" onclick="toggleReview(this)">Read more</span>
                </div>
                <!-- Review 3 -->
                <div class="review-card">
                    <div class="stars">★★★★★</div>
                    <span class="reviewer">Tina Denise</span>
                    <span class="review-date">30 Nov 2024</span>
                    <p class="review-text">Love this place. It's warm and inviting. The bread is delicious, amazing salad boxes and the cakes — well I have no words. They are just delicious and all at affordable prices. I definitely recommend.</p>
                    <span class="read-more" onclick="toggleReview(this)">Read more</span>
                </div>
                <!-- Review 4 -->
                <div class="review-card">
                    <div class="stars">★★★★★</div>
                    <span class="reviewer">Valerie Jones</span>
                    <span class="review-date">3 May 2025</span>
                    <p class="review-text">My husband and I had lunch here a few wtext">My husband and I had lunch here a few weeks ago: cheese on toast to eat in and cakes to take out. It was all extremely tasty, portion sizes were enormous, the owner was absolutely lovely and it was ridiculously cheap. Add to all that the fact that the decor is absolutely stunning. We just chanced upon it during a walk and were SO IMPRESSED. We hope to return soon and thoroughly thoroughly recommend it. Well done to all concerned. </p>
