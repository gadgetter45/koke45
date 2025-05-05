<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>山田太郎 | Webクリエイターのポートフォリオ</title>
  <link href="https://fonts.googleapis.com/css2?family=Noto+Sans+JP:wght@400;700&display=swap" rel="stylesheet">
  <style>
    * {
      box-sizing: border-box;
    }
    body {
      margin: 0;
      font-family: 'Noto Sans JP', sans-serif;
      background-color: #f4f6f8;
      color: #333;
      line-height: 1.6;
    }
    a {
      color: #0e76a8;
      text-decoration: none;
    }
    header {
      background: linear-gradient(to right, #0e76a8, #2d98da);
      color: white;
      padding: 100px 20px;
      text-align: center;
    }
    header h1 {
      font-size: 3em;
      margin-bottom: 10px;
    }
    header p {
      font-size: 1.2em;
      opacity: 0.9;
    }

    .container {
      max-width: 1100px;
      margin: auto;
      padding: 40px 20px;
    }

    section {
      margin-bottom: 60px;
    }

    h2 {
      font-size: 2em;
      margin-bottom: 20px;
      border-left: 8px solid #0e76a8;
      padding-left: 12px;
    }

    /* 自己紹介 */
    .about {
      display: grid;
      grid-template-columns: 1fr 2fr;
      gap: 30px;
      align-items: center;
    }

    .about img {
      width: 100%;
      border-radius: 50%;
      max-width: 250px;
    }

    .skills {
      margin-top: 20px;
    }

    .skill {
      margin-bottom: 15px;
    }

    .skill span {
      font-weight: bold;
    }

    .bar {
      background: #ddd;
      height: 10px;
      border-radius: 5px;
      overflow: hidden;
    }

    .bar div {
      height: 10px;
      background: #0e76a8;
    }

    /* ブログ */
    .blog-cards {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 20px;
    }

    .card {
      background: white;
      border-radius: 10px;
      box-shadow: 0 4px 10px rgba(0,0,0,0.1);
      padding: 20px;
      transition: transform 0.2s;
    }

    .card:hover {
      transform: translateY(-5px);
    }

    .card h3 {
      margin-top: 0;
    }

    /* お問い合わせ */
    .contact form {
      display: grid;
      gap: 15px;
    }

    .contact input,
    .contact textarea {
      padding: 10px;
      border: 1px solid #ccc;
      border-radius: 6px;
      font-size: 1em;
    }

    .contact button {
      padding: 10px 20px;
      background: #0e76a8;
      color: white;
      border: none;
      border-radius: 6px;
      font-size: 1em;
      cursor: pointer;
      transition: background 0.2s;
    }

    .contact button:hover {
      background: #095c87;
    }

    footer {
      background: #222;
      color: white;
      text-align: center;
      padding: 30px 20px;
    }

    .social a {
      margin: 0 10px;
      font-size: 1.5em;
    }

    @media (max-width: 768px) {
      .about {
        grid-template-columns: 1fr;
        text-align: center;
      }
    }
  </style>
</head>
<body>

<header>
  <h1>山田太郎</h1>
  <p>フロントエンド開発とデザインの交差点に生きるWebクリエイター</p>
</header>

<div class="container">

  <section>
    <h2>自己紹介</h2>
    <div class="about">
      <img src="https://via.placeholder.com/250" alt="プロフィール画像">
      <div>
        <p>こんにちは、東京在住のWebクリエイター、山田太郎です。React・Vueなどのフロントエンド技術を軸に、使いやすく美しいUI/UX設計を得意としています。趣味は写真とガジェットレビュー。気になったことはすぐコードに落とすタイプです。</p>
        <div class="skills">
          <div class="skill">
            <span>HTML/CSS</span>
            <div class="bar"><div style="width: 95%;"></div></div>
          </div>
          <div class="skill">
            <span>JavaScript</span>
            <div class="bar"><div style="width: 90%;"></div></div>
          </div>
          <div class="skill">
            <span>React</span>
            <div class="bar"><div style="width: 85%;"></div></div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <section>
    <h2>最新のブログ</h2>
    <div class="blog-cards">
      <div class="card">
        <h3>React vs Vue 徹底比較2025</h3>
        <p>どちらがプロジェクトに向いてる？学習コスト・パフォーマンス・将来性から分析しました。</p>
        <a href="#">→ 記事を読む</a>
      </div>
      <div class="card">
        <h3>【保存版】ポートフォリオに入れるべき6項目</h3>
        <p>採用担当者が「見たい！」と感じる情報とは？経験者目線でまとめました。</p>
        <a href="#">→ 記事を読む</a>
      </div>
      <div class="card">
        <h3>フリーランス1年目のリアル収支と学び</h3>
        <p>勢いで独立した1年目のリアルな体験談。収入・支出・心構えを赤裸々公開。</p>
        <a href="#">→ 記事を読む</a>
      </div>
    </div>
  </section>

  <section class="contact">
    <h2>お問い合わせ</h2>
    <form>
      <input type="text" placeholder="お名前" required>
      <input type="email" placeholder="メールアドレス" required>
      <textarea rows="5" placeholder="お問い合わせ内容" required></textarea>
      <button type="submit">送信</button>
    </form>
  </section>

</div>

<footer>
  <p>© 2025 山田太郎</p>
  <div class="social">
    <a href="#">🐦</a>
    <a href="#">💼</a>
    <a href="#">📷</a>
  </div>
</footer>

</body>
</html>
