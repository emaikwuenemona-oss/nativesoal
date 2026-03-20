<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>NativeSoal Fashion School</title>

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;500;700&display=swap" rel="stylesheet">

<style>
*{margin:0;padding:0;box-sizing:border-box;font-family:'Poppins',sans-serif}

body{
background:#0b0b0b;
color:white;
overflow-x:hidden;
}

header{
height:100vh;
display:flex;
align-items:center;
justify-content:center;
text-align:center;
padding:20px;
background:linear-gradient(rgba(0,0,0,.7),rgba(0,0,0,.7)),
url('https://images.unsplash.com/photo-1593032465171-8f0c8d7c9d8b?q=80&w=1974') center/cover;
animation:fadeIn 2s ease-in;
}

header h1{
font-size:3rem;
color:#d4af37;
letter-spacing:2px;
}

header p{
margin:20px 0;
font-size:1.2rem;
}

.btn{
display:inline-block;
padding:15px 35px;
background:#d4af37;
color:black;
font-weight:bold;
border-radius:30px;
text-decoration:none;
transition:.3s;
}

.btn:hover{
background:white;
transform:scale(1.05);
}

section{
padding:80px 20px;
max-width:1100px;
margin:auto;
}

.section-title{
text-align:center;
font-size:2.2rem;
color:#d4af37;
margin-bottom:50px;
}

.cards{
display:grid;
grid-template-columns:repeat(auto-fit,minmax(250px,1fr));
gap:30px;
}

.card{
background:#111;
padding:30px;
border-radius:15px;
transition:.4s;
border:1px solid rgba(212,175,55,.3);
}

.card:hover{
transform:translateY(-10px);
border-color:#d4af37;
}

.card h3{
color:#d4af37;
margin-bottom:15px;
}

.cta{
text-align:center;
padding:100px 20px;
background:linear-gradient(45deg,#000,#1a1a1a);
}

.cta h2{
font-size:2.5rem;
margin-bottom:20px;
}

.phone{
font-size:1.5rem;
color:#d4af37;
margin:20px 0;
}

footer{
text-align:center;
padding:30px;
background:#000;
font-size:.9rem;
opacity:.7;
}

.whatsapp{
position:fixed;
bottom:20px;
right:20px;
background:#25D366;
color:white;
padding:15px 18px;
border-radius:50%;
font-size:22px;
text-decoration:none;
box-shadow:0 4px 10px rgba(0,0,0,.4);
animation:pulse 2s infinite;
}

@keyframes pulse{
0%{transform:scale(1)}
50%{transform:scale(1.1)}
100%{transform:scale(1)}
}

@keyframes fadeIn{
from{opacity:0}
to{opacity:1}
}
</style>
</head>

<body>

<header>
<div>
<h1>NATIVESOAL FASHION SCHOOL</h1>
<p>Master the Art of Male Fashion & Professional Tailoring</p>
<a href="#programs" class="btn">Explore Programs</a>
</div>
</header>

<section id="programs">
<h2 class="section-title">Our Programs</h2>
<div class="cards">
<div class="card">
<h3>Fashion Design & Tailoring</h3>
<p>Learn professional garment construction for kaftans, suits, and modern menswear.</p>
</div>

<div class="card">
<h3>Pattern Drafting</h3>
<p>Master accurate measurements and pattern development techniques.</p>
</div>

<div class="card">
<h3>Creative Draping</h3>
<p>Understand fabric behavior and advanced garment shaping methods.</p>
</div>

<div class="card">
<h3>Fashion Business</h3>
<p>Learn branding, marketing, pricing, and how to grow your fashion brand.</p>
</div>
</div>
</section>

<section class="cta">
<h2>Start Your Fashion Journey Today</h2>
<p>Become a professional fashion designer with hands-on training.</p>
<div class="phone">📞 07032444289</div>
<a href="https://wa.me/2347032444289" class="btn">Chat on WhatsApp</a>
</section>

<footer>
© 2026 NativeSoal Fashion School • Warri, Nigeria
</footer>

<a class="whatsapp" href="https://wa.me/2347032444289">💬</a>

</body>
</html>
