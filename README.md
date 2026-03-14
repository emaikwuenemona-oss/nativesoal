<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Nativesoal Fashion Academy – Warri, Delta State</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,700;0,900;1,400&family=Cormorant+Garamond:wght@300;400;600&family=Montserrat:wght@300;400;600;700&display=swap" rel="stylesheet">
<style>
  :root {
    --gold: #C9A84C;
    --gold-light: #E8C97A;
    --dark: #0D0B08;
    --cream: #F5EFE0;
    --warm: #2A1F14;
    --accent: #8B3A3A;
    --white: #FEFCF8;
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  html { scroll-behavior: smooth; }

  body {
    font-family: 'Montserrat', sans-serif;
    background: var(--dark);
    color: var(--cream);
    overflow-x: hidden;
  }

  /* ── NAV ── */
  nav {
    position: fixed; top: 0; width: 100%; z-index: 1000;
    background: rgba(13,11,8,0.92);
    backdrop-filter: blur(12px);
    border-bottom: 1px solid rgba(201,168,76,0.2);
    display: flex; align-items: center; justify-content: space-between;
    padding: 0 5%;
    height: 70px;
  }
  .nav-logo {
    font-family: 'Playfair Display', serif;
    font-size: 1.3rem; font-weight: 900;
    color: var(--gold);
    letter-spacing: 2px;
    text-transform: uppercase;
  }
  .nav-logo span { color: var(--white); font-weight: 300; }
  .nav-links { display: flex; gap: 2rem; list-style: none; }
  .nav-links a {
    color: var(--cream); text-decoration: none;
    font-size: 0.78rem; letter-spacing: 1.5px; text-transform: uppercase;
    transition: color 0.3s;
  }
  .nav-links a:hover { color: var(--gold); }
  .nav-cta {
    background: var(--gold);
    color: var(--dark) !important;
    padding: 8px 20px;
    font-weight: 700 !important;
    transition: background 0.3s !important;
  }
  .nav-cta:hover { background: var(--gold-light) !important; color: var(--dark) !important; }

  /* ── HERO ── */
  #hero {
    min-height: 100vh;
    background: linear-gradient(135deg, #0D0B08 0%, #1a0f0a 50%, #0D0B08 100%);
    display: flex; align-items: center; justify-content: center;
    text-align: center;
    padding: 100px 5% 60px;
    position: relative;
    overflow: hidden;
  }
  .hero-bg-pattern {
    position: absolute; inset: 0;
    background-image:
      repeating-linear-gradient(45deg, rgba(201,168,76,0.03) 0px, rgba(201,168,76,0.03) 1px, transparent 1px, transparent 60px),
      repeating-linear-gradient(-45deg, rgba(201,168,76,0.03) 0px, rgba(201,168,76,0.03) 1px, transparent 1px, transparent 60px);
    animation: patternShift 20s linear infinite;
  }
  @keyframes patternShift { from { background-position: 0 0; } to { background-position: 60px 60px; } }

  .hero-badge {
    display: inline-block;
    border: 1px solid var(--gold);
    color: var(--gold);
    font-size: 0.7rem; letter-spacing: 3px; text-transform: uppercase;
    padding: 6px 18px; margin-bottom: 2rem;
    animation: fadeInUp 0.8s ease both;
  }
  .hero-title {
    font-family: 'Playfair Display', serif;
    font-size: clamp(2.8rem, 7vw, 6rem);
    font-weight: 900; line-height: 1.05;
    color: var(--white);
    margin-bottom: 1rem;
    animation: fadeInUp 0.8s ease 0.15s both;
  }
  .hero-title .accent { color: var(--gold); font-style: italic; }
  .hero-sub {
    font-family: 'Cormorant Garamond', serif;
    font-size: clamp(1.1rem, 2.5vw, 1.6rem);
    color: rgba(245,239,224,0.7);
    margin-bottom: 2.5rem;
    animation: fadeInUp 0.8s ease 0.3s both;
  }
  .hero-location {
    font-size: 0.75rem; letter-spacing: 2px; text-transform: uppercase;
    color: var(--gold-light); margin-bottom: 3rem;
    animation: fadeInUp 0.8s ease 0.45s both;
  }
  .hero-btns { display: flex; gap: 1rem; justify-content: center; flex-wrap: wrap; animation: fadeInUp 0.8s ease 0.6s both; }
  .btn-primary {
    background: var(--gold); color: var(--dark);
    padding: 14px 36px; font-weight: 700; font-size: 0.85rem;
    letter-spacing: 1.5px; text-transform: uppercase;
    border: none; cursor: pointer;
    transition: all 0.3s; text-decoration: none; display: inline-block;
  }
  .btn-primary:hover { background: var(--gold-light); transform: translateY(-2px); box-shadow: 0 8px 25px rgba(201,168,76,0.4); }
  .btn-outline {
    background: transparent; color: var(--cream);
    padding: 14px 36px; font-weight: 600; font-size: 0.85rem;
    letter-spacing: 1.5px; text-transform: uppercase;
    border: 1px solid rgba(245,239,224,0.4); cursor: pointer;
    transition: all 0.3s; text-decoration: none; display: inline-block;
  }
  .btn-outline:hover { border-color: var(--gold); color: var(--gold); transform: translateY(-2px); }

  @keyframes fadeInUp {
    from { opacity: 0; transform: translateY(30px); }
    to { opacity: 1; transform: translateY(0); }
  }

  /* ── STATS ── */
  .stats-bar {
    background: var(--gold);
    display: flex; justify-content: center; gap: 0;
    flex-wrap: wrap;
  }
  .stat-item {
    padding: 1.5rem 3rem;
    text-align: center; color: var(--dark);
    border-right: 1px solid rgba(13,11,8,0.2);
  }
  .stat-item:last-child { border-right: none; }
  .stat-num { font-family: 'Playfair Display', serif; font-size: 2rem; font-weight: 900; }
  .stat-label { font-size: 0.7rem; letter-spacing: 2px; text-transform: uppercase; margin-top: 2px; opacity: 0.7; }

  /* ── SECTION COMMON ── */
  section { padding: 90px 5%; }
  .section-label {
    font-size: 0.7rem; letter-spacing: 4px; text-transform: uppercase;
    color: var(--gold); margin-bottom: 1rem;
  }
  .section-title {
    font-family: 'Playfair Display', serif;
    font-size: clamp(2rem, 4vw, 3.2rem);
    font-weight: 900; line-height: 1.1;
    margin-bottom: 1.2rem;
  }
  .section-sub {
    font-family: 'Cormorant Garamond', serif;
    font-size: 1.15rem; color: rgba(245,239,224,0.65);
    max-width: 560px; line-height: 1.7;
  }
  .center { text-align: center; }
  .center .section-sub { margin: 0 auto; }

  /* ── ABOUT ── */
  #about { background: var(--warm); }
  .about-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 5rem; align-items: center; max-width: 1100px; margin: 0 auto; }
  .about-img-wrap {
    position: relative;
  }
  .about-img-placeholder {
    width: 100%; height: 420px;
    background: linear-gradient(135deg, #2A1F14, #1a0f0a);
    display: flex; align-items: center; justify-content: center;
    font-size: 5rem;
    border: 1px solid rgba(201,168,76,0.3);
    position: relative; overflow: hidden;
  }
  .about-img-placeholder::after {
    content: '';
    position: absolute; inset: 0;
    background: repeating-linear-gradient(45deg, transparent, transparent 20px, rgba(201,168,76,0.03) 20px, rgba(201,168,76,0.03) 21px);
  }
  .about-tag {
    position: absolute; bottom: -1rem; right: -1rem;
    background: var(--gold); color: var(--dark);
    padding: 1rem 1.5rem; font-weight: 700; font-size: 0.8rem;
    letter-spacing: 1px; text-transform: uppercase;
  }
  .about-features { margin-top: 2rem; display: flex; flex-direction: column; gap: 1rem; }
  .about-feature { display: flex; gap: 1rem; align-items: flex-start; }
  .feat-icon { color: var(--gold); font-size: 1.2rem; flex-shrink: 0; margin-top: 2px; }
  .feat-title { font-weight: 700; font-size: 0.9rem; margin-bottom: 2px; }
  .feat-desc { font-size: 0.82rem; color: rgba(245,239,224,0.6); line-height: 1.5; }

  /* ── COURSES ── */
  #courses { background: var(--dark); }
  .courses-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 1.5rem; margin-top: 3rem; }
  .course-card {
    background: var(--warm);
    border: 1px solid rgba(201,168,76,0.15);
    padding: 2rem; transition: all 0.3s;
    position: relative; overflow: hidden;
  }
  .course-card::before {
    content: ''; position: absolute; top: 0; left: 0; right: 0; height: 3px;
    background: var(--gold); transform: scaleX(0); transform-origin: left;
    transition: transform 0.3s;
  }
  .course-card:hover::before { transform: scaleX(1); }
  .course-card:hover { transform: translateY(-5px); border-color: rgba(201,168,76,0.4); }
  .course-icon { font-size: 2.5rem; margin-bottom: 1rem; }
  .course-level {
    font-size: 0.65rem; letter-spacing: 2px; text-transform: uppercase;
    color: var(--gold); margin-bottom: 0.5rem;
  }
  .course-name { font-family: 'Playfair Display', serif; font-size: 1.3rem; font-weight: 700; margin-bottom: 0.8rem; }
  .course-desc { font-size: 0.82rem; color: rgba(245,239,224,0.6); line-height: 1.6; margin-bottom: 1.2rem; }
  .course-duration { font-size: 0.75rem; color: var(--gold-light); font-weight: 600; }

  /* ── TUTORIALS / VIDEOS ── */
  #tutorials { background: #120e0a; }
  .videos-grid { display: grid; grid-template-columns: repeat(2, 1fr); gap: 1.5rem; margin-top: 3rem; max-width: 1000px; margin-left: auto; margin-right: auto; }
  .video-card {
    background: var(--warm);
    border: 1px solid rgba(201,168,76,0.15);
    overflow: hidden; transition: all 0.3s;
  }
  .video-card:hover { transform: translateY(-4px); border-color: rgba(201,168,76,0.4); }
  .video-embed {
    position: relative; padding-top: 56.25%; /* 16:9 */
    background: #0a0806;
  }
  .video-embed iframe {
    position: absolute; top: 0; left: 0; width: 100%; height: 100%;
    border: none;
  }
  .video-info { padding: 1.2rem; }
  .video-tag {
    font-size: 0.65rem; letter-spacing: 2px; text-transform: uppercase;
    color: var(--gold); margin-bottom: 0.4rem;
  }
  .video-title { font-family: 'Playfair Display', serif; font-size: 1rem; font-weight: 700; margin-bottom: 0.4rem; }
  .video-desc { font-size: 0.78rem; color: rgba(245,239,224,0.55); line-height: 1.5; }

  /* ── REGISTER ── */
  #register { background: var(--warm); }
  .register-wrap { display: grid; grid-template-columns: 1fr 1.6fr; gap: 5rem; align-items: start; max-width: 1100px; margin: 0 auto; }
  .register-info h2 { margin-bottom: 1rem; }
  .register-info .section-sub { margin-bottom: 2rem; }
  .contact-list { list-style: none; display: flex; flex-direction: column; gap: 0.9rem; }
  .contact-item { display: flex; gap: 0.8rem; align-items: center; font-size: 0.85rem; }
  .contact-icon { color: var(--gold); font-size: 1rem; }

  .reg-form {
    background: rgba(13,11,8,0.6);
    border: 1px solid rgba(201,168,76,0.2);
    padding: 2.5rem;
  }
  .form-title { font-family: 'Playfair Display', serif; font-size: 1.4rem; font-weight: 700; margin-bottom: 1.5rem; }
  .form-row { display: grid; grid-template-columns: 1fr 1fr; gap: 1rem; }
  .form-group { margin-bottom: 1.1rem; }
  .form-group label {
    display: block; font-size: 0.72rem; letter-spacing: 1.5px; text-transform: uppercase;
    color: rgba(245,239,224,0.6); margin-bottom: 0.4rem;
  }
  .form-group input, .form-group select, .form-group textarea {
    width: 100%; background: rgba(245,239,224,0.06);
    border: 1px solid rgba(245,239,224,0.15);
    color: var(--cream); padding: 0.75rem 1rem;
    font-family: 'Montserrat', sans-serif; font-size: 0.85rem;
    outline: none; transition: border-color 0.3s;
  }
  .form-group input:focus, .form-group select:focus, .form-group textarea:focus {
    border-color: var(--gold);
  }
  .form-group select option { background: var(--dark); }
  .form-group textarea { resize: vertical; min-height: 90px; }
  .form-submit {
    width: 100%; background: var(--gold); color: var(--dark);
    border: none; padding: 1rem; font-family: 'Montserrat', sans-serif;
    font-size: 0.85rem; font-weight: 700; letter-spacing: 2px;
    text-transform: uppercase; cursor: pointer; transition: all 0.3s;
    margin-top: 0.5rem;
  }
  .form-submit:hover { background: var(--gold-light); }

  /* ── DASHBOARD ── */
  #dashboard { background: var(--dark); }
  .dashboard-wrap { max-width: 1100px; margin: 0 auto; }
  .dash-controls { display: flex; gap: 1rem; margin: 2rem 0 1.5rem; flex-wrap: wrap; align-items: center; }
  .dash-search {
    flex: 1; min-width: 200px;
    background: var(--warm); border: 1px solid rgba(201,168,76,0.2);
    color: var(--cream); padding: 0.6rem 1rem;
    font-family: 'Montserrat', sans-serif; font-size: 0.85rem; outline: none;
  }
  .dash-search:focus { border-color: var(--gold); }
  .dash-filter {
    background: var(--warm); border: 1px solid rgba(201,168,76,0.2);
    color: var(--cream); padding: 0.6rem 1rem;
    font-family: 'Montserrat', sans-serif; font-size: 0.82rem; outline: none; cursor: pointer;
  }
  .dash-filter option { background: var(--dark); }
  .table-wrap { overflow-x: auto; }
  table { width: 100%; border-collapse: collapse; font-size: 0.82rem; }
  thead tr { background: var(--gold); color: var(--dark); }
  thead th { padding: 0.9rem 1rem; text-align: left; font-size: 0.7rem; letter-spacing: 2px; text-transform: uppercase; font-weight: 700; }
  tbody tr { border-bottom: 1px solid rgba(245,239,224,0.06); transition: background 0.2s; }
  tbody tr:hover { background: rgba(201,168,76,0.06); }
  tbody td { padding: 0.85rem 1rem; color: rgba(245,239,224,0.8); }
  .badge {
    display: inline-block; padding: 2px 10px;
    font-size: 0.65rem; letter-spacing: 1px; text-transform: uppercase; font-weight: 700;
    border-radius: 2px;
  }
  .badge-new { background: rgba(201,168,76,0.2); color: var(--gold-light); }
  .badge-active { background: rgba(50,150,80,0.2); color: #6fcf97; }
  .badge-completed { background: rgba(100,100,200,0.2); color: #a0a0ff; }
  .dash-empty { text-align: center; padding: 3rem; color: rgba(245,239,224,0.3); font-style: italic; }

  /* ── FOOTER ── */
  footer {
    background: #080604;
    border-top: 1px solid rgba(201,168,76,0.15);
    padding: 3rem 5% 2rem;
  }
  .footer-grid { display: grid; grid-template-columns: 2fr 1fr 1fr; gap: 3rem; margin-bottom: 2.5rem; }
  .footer-brand { font-family: 'Playfair Display', serif; font-size: 1.4rem; font-weight: 900; color: var(--gold); margin-bottom: 0.8rem; }
  .footer-tagline { font-family: 'Cormorant Garamond', serif; font-size: 1rem; color: rgba(245,239,224,0.5); line-height: 1.6; }
  .footer-col h4 { font-size: 0.7rem; letter-spacing: 3px; text-transform: uppercase; color: var(--gold); margin-bottom: 1rem; }
  .footer-col ul { list-style: none; display: flex; flex-direction: column; gap: 0.5rem; }
  .footer-col ul a { color: rgba(245,239,224,0.55); text-decoration: none; font-size: 0.82rem; transition: color 0.3s; }
  .footer-col ul a:hover { color: var(--gold); }
  .footer-bottom { border-top: 1px solid rgba(245,239,224,0.07); padding-top: 1.5rem; display: flex; justify-content: space-between; align-items: center; flex-wrap: gap; }
  .footer-copy { font-size: 0.75rem; color: rgba(245,239,224,0.3); }

  /* ── MODAL ── */
  .modal-overlay {
    display: none; position: fixed; inset: 0;
    background: rgba(0,0,0,0.85); z-index: 2000;
    align-items: center; justify-content: center;
    backdrop-filter: blur(6px);
  }
  .modal-overlay.active { display: flex; }
  .modal-box {
    background: var(--warm); border: 1px solid var(--gold);
    padding: 3rem; max-width: 440px; width: 90%; text-align: center;
    animation: fadeInUp 0.4s ease;
  }
  .modal-icon { font-size: 3rem; margin-bottom: 1rem; }
  .modal-title { font-family: 'Playfair Display', serif; font-size: 1.6rem; font-weight: 900; color: var(--gold); margin-bottom: 0.8rem; }
  .modal-msg { color: rgba(245,239,224,0.7); margin-bottom: 1.5rem; font-size: 0.9rem; line-height: 1.6; }
  .modal-id { font-family: 'Playfair Display', serif; font-size: 1.1rem; color: var(--gold-light); font-weight: 700; margin-bottom: 1.5rem; }
  .modal-close { background: var(--gold); color: var(--dark); border: none; padding: 0.8rem 2.5rem; font-family: 'Montserrat', sans-serif; font-weight: 700; letter-spacing: 2px; text-transform: uppercase; cursor: pointer; font-size: 0.82rem; }

  /* ── RESPONSIVE ── */
  @media (max-width: 768px) {
    .about-grid, .register-wrap, .footer-grid { grid-template-columns: 1fr; gap: 2.5rem; }
    .form-row { grid-template-columns: 1fr; }
    .nav-links { display: none; }
    .footer-grid { grid-template-columns: 1fr 1fr; }
    .stat-item { padding: 1.2rem 1.5rem; }
  }
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <div class="nav-logo">Nativesoal <span>Fashion Academy</span></div>
  <ul class="nav-links">
    <li><a href="#about">About</a></li>
    <li><a href="#courses">Courses</a></li>
    <li><a href="#tutorials">Tutorials</a></li>
    <li><a href="#dashboard">Students</a></li>
    <li><a href="#register" class="nav-cta">Register Now</a></li>
  </ul>
</nav>

<!-- HERO -->
<section id="hero">
  <div class="hero-bg-pattern"></div>
  <div style="position:relative; z-index:1;">
    <div class="hero-badge">✦ Warri, Delta State · Est. 2020</div>
    <h1 class="hero-title">Where Nigerian <span class="accent">Fashion</span><br>Meets Mastery</h1>
    <p class="hero-sub">Professional sewing & fashion design training<br>rooted in African creativity</p>
    <p class="hero-location">📍 Warri, Delta State &nbsp;|&nbsp; 📞 07032444289</p>
    <div class="hero-btns">
      <a href="#register" class="btn-primary">Enroll Today</a>
      <a href="#tutorials" class="btn-outline">Watch Free Tutorials</a>
    </div>
  </div>
</section>

<!-- STATS -->
<div class="stats-bar">
  <div class="stat-item"><div class="stat-num">500+</div><div class="stat-label">Students Trained</div></div>
  <div class="stat-item"><div class="stat-num">12</div><div class="stat-label">Courses Offered</div></div>
  <div class="stat-item"><div class="stat-num">5★</div><div class="stat-label">Community Rating</div></div>
  <div class="stat-item"><div class="stat-num">100%</div><div class="stat-label">Practical Training</div></div>
</div>

<!-- ABOUT -->
<section id="about">
  <div class="about-grid">
    <div class="about-img-wrap">
      <div class="about-img-placeholder">✂️</div>
      <div class="about-tag">Est. in Warri · Delta State</div>
    </div>
    <div>
      <p class="section-label">About the Academy</p>
      <h2 class="section-title">Fashion Skills That Open Doors</h2>
      <p class="section-sub">Nativesoal Fashion Academy is Warri's leading fashion design school, equipping students with professional sewing, pattern drafting, and design skills for modern and traditional African fashion.</p>
      <div class="about-features">
        <div class="about-feature">
          <div class="feat-icon">🧵</div>
          <div><div class="feat-title">Hands-On Learning</div><div class="feat-desc">Every student gets practical machine time from day one — no passive lectures.</div></div>
        </div>
        <div class="about-feature">
          <div class="feat-icon">👗</div>
          <div><div class="feat-title">African & Contemporary Design</div><div class="feat-desc">We blend native Nigerian aesthetics with modern international fashion techniques.</div></div>
        </div>
        <div class="about-feature">
          <div class="feat-icon">🏆</div>
          <div><div class="feat-title">Career-Ready Graduates</div><div class="feat-desc">Our graduates work in top fashion houses, run their own brands, and sell globally.</div></div>
        </div>
        <div class="about-feature">
          <div class="feat-icon">📜</div>
          <div><div class="feat-title">Certified Programmes</div><div class="feat-desc">Receive an industry-recognised certificate upon completing your course.</div></div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- COURSES -->
<section id="courses">
  <div class="center">
    <p class="section-label">Our Programmes</p>
    <h2 class="section-title">Choose Your Path</h2>
    <p class="section-sub">From beginner basics to advanced couture — find the course that matches your level and ambition.</p>
  </div>
  <div class="courses-grid">
    <div class="course-card">
      <div class="course-icon">🧶</div>
      <div class="course-level">Beginner</div>
      <div class="course-name">Basic Sewing Skills</div>
      <p class="course-desc">Learn to thread machines, make straight seams, basic stitches, and complete your first simple garment.</p>
      <div class="course-duration">⏱ 4 Weeks · Part-Time Available</div>
    </div>
    <div class="course-card">
      <div class="course-icon">✂️</div>
      <div class="course-level">Intermediate</div>
      <div class="course-name">Pattern Drafting & Cutting</div>
      <p class="course-desc">Master body measurement, paper pattern creation, fabric cutting techniques for fitted garments.</p>
      <div class="course-duration">⏱ 6 Weeks · Flexible Hours</div>
    </div>
    <div class="course-card">
      <div class="course-icon">👘</div>
      <div class="course-level">Intermediate</div>
      <div class="course-name">Ankara & Native Wear</div>
      <p class="course-desc">Specialise in African print fashion — senator styles, bubu, agbada, and flowing native designs.</p>
      <div class="course-duration">⏱ 8 Weeks · Certificate Awarded</div>
    </div>
    <div class="course-card">
      <div class="course-icon">👗</div>
      <div class="course-level">Advanced</div>
      <div class="course-name">Ladies Fashion & Gowns</div>
      <p class="course-desc">Create ball gowns, fitted dresses, bridal wear, and ready-to-wear womenswear collections.</p>
      <div class="course-duration">⏱ 12 Weeks · Portfolio Included</div>
    </div>
    <div class="course-card">
      <div class="course-icon">👔</div>
      <div class="course-level">Advanced</div>
      <div class="course-name">Men's Tailoring</div>
      <p class="course-desc">Bespoke suit construction, trousers, shirts, and traditional men's attire for discerning clients.</p>
      <div class="course-duration">⏱ 10 Weeks · Professional Level</div>
    </div>
    <div class="course-card">
      <div class="course-icon">💼</div>
      <div class="course-level">Business</div>
      <div class="course-name">Fashion Entrepreneurship</div>
      <p class="course-desc">Launch and grow your fashion brand — pricing, marketing, social media, and client management.</p>
      <div class="course-duration">⏱ 4 Weeks · Business Certificate</div>
    </div>
  </div>
</section>

<!-- TUTORIALS -->
<section id="tutorials">
  <div class="center">
    <p class="section-label">Free Video Tutorials</p>
    <h2 class="section-title">Learn Before You Join</h2>
    <p class="section-sub">Explore our curated beginner sewing tutorials from YouTube — a taste of what we teach at the Academy.</p>
  </div>
  <div class="videos-grid">
    <div class="video-card">
      <div class="video-embed">
        <iframe src="https://www.youtube.com/embed/FWbLNWN2H24" title="How to use a sewing machine" allowfullscreen loading="lazy"></iframe>
      </div>
      <div class="video-info">
        <div class="video-tag">Beginner · Machine Sewing</div>
        <div class="video-title">How to Use a Sewing Machine</div>
        <p class="video-desc">A complete beginner's guide to threading, tension, and making your first seam on a sewing machine.</p>
      </div>
    </div>
    <div class="video-card">
      <div class="video-embed">
        <iframe src="https://www.youtube.com/embed/4wnXMN_Sb8w" title="How to cut and sew a simple skirt" allowfullscreen loading="lazy"></iframe>
      </div>
      <div class="video-info">
        <div class="video-tag">Beginner · Garment Making</div>
        <div class="video-title">How to Cut & Sew a Simple Skirt</div>
        <p class="video-desc">Follow along step by step to complete your first wearable skirt — from cutting fabric to the final finish.</p>
      </div>
    </div>
    <div class="video-card">
      <div class="video-embed">
        <iframe src="https://www.youtube.com/embed/gyMXo5nep44" title="Essential Sewing Tools Explained" allowfullscreen loading="lazy"></iframe>
      </div>
      <div class="video-info">
        <div class="video-tag">Tips · Tools & Setup</div>
        <div class="video-title">Essential Sewing Tools Explained</div>
        <p class="video-desc">Everything you need to set up your sewing kit — the must-have tools before your very first class.</p>
      </div>
    </div>
    <div class="video-card">
      <div class="video-embed">
        <iframe src="https://www.youtube.com/embed/WpALBUN0cuI" title="Sewing Perfectly Straight Lines" allowfullscreen loading="lazy"></iframe>
      </div>
      <div class="video-info">
        <div class="video-tag">Beginner · Technique</div>
        <div class="video-title">Sewing Perfectly Straight Lines</div>
        <p class="video-desc">Master your stitch guides and presser foot to always sew confident, clean, straight seams every time.</p>
      </div>
    </div>
  </div>
</section>

<!-- REGISTER -->
<section id="register">
  <div class="register-wrap">
    <div class="register-info">
      <p class="section-label">Enroll Now</p>
      <h2 class="section-title">Start Your Fashion Journey</h2>
      <p class="section-sub">Fill in the form to register your interest. Our team will contact you within 24 hours to confirm your place and schedule.</p>
      <ul class="contact-list" style="margin-top:2rem;">
        <li class="contact-item"><span class="contact-icon">📍</span> Warri, Delta State, Nigeria</li>
        <li class="contact-item"><span class="contact-icon">📞</span> 07032444289</li>
        <li class="contact-item"><span class="contact-icon">✉️</span> <a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="325c53465b4457415d535e5e465672555f535b5e1c515d5f">[email&#160;protected]</a></li>
        <li class="contact-item"><span class="contact-icon">🕐</span> Mon – Sat · 8:00 AM – 6:00 PM</li>
        <li class="contact-item"><span class="contact-icon">🎓</span> Flexible schedules available</li>
      </ul>
    </div>
    <div class="reg-form">
      <div class="form-title">Student Registration Form</div>
      <div class="form-row">
        <div class="form-group">
          <label>First Name *</label>
          <input type="text" id="fname" placeholder="e.g. Amaka" required>
        </div>
        <div class="form-group">
          <label>Last Name *</label>
          <input type="text" id="lname" placeholder="e.g. Okafor" required>
        </div>
      </div>
      <div class="form-group">
        <label>Email Address *</label>
        <input type="email" id="email" placeholder="your@email.com" required>
      </div>
      <div class="form-row">
        <div class="form-group">
          <label>Phone Number *</label>
          <input type="tel" id="phone" placeholder="080XXXXXXXX" required>
        </div>
        <div class="form-group">
          <label>Age</label>
          <input type="number" id="age" placeholder="e.g. 22" min="12" max="70">
        </div>
      </div>
      <div class="form-group">
        <label>Select Course *</label>
        <select id="course" required>
          <option value="">— Choose a Programme —</option>
          <option>Basic Sewing Skills (4 Weeks)</option>
          <option>Pattern Drafting & Cutting (6 Weeks)</option>
          <option>Ankara & Native Wear (8 Weeks)</option>
          <option>Ladies Fashion & Gowns (12 Weeks)</option>
          <option>Men's Tailoring (10 Weeks)</option>
          <option>Fashion Entrepreneurship (4 Weeks)</option>
        </select>
      </div>
      <div class="form-group">
        <label>Preferred Schedule</label>
        <select id="schedule">
          <option>Morning (8am – 12pm)</option>
          <option>Afternoon (1pm – 5pm)</option>
          <option>Weekend Only</option>
          <option>Full Day</option>
        </select>
      </div>
      <div class="form-group">
        <label>Previous Experience</label>
        <textarea id="experience" placeholder="Tell us a little about your sewing background (or write 'None' if you're a complete beginner)"></textarea>
      </div>
      <button class="form-submit" onclick="registerStudent()">Submit Registration ✦</button>
    </div>
  </div>
</section>

<!-- DASHBOARD -->
<section id="dashboard">
  <div class="dashboard-wrap">
    <p class="section-label">Student Dashboard</p>
    <h2 class="section-title">Registered Students</h2>
    <p class="section-sub" style="margin-bottom:0;">View all enrolled and pending students in the academy database.</p>
    <div class="dash-controls">
      <input class="dash-search" type="text" id="searchInput" placeholder="Search by name, course, or phone…" oninput="filterTable()">
      <select class="dash-filter" id="statusFilter" onchange="filterTable()">
        <option value="">All Statuses</option>
        <option value="new">New</option>
        <option value="active">Active</option>
        <option value="completed">Completed</option>
      </select>
      <select class="dash-filter" id="courseFilter" onchange="filterTable()">
        <option value="">All Courses</option>
        <option>Basic Sewing Skills</option>
        <option>Pattern Drafting</option>
        <option>Ankara & Native Wear</option>
        <option>Ladies Fashion & Gowns</option>
        <option>Men's Tailoring</option>
        <option>Fashion Entrepreneurship</option>
      </select>
    </div>
    <div class="table-wrap">
      <table id="studentTable">
        <thead>
          <tr>
            <th>ID</th>
            <th>Student Name</th>
            <th>Phone</th>
            <th>Course</th>
            <th>Schedule</th>
            <th>Status</th>
            <th>Date</th>
          </tr>
        </thead>
        <tbody id="tableBody">
          <!-- Pre-loaded sample data -->
        </tbody>
      </table>
      <div class="dash-empty" id="emptyMsg" style="display:none;">No students match your search.</div>
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <div class="footer-grid">
    <div>
      <div class="footer-brand">Nativesoal Fashion Academy</div>
      <p class="footer-tagline">Empowering creatives in Warri and across the Niger Delta with world-class fashion design education since 2020.</p>
    </div>
    <div class="footer-col">
      <h4>Quick Links</h4>
      <ul>
        <li><a href="#about">About Us</a></li>
        <li><a href="#courses">Courses</a></li>
        <li><a href="#tutorials">Free Tutorials</a></li>
        <li><a href="#register">Register</a></li>
        <li><a href="#dashboard">Student Portal</a></li>
      </ul>
    </div>
    <div class="footer-col">
      <h4>Contact</h4>
      <ul>
        <li><a href="#">📍 Warri, Delta State</a></li>
        <li><a href="tel:07032444289">📞 07032444289</a></li>
        <li><a href="/cdn-cgi/l/email-protection#ff919e8b96899a8c909e93938b9bbf98929e9693d19c9092">✉️ <span class="__cf_email__" data-cfemail="553b34213c2330263a3439392131153238343c397b363a38">[email&#160;protected]</span></a></li>
        <li><a href="#">🕐 Mon–Sat, 8am–6pm</a></li>
      </ul>
    </div>
  </div>
  <div class="footer-bottom">
    <div class="footer-copy">© 2025 Nativesoal Fashion Academy · Warri, Delta State · All rights reserved.</div>
    <div class="footer-copy">Built for 3MTT Presentation ✦</div>
  </div>
</footer>

<!-- SUCCESS MODAL -->
<div class="modal-overlay" id="successModal">
  <div class="modal-box">
    <div class="modal-icon">🎉</div>
    <div class="modal-title">Registration Successful!</div>
    <p class="modal-msg">Welcome to <strong>Nativesoal Fashion Academy</strong>. Your application has been received. We'll contact you within 24 hours.</p>
    <div class="modal-id" id="studentId"></div>
    <button class="modal-close" onclick="closeModal()">Close</button>
  </div>
</div>

<script data-cfasync="false" src="/cdn-cgi/scripts/5c5dd728/cloudflare-static/email-decode.min.js"></script><script>
  // ── SAMPLE DATA ──
  let students = [
    { id: 'NSA-0001', name: 'Chinwe Okafor', phone: '08031234567', course: 'Basic Sewing Skills', schedule: 'Morning', status: 'active', date: '2025-01-15' },
    { id: 'NSA-0002', name: 'Emeka Eze', phone: '08023456789', course: 'Men\'s Tailoring', schedule: 'Afternoon', status: 'active', date: '2025-01-22' },
    { id: 'NSA-0003', name: 'Blessing Aghedo', phone: '09012345678', course: 'Ankara & Native Wear', schedule: 'Weekend Only', status: 'completed', date: '2024-11-10' },
    { id: 'NSA-0004', name: 'Ifeoma Nwachukwu', phone: '07098765432', course: 'Ladies Fashion & Gowns', schedule: 'Full Day', status: 'new', date: '2025-02-05' },
    { id: 'NSA-0005', name: 'Rotimi Adeyemi', phone: '08055678901', course: 'Pattern Drafting', schedule: 'Morning', status: 'active', date: '2025-02-12' },
    { id: 'NSA-0006', name: 'Ngozi Okolie', phone: '08067890123', course: 'Fashion Entrepreneurship', schedule: 'Weekend Only', status: 'completed', date: '2024-12-01' },
  ];

  let idCounter = students.length + 1;

  function renderTable(data) {
    const tbody = document.getElementById('tableBody');
    const empty = document.getElementById('emptyMsg');
    if (!data.length) { tbody.innerHTML = ''; empty.style.display = 'block'; return; }
    empty.style.display = 'none';
    tbody.innerHTML = data.map(s => `
      <tr>
        <td style="color:var(--gold);font-weight:700;font-size:0.75rem;">${s.id}</td>
        <td>${s.name}</td>
        <td>${s.phone}</td>
        <td>${s.course}</td>
        <td>${s.schedule}</td>
        <td><span class="badge badge-${s.status}">${s.status.charAt(0).toUpperCase()+s.status.slice(1)}</span></td>
        <td style="color:rgba(245,239,224,0.45);font-size:0.78rem;">${s.date}</td>
      </tr>
    `).join('');
  }

  function filterTable() {
    const q = document.getElementById('searchInput').value.toLowerCase();
    const status = document.getElementById('statusFilter').value.toLowerCase();
    const course = document.getElementById('courseFilter').value.toLowerCase();
    const filtered = students.filter(s => {
      const matchQ = !q || s.name.toLowerCase().includes(q) || s.phone.includes(q) || s.course.toLowerCase().includes(q);
      const matchS = !status || s.status === status;
      const matchC = !course || s.course.toLowerCase().includes(course);
      return matchQ && matchS && matchC;
    });
    renderTable(filtered);
  }

  function registerStudent() {
    const fname = document.getElementById('fname').value.trim();
    const lname = document.getElementById('lname').value.trim();
    const email = document.getElementById('email').value.trim();
    const phone = document.getElementById('phone').value.trim();
    const course = document.getElementById('course').value;
    const schedule = document.getElementById('schedule').value;

    if (!fname || !lname || !email || !phone || !course) {
      alert('Please fill in all required fields (*)');
      return;
    }

    const today = new Date().toISOString().split('T')[0];
    const newId = 'NSA-' + String(++idCounter).padStart(4, '0');
    const shortCourse = course.split('(')[0].trim();
    const student = { id: newId, name: fname + ' ' + lname, phone, course: shortCourse, schedule, status: 'new', date: today };
    students.unshift(student);
    renderTable(students);

    document.getElementById('studentId').textContent = 'Your Student ID: ' + newId;
    document.getElementById('successModal').classList.add('active');

    // Reset form
    ['fname','lname','email','phon
