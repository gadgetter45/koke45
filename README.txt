<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>koke | Gadgetter </title>
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
  <h1>koke</h1>
  <p>群馬県在住のガジェッター</p>
</header>

<div class="container">

  <section>
    <h2>自己紹介</h2>
    <div class="about">
      <img src="https://via.placeholder.com/250" alt="プロフィール画像">
      <div>
        <p>こんにちは、群馬在住のYoutuber兼ガジェッター、kokeです。IPhoneの脱獄やandroid端末のwindows化などを楽しく投稿しています。</p>
        <div class="skills">
          <div class="skill">
            <span>HTML/金欠率</span>
            <div class="bar"><div style="width: 95%;"></div></div>
          </div>
          <div class="skill">
            <span>ガジェ知識</span>
            <div class="bar"><div style="width: 50%;"></div></div>
          </div>
          <div class="浮上率">
            <span>React</span>
            <div class="bar"><div style="width: 5%;"></div></div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <section>
    <h2>最新のブログ</h2>
    <div class="blog-cards">
      <div class="card">
        <h3>IPhone5は2025年にどこまで使えるか？</h3>
        <p>ios10,A6チップの限界に挑みます。</p>
        
      </div>
      <div class="card">
        <h3>IPhone4の分解と修復</h3>
        <p>リンゴループ化したIPhone4を復活させます。</p>
      
      </div>
      <div class="card">
        <h3>購入したIPhoneをレビュー‼</h3>
        <p>メルカリにて破格で購入したIPhone三台をレビューします</p>
       
      </div>
    </div>
  </section>

  <section class="contact">
    <h2>このサイトはβ版です。</h2>
   
  </section>

</div>

<footer>
  <p>© 2025 koke</p>
  <div class="social">
    <a href="#">Twitter</a>
 
  </div>
</footer>

</body>
</html>
