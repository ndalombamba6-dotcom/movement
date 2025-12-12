<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Movement Clothing</title>
  <style>
    :root {
      --movement-dark: #000000;
      --movement-grey: #1a1a1a;
      --movement-beige: #e8dcc1;
    }
    body { margin:0; font-family: Arial, sans-serif; background: var(--movement-grey); color: var(--movement-beige); transition: background 0.6s, color 0.6s; }
    header { background: var(--movement-dark); color: var(--movement-beige); padding: 20px; text-align:center; position: sticky; top:0; z-index:50; }
    nav a { margin: 0 15px; color: var(--movement-beige); text-decoration: none; font-weight: bold; }
    section { padding: 60px 20px; max-width: 1200px; margin: auto; }
    .hero { height: 80vh; display:flex; flex-direction:column; align-items:center; justify-content:center; color: var(--movement-beige); text-shadow:0 0 10px #000; position: relative; }
    .grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(250px,1fr)); gap: 20px; }
    .card { background: #2a2a2a; padding: 20px; border-radius: 10px; box-shadow:0 2px 10px rgba(0,0,0,0.4); transition: transform 0.3s, box-shadow 0.3s; }
    .card:hover { transform: translateY(-5px); box-shadow:0 4px 20px rgba(0,0,0,0.6); }
    footer { background: var(--movement-dark); color: var(--movement-beige); text-align:center; padding:20px; margin-top:40px; }
    .btn { background: var(--movement-beige); color:#000; padding:10px 20px; border-radius:5px; display:inline-block; text-decoration:none; font-weight:bold; }
    .reveal { opacity:0; transform: translateY(40px); transition:0.8s ease; }
    .reveal.active { opacity:1; transform: translateY(0); }
  </style>
</head>
<body>

<!-- =================== HEADER & NAV =================== -->
<header>
  <nav>
    <a href="#page-home">Home</a>
    <a href="#page-shop">Shop</a>
    <a href="#page-lookbook">Lookbook</a>
    <a href="#page-about">About</a>
    <a href="#page-blog">Blog</a>
    <a href="#page-faq">FAQ</a>
    <a href="#page-contact">Contact</a>
  </nav>
</header>

<!-- =================== PAGE 1: HOME =================== -->
<section id="page-home" class="hero reveal">
  <h1>Movement Clothing</h1>
  <p style="font-size:1.5em; margin-top:10px;">Starting the Movement — Gym & Street Wear</p>
</section>

<!-- =================== PAGE 2: SHOP =================== -->
<section id="page-shop" class="reveal">
  <h2>Shop</h2>
  <div class="grid">
    <div class="card"><h3>Sweatpants</h3><p>Comfortable premium sweatpants for gym & street wear.</p></div>
    <div class="card"><h3>T-Shirts</h3><p>Minimal everyday tees designed for both gym and street style.</p></div>
  </div>
</section>

<!-- =================== PAGE 3: LOOKBOOK =================== -->
<section id="page-lookbook" class="reveal">
  <h2>Lookbook</h2>
  <div class="grid">
    <div class="card">Look 1</div>
    <div class="card">Look 2</div>
    <div class="card">Look 3</div>
  </div>
</section>

<!-- =================== PAGE 4: ABOUT =================== -->
<section id="page-about" class="reveal">
  <h2>About Movement</h2>
  <p>Movement is a South African-born brand specializing in gym and street wear, built around expression, culture, and identity. Our mission is to create clothing that empowers people to move boldly — in style, in confidence, and in purpose.</p>
  <p>Every piece is crafted with detail, comfort, and urban influence, designed for those who lead with authenticity.</p>
</section>

<!-- =================== PAGE 5: BLOG =================== -->
<section id="page-blog" class="reveal">
  <h2>Movement Blog</h2>
  <div class="grid">
    <div class="card">
      <h3>The Rise of South African Streetwear</h3>
      <p>South Africa’s fashion scene is evolving fast. Gym and street wear brands are redefining urban style and inspiring movement culture.</p>
    </div>
    <div class="card">
      <h3>How to Style Gym & Street Wear</h3>
      <p>Learn how to mix comfort and style with our sweatpants and T-shirts, perfect for both workout sessions and urban streets.</p>
    </div>
  </div>
</section>

<!-- =================== PAGE 6: FAQ =================== -->
<section id="page-faq" class="reveal">
  <h2>Frequently Asked Questions</h2>
  <div class="card">
    <h3>Do you ship in South Africa?</h3>
    <p>Yes, we deliver nationwide. Delivery takes 2–4 working days.</p>
  </div>
  <div class="card">
    <h3>What payment methods do you accept?</h3>
    <p>We accept EFT, card payments, and mobile-friendly methods.</p>
  </div>
  <div class="card">
    <h3>Can I return or exchange items?</h3>
    <p>Yes — items may be returned within 7 days if unworn and undamaged.</p>
  </div>
</section>

<!-- =================== PAGE 7: CONTACT =================== -->
<section id="page-contact" class="reveal">
  <h2>Contact Us</h2>
  <p>Phone: 065 806 8348</p>
  <p>Email: support@movement.co.za</p>
  <p>Instagram: @movementwear</p>
  <a class="btn" href="mailto:support@movement.co.za">Send Email</a>
</section>

<!-- =================== FOOTER =================== -->
<footer>
  <p>© 2025 Movement Clothing. All rights reserved.</p>
</footer>

<script>
  // Scroll reveal animation
  const reveals = document.querySelectorAll('.reveal');
  window.addEventListener('scroll', () => {
    reveals.forEach(el => {
      const rect = el.getBoundingClientRect();
      if(rect.top < window.innerHeight - 100) el.classList.add('active');
    });
  });

  // Smooth scrolling for nav links
  document.querySelectorAll('nav a').forEach(link => {
    link.addEventListener('click', e => {
      e.preventDefault();
      const target = document.querySelector(link.getAttribute('href'));
      target.scrollIntoView({behavior:'smooth'});
    });
  });
</script>

</body>
</html>
