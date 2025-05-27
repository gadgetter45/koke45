<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <meta name="description" content="群馬のガジェッターkokeの公式サイト。iPhone脱獄、Androidカスタマイズ、最新ガジェットレビューを配信！">
  <meta name="keywords" content="ガジェット, iPhone, Android, 脱獄, koke, 群馬, YouTuber, テックレビュー">
  <meta name="author" content="koke">
  <meta property="og:title" content="koke | ガジェッター">
  <meta property="og:description" content="最新ガジェットレビューをYouTubeとブログで！">
  <meta property="og:image" content="https://pbs.twimg.com/profile_images/1905204578142060544/Uy9o3amd_400x400.jpg">
  <meta property="og:url" content="https://koke-gadgetter.com">
  <meta name="twitter:card" content="summary_large_image">
  <title>koke | ガジェッター</title>
  <link rel="icon" href="https://via.placeholder.com/32" type="image/x-icon">
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&display=swap" rel="stylesheet">
  <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css" rel="stylesheet">
  <style>
    :root {
      --bg: #fafafa;
      --text: #1f2937;
      --primary: #2563eb;
      --accent: #14b8a6;
      --card-bg: #ffffff;
      --border: #e5e7eb;
    }

    [data-theme="dark"] {
      --bg: #1f2937;
      --text: #f3f4f6;
      --card-bg: #374151;
      --border: #4b5563;
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      scroll-behavior: smooth;
    }

    body {
      font-family: 'Inter', sans-serif;
      background: var(--bg);
      color: var(--text);
      line-height: 1.6;
      transition: background 0.2s, color 0.2s;
    }

    a {
      color: var(--accent);
      text-decoration: none;
      transition: color 0.2s;
    }

    /* Navigation */
    nav {
      background: var(--card-bg);
      padding: 1rem;
      box-shadow: 0 2px 4px rgba(0, 0, 0, 0.05);
      position: sticky;
      top: 0;
      z-index: 1000;
    }

    .nav-container {
      max-width: 1280px;
      margin: auto;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    .nav-logo {
      font-size: 1.5rem;
      font-weight: 700;
      color: var(--primary);
    }

    .nav-links {
      display: flex;
      gap: 1.5rem;
    }

    .nav-links a {
      font-size: 1rem;
      font-weight: 600;
      color: var(--text);
    }

    .nav-links a:hover {
      color: var(--accent);
    }

    .hamburger {
      display: none;
      font-size: 1.5rem;
      background: none;
      border: none;
      color: var(--text);
      cursor: pointer;
    }

    @media (max-width: 768px) {
      .nav-links {
        display: none;
        flex-direction: column;
        position: absolute;
        top: 60px;
        left: 0;
        width: 100%;
        background: var(--card-bg);
        padding: 1rem;
        box-shadow: 0 2px 4px rgba(0, 0, 0, 0.05);
      }

      .nav-links.active {
        display: flex;
      }

      .hamburger {
        display: block;
      }
    }

    /* Header */
    header {
      background: var(--primary);
      color: #fff;
      text-align: center;
      padding: 4rem 1rem;
    }

    header h1 {
      font-size: 2.5rem;
      font-weight: 700;
      margin-bottom: 0.5rem;
    }

    header p {
      font-size: 1.1rem;
      opacity: 0.9;
      margin-bottom: 1.5rem;
    }

    .cta {
      display: inline-block;
      padding: 0.8rem 2rem;
      background: var(--accent);
      color: #fff;
      border-radius: 8px;
      font-weight: 600;
      transition: background 0.2s, transform 0.2s;
    }

    .cta:hover {
      background: #0d9488;
      transform: translateY(-2px);
    }

    /* Container */
    .container {
      max-width: 1280px;
      margin: auto;
      padding: 2rem 1rem;
    }

    h2 {
      font-size: 1.8rem;
      font-weight: 700;
      margin-bottom: 1rem;
      color: var(--primary);
    }

    /* About */
    .about {
      background: var(--card-bg);
      padding: 1.5rem;
      border-radius: 8px;
      display: flex;
      gap: 1.5rem;
      align-items: center;
    }

    .about img {
      width: 120px;
      height: 120px;
      border-radius: 50%;
      object-fit: cover;
    }

    .about p {
      font-size: 1rem;
    }

    /* Gadget Search */
    .gadget-search {
      display: flex;
      gap: 0.5rem;
      margin-bottom: 1.5rem;
      max-width: 400px;
    }

    .gadget-search input {
      flex: 1;
      padding: 0.8rem;
      border: 1px solid var(--border);
      border-radius: 8px;
      font-size: 1rem;
    }

    .gadget-search button {
      padding: 0.8rem 1.5rem;
      background: var(--accent);
      color: #fff;
      border: none;
      border-radius: 8px;
      cursor: pointer;
    }

    .gadget-search button:hover {
      background: #0d9488;
    }

    /* Gadget Grid */
    .gadget-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      gap: 1rem;
    }

    .gadget-card {
      background: var(--card-bg);
      border-radius: 8px;
      overflow: hidden;
      transition: transform 0.2s;
    }

    .gadget-card:hover {
      transform: translateY(-4px);
    }

    .gadget-card img {
      width: 100%;
      height: 180px;
      object-fit: cover;
    }

    .gadget-content {
      padding: 1rem;
    }

    .gadget-content h3 {
      font-size: 1.3rem;
      font-weight: 600;
      margin-bottom: 0.5rem;
    }

    /* Links */
    .links-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
      gap: 1rem;
    }

    .link-card {
      background: var(--card-bg);
      padding: 1rem;
      border-radius: 8px;
      text-align: center;
    }

    .link-card a {
      font-size: 1.1rem;
      font-weight: 600;
      color: var(--primary);
    }

    /* Spotify */
    .spotify-widget {
      max-width: 400px;
      margin: 1.5rem auto;
    }

    /* News */
    .news-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      gap: 1rem;
    }

    .news-card {
      background: var(--card-bg);
      padding: 1rem;
      border-radius: 8px;
    }

    .news-card h3 {
      font-size: 1.2rem;
      margin-bottom: 0.5rem;
    }

    /* Theme Toggle */
    .theme-toggle {
      position: fixed;
      top: 1rem;
      right: 1rem;
      background: none;
      border: none;
      font-size: 1.5rem;
      color: var(--text);
      cursor: pointer;
    }

    /* Responsive */
    @media (max-width: 768px) {
      header h1 {
        font-size: 2rem;
      }

      header p {
        font-size: 1rem;
      }

      .about {
        flex-direction: column;
        text-align: center;
      }

      .about img {
        margin: auto;
      }
    }

    @media (max-width: 480px) {
      .cta {
        padding: 0.6rem 1.5rem;
        font-size: 0.9rem;
      }
    }
  </style>
</head>
<body data-theme="light">
  <!-- Theme Toggle -->
  <button class="theme-toggle" aria-label="テーマ切り替え">
    <i class="fas fa-moon"></i>
  </button>

  <!-- Navigation -->
  <nav role="navigation">
    <div class="nav-container">
      <div class="nav-logo">koke</div>
      <button class="hamburger" aria-label="メニューを開く">
        <i class="fas fa-bars"></i>
      </button>
      <div class="nav-links">
        <a href="#home">ホーム</a>
        <a href="#about">自己紹介</a>
        <a href="#gadgets">ガジェット</a>
        <a href="#links">リンク</a>
      </div>
    </div>
  </nav>

  <!-- Header -->
  <header id="home" role="banner">
    <h1>koke</h1>
    <p>群馬のガジェッター | ガジェットレビューとカスタマイズ</p>
    <a href="https://x.com/gadgetter45" class="cta">Twitterでフォロー</a>
  </header>

  <!-- Main Content -->
  <div class="container">
    <!-- About -->
    <section id="about" role="region" aria-labelledby="about-heading">
      <h2 id="about-heading">自己紹介</h2>
      <div class="about">
        <img src="https://pbs.twimg.com/profile_images/1905204578142060544/Uy9o3amd_400x400.jpg" alt="kokeのプロフィール写真" loading="lazy">
        <p>群馬在住のkokeです。iPhone脱獄、Androidカスタマイズ、最新ガジェットのレビューをYouTubeとブログで発信しています！</p>
      </div>
    </section>

    <!-- Gadgets -->
    <section id="gadgets" role="region" aria-labelledby="gadgets-heading">
      <h2 id="gadgets-heading">ガジェットレビュー</h2>
      <div class="gadget-search">
        <input type="text" id="gadget-search-input" placeholder="ガジェットを検索..." aria-label="ガジェット検索">
        <button onclick="searchGadgets()">検索</button>
      </div>
      <div class="gadget-grid" id="gadget-grid">
        <div class="gadget-card" data-tags="surface, tablet">
          <img src="https://via.placeholder.com/280x180" alt="Surface" loading="lazy">
          <div class="gadget-content">
            <h3>Surfaceレビュー</h3>
            <p>メルカリで購入した3万円のSurfaceを徹底レビュー。</p>
            <a href="https://gadgetter45.blogspot.com" class="cta">詳細</a>
          </div>
        </div>
        <div class="gadget-card" data-tags="iphone, jailbreak">
          <img src="https://guide-images.cdn.ifixit.com/igi/sX5iMoIvYMbCvHoF.medium" alt="iPhone 5s" loading="lazy">
          <div class="gadget-content">
            <h3>iPhone 5s脱獄ガイド</h3>
            <p>iOS 12での脱獄手順をステップごとに解説。</p>
            <a href="https://gadgetter45.blogspot.com" class="cta">詳細</a>
          </div>
        </div>
      </div>
    </section>

    <!-- Links & Spotify -->
    <section id="links" role="region" aria-labelledby="links-heading">
      <h2 id="links-heading">リンク</h2>
      <div class="links-grid">
        <div class="link-card">
          <a href="https://x.com/gadgetter45" target="_blank" rel="noopener">Twitter</a>
          <p>最新情報やつぶやきをチェック！</p>
        </div>
        <div class="link-card">
          <a href="https://www.youtube.com/@Koke_Gadget" target="_blank" rel="noopener">YouTube</a>
          <p>ガジェットレビュー動画</p>
        </div>
        <div class="link-card">
          <a href="https://gadgetter45.blogspot.com" target="_blank" rel="noopener">ブログ</a>
          <p>詳細なレビュー記事</p>
        </div>
      </div>
      <div class="spotify-widget">
        <h3>作業用BGM</h3>
        <iframe style="border-radius:8px" src="https://open.spotify.com/embed/playlist/37i9dQZF1DXcBWIGoYBM5M" width="100%" height="152" frameBorder="0" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" loading="lazy"></iframe>
      </div>
    </section>

    <!-- News -->
    <section id="news" role="region" aria-labelledby="news-heading">
      <h2 id="news-heading">最新ニュース</h2>
      <div class="news-grid" id="news-grid"></div>
    </section>
  </div>

  <!-- Footer -->
  <footer role="contentinfo">
    <div class="social">
      <a href="https://x.com/gadgetter45" aria-label="Twitter"><i class="fab fa-twitter"></i></a>
      <a href="https://www.youtube.com/@Koke_Gadget" aria-label="YouTube"><i class="fab fa-youtube"></i></a>
    </div>
    <p>© 2025 koke. All Rights Reserved.</p>
  </footer>

  <!-- Scripts -->
  <script>
    // Navigation Toggle
    const hamburger = document.querySelector(".hamburger");
    const navLinks = document.querySelector(".nav-links");
    hamburger.addEventListener("click", () => {
      navLinks.classList.toggle("active");
    });

    // Theme Toggle
    const themeToggle = document.querySelector(".theme-toggle");
    themeToggle.addEventListener("click", () => {
      document.body.dataset.theme = document.body.dataset.theme === "light" ? "dark" : "light";
      themeToggle.innerHTML = document.body.dataset.theme === "light" ? '<i class="fas fa-moon"></i>' : '<i class="fas fa-sun"></i>';
      localStorage.setItem("theme", document.body.dataset.theme);
    });

    if (localStorage.getItem("theme") === "dark") {
      document.body.dataset.theme = "dark";
      themeToggle.innerHTML = '<i class="fas fa-sun"></i>';
    }

    // Gadget Search
    function searchGadgets() {
      const input = document.getElementById("gadget-search-input").value.toLowerCase();
      const cards = document.querySelectorAll(".gadget-card");
      cards.forEach(card => {
        const title = card.querySelector("h3").textContent.toLowerCase();
        const tags = card.dataset.tags.toLowerCase();
        card.style.display = title.includes(input) || tags.includes(input) ? "block" : "none";
      });
    }

    // News Fetch
    async function fetchNews() {
      const newsGrid = document.getElementById("news-grid");
      try {
        const response = await fetch("https://newsapi.org/v2/top-headlines?category=technology&apiKey=YOUR_NEWS_API_KEY");
        const data = await response.json();
        data.articles.slice(0, 3).forEach(article => {
          const card = document.createElement("div");
          card.className = "news-card";
          card.innerHTML = `
            <h3><a href="${article.url}" target="_blank" rel="noopener">${article.title}</a></h3>
            <p>${article.description || "詳細はリンク先で"}</p>
          `;
          newsGrid.appendChild(card);
        });
      } catch {
        newsGrid.innerHTML = "<p>ニュースの取得に失敗しました。</p>";
      }
    }

    fetchNews();
  </script>
</body>
</html>