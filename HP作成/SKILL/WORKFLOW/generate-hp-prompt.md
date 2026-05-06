<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <meta name="format-detection" content="telephone=no" />
  <title>伊東尚悟 | 北海道議会議員（釧路）公式サイト</title>
  <meta name="description" content="伊東尚悟公式サイト。誇りと希望を持てる北海道・釧路を目指し、政策・活動・メッセージを発信します。" />
  <link rel="canonical" href="https://example.com/" />
  <meta property="og:type" content="website" />
  <meta property="og:url" content="https://example.com/" />
  <meta property="og:title" content="伊東尚悟 | 北海道議会議員（釧路）公式サイト" />
  <meta property="og:description" content="誇りと希望を持てる北海道・釧路を創る。伊東尚悟の政策と活動を掲載しています。" />
  <meta property="og:image" content="./assets/og/ogp.jpg" />
  <meta name="twitter:card" content="summary_large_image" />
  <meta name="twitter:title" content="伊東尚悟 | 北海道議会議員（釧路）公式サイト" />
  <meta name="twitter:description" content="誇りと希望を持てる北海道・釧路を創る。伊東尚悟の政策と活動を掲載しています。" />
  <meta name="twitter:image" content="./assets/og/ogp.jpg" />
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link href="https://fonts.googleapis.com/css2?family=Noto+Sans+JP:wght@400;500;700;900&display=swap" rel="stylesheet" />
  <script type="application/ld+json">
  {
    "@context": "https://schema.org",
    "@graph": [
      {
        "@type": "Person",
        "name": "伊東尚悟",
        "jobTitle": "北海道議会議員",
        "description": "釧路地域を中心に活動する北海道議会議員",
        "url": "https://example.com/"
      },
      {
        "@type": "WebSite",
        "name": "伊東尚悟公式サイト",
        "url": "https://example.com/",
        "inLanguage": "ja"
      },
      {
        "@type": "Organization",
        "name": "伊東尚悟後援会",
        "url": "https://example.com/"
      }
    ]
  }
  </script>
  <style>
    :root {
      --color-primary: #0f2747;
      --color-primary-strong: #0a1b33;
      --color-accent: #f59e0b;
      --color-bg: #f8fafc;
      --color-surface: #ffffff;
      --color-text: #1f2937;
      --color-text-muted: #6b7280;
      --font-base: "Noto Sans JP", "Hiragino Kaku Gothic ProN", sans-serif;
      --font-size-sm: 0.875rem;
      --font-size-md: 1rem;
      --font-size-lg: 1.25rem;
      --font-size-xl: 2rem;
      --space-1: 0.25rem;
      --space-2: 0.5rem;
      --space-3: 0.75rem;
      --space-4: 1rem;
      --space-6: 1.5rem;
      --space-8: 2rem;
      --space-12: 3rem;
      --radius-sm: 0.375rem;
      --radius-md: 0.75rem;
      --radius-lg: 1rem;
      --shadow-sm: 0 1px 2px rgba(15, 39, 71, 0.08);
      --shadow-md: 0 8px 24px rgba(15, 39, 71, 0.12);
      --container: 1120px;
    }

    * { box-sizing: border-box; }
    html { scroll-behavior: smooth; }
    body {
      margin: 0;
      font-family: var(--font-base);
      font-size: var(--font-size-md);
      color: var(--color-text);
      line-height: 1.7;
      background: var(--color-bg);
    }
    a { color: inherit; text-decoration: none; }
    img { max-width: 100%; display: block; }
    .container { width: min(var(--container), calc(100% - 2rem)); margin: 0 auto; }
    .skip-link {
      position: absolute;
      left: -999px;
      top: 0;
      z-index: 200;
      background: var(--color-surface);
      color: var(--color-primary);
      padding: 0.6rem 0.9rem;
      border-radius: var(--radius-sm);
      box-shadow: var(--shadow-sm);
    }
    .skip-link:focus { left: 1rem; top: 1rem; }

    .site-header {
      position: sticky;
      top: 0;
      z-index: 120;
      background: rgba(255, 255, 255, 0.95);
      border-bottom: 1px solid rgba(15, 39, 71, 0.12);
      backdrop-filter: blur(10px);
    }
    .header-row {
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 1rem;
      min-height: 72px;
    }
    .brand-title {
      margin: 0;
      font-size: 1.5rem;
      font-weight: 900;
      line-height: 1.2;
      color: var(--color-primary);
    }
    .brand-sub {
      margin: 0.1rem 0 0;
      font-size: var(--font-size-sm);
      color: var(--color-text-muted);
    }
    .menu-toggle {
      width: 44px;
      height: 44px;
      border: 1px solid rgba(15, 39, 71, 0.2);
      border-radius: var(--radius-sm);
      background: var(--color-surface);
      color: var(--color-primary);
      display: inline-flex;
      align-items: center;
      justify-content: center;
      cursor: pointer;
    }
    .site-nav { display: none; border-top: 1px solid rgba(15, 39, 71, 0.12); }
    .site-nav.is-open { display: block; }
    .site-nav ul {
      list-style: none;
      margin: 0;
      padding: 0.75rem 0 1rem;
      display: grid;
      gap: 0.5rem;
    }
    .site-nav a {
      display: block;
      padding: 0.55rem 0.7rem;
      border-radius: var(--radius-sm);
      font-weight: 500;
    }
    .site-nav a:hover,
    .site-nav a:focus-visible { background: rgba(15, 39, 71, 0.08); outline: none; }

    .hero {
      position: relative;
      min-height: 80vh;
      color: #fff;
      display: flex;
      align-items: center;
      background-image: linear-gradient(110deg, rgba(10, 27, 51, 0.93), rgba(15, 39, 71, 0.72)), url("./assets/hero/hero-main.jpg");
      background-size: cover;
      background-position: center;
    }
    .hero-inner { padding: 4.5rem 0 4rem; }
    .hero-eyebrow {
      margin: 0;
      letter-spacing: 0.16em;
      font-size: 0.8rem;
      font-weight: 700;
      color: #f7c76d;
    }
    h1 {
      margin: 0.7rem 0 0;
      font-size: clamp(1.8rem, 3.8vw, 3.2rem);
      line-height: 1.25;
      font-weight: 900;
    }
    .hero-copy {
      max-width: 700px;
      margin-top: var(--space-4);
      color: rgba(255, 255, 255, 0.92);
      font-size: var(--font-size-lg);
    }
    .cta-row {
      margin-top: var(--space-8);
      display: flex;
      flex-wrap: wrap;
      gap: 0.75rem;
    }
    .btn {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      min-height: 48px;
      padding: 0.75rem 1.2rem;
      border-radius: 999px;
      font-weight: 700;
      border: 1px solid transparent;
      transition: transform 0.2s ease, box-shadow 0.2s ease, background-color 0.2s ease;
    }
    .btn:focus-visible { outline: 2px solid #fff; outline-offset: 2px; }
    .btn-primary {
      color: #1f1f1f;
      background: var(--color-accent);
      box-shadow: var(--shadow-sm);
    }
    .btn-secondary {
      color: #fff;
      border-color: rgba(255, 255, 255, 0.8);
      background: transparent;
    }
    .btn-dark {
      color: #fff;
      background: var(--color-primary);
    }
    .btn-outline {
      color: var(--color-primary);
      border-color: rgba(15, 39, 71, 0.35);
      background: var(--color-surface);
    }
    .btn:hover { transform: translateY(-1px); box-shadow: var(--shadow-md); }

    section { padding: 4.25rem 0; }
    .surface { background: var(--color-surface); }
    .section-head { margin-bottom: var(--space-8); }
    .section-label {
      margin: 0;
      color: var(--color-accent);
      letter-spacing: 0.16em;
      font-size: 0.75rem;
      font-weight: 700;
    }
    h2 {
      margin: 0.4rem 0 0;
      font-size: clamp(1.5rem, 3vw, var(--font-size-xl));
      line-height: 1.35;
      color: var(--color-primary);
    }
    .lead { margin-top: var(--space-3); color: var(--color-text-muted); max-width: 760px; }
    .card-grid {
      display: grid;
      gap: var(--space-4);
      grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
    }
    .card {
      background: var(--color-surface);
      border: 1px solid rgba(15, 39, 71, 0.12);
      border-radius: var(--radius-md);
      padding: 1.2rem;
      box-shadow: var(--shadow-sm);
    }
    .card h3 { margin: 0; font-size: 1.08rem; color: var(--color-primary); }
    .card p { margin: 0.55rem 0 0; color: var(--color-text-muted); }
    .accent-band {
      background: linear-gradient(135deg, rgba(245, 158, 11, 0.18), rgba(15, 39, 71, 0.06));
      border: 1px solid rgba(245, 158, 11, 0.28);
      border-radius: var(--radius-lg);
      padding: 1.3rem;
      margin-top: var(--space-6);
    }
    .message-block {
      background: var(--color-surface);
      border-radius: var(--radius-lg);
      box-shadow: var(--shadow-sm);
      border: 1px solid rgba(15, 39, 71, 0.1);
      padding: 1.4rem;
    }
    .message-block p { margin: 0 0 0.9rem; }
    .message-block p:last-child { margin-bottom: 0; }
    .timeline {
      list-style: none;
      margin: 0;
      padding: 0;
      display: grid;
      gap: var(--space-4);
    }
    .timeline li {
      background: var(--color-surface);
      border-radius: var(--radius-md);
      border: 1px solid rgba(15, 39, 71, 0.12);
      padding: 1rem 1.1rem;
      box-shadow: var(--shadow-sm);
    }
    .timeline strong { color: var(--color-primary); }
    .faq-list { display: grid; gap: var(--space-3); }
    details {
      background: var(--color-surface);
      border-radius: var(--radius-md);
      border: 1px solid rgba(15, 39, 71, 0.12);
      padding: 0.9rem 1rem;
    }
    summary {
      cursor: pointer;
      font-weight: 700;
      color: var(--color-primary);
    }
    details p { margin: 0.75rem 0 0; color: var(--color-text-muted); }
    .cta-panel {
      background: linear-gradient(140deg, var(--color-primary), var(--color-primary-strong));
      color: #fff;
      border-radius: var(--radius-lg);
      padding: 1.6rem;
      box-shadow: var(--shadow-md);
    }
    .cta-panel h3 { margin: 0; font-size: 1.3rem; }
    .cta-panel p { margin: 0.6rem 0 0; color: rgba(255, 255, 255, 0.9); }
    .cta-panel .cta-row { margin-top: 1rem; }
    .contact-form {
      margin-top: var(--space-6);
      display: grid;
      gap: var(--space-3);
    }
    .contact-form label { font-weight: 700; color: var(--color-primary); }
    .contact-form input,
    .contact-form textarea {
      width: 100%;
      font: inherit;
      color: var(--color-text);
      padding: 0.75rem 0.85rem;
      border-radius: var(--radius-sm);
      border: 1px solid rgba(15, 39, 71, 0.25);
      background: #fff;
    }
    .contact-form textarea { min-height: 160px; resize: vertical; }
    .contact-form input:focus,
    .contact-form textarea:focus {
      outline: 2px solid rgba(245, 158, 11, 0.5);
      border-color: var(--color-accent);
    }
    .status {
      margin-top: 0.75rem;
      padding: 0.65rem 0.8rem;
      border-radius: var(--radius-sm);
      background: #ecfdf5;
      color: #065f46;
      font-size: var(--font-size-sm);
      display: none;
    }
    .status.is-show { display: block; }
    .site-footer {
      background: var(--color-primary-strong);
      color: rgba(255, 255, 255, 0.9);
      padding: 2.4rem 0;
    }
    .site-footer a { text-decoration: underline; }
    .foot-title { margin: 0; font-size: 1rem; color: #f5c573; }
    .copy { margin-top: var(--space-6); font-size: 0.8rem; color: rgba(255, 255, 255, 0.6); }
    .text-center { text-align: center; }

    @media (min-width: 900px) {
      .menu-toggle { display: none; }
      .site-nav {
        display: block;
        border-top: 0;
      }
      .site-nav ul {
        display: flex;
        align-items: center;
        justify-content: flex-end;
        gap: 0.2rem;
        padding: 0;
      }
      .header-row { min-height: 84px; }
      section { padding: 5rem 0; }
      .hero-inner { padding: 6.2rem 0 5.5rem; }
    }
  </style>
</head>
<body>
  <a class="skip-link" href="#main">メインコンテンツへ移動</a>

  <header class="site-header">
    <div class="container header-row">
      <a href="#hero" aria-label="ページ先頭へ">
        <p class="brand-title">伊東 尚悟</p>
        <p class="brand-sub">北海道議会議員（釧路）公式サイト</p>
      </a>
      <button id="menu-toggle" class="menu-toggle" type="button" aria-expanded="false" aria-controls="global-nav" aria-label="メニューを開く">
        <svg width="20" height="20" viewBox="0 0 24 24" fill="none" aria-hidden="true">
          <path d="M4 6h16M4 12h16M4 18h16" stroke="currentColor" stroke-width="2" stroke-linecap="round" />
        </svg>
      </button>
      <nav id="global-nav" class="site-nav" aria-label="グローバルナビゲーション">
        <ul>
          <li><a href="#message">メッセージ</a></li>
          <li><a href="#problem">地域課題</a></li>
          <li><a href="#solution">解決策</a></li>
          <li><a href="#strength">強み</a></li>
          <li><a href="#flow">ご参加方法</a></li>
          <li><a href="#faq">FAQ</a></li>
          <li><a href="#contact">お問い合わせ</a></li>
        </ul>
      </nav>
    </div>
  </header>

  <main id="main">
    <section id="hero" class="hero">
      <div class="container hero-inner">
        <p class="hero-eyebrow">KUSHIRO / HOKKAIDO</p>
        <h1>誇りと希望を持てる北海道、<br />釧路を創る。</h1>
        <p class="hero-copy">現場の声を起点に、暮らし・産業・子育て・防災の課題に向き合い、次の世代へ誇れる地域の未来を形にします。</p>
        <div class="cta-row">
          <a class="btn btn-primary" href="#contact">ご意見を送る</a>
          <a class="btn btn-secondary" href="#solution">重点政策を見る</a>
        </div>
      </div>
    </section>

    <section id="message" class="surface">
      <div class="container">
        <div class="section-head">
          <p class="section-label">MESSAGE</p>
          <h2>一人ひとりの声に耳を傾ける政治へ</h2>
        </div>
        <div class="message-block">
          <p>私は釧路市議会議員として3期9年、地域の現場で課題解決に取り組んできました。物価高騰や人口減少、産業構造の変化のなかで、「明日の暮らしが不安だ」という切実な声を受け止めてきました。</p>
          <p>だからこそ、政治に必要なのは机上の理屈だけではなく、現場の実感に寄り添い、具体策へ落とし込む実行力です。</p>
          <p>釧路の可能性を信じ、誰もが希望を持てる北海道を、皆さまとともに実現していきます。</p>
          <p><strong>伊東 尚悟</strong></p>
        </div>
      </div>
    </section>

    <section id="problem">
      <div class="container">
        <div class="section-head">
          <p class="section-label">PROBLEM</p>
          <h2>今、釧路が向き合う3つの課題</h2>
          <p class="lead">情報を整理し、優先度を明確にして取り組むことが、成果につながる第一歩です。</p>
        </div>
        <div class="card-grid">
          <article class="card">
            <h3>暮らしの不安の拡大</h3>
            <p>物価高騰と実質賃金の伸び悩みが、家庭の家計に大きな負担を与えています。</p>
          </article>
          <article class="card">
            <h3>地域産業の担い手不足</h3>
            <p>一次産業・観光・中小企業で人材確保が難しく、地域経済の循環が弱まっています。</p>
          </article>
          <article class="card">
            <h3>子育て・教育環境の地域差</h3>
            <p>家庭背景や居住エリアによって、教育機会と支援の受けやすさに差が生まれています。</p>
          </article>
        </div>
      </div>
    </section>

    <section id="solution" class="surface">
      <div class="container">
        <div class="section-head">
          <p class="section-label">SOLUTION</p>
          <h2>課題に対する重点政策</h2>
          <p class="lead">「暮らし」「産業」「未来」の3軸で、実行可能な政策を積み重ねます。</p>
        </div>
        <div class="card-grid">
          <article class="card">
            <h3>生活を守る支援強化</h3>
            <p>生活コストの上昇に対し、子育て世帯・高齢世帯・働く世代を支える制度の拡充を進めます。</p>
          </article>
          <article class="card">
            <h3>地元産業の競争力向上</h3>
            <p>現場ニーズに合わせた設備投資・販路開拓・担い手育成支援を一体で推進します。</p>
          </article>
          <article class="card">
            <h3>教育と防災への投資</h3>
            <p>子どもの学びと地域防災の両輪を強化し、将来不安の少ないまちづくりを進めます。</p>
          </article>
        </div>
        <div class="accent-band">
          <strong>政策は「つくって終わり」ではありません。</strong>
          <p>実行状況と成果を分かりやすく公開し、改善を続けることで、地域の信頼に応えます。</p>
        </div>
      </div>
    </section>

    <section id="strength">
      <div class="container">
        <div class="section-head">
          <p class="section-label">STRENGTHS</p>
          <h2>伊東尚悟の3つの強み</h2>
        </div>
        <div class="card-grid">
          <article class="card">
            <h3>現場起点の対話力</h3>
            <p>生活者・事業者・若者・高齢者まで、立場の違う声を丁寧に聞き取り、政策に反映します。</p>
          </article>
          <article class="card">
            <h3>議会での継続的な実行</h3>
            <p>市議会3期9年の経験を土台に、課題を継続的に追い、具体的な改善につなげます。</p>
          </article>
          <article class="card">
            <h3>未来志向の地域ビジョン</h3>
            <p>目先の対処だけでなく、5年後・10年後を見据えた持続可能な地域づくりを進めます。</p>
          </article>
        </div>
      </div>
    </section>

    <section id="voice" class="surface">
      <div class="container">
        <div class="section-head">
          <p class="section-label">VOICE / CASE</p>
          <h2>活動を支える声と実績</h2>
        </div>
        <div class="card-grid">
          <article class="card">
            <h3>地域事業者の声</h3>
            <p>「小さな事業者の悩みに具体策で応えてくれる。相談のハードルが低いのが心強い。」</p>
          </article>
          <article class="card">
            <h3>子育て世代の声</h3>
            <p>「制度の説明が分かりやすく、何をどう改善したいのかが明確。安心して話せる。」</p>
          </article>
          <article class="card">
            <h3>地域活動での実践</h3>
            <p>街頭対話、地域行事、防災訓練など、顔の見える活動を継続して実施しています。</p>
          </article>
        </div>
        <div class="cta-row">
          <a class="btn btn-dark" href="#contact">活動へのご意見・ご提案はこちら</a>
        </div>
      </div>
    </section>

    <section id="flow">
      <div class="container">
        <div class="section-head">
          <p class="section-label">FLOW</p>
          <h2>ご参加・ご相談の流れ</h2>
        </div>
        <ol class="timeline">
          <li><strong>1. ご連絡</strong><br />お問い合わせフォームから、ご意見・ご相談・参加希望をお寄せください。</li>
          <li><strong>2. 内容確認</strong><br />事務所より内容を確認し、必要に応じて面談やオンラインでの対話機会をご案内します。</li>
          <li><strong>3. 対話・反映</strong><br />いただいた声を活動や政策提案に反映し、進捗を継続的に発信します。</li>
        </ol>
      </div>
    </section>

    <section id="faq" class="surface">
      <div class="container">
        <div class="section-head">
          <p class="section-label">FAQ</p>
          <h2>よくあるご質問</h2>
        </div>
        <div class="faq-list">
          <details>
            <summary>Q. 後援会に入会するにはどうすればよいですか？</summary>
            <p>A. お問い合わせフォームから「後援会入会希望」とご連絡ください。担当より手続きをご案内します。</p>
          </details>
          <details>
            <summary>Q. 政策への意見は誰でも送れますか？</summary>
            <p>A. はい。釧路地域にお住まいの方に限らず、北海道の未来に関するご意見を広く受け付けています。</p>
          </details>
          <details>
            <summary>Q. イベント情報はどこで確認できますか？</summary>
            <p>A. 本サイトのお知らせ欄および公式SNSで随時ご案内します。詳細はお問い合わせでも確認できます。</p>
          </details>
        </div>
      </div>
    </section>

    <section aria-label="中段CTA">
      <div class="container">
        <div class="cta-panel">
          <h3>釧路の未来づくりに、あなたの声を。</h3>
          <p>暮らしのこと、仕事のこと、子育てのこと。小さな声が、地域を動かす力になります。</p>
          <div class="cta-row">
            <a class="btn btn-primary" href="#contact">ご意見を送る</a>
            <a class="btn btn-secondary" href="#footer">事務所情報を見る</a>
          </div>
        </div>
      </div>
    </section>

    <section id="contact">
      <div class="container">
        <div class="section-head">
          <p class="section-label">CONTACT</p>
          <h2>お問い合わせ</h2>
          <p class="lead">取材依頼、政策へのご意見、後援会に関するご連絡を受け付けています。</p>
        </div>
        <form id="contact-form" class="contact-form">
          <div>
            <label for="name">お名前</label>
            <input id="name" name="name" type="text" required autocomplete="name" />
          </div>
          <div>
            <label for="email">メールアドレス</label>
            <input id="email" name="email" type="email" required autocomplete="email" />
          </div>
          <div>
            <label for="message">お問い合わせ内容</label>
            <textarea id="message" name="message" required></textarea>
          </div>
          <div class="cta-row">
            <button class="btn btn-dark" type="submit">送信する</button>
          </div>
        </form>
        <p id="form-status" class="status" role="status" aria-live="polite"></p>
      </div>
    </section>
  </main>

  <footer id="footer" class="site-footer">
    <div class="container">
      <p class="foot-title">伊東尚悟 後援会事務所</p>
      <address>
        〒085-0018 北海道釧路市〇〇〇〇（公開時に修正）<br />
        TEL: <a href="tel:0000000000">000-000-0000</a><br />
        MAIL: <a href="mailto:info@example.com">info@example.com</a>
      </address>
      <div class="cta-row">
        <a class="btn btn-primary" href="#contact">お問い合わせする</a>
      </div>
      <p class="copy">© 2026 伊東尚悟 後援会事務所</p>
    </div>
  </footer>

  <script>
    (function () {
      var toggle = document.getElementById("menu-toggle");
      var nav = document.getElementById("global-nav");
      if (!toggle || !nav) return;

      toggle.addEventListener("click", function () {
        var opened = nav.classList.toggle("is-open");
        toggle.setAttribute("aria-expanded", opened ? "true" : "false");
        toggle.setAttribute("aria-label", opened ? "メニューを閉じる" : "メニューを開く");
      });

      nav.querySelectorAll("a").forEach(function (link) {
        link.addEventListener("click", function () {
          if (window.innerWidth >= 900) return;
          nav.classList.remove("is-open");
          toggle.setAttribute("aria-expanded", "false");
          toggle.setAttribute("aria-label", "メニューを開く");
        });
      });
    })();

    (function () {
      var form = document.getElementById("contact-form");
      var status = document.getElementById("form-status");
      if (!form || !status) return;

      form.addEventListener("submit", function (event) {
        event.preventDefault();
        if (!form.checkValidity()) {
          form.reportValidity();
          return;
        }
        status.textContent = "お問い合わせを受け付けました（デモ表示）。担当よりご連絡いたします。";
        status.classList.add("is-show");
        form.reset();
      });
    })();
  </script>
</body>
</html>
