# ORPHION_WD_01

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Furniture  Interiors</title>

  <!-- Google Fonts -->
  <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@500;700&family=Inter:wght@300;400;500&display=swap" rel="stylesheet">

  <style>
    :root {
      --bg-light: #f7f6f4;
      --bg-dark: #1e1e1e;
      --text-dark: #1e1e1e;
      --text-light: #ffffff;
      --accent: #b79b6c;
    }

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Inter', sans-serif;
      background-color: var(--bg-light);
      color: var(--text-dark);
      line-height: 1.6;
    }

    /* ==== NAVBAR ====*/
    header {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      z-index: 1000;
      transition: all 0.4s ease;
    }

    .navbar {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 28px 80px;
      background: transparent;
      transition: all 0.4s ease;
    }

    .navbar.scrolled {
      background: rgba(30, 30, 30, 0.95);
      padding: 16px 80px;
      box-shadow: 0 8px 30px rgba(0,0,0,0.2);
    }

    .logo {
      font-family: 'Playfair Display', serif;
      font-size: 1.6rem;
      letter-spacing: 1px;
      color: var(--text-light);
    }

    .navbar.scrolled .logo {
      color: var(--text-light);
    }

    nav ul {
      list-style: none;
      display: flex;
      gap: 40px;
    }

    nav a {
      text-decoration: none;
      font-size: 0.95rem;
      color: var(--text-light);
      position: relative;
    }

    nav a::after {
      content: '';
      position: absolute;
      bottom: -6px;
      left: 0;
      width: 0;
      height: 2px;
      background: var(--accent);
      transition: width 0.3s ease;
    }

    nav a:hover::after {
      width: 100%;
    }

    /* ==== HERO ==== */
    .hero {
      height: 100vh;
      background:
        linear-gradient(rgba(0,0,0,0.45), rgba(0,0,0,0.45)),
        url("https://images.unsplash.com/photo-1600585154340-be6161a56a0c") center/cover no-repeat;
      display: flex;
      align-items: center;
      padding: 0 80px;
      color: var(--text-light);
    }

    .hero-content {
      max-width: 700px;
    }

    .hero h1 {
      font-family: 'Playfair Display', serif;
      font-size: 3.8rem;
      line-height: 1.2;
      margin-bottom: 24px;
    }

    .hero p {
      font-size: 1.1rem;
      margin-bottom: 40px;
      opacity: 0.9;
    }

    .btn {
      display: inline-block;
      padding: 14px 36px;
      border: 1px solid var(--accent);
      color: var(--text-light);
      text-decoration: none;
      letter-spacing: 1px;
      transition: all 0.3s ease;
    }

    .btn:hover {
      background: var(--accent);
      color: var(--bg-dark);
    }

    /*=== SECTION === */
    section {
      padding: 120px 80px;
    }

    .section-title {
      font-family: 'Playfair Display', serif;
      font-size: 2.5rem;
      margin-bottom: 24px;
    }

    .section-text {
      max-width: 600px;
      font-size: 1rem;
      opacity: 0.85;
    }

    /* === FOOTER ==== */
    footer {
      background: var(--bg-dark);
      color: var(--text-light);
      text-align: center;
      padding: 40px 20px;
      font-size: 0.85rem;
      opacity: 0.8;
    }

    /* ==== RESPONSIVE === */
    @media (max-width: 900px) {
      .navbar {
        padding: 20px 40px;
      }

      .navbar.scrolled {
        padding: 14px 40px;
      }

      .hero {
        padding: 0 40px;
      }

      section {
        padding: 80px 40px;
      }

      .hero h1 {
        font-size: 2.8rem;
      }
    }
  </style>
</head>
<body>

  <!-- NAV -->
  <header>
    <div class="navbar" id="navbar">
      <div class="logo">Lumina</div>
      <nav>
        <ul>
          <li><a href="#">Home</a></li>
          <li><a href="#">Projects</a></li>
          <li><a href="#">Studio</a></li>
          <li><a href="#">Contact</a></li>
        </ul>
      </nav>
    </div>
  </header>

  <!-- HERO -->
  <section class="hero">
    <div class="hero-content">
      <h1>Designing Spaces That Tell Your Story</h1>
      <p>
        We craft refined interiors where modern elegance meets timeless comfort.
        Every space is designed to feel intentional, warm, and unforgettable.
      </p>
      <a href="#" class="btn">View Our Work</a>
    </div>
  </section>

  <!-- ABOUT -->
  <section>
    <h2 class="section-title">Our Philosophy</h2>
    <p class="section-text">
      At Furniture Interiors, we believe exceptional design is born from balance:
      form and function, beauty and comfort, restraint and expression.
    </p>
  </section>

  <!-- FOOTER -->
  <footer>
    © 2026 Furniture Interiors — Crafted with intention
  </footer>

  <!-- SCROLL SCRIPT -->
  <script>
    const navbar = document.getElementById("navbar");

    window.addEventListener("scroll", () => {
      if (window.scrollY > 80) {
        navbar.classList.add("scrolled");
      } else {
        navbar.classList.remove("scrolled");
      }
    });
  </script>

</body>
</html>
