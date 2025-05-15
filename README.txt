<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <meta name="description" content="群馬在住のガジェッターkokeの公式サイト。iPhone脱獄、Androidカスタマイズ、最新ガジェットレビューを配信。">
  <meta name="keywords" content="ガジェット, iPhone, Android, 脱獄, koke, 群馬, YouTuber">
  <meta name="author" content="koke">
  <meta property="og:title" content="koke | 群馬のガジェッター & YouTuber">
  <meta property="og:description" content="群馬在住のガジェッターkokeの公式サイト。iPhone脱獄、Androidカスタマイズ、最新ガジェットレビューを配信。">
  <meta property="og:image" content="https://pbs.twimg.com/profile_images/1905204578142060544/Uy9o3amd_400x400.jpg">
  <meta property="og:url" content="https://koke-gadgetter.com">
  <meta name="twitter:card" content="summary_large_image">
  <title>koke | 群馬のガジェッター & YouTuber</title>
  <link rel="icon" href="https://via.placeholder.com/32" type="image/x-icon">
  <link href="https://fonts.googleapis.com/css2?family=Noto+Sans+JP:wght@400;700&family=Poppins:wght@400;700&display=swap" rel="stylesheet">
  <link href="https://cdnjs.cloudflare.com/ajax/libs/aos/2.3.4/aos.css" rel="stylesheet">
  <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css" rel="stylesheet">
  <style>
    :root {
      --primary: #0e76a8;
      --secondary: #8e44ad;
      --accent: #00d4ff;
      --bg-light: #f4f6f8;
      --bg-dark: #1a1a1a;
      --text-light: #333;
      --text-dark: #e0e0e0;
      --card-bg-light: #fff;
      --card-bg-dark: #2c2c2c;
    }

    [data-theme="dark"] {
      --bg-light: var(--bg-dark);
      --text-light: var(--text-dark);
      --card-bg-light: var(--card-bg-dark);
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      scroll-behavior: smooth;
    }

    body {
      font-family: 'Noto Sans JP', sans-serif;
      background: var(--bg-light);
      color: var(--text-light);
      line-height: 1.6;
      overflow-x: hidden;
      transition: background 0.3s, color 0.3s;
      cursor: none;
    }

    a {
      color: var(--accent);
      text-decoration: none;
      transition: color 0.3s;
    }

    /* Custom Cursor */
    .cursor {
      position: fixed;
      width: 20px;
      height: 20px;
      border: 2px solid var(--accent);
      border-radius: 50%;
      pointer-events: none;
      transform: translate(-50%, -50%);
      transition: all 0.1s ease;
      z-index: 9999;
    }

    .cursor.hovered {
      width: 30px;
      height: 30px;
      background: var(--accent);
      opacity: 0.4;
    }

    /* Header */
    header {
      position: relative;
      height: 100vh;
      background: linear-gradient(135deg, var(--primary), var(--secondary));
      color: #fff;
      display: flex;
      align-items: center;
      justify-content: center;
      text-align: center;
      overflow: hidden;
    }

    #particles-js {
      position: absolute;
      width: 100%;
      height: 100%;
      top: 0;
      left: 0;
      z-index: 0;
    }

    header .hero-content {
      z-index: 1;
    }

    header h1 {
      font-family: 'Poppins', sans-serif;
      font-size: 4.5em;
      margin-bottom: 10px;
      animation: fadeInDown 1s ease;
    }

    header p {
      font-size: 1.5em;
      opacity: 0.9;
      margin-bottom: 20px;
      animation: fadeInUp 1s ease 0.3s both;
    }

    header .cta {
      display: inline-block;
      padding: 15px 30px;
      background: var(--accent);
      color: #fff;
      font-size: 1.2em;
      border-radius: 50px;
      box-shadow: 0 4px 15px rgba(0, 212, 255, 0.4);
      transition: transform 0.3s, box-shadow 0.3s;
      animation: fadeInUp 1s ease 0.6s both;
    }

    header .cta:hover {
      transform: translateY(-5px);
      box-shadow: 0 8px 20px rgba(0, 212, 255, 0.6);
    }

    /* Container */
    .container {
      max-width: 1200px;
      margin: auto;
      padding: 60px 20px;
    }

    section {
      margin-bottom: 80px;
    }

    h2 {
      font-family: 'Poppins', sans-serif;
      font-size: 2.5em;
      margin-bottom: 30px;
      border-left: 8px solid var(--accent);
      padding-left: 15px;
    }

    /* About */
    .about {
      display: grid;
      grid-template-columns: 1fr 2fr;
      gap: 40px;
      align-items: center;
      background: var(--card-bg-light);
      padding: 30px;
      border-radius: 15px;
      box-shadow: 0 8px 20px rgba(0, 0, 0, 0.1);
      transition: background 0.3s;
    }

    .about img {
      width: 250px;
      height: 250px;
      border-radius: 50%;
      object-fit: cover;
      transition: transform 0.3s;
    }

    .about img:hover {
      transform: scale(1.05);
    }

    .skills {
      margin-top: 20px;
    }

    .skill {
      margin-bottom: 20px;
    }

    .skill span {
      font-weight: bold;
      display: block;
      margin-bottom: 5px;
    }

    .bar {
      background: #ddd;
      height: 12px;
      border-radius: 6px;
      overflow: hidden;
    }

    .bar div {
      height: 100%;
      background: var(--accent);
      width: 0;
      transition: width 1s ease;
    }

    /* Blog */
    .blog-cards {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
      gap: 30px;
    }

    .card {
      background: var(--card-bg-light);
      border-radius: 15px;
      box-shadow: 0 8px 20px rgba(0, 0, 0, 0.1);
      overflow: hidden;
      transition: transform 0.3s, box-shadow 0.3s;
    }

    .card:hover {
      transform: translateY(-10px);
      box-shadow: 0 12px 25px rgba(0, 0, 0, 0.2);
    }

    .card img {
      width: 100%;
      height: 200px;
      object-fit: cover;
    }

    .card-content {
      padding: 20px;
    }

    .card h3 {
      font-family: 'Poppins', sans-serif;
      font-size: 1.5em;
      margin-bottom: 10px;
    }

    .card .meta {
      color: #777;
      font-size: 0.9em;
      margin-bottom: 10px;
    }

    .card p {
      margin-bottom: 15px;
    }

    .card .read-more {
      display: inline-block;
      padding: 10px 20px;
      background: var(--accent);
      color: #fff;
      border-radius: 25px;
      transition: background 0.3s, transform 0.3s;
    }

    .card .read-more:hover {
      background: var(--primary);
      transform: translateY(-3px);
    }

    /* Contact */
    .contact form {
      display: grid;
      gap: 20px;
      max-width: 600px;
      margin: auto;
      background: var(--card-bg-light);
      padding: 30px;
      border-radius: 15px;
      box-shadow: 0 8px 20px rgba(0, 0, 0, 0.1);
      transition: background 0.3s;
    }

    .contact input,
    .contact textarea {
      padding: 15px;
      border: 2px solid #ccc;
      border-radius: 8px;
      font-size: 1em;
      transition: border-color 0.3s;
    }

    .contact input:focus,
    .contact textarea:focus {
      border-color: var(--accent);
      outline: none;
    }

    .contact button {
      padding: 15px;
      background: var(--accent);
      color: #fff;
      border: none;
      border-radius: 8px;
      font-size: 1.1em;
      cursor: pointer;
      transition: background 0.3s, transform 0.3s;
    }

    .contact button:hover {
      background: var(--primary);
      transform: translateY(-3px);
    }

    /* Footer */
    footer {
      background: var(--primary);
      color: #fff;
      padding: 40px 20px;
      text-align: center;
    }

    footer .social a {
      margin: 0 15px;
      font-size: 1.8em;
      color: #fff;
      transition: color 0.3s, transform 0.3s;
    }

    footer .social a:hover {
      color: var(--accent);
      transform: scale(1.2);
    }

    footer .newsletter {
      margin: 20px 0;
    }

    footer .newsletter input {
      padding: 10px;
      border: none;
      border-radius: 5px 0 0 5px;
      width: 200px;
    }

    footer .newsletter button {
      padding: 10px 20px;
      background: var(--accent);
      color: #fff;
      border: none;
      border-radius: 0 5px 5px 0;
      cursor: pointer;
      transition: background 0.3s;
    }

    footer .newsletter button:hover {
      background: var(--secondary);
    }

    /* Back to Top */
    .back-to-top {
      position: fixed;
      bottom: 20px;
      right: 20px;
      background: var(--accent);
      color: #fff;
      width: 50px;
      height: 50px;
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 1.5em;
      opacity: 0;
      transition: opacity 0.3s, transform 0.3s;
      cursor: pointer;
    }

    .back-to-top.visible {
      opacity: 1;
    }

    .back-to-top:hover {
      transform: translateY(-5px);
    }

    /* Dark Mode Toggle */
    .theme-toggle {
      position: fixed;
      top: 20px;
      right: 20px;
      background: none;
      border: none;
      font-size: 1.5em;
      color: var(--text-light);
      cursor: pointer;
      z-index: 1000;
    }

    /* Animations */
    @keyframes fadeInDown {
      from { opacity: 0; transform: translateY(-20px); }
      to { opacity: 1; transform: translateY(0); }
    }

    @keyframes fadeInUp {
      from { opacity: 0; transform: translateY(20px); }
      to { opacity: 1; transform: translateY(0); }
    }

    /* Responsive */
    @media (max-width: 768px) {
      header h1 {
        font-size: 2.5em;
      }

      header p {
        font-size: 1.2em;
      }

      .about {
        grid-template-columns: 1fr;
        text-align: center;
      }

      .about img {
        margin: auto;
      }

      h2 {
        font-size: 2em;
      }

      .card img {
        height: 150px;
      }
    }

    @media (max-width: 480px) {
      header h1 {
        font-size: 2em;
      }

      header .cta {
        padding: 10px 20px;
        font-size: 1em;
      }

      .container {
        padding: 30px 15px;
      }
    }
  </style>
</head>
<body data-theme="light">
  <!-- Custom Cursor -->
  <div class="cursor"></div>

  <!-- Theme Toggle -->
  <button class="theme-toggle" aria-label="テーマを切り替え">
    <i class="fas fa-moon"></i>
  </button>

  <!-- Header -->
  <header role="banner">
    <div id="particles-js"></div>
    <div class="hero-content">
      <h1 data-aos="fade-down">koke</h1>
      <p data-aos="fade-up">群馬のガジェッター & YouTuber</p>
      <a href="https://youtube.com/@koke" class="cta" data-aos="fade-up" data-aos-delay="200">YouTubeをチェック</a>
    </div>
  </header>

  <!-- Main Content -->
  <div class="container">
    <!-- About -->
    <section role="region" aria-labelledby="about-heading">
      <h2 id="about-heading" data-aos="fade-right">自己紹介</h2>
      <div class="about" data-aos="fade-up">
        <img src="https://pbs.twimg.com/profile_images/1905204578142060544/Uy9o3amd_400x400.jpg" alt="kokeのプロフィール写真" loading="lazy">
        <div>
          <p>こんにちは、群馬在住のYouTuber兼ガジェッター、kokeです。iPhoneの脱獄やAndroid端末のWindows化など、ガジェットの可能性を追求しています！</p>
          <div class="skills">
            <div class="skill">
              <span>金欠率</span>
              <div class="bar"><div style="width: 95%;" class="skill-bar"></div></div>
            </div>
            <div class="skill">
              <span>頭</span>
              <div class="bar"><div style="width: 45%;" class="skill-bar"></div></div>
            </div>
            <div class="skill">
              <span>恋愛</span>
              <div class="bar"><div style="width: 5%;" class="skill-bar"></div></div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Blog -->
    <section role="region" aria-labelledby="blog-heading">
      <h2 id="blog-heading" data-aos="fade-right">最新のブログ</h2>
      <div class="blog-cards">
        <div class="card" data-aos="fade-up">
          <img src="https://via.placeholder.com/400x200?text=iPhone5" alt="iPhone5の画像" loading="lazy">
          <div class="card-content">
            <div class="meta">2025年5月10日 | ガジェット</div>
            <h3>iPhone5は2025年にどこまで使えるか？</h3>
            <p>iOS10とA6チップの限界に挑みます。古いデバイスを現代で活用する方法を検証！</p>
            <a href="/blog/iphone5" class="read-more">詳細を読む</a>
          </div>
        </div>
        <div class="card" data-aos="fade-up" data-aos-delay="100">
          <img src="https://via.placeholder.com/400x200?text=iPhone4" alt="iPhone4の画像" loading="lazy">
          <div class="card-content">
            <div class="meta">2025年5月5日 | 修理</div>
            <h3>iPhone4の分解と修復</h3>
            <p>リンゴループ化したiPhone4を復活！分解から修復までの全工程を解説。</p>
            <a href="/blog/iphone4" class="read-more">詳細を読む</a>
          </div>
        </div>
        <div class="card" data-aos="fade-up" data-aos-delay="200">
          <img src="https://via.placeholder.com/400x200?text=iPhoneReview" alt="iPhoneレビューの画像" loading="lazy">
          <div class="card-content">
            <div class="meta">2025年4月30日 | レビュー</div>
            <h3>メルカリで購入したiPhoneをレビュー</h3>
            <p>破格で手に入れたiPhoneの実力は？開封から使用感まで徹底レビュー！</p>
            <a href="/blog/iphone-review" class="read-more">詳細を読む</a>
          </div>
        </div>
      </div>
    </section>

    <!-- Contact -->
    <section class="contact" role="region" aria-labelledby="contact-heading">
      <h2 id="contact-heading" data-aos="fade-right">お問い合わせ</h2>
      <form action="https://formspree.io/f/your-formspree-id" method="POST" data-aos="fade-up">
        <input type="text" name="name" placeholder="お名前" required>
        <input type="email" name="email" placeholder="メールアドレス" required>
        <textarea name="message" placeholder="メッセージ" rows="6" required></textarea>
        <button type="submit">送信</button>
      </form>
    </section>
  </div>

  <!-- Footer -->
  <footer role="contentinfo">
    <div class="newsletter">
      <h3>ニュースレターに登録</h3>
      <form action="/subscribe" method="POST">
        <input type="email" name="email" placeholder="メールアドレスを入力" required>
        <button type="submit">登録</button>
      </form>
    </div>
    <div class="social">
      <a href="https://twitter.com/koke" aria-label="Twitter"><i class="fab fa-twitter"></i></a>
      <a href="https://instagram.com/koke" aria-label="Instagram"><i class="fab fa-instagram"></i></a>
      <a href="https://facebook.com/koke" aria-label="Facebook"><i class="fab fa-facebook"></i></a>
    </div>
    <p>© 2025 koke. All Rights Reserved.</p>
  </footer>

  <!-- Back to Top -->
  <a href="#" class="back-to-top" aria-label="ページのトップに戻る"><i class="fas fa-chevron-up"></i></a>

  <!-- Scripts -->
  <script src="https://cdnjs.cloudflare.com/ajax/libs/particles.js/2.0.0/particles.min.js"></script>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/aos/2.3.4/aos.js"></script>
  <script>
    // Particle.js
    particlesJS("particles-js", {
      particles: {
        number: { value: 80, density: { enable: true, value_area: 800 } },
        color: { value: "#ffffff" },
        shape: { type: "circle" },
        opacity: { value: 0.5, random: true },
        size: { value: 3, random: true },
        line_linked: { enable: true, distance: 150, color: "#ffffff", opacity: 0.4, width: 1 },
        move: { enable: true, speed: 2, direction: "none", random: true }
      },
      interactivity: {
        detect_on: "canvas",
        events: { onhover: { enable: true, mode: "repulse" }, onclick: { enable: true, mode: "push" } },
        modes: { repulse: { distance: 100 }, push: { particles_nb: 4 } }
      },
      retina_detect: true
    });

    // AOS
    AOS.init({ duration: 1000, once: true });

    // Custom Cursor
    const cursor = document.querySelector(".cursor");
    document.addEventListener("mousemove", (e) => {
      cursor.style.left = e.clientX + "px";
      cursor.style.top = e.clientY + "px";
    });

    document.querySelectorAll("a, button, .card").forEach(el => {
      el.addEventListener("mouseenter", () => cursor.classList.add("hovered"));
      el.addEventListener("mouseleave", () => cursor.classList.remove("hovered"));
    });

    // Dark Mode Toggle
    const themeToggle = document.querySelector(".theme-toggle");
    const body = document.body;
    themeToggle.addEventListener("click", () => {
      body.dataset.theme = body.dataset.theme === "light" ? "dark" : "light";
      themeToggle.innerHTML = body.dataset.theme === "light" ? '<i class="fas fa-moon"></i>' : '<i class="fas fa-sun"></i>';
      localStorage.setItem("theme", body.dataset.theme);
    });

    if (localStorage.getItem("theme") === "dark") {
      body.dataset.theme = "dark";
      themeToggle.innerHTML = '<i class="fas fa-sun"></i>';
    }

    // Skill Bar Animation
    const skillBars = document.querySelectorAll(".skill-bar");
    const animateBars = () => {
      skillBars.forEach(bar => {
        const rect = bar.getBoundingClientRect();
        if (rect.top < window.innerHeight && rect.bottom >= 0) {
          bar.style.width = bar.parentElement.style.width;
        }
      });
    };

    window.addEventListener("scroll", animateBars);
    animateBars();

    // Back to Top
    const backToTop = document.querySelector(".back-to-top");
    window.addEventListener("scroll", () => {
      backToTop.classList.toggle("visible", window.scrollY > 300);
    });

    // Form Validation
    const form = document.querySelector(".contact form");
    form.addEventListener("submit", (e) => {
      const inputs = form.querySelectorAll("input, textarea");
      let valid = true;
      inputs.forEach(input => {
        if (!input.value) {
          input.style.borderColor = "red";
          valid = false;
        } else {
          input.style.borderColor = "#ccc";
        }
      });
      if (!valid) e.preventDefault();
    });
  </script>
</body>
</html>
