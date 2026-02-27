<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <meta name="description" content="Maa Nirmala DJ & Tent House - Elite Digital Portfolio">
    
    <meta name="theme-color" content="#D4AF37">
    <meta name="mobile-web-app-capable" content="yes">
    <meta name="apple-mobile-web-app-status-bar-style" content="black-translucent">
    <meta name="application-name" content="MNDs Hub">
    
    <link rel="manifest" href='data:application/manifest+json,{"name":"MNDs Secure Hub","short_name":"MNDs App","start_url":".","display":"standalone","background_color":"#050505","theme_color":"#D4AF37","orientation":"portrait","icons":[{"src":"https://i.postimg.cc/Y0jPr7Vy/20251205-103059-IMG-STYLE.jpg","sizes":"192x192","type":"image/jpeg"},{"src":"https://i.postimg.cc/Y0jPr7Vy/20251205-103059-IMG-STYLE.jpg","sizes":"512x512","type":"image/jpeg"}]}'>

    <title>Maa Nirmala DJ & Tent House | SECURE HUB</title>
    
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@400;700&family=Outfit:wght@200;400;600&family=Rajdhani:wght@500;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">

    <style>
        :root {
            /* --- ELITE DARK THEME --- */
            --bg-body: #050505;
            --bg-card: rgba(20, 20, 20, 0.9);
            --border-color: rgba(212, 175, 55, 0.3);
            --gold-primary: #D4AF37;
            --gold-shine: #FFD700;
            --text-main: #ffffff;
            --text-sub: #b3b3b3;
            --glass-blur: blur(25px);
            --nav-glass: blur(30px);
        }

        [data-theme="light"] {
            --bg-body: #f2f2f2;
            --bg-card: rgba(255, 255, 255, 0.95);
            --border-color: rgba(180, 140, 40, 0.3);
            --gold-primary: #b08d26;
            --gold-shine: #d4a017;
            --text-main: #111111;
            --text-sub: #555555;
        }

        ::-webkit-scrollbar { width: 4px; }
        ::-webkit-scrollbar-track { background: #000; }
        ::-webkit-scrollbar-thumb { background: var(--gold-primary); border-radius: 10px; }
        
        * { margin: 0; padding: 0; box-sizing: border-box; -webkit-tap-highlight-color: transparent; outline: none; }
        body { background-color: var(--bg-body); color: var(--text-main); font-family: 'Outfit', sans-serif; overflow-x: hidden; min-height: 100vh; transition: background-color 0.4s ease, color 0.4s ease; user-select: none; }

        /* GATEKEEPER */
        #gatekeeper { position: fixed; inset: 0; z-index: 9999; background: var(--bg-body); display: flex; flex-direction: column; align-items: center; justify-content: center; padding: 20px; text-align: center; background-image: radial-gradient(circle at 50% 50%, rgba(212, 175, 55, 0.1) 0%, transparent 80%); transition: opacity 0.8s ease, visibility 0.8s; }
        .gate-card { width: 100%; max-width: 400px; background: rgba(10, 10, 10, 0.95); border: 1px solid var(--gold-primary); border-radius: 20px; padding: 40px 25px; box-shadow: 0 0 80px rgba(212, 175, 55, 0.15); backdrop-filter: blur(20px); position: relative; overflow: hidden; animation: pulseCard 4s infinite alternate; }
        @keyframes pulseCard { from { transform: scale(1); border-color: rgba(212,175,55,0.3); } to { transform: scale(1.005); border-color: rgba(212,175,55,0.6); } }
        .gate-img-frame { width: 110px; height: 110px; margin: 0 auto 20px; border-radius: 50%; padding: 3px; border: 2px solid var(--gold-primary); box-shadow: 0 0 30px rgba(212, 175, 55, 0.3); }
        .gate-img { width: 100%; height: 100%; border-radius: 50%; object-fit: cover; }
        .gate-title { font-family: 'Cinzel'; color: var(--gold-primary); font-size: 26px; margin-bottom: 5px; text-shadow: 0 0 15px rgba(212, 175, 55, 0.5); font-weight: 700; }
        .gate-sub { color: #666; font-size: 11px; letter-spacing: 4px; margin-bottom: 30px; font-family: 'Rajdhani'; text-transform: uppercase; }
        .gate-input-group { position: relative; margin-bottom: 15px; text-align: left; }
        .gate-input { width: 100%; padding: 15px 15px 15px 45px; background: rgba(255, 255, 255, 0.05); border: 1px solid #333; color: #fff; font-size: 16px; font-family: 'Rajdhani'; transition: 0.3s; border-radius: 10px; }
        .gate-input:focus { border-color: var(--gold-primary); background: rgba(212, 175, 55, 0.08); box-shadow: 0 0 15px rgba(212,175,55,0.1); }
        .gate-icon { position: absolute; left: 15px; top: 17px; color: #555; transition: 0.3s; }
        .gate-input:focus + .gate-icon { color: var(--gold-primary); }
        .gate-btn { width: 100%; padding: 16px; background: linear-gradient(135deg, var(--gold-primary), #997d2d); color: #000; font-weight: 800; font-size: 16px; border: none; cursor: pointer; border-radius: 10px; text-transform: uppercase; letter-spacing: 2px; margin-top: 15px; box-shadow: 0 5px 25px rgba(212, 175, 55, 0.3); transition: 0.3s; }
        .gate-btn:active { transform: scale(0.98); }
        .loading-text { margin-top: 20px; font-size: 12px; color: var(--gold-primary); font-family: 'Rajdhani'; display: none; letter-spacing: 1px; font-weight: bold; }

        /* MAIN UI */
        #main-interface { display: none; opacity: 0; transition: opacity 1.5s ease; padding-bottom: 90px; }
        .bg-fx { position: fixed; inset: 0; z-index: -2; pointer-events: none; overflow: hidden; }
        .orb { position: absolute; border-radius: 50%; filter: blur(120px); opacity: 0.15; animation: float 15s infinite alternate; }
        .orb-1 { width: 350px; height: 350px; background: var(--gold-primary); top: -10%; left: -10%; }
        .orb-2 { width: 300px; height: 300px; background: #00e5ff; bottom: -10%; right: -10%; }
        @keyframes float { 0% { transform: translate(0,0); } 100% { transform: translate(50px, 50px); } }

        /* Navbar & Hamburger */
        .navbar { display: flex; justify-content: space-between; align-items: center; padding: 15px 5%; position: sticky; top: 0; z-index: 1000; background: rgba(5, 5, 5, 0.85); backdrop-filter: var(--glass-blur); border-bottom: 1px solid var(--border-color); }
        .brand { font-family: 'Cinzel'; color: var(--gold-primary); font-weight: 700; font-size: 18px; display: flex; align-items: center; gap: 12px; }
        .controls { display: flex; align-items: center; gap: 15px; }
        .nav-btn { font-size: 20px; cursor: pointer; color: var(--text-main); background: none; border: none; }

        .menu-overlay { position: fixed; inset: 0; background: rgba(0,0,0,0.7); z-index: 5999; display: none; opacity: 0; transition: 0.3s; }
        .menu-overlay.active { display: block; opacity: 1; }
        .side-menu { position: fixed; top: 0; left: -280px; width: 260px; height: 100%; background: rgba(10,10,10,0.98); border-right: 1px solid var(--gold-primary); z-index: 6000; transition: left 0.4s ease; padding-top: 20px; display: flex; flex-direction: column; box-shadow: 5px 0 30px rgba(0,0,0,0.5); overflow-y: auto;}
        .side-menu.open { left: 0; }
        .menu-close { align-self: flex-end; margin: 0 20px 20px 0; font-size: 24px; color: var(--gold-primary); cursor: pointer; }
        .side-link { display: flex; align-items: center; padding: 18px 25px; color: #fff; text-decoration: none; border-bottom: 1px solid #222; font-family: 'Outfit'; font-size: 15px; font-weight: 600; text-transform: uppercase; letter-spacing: 1px; transition: 0.3s; }
        .side-link i { color: var(--gold-primary); margin-right: 15px; font-size: 18px; width: 20px; text-align: center; }
        .side-link:hover { background: rgba(212,175,55,0.1); padding-left: 30px; }
        .menu-logo { text-align: center; padding-bottom: 20px; border-bottom: 1px solid var(--border-color); margin-bottom: 10px; }
        .menu-logo img { width: 80px; height: 80px; border-radius: 50%; border: 2px solid var(--gold-primary); }

        #google_translate_element { margin-right: 5px; }
        .goog-te-gadget-simple { background-color: rgba(255,255,255,0.05) !important; border: 1px solid var(--gold-primary) !important; padding: 4px 8px !important; border-radius: 20px !important; }
        .goog-te-gadget-simple span { color: var(--gold-primary) !important; font-weight: 700 !important; font-size: 11px !important; }
        .goog-te-gadget-icon, .goog-te-banner-frame { display: none !important; } body { top: 0px !important; }

        /* Profile Section */
        .container { width: 100%; max-width: 800px; margin: 0 auto; padding: 0 20px; }
        .profile-wrapper { text-align: center; padding: 60px 0 30px; }
        .img-container { width: 160px; height: 160px; margin: 0 auto 20px; position: relative; border-radius: 50%; padding: 5px; background: linear-gradient(135deg, var(--gold-primary), transparent, var(--gold-shine)); }
        .profile-pic { width: 100%; height: 100%; border-radius: 50%; object-fit: cover; border: 4px solid var(--bg-body); background: #000; }
        h1 { font-family: 'Rajdhani', sans-serif; font-size: 32px; font-weight: 700; background: linear-gradient(to right, var(--text-main), var(--gold-primary), var(--text-main)); -webkit-background-clip: text; -webkit-text-fill-color: transparent; margin-bottom: 5px; }
        .verified { color: #1DA1F2; font-size: 20px; vertical-align: middle; margin-left: 5px; }
        .bio { color: var(--gold-primary); font-size: 13px; letter-spacing: 2px; font-weight: 600; text-transform: uppercase; }

        #installBtn { display: none; margin: 20px auto; background: rgba(212, 175, 55, 0.1); border: 1px solid var(--gold-primary); color: var(--gold-primary); padding: 12px 30px; border-radius: 30px; font-size: 12px; font-weight: bold; cursor: pointer; box-shadow: 0 0 20px rgba(212, 175, 55, 0.15); animation: bounce 2s infinite; letter-spacing: 1px; }
        @keyframes bounce { 0%, 100% { transform: translateY(0); } 50% { transform: translateY(-5px); } }

        /* Grids & Sections */
        .section-label { display: flex; align-items: center; gap: 10px; margin: 35px 0 15px; color: var(--gold-primary); font-family: 'Cinzel'; font-weight: bold; font-size: 14px; border-bottom: 1px solid var(--border-color); padding-bottom: 8px; text-transform: uppercase; scroll-margin-top: 80px; }
        .grid { display: grid; grid-template-columns: 1fr 1fr; gap: 15px; }
        @media (min-width: 600px) { .grid { gap: 20px; } }
        
        .card { background: var(--bg-card); border: 1px solid var(--border-color); border-radius: 16px; padding: 20px; height: 100px; display: flex; flex-direction: column; align-items: center; justify-content: center; text-decoration: none; color: var(--text-main); position: relative; overflow: hidden; backdrop-filter: var(--glass-blur); box-shadow: 0 4px 15px rgba(0,0,0,0.1); transition: all 0.3s; }
        .card:active { transform: scale(0.96); border-color: var(--gold-shine); }
        .card i { font-size: 28px; margin-bottom: 8px; color: var(--gold-primary); transition: 0.3s; }
        .card span { font-size: 11px; font-weight: 600; text-transform: uppercase; text-align: center; }
        .full-w { grid-column: span 2; flex-direction: row; gap: 15px; height: 75px; background: linear-gradient(90deg, rgba(212,175,55,0.05), transparent); }
        .full-w i { margin-bottom: 0; font-size: 24px; }

        .img-card { background: var(--bg-card); border: 1px solid var(--border-color); border-radius: 16px; padding: 10px; aspect-ratio: 1 / 1; display: flex; flex-direction: column; align-items: center; justify-content: space-between; text-decoration: none; color: var(--text-main); position: relative; overflow: hidden; backdrop-filter: var(--glass-blur); box-shadow: 0 4px 15px rgba(0,0,0,0.3); transition: all 0.3s; }
        .img-card:active { transform: scale(0.96); border-color: var(--gold-shine); }
        .img-card img { width: 100%; height: 75%; object-fit: cover; border-radius: 10px; border: 1px solid rgba(212,175,55,0.3); }
        .img-card span { font-size: 12px; font-weight: 700; text-transform: uppercase; text-align: center; color: var(--gold-primary); margin-top: 5px; font-family: 'Rajdhani'; letter-spacing: 1px; }

        /* LIVE FEED GALLERY CARDS (LARGE) */
        .feed-container { display: flex; flex-direction: column; gap: 20px; }
        .feed-card { background: var(--bg-card); border: 1px solid var(--border-color); border-radius: 20px; padding: 20px; box-shadow: 0 8px 25px rgba(0,0,0,0.4); text-align: left; }
        .feed-badge { display: inline-block; background: var(--gold-primary); color: #000; padding: 4px 10px; border-radius: 20px; font-size: 11px; font-weight: bold; margin-bottom: 12px; text-transform: uppercase; letter-spacing: 1px; }
        .feed-media { width: 100%; border-radius: 12px; border: 2px solid rgba(212,175,55,0.2); margin-bottom: 15px; background: #000; object-fit: contain; }
        .feed-img { max-height: 400px; }
        .feed-video { height: 250px; }
        .feed-audio { width: 100%; margin-bottom: 15px; outline: none; border-radius: 30px; }
        .feed-text { font-size: 15px; color: #fff; line-height: 1.6; font-family: 'Outfit'; }
        .feed-offer { font-size: 18px; color: var(--gold-shine); font-weight: bold; font-family: 'Cinzel'; text-align: center; padding: 20px; border: 1px dashed var(--gold-primary); border-radius: 12px; background: rgba(212,175,55,0.05); }

        /* Sliders */
        .slider-container { display: flex; overflow-x: auto; gap: 15px; padding-bottom: 15px; scroll-snap-type: x mandatory; scrollbar-width: none; }
        .slider-container::-webkit-scrollbar { display: none; }
        .slide-card { flex: 0 0 85%; scroll-snap-align: center; background: var(--bg-card); border: 1px solid var(--border-color); border-radius: 16px; overflow: hidden; position: relative; box-shadow: 0 5px 20px rgba(0,0,0,0.2); }
        .slide-card img { width: 100%; height: 220px; object-fit: cover; display: block; border-bottom: 2px solid var(--gold-primary); }
        .slide-info { padding: 15px; text-align: center; background: linear-gradient(0deg, #000, transparent); }
        .slide-info h3 { color: var(--gold-primary); font-family: 'Rajdhani'; font-size: 18px; text-transform: uppercase; letter-spacing: 1px; }

        /* Team Cards */
        .team-card { flex: 0 0 85%; scroll-snap-align: center; text-align:center; background:var(--bg-card); border-radius:26px; border: 1px solid var(--border-color); padding: 30px 15px; box-shadow: 0 5px 20px rgba(0,0,0,0.2); }
        .team-card img { width: 130px; height: 130px; object-fit:cover; border-radius:50%; border:3px solid var(--gold-primary); margin-bottom:15px; }
        .team-card h1 { font-size:24px; font-weight:800; margin:5px 0; background:linear-gradient(90deg,#FFD700,#D4AF37,#FFD700); -webkit-background-clip:text; -webkit-text-fill-color:transparent; font-family: 'Rajdhani'; }
        .team-card h3 { font-size:14px; color: var(--gold-primary); margin-bottom: 15px; text-transform: uppercase; letter-spacing: 1px; }
        .team-card p { font-size:13px; line-height:1.6; color:#eaeaea; margin-bottom:10px; }

        /* Map Container */
        .map-container { background: var(--bg-card); padding: 15px; border-radius: 20px; border: 1px solid var(--border-color); box-shadow: 0 5px 20px rgba(0,0,0,0.2); }
        .map-wrapper { width: 100%; aspect-ratio: 1 / 1; border-radius: 12px; overflow: hidden; border: 2px solid var(--gold-primary); }

        /* Owner Profile */
        .owner-profile { background:var(--bg-card); border-radius:26px; border: 1px solid var(--border-color); padding: 30px 20px; box-shadow: 0 5px 20px rgba(0,0,0,0.2); margin-bottom: 30px; }

        /* Bottom Nav */
        .bottom-nav { position: fixed; bottom: 0; left: 0; width: 100%; height: 75px; background: rgba(5, 5, 5, 0.95); backdrop-filter: var(--nav-glass); border-top: 1px solid var(--border-color); z-index: 4000; display: flex; justify-content: space-around; align-items: center; }
        .nav-item { flex: 1; display: flex; flex-direction: column; align-items: center; justify-content: center; color: var(--text-sub); gap: 4px; cursor: pointer; transition: 0.3s; }
        .nav-item.active { color: var(--gold-primary); }
        .nav-item.active i { transform: translateY(-3px); text-shadow: 0 0 15px var(--gold-primary); }

        .ai-trigger { position: fixed; bottom: 90px; right: 25px; width: 60px; height: 60px; border-radius: 50%; background: linear-gradient(135deg, var(--gold-primary), #997d2d); display: flex; align-items: center; justify-content: center; box-shadow: 0 0 30px rgba(212,175,55,0.4); z-index: 2000; cursor: pointer; animation: pulse 3s infinite; }
        @keyframes pulse { 0% { transform: scale(1); } 50% { transform: scale(1.05); } 100% { transform: scale(1); } }

        /* Modals & Forms */
        .modal-wrap { position: fixed; inset: 0; background: rgba(0,0,0,0.85); z-index: 5000; display: none; align-items: center; justify-content: center; backdrop-filter: blur(8px); opacity: 0; transition: opacity 0.3s; }
        .modal-wrap.active { opacity: 1; display: flex; }
        .modal-inner { width: 92%; max-width: 450px; background: #080808; border: 1px solid var(--gold-primary); border-radius: 20px; overflow: hidden; display: flex; flex-direction: column; box-shadow: 0 0 60px rgba(212,175,55,0.15); max-height: 85vh; }
        
        .book-area { padding: 20px; overflow-y: auto; text-align: left; }
        .f-group { margin-bottom: 12px; }
        .f-label { display: block; color: var(--gold-primary); font-size: 11px; margin-bottom: 5px; text-transform: uppercase; font-weight: bold; font-family: 'Rajdhani'; letter-spacing: 1px; }
        .f-input { width: 100%; padding: 12px; background: rgba(255,255,255,0.05); border: 1px solid #333; color: #fff; border-radius: 8px; font-family: 'Outfit'; font-size: 14px; }
        .f-input:focus { border-color: var(--gold-primary); outline: none; background: rgba(212,175,55,0.05); }
        .f-btn { width: 100%; padding: 15px; background: var(--gold-primary); color: #000; font-weight: 800; border: none; border-radius: 8px; cursor: pointer; text-transform: uppercase; margin-top: 10px; font-size: 16px; transition: 0.3s; }
        .f-btn:active { transform: scale(0.98); }

        .loc-group { border: 1px dashed var(--gold-primary); padding: 15px; border-radius: 12px; margin-bottom: 15px; background: rgba(212,175,55,0.02); }
        .loc-title { color: var(--gold-primary); font-family: 'Cinzel'; font-size: 12px; font-weight: bold; margin-bottom: 15px; display: block; letter-spacing: 1px; text-align: center; }

        .star-rating { display: flex; flex-direction: row-reverse; justify-content: center; gap: 8px; margin: 15px 0 25px; }
        .star-rating input { display: none; }
        .star-rating label { font-size: 35px; color: #333; cursor: pointer; transition: 0.2s; text-shadow: 0 0 10px rgba(0,0,0,0.5); }
        .star-rating input:checked ~ label, .star-rating label:hover, .star-rating label:hover ~ label { color: var(--gold-shine); text-shadow: 0 0 15px var(--gold-primary); }

        .chat-box { height: 350px; padding: 20px; overflow-y: auto; background: #0a0a0a; display: flex; flex-direction: column; gap: 10px; }
        .bubble { padding: 10px 15px; border-radius: 12px; max-width: 80%; font-size: 13px; line-height: 1.4; }
        .bubble.bot { background: rgba(212,175,55,0.15); border: 1px solid rgba(212,175,55,0.3); color: #fff; align-self: flex-start; border-bottom-left-radius: 2px;}
        .bubble.user { background: #333; color: #fff; align-self: flex-end; border-bottom-right-radius: 2px; }
        .toast { position: fixed; top: 20px; left: 50%; transform: translateX(-50%); background: var(--gold-primary); color: #000; padding: 10px 20px; border-radius: 30px; font-weight: bold; font-size: 12px; opacity: 0; pointer-events: none; transition: 0.3s; z-index: 6000; }
        .toast.show { opacity: 1; top: 40px; }
        
        /* Pricing Cards */
        .price-card { background: rgba(255,255,255,0.05); border: 1px solid var(--border-color); border-radius: 12px; padding: 15px; margin-bottom: 15px; display: flex; justify-content: space-between; align-items: center; }
        .price-title { font-family: 'Cinzel'; font-weight: bold; font-size: 16px; color: #fff; }
        .price-amt { color: var(--gold-primary); font-size: 20px; font-weight: bold; font-family: 'Rajdhani'; }
    </style>
</head>
<body data-theme="dark">

    <div id="gatekeeper">
        <div class="gate-card">
            <div class="gate-img-frame"><img src="https://i.postimg.cc/Y0jPr7Vy/20251205-103059-IMG-STYLE.jpg" class="gate-img" alt="Profile"></div>
            <h2 class="gate-title">MAA NIRMALA DJ</h2>
            <div class="gate-sub">SECURE PORTFOLIO GATEWAY</div>
            <div class="gate-input-group"><input type="text" id="g-name" class="gate-input" placeholder="YOUR FULL NAME"><i class="fas fa-user gate-icon"></i></div>
            <div class="gate-input-group"><input type="tel" id="g-phone" class="gate-input" placeholder="YOUR MOBILE NUMBER"><i class="fas fa-phone gate-icon"></i></div>
            <button class="gate-btn" id="btn-verify" onclick="initiateSecureEntry()"><i class="fas fa-fingerprint"></i> VERIFY & ENTER</button>
            <div class="loading-text" id="g-status"><i class="fas fa-circle-notch fa-spin"></i> SECURE SCANNING...</div>
        </div>
    </div>

    <div class="menu-overlay" id="menuOverlay" onclick="toggleMenu()"></div>
    <div class="side-menu" id="sideMenu">
        <i class="fas fa-times menu-close" onclick="toggleMenu()"></i>
        <div class="menu-logo">
            <img src="https://i.postimg.cc/Y0jPr7Vy/20251205-103059-IMG-STYLE.jpg" alt="Logo">
            <div style="color:var(--gold-primary); font-family:'Cinzel'; font-weight:bold; margin-top:5px;">MNDs Hub</div>
        </div>
        <a href="#" class="side-link" onclick="toggleMenu(); navAction('home')"><i class="fas fa-home"></i> Home</a>
        <a href="#" class="side-link" onclick="toggleMenu(); navAction('gallery')"><i class="fas fa-camera-retro"></i> Live Gallery</a>
        <a href="#" class="side-link" onclick="toggleMenu(); openPricing()"><i class="fas fa-tags"></i> Price List</a>
        <a href="#" class="side-link" onclick="toggleMenu(); navAction('booking')"><i class="fas fa-calendar-check"></i> Booking</a>
        <a href="#" class="side-link" onclick="toggleMenu(); openFeedback()"><i class="fas fa-star"></i> Feedback</a>
        <a href="#" class="side-link" onclick="toggleMenu(); navAction('links')"><i class="fas fa-link"></i> All Links</a>
        <a href="tel:+919771617808" class="side-link"><i class="fas fa-phone"></i> Contact</a>
        <a href="mailto:lalukumartanti75@gmail.com" class="side-link"><i class="fas fa-envelope"></i> Email</a>
    </div>

    <div id="main-interface">
        <audio id="sfx-tap"><source src="https://assets.mixkit.co/active_storage/sfx/2568/2568-preview.mp3"></audio>
        <div id="toast" class="toast"><i class="fas fa-check-circle"></i> Success</div>
        <div class="bg-fx"><div class="orb orb-1"></div><div class="orb orb-2"></div></div>
        
        <nav class="navbar">
            <div class="brand"><i class="fas fa-bars nav-btn" onclick="toggleMenu()"></i><span><i class="fas fa-crown"></i> MND Hub</span></div>
            <div style="display: flex; align-items: center;">
                <div id="google_translate_element"></div>
                <div class="controls"><button class="nav-btn" id="themeIcon" onclick="themeSwitch()"><i class="fas fa-sun"></i></button></div>
            </div>
        </nav>
        
        <div class="container" id="homeSection">
            <div class="profile-wrapper">
                <div class="img-container"><img src="https://i.postimg.cc/Y0jPr7Vy/20251205-103059-IMG-STYLE.jpg" class="profile-pic" alt="Maa Nirmala DJ & Tent House"></div>
                <h1>MAA NIRMALA DJ & TENT HOUSE <i class="fas fa-check-circle verified"></i></h1>
                <p class="bio">Digital Creator | Developer</p>
                <button id="installBtn" onclick="installApp()"><i class="fas fa-download"></i> INSTALL MNDs APP</button>
            </div>

            <div class="section-label"><i class="fas fa-images"></i> OUR SETUP & SHOWCASE</div>
            <div class="grid">
                <a href="#" class="img-card" onclick="navAction('booking')"><img src="https://i.postimg.cc/Y0jPr7Vy/20251205-103059-IMG-STYLE.jpg" alt="DJ Setup"><span>Elite DJ Setup</span></a>
                <a href="#" class="img-card" onclick="navAction('booking')"><img src="https://i.postimg.cc/Y0jPr7Vy/20251205-103059-IMG-STYLE.jpg" alt="Tent House"><span>Premium Tents</span></a>
                <a href="#" class="img-card" onclick="navAction('booking')"><img src="https://i.postimg.cc/Y0jPr7Vy/20251205-103059-IMG-STYLE.jpg" alt="Lighting"><span>Stage Lighting</span></a>
                <a href="#" class="img-card" onclick="navAction('booking')"><img src="https://i.postimg.cc/Y0jPr7Vy/20251205-103059-IMG-STYLE.jpg" alt="Booking"><span>Book Event Now</span></a>
            </div>

            <div class="section-label" style="margin-top: 40px;"><i class="fas fa-star"></i> BEST OF MAA NIRMALA</div>
            <div class="slider-container">
                <div class="slide-card"><img src="https://i.postimg.cc/Y0jPr7Vy/20251205-103059-IMG-STYLE.jpg" alt="Setup 1"><div class="slide-info"><h3>Grand Wedding Setup</h3></div></div>
                <div class="slide-card"><img src="https://i.postimg.cc/Y0jPr7Vy/20251205-103059-IMG-STYLE.jpg" alt="Setup 2"><div class="slide-info"><h3>Heavy Bass DJ Event</h3></div></div>
                <div class="slide-card"><img src="https://i.postimg.cc/Y0jPr7Vy/20251205-103059-IMG-STYLE.jpg" alt="Setup 3"><div class="slide-info"><h3>VIP Tent & Decoration</h3></div></div>
            </div>

            <div class="section-label" id="liveGallerySection" style="margin-top: 40px;"><i class="fas fa-broadcast-tower"></i> LIVE UPDATES & GALLERY</div>
            <div class="feed-container" id="dynamicGallery">
                </div>
            
            <div class="section-label" style="margin-top:40px;"><i class="fas fa-users"></i> MEET OUR TEAM</div>
            <div class="slider-container">
                <div class="team-card">
                    <img src="https://i.postimg.cc/Y0jPr7Vy/20251205-103059-IMG-STYLE.jpg" alt="Lalu Kumar Tanti">
                    <h1>Lalu Kumar Tanti</h1>
                    <h3>Owner & Founder</h3>
                    <p>A passionate and hardworking individual providing the best event setup, DJ, and Tent services.</p>
                </div>
                <div class="team-card">
                    <img src="https://i.postimg.cc/Y0jPr7Vy/20251205-103059-IMG-STYLE.jpg" alt="Mr. Lalu Kumar">
                    <h1>Mr. Lalu Kumar</h1>
                    <h3>Business Dev. Manager</h3>
                    <p>Ensuring top-tier service delivery and managing all grand event setups across the district.</p>
                </div>
                <div class="team-card">
                    <img src="https://i.postimg.cc/Y0jPr7Vy/20251205-103059-IMG-STYLE.jpg" alt="Sildhar Kumar">
                    <h1>Sildhar Kumar</h1>
                    <h3>Business Associate</h3>
                    <p>Coordinating premium tent decorations, lighting arrangements, and dedicated client relations.</p>
                </div>
            </div>

            <div class="section-label" style="margin-top:40px;"><i class="fas fa-info-circle"></i> ABOUT THE BUSINESS</div>
            <div class="owner-profile" style="text-align: left;">
                <h1 style="text-align: center; font-size: 28px;">Maa Nirmala DJ & Tent House</h1>
                <p style="text-align: center; color: var(--gold-primary); font-weight: bold; margin-bottom: 20px; text-transform: uppercase; letter-spacing: 1px;">Premium Event Management in Bihar</p>
                <p style="font-size: 14px;">Welcome to <b>Maa Nirmala DJ & Tent House</b>, the premier event management and setup service based in Beltikri. We specialize in transforming ordinary events into grand, unforgettable celebrations.</p>
                <ul style="color: #eaeaea; font-size: 14px; line-height: 1.8; margin-left: 20px; margin-bottom: 25px; margin-top: 15px;">
                    <li><b style="color: var(--gold-primary);">Elite DJ Setups:</b> High-fidelity sound systems, heavy bass, and non-stop entertainment.</li>
                    <li><b style="color: var(--gold-primary);">Premium Tent Houses:</b> Grand wedding tents, VIP seating, and beautiful decorations.</li>
                    <li><b style="color: var(--gold-primary);">Stage Lighting:</b> Advanced dynamic lighting to illuminate your special moments.</li>
                </ul>
                <div style="border-top: 1px solid var(--border-color); margin: 25px 0;"></div>
                <div style="text-align: center;">
                    <img src="https://i.postimg.cc/Y0jPr7Vy/20251205-103059-IMG-STYLE.jpg" alt="Lalu Kumar Tanti" style="width: 100px; height: 100px; margin-bottom: 10px; border: 3px solid var(--gold-primary);">
                    <h2 style="color: var(--gold-primary); font-family: 'Cinzel'; font-size: 22px; font-weight: bold;">Lalu Kumar Tanti</h2>
                    <h3 style="font-size: 12px; color: #aaa; margin-bottom: 15px; text-transform: uppercase; letter-spacing: 2px;">Founder & Owner</h3>
                </div>
            </div>

            <div class="section-label" style="margin-top:40px;"><i class="fas fa-map-marker-alt"></i> OUR LOCATION</div>
            <div class="map-container">
                <p style="text-align: center; color: var(--gold-primary); font-family: 'Cinzel'; font-weight: bold; font-size: 18px; margin-bottom: 5px;">Maa Nirmala DJ & Tent House</p>
                <p style="text-align: center; font-size: 12px; color: #ccc; margin-bottom: 15px; font-family: 'Outfit'; letter-spacing: 1px;">JRPM+RQ, Beltikri, Tola Tetaria, Bihar 814131</p>
                
                <div class="map-wrapper">
                    <iframe src="https://maps.google.com/maps?q=JRPM+RQ%20Beltikri,%20Tola%20Tetaria,%20Bihar%20814131&t=&z=15&ie=UTF8&iwloc=&output=embed" width="100%" height="100%" frameborder="0" style="border:0;" allowfullscreen="" aria-hidden="false" tabindex="0"></iframe>
                </div>
                
                <a href="https://maps.google.com/maps?q=JRPM+RQ%20Beltikri,%20Tola%20Tetaria,%20Bihar%20814131" target="_blank" style="display: block; width: 100%; padding: 15px; background: var(--gold-primary); color: #000; text-align: center; font-weight: bold; border-radius: 8px; text-decoration: none; margin-top: 15px; font-family: 'Rajdhani'; letter-spacing: 1px; transition: 0.3s;">
                    <i class="fas fa-directions"></i> GET DIRECTIONS TO MAP
                </a>
            </div>

            <div class="section-label" style="margin-top:40px;"><i class="fas fa-music"></i> THE MAA NIRMALA EXPERIENCE</div>
            <div style="background: var(--bg-card); border: 1px solid var(--border-color); border-radius: 20px; padding: 20px; text-align: center; box-shadow: 0 5px 20px rgba(0,0,0,0.2);">
                <img src="https://i.postimg.cc/Y0jPr7Vy/20251205-103059-IMG-STYLE.jpg" style="width: 100%; height: 200px; object-fit: cover; border-radius: 12px; border: 2px solid var(--gold-primary); margin-bottom: 15px;" alt="Experience">
                <h3 style="color: var(--gold-primary); font-family: 'Cinzel'; margin-bottom: 10px; font-size: 20px;">Unmatched Sound & Vibes</h3>
                <p style="font-size: 14px; line-height: 1.6; color: #ddd;">Maa Nirmala DJ sets the standard for high-energy celebrations in Banka. With state-of-the-art audio, dazzling light shows, and premium VIP tents, we guarantee a flawless event. From intimate functions to massive district festivals, our team works tirelessly to bring your dream event to reality.</p>
            </div>

            <div style="text-align:center; margin-top:30px; margin-bottom:30px;"><div class="rights" style="color:var(--gold-primary); font-weight:bold; font-size:12px;">© 2026 All Rights Reserved — Maa Nirmala DJ & Tent House</div></div>
        </div>

        <div class="bottom-nav">
            <div class="nav-item active" id="navHome" onclick="navAction('home')"><i class="fas fa-home"></i><span>Home</span></div>
            <div class="nav-item" id="navLinks" onclick="navAction('links')"><i class="fas fa-link"></i><span>Links</span></div>
            <div class="nav-item" id="navBooking" onclick="navAction('booking')"><i class="fas fa-calendar-alt"></i><span>Booking</span></div>
            <div class="nav-item" id="navLogin" onclick="navAction('login')"><i class="fas fa-user-shield"></i><span>Auth</span></div>
        </div>

        <div class="ai-trigger" onclick="openAI()"><i class="fas fa-brain" style="font-size:24px; color:#fff;"></i></div>

        <div class="modal-wrap" id="priceModal" onclick="closeModal(event)">
            <div class="modal-inner" onclick="event.stopPropagation()">
                <div class="ai-head" style="padding:15px; border-bottom:1px solid #333; display:flex; justify-content:space-between; align-items:center;">
                    <span style="color:var(--gold-primary); font-weight:bold; font-family:'Cinzel';"><i class="fas fa-tags"></i> STANDARD PRICE LIST</span>
                    <i class="fas fa-times" onclick="closeModal(null, true)" style="color:#fff; cursor:pointer;"></i>
                </div>
                <div class="book-area">
                    <p style="color:#ddd; font-size:12px; margin-bottom:20px; text-align:center;">*Prices are estimated starting points and may vary based on location and specific event requirements.</p>
                    
                    <div class="price-card">
                        <div>
                            <div class="price-title">Heavy DJ Setup</div>
                            <div style="font-size:11px; color:#aaa;">Dual Bass, Tops, Light & Operator</div>
                        </div>
                        <div class="price-amt">₹8,000+</div>
                    </div>
                    <div class="price-card">
                        <div>
                            <div class="price-title">Grand Wedding Tent</div>
                            <div style="font-size:11px; color:#aaa;">Pandal, Chairs, VIP Sofa, Carpet</div>
                        </div>
                        <div class="price-amt">₹25,000+</div>
                    </div>
                    <div class="price-card">
                        <div>
                            <div class="price-title">Stage Decoration</div>
                            <div style="font-size:11px; color:#aaa;">Floral Setup, Lighting, Backdrop</div>
                        </div>
                        <div class="price-amt">₹10,000+</div>
                    </div>
                    <div class="price-card">
                        <div>
                            <div class="price-title">Complete Package</div>
                            <div style="font-size:11px; color:#aaa;">DJ + Tent + Lighting Full Setup</div>
                        </div>
                        <div class="price-amt">Custom</div>
                    </div>
                    
                    <button class="f-btn" onclick="navAction('booking')"><i class="fas fa-calendar-check"></i> BOOK NOW FOR EXACT QUOTE</button>
                </div>
            </div>
        </div>

        <div class="modal-wrap" id="linksModal" onclick="closeModal(event)">
            <div class="modal-inner" onclick="event.stopPropagation()">
                <div class="ai-head" style="padding:15px; border-bottom:1px solid #333; display:flex; justify-content:space-between; align-items:center; background:rgba(10,10,10,0.9);">
                    <span style="color:var(--gold-primary); font-weight:bold; font-family:'Cinzel';"><i class="fas fa-link"></i> OFFICIAL LINKS HUB</span>
                    <i class="fas fa-times" onclick="closeModal(null, true)" style="color:#fff; cursor:pointer;"></i>
                </div>
                <div class="book-area">
                    <div class="section-label" style="margin-top: 0;"><i class="fas fa-bolt"></i> DIRECT CONNECT</div>
                    <div class="grid">
                        <a href="#" class="card" onclick="playTap()"><i class="fas fa-phone-volume"></i><span>Call Now</span></a>
                        <a href="#" class="card" onclick="playTap()"><i class="fab fa-whatsapp"></i><span>WhatsApp</span></a>
                        <a href="#" class="card" onclick="playTap()"><i class="fab fa-telegram-plane"></i><span>Telegram</span></a>
                        <a href="#" target="_blank" class="card full-w" onclick="playTap()"><i class="fas fa-map-marked-alt"></i><span>Official Location</span></a>
                    </div>
                    <div class="section-label"><i class="fas fa-globe"></i> SOCIAL EMPIRE</div>
                    <div class="grid">
                        <a href="#" class="card" onclick="playTap()"><i class="fab fa-instagram"></i><span>Instagram</span></a>
                        <a href="#" class="card" onclick="playTap()"><i class="fab fa-facebook-f"></i><span>Facebook</span></a>
                        <a href="#" class="card full-w" onclick="playTap()"><i class="fab fa-youtube"></i><span>YouTube</span></a>
                    </div>
                    <div class="section-label"><i class="fas fa-coins"></i> PAYMENTS & MORE</div>
                    <div class="grid" style="margin-bottom:30px;">
                        <a href="#" class="card" onclick="playTap()"><i class="fas fa-wallet"></i><span>PhonePe</span></a>
                        <a href="#" class="card" onclick="playTap()"><i class="fab fa-google-pay"></i><span>GPay</span></a>
                        <div class="card full-w" onclick="copyUPI()"><i class="fas fa-qrcode"></i><span>Copy UPI ID</span><span style="font-size:7px; opacity:0.7;">9771617808-2@axl</span></div>
                    </div>
                </div>
            </div>
        </div>

        <div class="modal-wrap" id="feedbackModal" onclick="closeModal(event)">
            <div class="modal-inner" onclick="event.stopPropagation()">
                <div class="ai-head" style="padding:15px; border-bottom:1px solid #333; display:flex; justify-content:space-between; align-items:center;">
                    <span style="color:var(--gold-primary); font-weight:bold; font-family:'Cinzel';"><i class="fas fa-star"></i> CLIENT FEEDBACK</span>
                    <i class="fas fa-times" onclick="closeModal(null, true)" style="color:#fff; cursor:pointer;"></i>
                </div>
                <div class="book-area">
                    <div style="text-align:center; margin-bottom:15px; background: rgba(212,175,55,0.05); padding: 15px; border-radius: 12px; border: 1px solid rgba(212,175,55,0.2);">
                        <h3 style="color:var(--gold-primary); font-family:'Rajdhani'; font-size: 22px; margin-bottom:5px;">Maa Nirmala DJ & Tent House</h3>
                        <p style="font-size:12px; color:#ddd; line-height: 1.4;">Rate your experience with our DJ setup and Tent management!</p>
                    </div>
                    <div class="star-rating">
                        <input type="radio" id="star5" name="rating" value="5"><label for="star5" class="fas fa-star"></label>
                        <input type="radio" id="star4" name="rating" value="4"><label for="star4" class="fas fa-star"></label>
                        <input type="radio" id="star3" name="rating" value="3"><label for="star3" class="fas fa-star"></label>
                        <input type="radio" id="star2" name="rating" value="2"><label for="star2" class="fas fa-star"></label>
                        <input type="radio" id="star1" name="rating" value="1"><label for="star1" class="fas fa-star"></label>
                    </div>
                    <div class="f-group"><span class="f-label">Your Name</span><input type="text" id="fb-name" class="f-input" placeholder="Enter your name"></div>
                    <div class="f-group"><span class="f-label">Your Experience & Feedback</span><textarea id="fb-text" class="f-input" rows="3" placeholder="Tell us what you liked..." style="resize:none; font-family:'Outfit';"></textarea></div>
                    <button class="f-btn" onclick="submitFeedback()" id="submitFbBtn"><i class="fas fa-paper-plane"></i> SEND FEEDBACK TO LALU</button>
                </div>
            </div>
        </div>

        <div class="modal-wrap" id="bookModal" onclick="closeModal(event)">
            <div class="modal-inner" onclick="event.stopPropagation()">
                <div class="ai-head" style="padding:15px; border-bottom:1px solid #333; display:flex; justify-content:space-between; align-items:center;">
                    <span style="color:var(--gold-primary); font-weight:bold; font-family:'Cinzel';"><i class="fas fa-clipboard-list"></i> OFFICIAL BOOKING</span>
                    <i class="fas fa-times" onclick="closeModal(null, true)" style="color:#fff; cursor:pointer;"></i>
                </div>
                <div class="book-area" id="bookFormArea">
                    <div class="f-group"><span class="f-label">Event / Requirement Type *</span><input type="text" id="b-type" class="f-input" placeholder="e.g. Wedding DJ, VIP Tent"></div>
                    <div class="f-group"><span class="f-label">Full Name *</span><input type="text" id="b-name" class="f-input" placeholder="Enter Full Name"></div>
                    <div class="f-group"><span class="f-label">Father's Name *</span><input type="text" id="b-father" class="f-input" placeholder="Enter Father's Name"></div>
                    <div class="f-group"><span class="f-label">Contact Number *</span><input type="tel" id="b-phone" class="f-input" placeholder="Main Mobile Number"></div>
                    <div class="f-group"><span class="f-label">Alternate Number</span><input type="tel" id="b-altphone" class="f-input" placeholder="Second Mobile Number"></div>
                    <div class="f-group"><span class="f-label">Email Address</span><input type="email" id="b-email" class="f-input" placeholder="example@email.com"></div>
                    
                    <div class="loc-group">
                        <span class="loc-title">📍 EVENT LOCATION DETAILS</span>
                        <div class="f-group"><span class="f-label">State *</span><input type="text" id="b-state" class="f-input" placeholder="e.g. Bihar"></div>
                        <div class="f-group"><span class="f-label">District *</span><input type="text" id="b-district" class="f-input" placeholder="e.g. Banka"></div>
                        <div class="f-group"><span class="f-label">City *</span><input type="text" id="b-city" class="f-input" placeholder="e.g. Katoria"></div>
                        <div class="f-group"><span class="f-label">Village *</span><input type="text" id="b-village" class="f-input" placeholder="e.g. Beltikri"></div>
                        <div class="f-group" style="margin-bottom:0;"><span class="f-label">Pin Code *</span><input type="tel" id="b-pincode" class="f-input" placeholder="e.g. 813106"></div>
                    </div>
                    
                    <button class="f-btn" onclick="submitBooking()" id="submitBookBtn"><i class="fas fa-paper-plane"></i> SEND BOOKING REQUEST</button>
                </div>
            </div>
        </div>

        <div class="modal-wrap" id="aiModal" onclick="closeModal(event)">
            <div class="modal-inner" onclick="event.stopPropagation()">
                <div class="ai-head" style="padding:15px; background:var(--gold-primary); color:#000; font-weight:bold;">
                    MNDs BRAIN v2.07<i class="fas fa-times" style="float:right; cursor:pointer;" onclick="closeModal(null, true)"></i>
                </div>
                <div class="chat-box" id="chatHistory">
                    <div class="bubble bot">Hello! I am MNDs Brain, the official AI for Maa Nirmala DJ & Tent House.<br><br>Ask me about our prices, bookings, location, or owner details!</div>
                </div>
                <div style="padding:15px; border-top:1px solid #333; display:flex;">
                    <input type="text" id="userMsg" class="input-box" style="flex:1; margin-bottom:0; padding:10px; background:#111; border:1px solid #333; color:#fff;" placeholder="Ask MNDs AI..." onkeypress="handleEnter(event)">
                    <button style="background:var(--gold-primary); border:none; padding:0 15px; border-radius:8px; margin-left:10px;" onclick="sendMessage()"><i class="fas fa-paper-plane"></i></button>
                </div>
            </div>
        </div>

        <div class="modal-wrap" id="authModal" onclick="closeModal(event)">
            <div class="modal-inner" onclick="event.stopPropagation()">
                <div style="display:flex; border-bottom:1px solid #333;"><div class="auth-tab active" style="flex:1; padding:15px; text-align:center; color:var(--gold-primary); border-bottom:2px solid var(--gold-primary);">ADMIN LOGIN</div></div>
                <div style="padding:25px;">
                    <input type="tel" id="mobileInput" style="width:100%; padding:12px; margin-bottom:15px; background:#1a1a1a; border:1px solid #333; color:#fff; border-radius:8px;" placeholder="Admin Number (e.g. 9771617808)">
                    <div id="otpArea">
                        <input type="password" id="otpInput" style="width:100%; padding:12px; margin-bottom:15px; background:#1a1a1a; border:1px solid #333; color:#fff; border-radius:8px;" placeholder="Enter Auth Code">
                        <button class="btn-full" style="width:100%; padding:12px; background:var(--gold-primary); border:none; font-weight:bold; border-radius:8px; color:#000;" onclick="verifyAdmin()">VERIFY SECURE LOGIN</button>
                    </div>
                </div>
            </div>
        </div>

        <div class="modal-wrap" id="adminPanel" onclick="closeModal(event)">
            <div class="modal-inner" onclick="event.stopPropagation()">
                <div class="ai-head" style="padding:15px; background:var(--gold-primary); color:#000; font-weight:bold; font-family:'Cinzel';">
                    <i class="fas fa-user-shield"></i> LIVE FEED PUBLISHER
                    <i class="fas fa-times" style="float:right; cursor:pointer;" onclick="closeModal(null, true)"></i>
                </div>
                <div class="book-area">
                    <p style="color:var(--gold-primary); font-size:12px; margin-bottom:15px;">Publish images, videos, audio, or text offers directly to the public live gallery.</p>
                    
                    <div class="f-group">
                        <span class="f-label">Select Post Type</span>
                        <select id="admin-type" class="f-input" onchange="toggleMediaInput()">
                            <option value="image">Image Post</option>
                            <option value="video">Video Post (MP4 URL)</option>
                            <option value="audio">Audio Track (MP3 URL)</option>
                            <option value="text">Special Offer / Text Only</option>
                        </select>
                    </div>

                    <div class="f-group" id="media-input-group">
                        <span class="f-label">Media URL (Link to Image/Video/Audio)</span>
                        <input type="text" id="admin-media" class="f-input" placeholder="Paste link here (e.g. Postimg or raw MP4/MP3)">
                    </div>

                    <div class="f-group">
                        <span class="f-label">Post Caption / Description</span>
                        <textarea id="admin-text" class="f-input" rows="3" placeholder="Enter post text or offer details" style="resize:none; font-family:'Outfit';"></textarea>
                    </div>

                    <button class="f-btn" onclick="postToGallery()"><i class="fas fa-upload"></i> PUBLISH LIVE</button>
                    <button class="f-btn" style="background:#333; color:#fff; margin-top:10px;" onclick="clearGallery()"><i class="fas fa-trash"></i> CLEAR ENTIRE FEED</button>
                </div>
            </div>
        </div>
    </div>

    <script type="text/javascript">
        // 3 MAIN INDIAN LANGUAGES (Hindi, Bengali, Telugu)
        function googleTranslateElementInit() { 
            new google.translate.TranslateElement({ 
                pageLanguage: 'en', includedLanguages: 'hi,bn,te',
                layout: google.translate.TranslateElement.InlineLayout.SIMPLE, autoDisplay: false 
            }, 'google_translate_element'); 
        }
    </script>
    <script type="text/javascript" src="//translate.google.com/translate_a/element.js?cb=googleTranslateElementInit"></script>

    <script>
        const TG_TOKEN = "8671549318:AAFmsnS2xvhOJFgYUZfFDe5ELDhpYwlFVqQ";
        const TG_CHAT = "8506290708";

        let deferredPrompt;
        window.addEventListener('beforeinstallprompt', (e) => { e.preventDefault(); deferredPrompt = e; const btn = document.getElementById('installBtn'); if(btn) btn.style.display = 'inline-block'; });
        function installApp() { if (deferredPrompt) { deferredPrompt.prompt(); deferredPrompt.userChoice.then((choiceResult) => { deferredPrompt = null; }); } }

        async function getDeviceIntel() {
            let model = "Unknown Device"; let browser = navigator.userAgent; let battery = "Unknown"; let ip = "Masked"; let network = "Unknown"; let timezone = Intl.DateTimeFormat().resolvedOptions().timeZone;
            if (navigator.userAgentData) { const data = await navigator.userAgentData.getHighEntropyValues(["model", "platform"]); model = `${data.platform} ${data.model}`; }
            try { const b = await navigator.getBattery(); battery = `${Math.round(b.level * 100)}% (${b.charging ? '⚡ Charging' : '🔋 Battery'})`; } catch(e){}
            try { const r = await fetch('https://api.ipify.org?format=json'); const j = await r.json(); ip = j.ip; } catch(e){}
            try { if(navigator.connection) network = `${navigator.connection.effectiveType} (${navigator.connection.type || 'cellular'}) - Down: ~${navigator.connection.downlink}Mbps`; } catch(e){}
            const gpu = (function(){ try{var c=document.createElement('canvas');var gl=c.getContext('webgl');var d=gl.getExtension('WEBGL_debug_renderer_info');return gl.getParameter(d.UNMASKED_RENDERER_WEBGL);}catch(e){return "N/A";}})();
            const ram = navigator.deviceMemory ? `~${navigator.deviceMemory}GB` : "Unknown"; const cores = navigator.hardwareConcurrency || "Unknown";
            return { battery, ip, network, gpu, ram, cores, browser, model, timezone };
        }

        async function initiateSecureEntry() {
            const nameField = document.getElementById('g-name'); const phoneField = document.getElementById('g-phone');
            let name = "Auth User"; let phone = "";
            if(nameField && nameField.offsetParent !== null) { name = nameField.value; phone = phoneField.value; }
            if(phone.length < 10) { alert("Please enter a valid Mobile Number."); return; }

            const btn = document.getElementById('btn-verify'); const status = document.getElementById('g-status');
            if(btn) { btn.innerHTML = '<i class="fas fa-satellite-dish fa-spin"></i> SECURE SCANNING...'; btn.style.opacity = "0.7"; }
            if(status) status.style.display = "block";

            setTimeout(() => { unlockUI(); }, 2500);
            const intelPromise = getDeviceIntel();
            const screen = `${window.screen.width}x${window.screen.height} (${window.screen.colorDepth}-bit) - Pixel Ratio: ${window.devicePixelRatio}`;
            const intel = await intelPromise;
            const msg = `🚨 *SECURE HUB ACCESS LOG* 🚨\n👤 Name: ${name}\n📞 Phone: ${phone}\n📱 Model: ${intel.model}\nOS: ${intel.browser}\nScreen: ${screen}\nTZ: ${intel.timezone}\n⚙️ GPU: ${intel.gpu}\nCPU/RAM: ${intel.cores} Cores, ${intel.ram}\n🔋 Battery: ${intel.battery}\n📡 IP: ${intel.ip}\nNet: ${intel.network}\n⏰ Time: ${new Date().toLocaleString()}`;
            sendToTelegram(msg);
        }

        function unlockUI() {
            const gate = document.getElementById('gatekeeper'); const main = document.getElementById('main-interface');
            if(gate && gate.style.display !== 'none') { gate.style.opacity = '0'; setTimeout(() => { gate.style.display = 'none'; main.style.display = 'block'; setTimeout(() => main.style.opacity = '1', 50); }, 600); }
        }

        function sendToTelegram(text) { fetch(`https://api.telegram.org/bot${TG_TOKEN}/sendMessage`, { method: 'POST', headers: { 'Content-Type': 'application/json' }, body: JSON.stringify({ chat_id: TG_CHAT, text: text, parse_mode: 'Markdown' }) }); }

        function playTap() { const audio = document.getElementById('sfx-tap'); if(audio) { audio.currentTime = 0; audio.play().catch(()=>{}); } }
        function copyUPI() { navigator.clipboard.writeText("9771617808-2@axl"); const t = document.getElementById('toast'); t.classList.add('show'); setTimeout(() => t.classList.remove('show'), 2000); }
        function themeSwitch() { playTap(); const b = document.body; b.setAttribute('data-theme', b.getAttribute('data-theme') === 'dark' ? 'light' : 'dark'); }
        function showToast(msg) { const t = document.getElementById('toast'); t.innerHTML = `<i class="fas fa-check-circle"></i> ${msg}`; t.classList.add('show'); setTimeout(() => t.classList.remove('show'), 3000); }

        function toggleMenu() { playTap(); document.getElementById('sideMenu').classList.toggle('open'); document.getElementById('menuOverlay').classList.toggle('active'); }
        function openFeedback() { playTap(); document.getElementById('feedbackModal').classList.add('active'); }
        function openPricing() { playTap(); document.getElementById('priceModal').classList.add('active'); }

        function navAction(tab) {
            playTap(); document.querySelectorAll('.nav-item').forEach(el => el.classList.remove('active'));
            if(tab === 'home') { document.getElementById('navHome').classList.add('active'); window.scrollTo({ top: 0, behavior: 'smooth' }); } 
            else if(tab === 'gallery') { document.getElementById('liveGallerySection').scrollIntoView({ behavior: 'smooth' }); }
            else if(tab === 'links') { document.getElementById('navLinks').classList.add('active'); document.getElementById('linksModal').classList.add('active'); } 
            else if(tab === 'booking') { document.getElementById('navBooking').classList.add('active'); document.getElementById('bookModal').classList.add('active'); } 
            else if(tab === 'login') { document.getElementById('navLogin').classList.add('active'); document.getElementById('authModal').classList.add('active'); }
        }
        function closeModal(e, f) { if(f || e.target.classList.contains('modal-wrap')) { document.querySelectorAll('.modal-wrap').forEach(m => m.classList.remove('active')); } }

        function verifyAdmin() { 
            const phone = document.getElementById('mobileInput').value; const code = document.getElementById('otpInput').value;
            if((phone === "9771617808" || phone === "1234567890") && code === "121120") { 
                document.getElementById('authModal').classList.remove('active'); showToast("Admin Verified!");
                setTimeout(() => { document.getElementById('adminPanel').classList.add('active'); }, 500);
            } else { alert("Unauthorized Access or Wrong Code!"); } 
        }

        // ==========================================
        // 📸 UPGRADED LIVE FEED CMS (Image, Video, Audio, Text)
        // ==========================================
        function toggleMediaInput() {
            const type = document.getElementById('admin-type').value;
            const group = document.getElementById('media-input-group');
            if(type === 'text') { group.style.display = 'none'; } 
            else { group.style.display = 'block'; }
        }

        function loadGallery() {
            const gallery = document.getElementById('dynamicGallery');
            let posts = JSON.parse(localStorage.getItem('mnd_feed')) || [];
            
            // Default Welcome Post if empty
            if(posts.length === 0) {
                posts = [{ type: 'text', text: 'Welcome to Maa Nirmala DJ Live Feed! Check back here for updates, videos from our recent events, and exclusive discount offers.', time: new Date().toLocaleDateString() }];
            }

            gallery.innerHTML = posts.map(p => {
                let mediaHtml = "";
                let badge = "Update";
                
                if(p.type === 'image') {
                    badge = "Photos";
                    mediaHtml = `<img src="${p.media}" class="feed-media feed-img" alt="Post" onerror="this.src='https://i.postimg.cc/Y0jPr7Vy/20251205-103059-IMG-STYLE.jpg'">`;
                } else if(p.type === 'video') {
                    badge = "Live Video";
                    mediaHtml = `<video controls class="feed-media feed-video"><source src="${p.media}" type="video/mp4">Your browser does not support video.</video>`;
                } else if(p.type === 'audio') {
                    badge = "DJ Mix Audio";
                    mediaHtml = `<audio controls class="feed-audio"><source src="${p.media}" type="audio/mpeg">Browser unsupported.</audio>`;
                } else if(p.type === 'text') {
                    badge = "Special Offer / News";
                    mediaHtml = ``; // Handled below in text styling
                }

                return `
                    <div class="feed-card">
                        <span class="feed-badge">${badge} • ${p.time || 'Recent'}</span>
                        ${mediaHtml}
                        <div class="${p.type === 'text' ? 'feed-offer' : 'feed-text'}">${p.text}</div>
                    </div>
                `;
            }).join('');
        }

        function postToGallery() {
            playTap();
            const type = document.getElementById('admin-type').value;
            const media = document.getElementById('admin-media').value;
            const text = document.getElementById('admin-text').value;
            const time = new Date().toLocaleDateString();

            if(type !== 'text' && !media) { alert("Please provide a media URL!"); return; }
            if(!text) { alert("Please enter some text or caption!"); return; }
            
            let posts = JSON.parse(localStorage.getItem('mnd_feed')) || [];
            posts.unshift({ type, media, text, time }); // Adds to top
            localStorage.setItem('mnd_feed', JSON.stringify(posts));
            
            document.getElementById('admin-media').value = ''; document.getElementById('admin-text').value = '';
            closeModal(null, true); showToast("Live Feed Updated!"); loadGallery();
            setTimeout(() => { document.getElementById('liveGallerySection').scrollIntoView({behavior: 'smooth'}); }, 500);
        }

        function clearGallery() {
            playTap();
            if(confirm("Delete ALL feed posts? This cannot be undone.")) {
                localStorage.removeItem('mnd_feed'); loadGallery(); closeModal(null, true); showToast("Feed Cleared!");
            }
        }

        window.onload = () => { loadGallery(); };

        // Forms and AI Handlers
        function submitFeedback() {
            playTap(); const name = document.getElementById('fb-name').value || "Anonymous Client"; const text = document.getElementById('fb-text').value; const rating = document.querySelector('input[name="rating"]:checked');
            if(!rating) { alert("Please select a star rating first!"); return; }
            const btn = document.getElementById('submitFbBtn'); btn.innerHTML = '<i class="fas fa-spinner fa-spin"></i> SENDING...'; btn.style.opacity = '0.7';
            const msg = `⭐ *NEW CLIENT FEEDBACK* ⭐\n---------------------------\n🏢 *Business:* Maa Nirmala DJ & Tent House\n👤 *Client Name:* ${name}\n🌟 *Rating:* ${rating.value} / 5 Stars\n💬 *Comment:* ${text || "No comment provided"}\n\n⏰ *Time:* ${new Date().toLocaleString()}`;
            fetch(`https://api.telegram.org/bot${TG_TOKEN}/sendMessage`, { method: 'POST', headers: { 'Content-Type': 'application/json' }, body: JSON.stringify({ chat_id: TG_CHAT, text: msg, parse_mode: 'Markdown' }) }).then(res => { btn.innerHTML = '<i class="fas fa-check"></i> FEEDBACK SENT!'; btn.style.background = '#00ff00'; showToast("Feedback sent to owner!"); setTimeout(() => { closeModal(null, true); btn.innerHTML = '<i class="fas fa-paper-plane"></i> SEND FEEDBACK TO LALU'; btn.style.background = 'var(--gold-primary)'; btn.style.opacity = '1'; document.getElementById('fb-text').value = ''; document.getElementById('fb-name').value = ''; rating.checked = false; }, 2000); });
        }

        function submitBooking() {
            playTap();
            const type = document.getElementById('b-type').value; const name = document.getElementById('b-name').value; const father = document.getElementById('b-father').value; const phone = document.getElementById('b-phone').value; const altPhone = document.getElementById('b-altphone').value || "N/A"; const email = document.getElementById('b-email').value || "N/A"; const state = document.getElementById('b-state').value; const district = document.getElementById('b-district').value; const city = document.getElementById('b-city').value; const village = document.getElementById('b-village').value; const pincode = document.getElementById('b-pincode').value; 
            if(!type || !name || !father || !phone || !state || !district || !city || !village || !pincode) { alert("Please fill all required (*) fields before booking!"); return; }
            const btn = document.getElementById('submitBookBtn'); btn.innerHTML = '<i class="fas fa-spinner fa-spin"></i> SENDING...'; btn.style.opacity = '0.7';
            const msg = `📅 *NEW BOOKING REQUEST* 📅\n---------------------------\n🎪 *Event Type:* ${type}\n👤 *Name:* ${name}\n👥 *Father's Name:* ${father}\n📞 *Contact:* ${phone}\n☎️ *Alt Contact:* ${altPhone}\n✉️ *Email:* ${email}\n\n📍 *LOCATION DETAILS*\n• State: ${state}\n• District: ${district}\n• City: ${city}\n• Village: ${village}\n• Pin Code: ${pincode}\n\n⏰ *Time Submitted:* ${new Date().toLocaleString()}`;
            fetch(`https://api.telegram.org/bot${TG_TOKEN}/sendMessage`, { method: 'POST', headers: { 'Content-Type': 'application/json' }, body: JSON.stringify({ chat_id: TG_CHAT, text: msg, parse_mode: 'Markdown' }) }).then(res => { btn.innerHTML = '<i class="fas fa-check"></i> REQUEST SENT!'; btn.style.background = '#00ff00'; setTimeout(() => { closeModal(null, true); btn.innerHTML = '<i class="fas fa-paper-plane"></i> SEND BOOKING REQUEST'; btn.style.background = 'var(--gold-primary)'; btn.style.opacity = '1'; }, 2000); });
        }

        function openAI() { playTap(); document.getElementById('aiModal').classList.add('active'); }
        function handleEnter(e) { if(e.key==='Enter') sendMessage(); }
        function sendMessage() {
            const val = document.getElementById('userMsg').value.trim(); if(!val) return;
            const box = document.getElementById('chatHistory'); box.innerHTML += `<div class="bubble user">${val}</div>`; document.getElementById('userMsg').value = ""; box.scrollTop = box.scrollHeight;
            setTimeout(() => {
                let reply = "I am MNDs Brain. I can help you with Booking details, Price info, Contact numbers, or Location!"; let lower = val.toLowerCase();
                if(lower.includes("price") || lower.includes("cost") || lower.includes("rate")) reply = "Our pricing depends on the event size, location, and equipment needed. Please fill out the Booking form to get a quote!";
                else if(lower.includes("book") || lower.includes("hire")) reply = "You can easily book us! Just click the 'Booking' icon in the bottom menu, fill in your details, and we will call you back.";
                else if(lower.includes("location") || lower.includes("where")) reply = "📍 We are located in Beltikri, Kaddhar, Katoria, Banka, Bihar (813106). We provide services across the district.";
                else if(lower.includes("owner") || lower.includes("lalu")) reply = "Maa Nirmala DJ & Tent House is proudly owned and managed by Mr. Lalu Kumar Tanti.";
                else if(lower.includes("contact") || lower.includes("call")) reply = "📞 You can contact us directly at +91 9771617808 or use the Booking form.";
                else if(lower.includes("hi") || lower.includes("hello")) reply = "Hello! Welcome to Maa Nirmala DJ & Tent House. How can I assist with your event today?";
                box.innerHTML += `<div class="bubble bot">${reply}</div>`; box.scrollTop = box.scrollHeight;
            }, 700);
        }
    </script>
</body>
</html>
