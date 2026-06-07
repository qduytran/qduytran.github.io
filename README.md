<!DOCTYPE html>
<html lang="vi">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Tên Của Bạn — Blog Cá Nhân</title>
  <meta name="description" content="Blog chia sẻ cuộc sống, trải nghiệm và những điều thú vị mỗi ngày." />

  <!-- Fonts -->
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,700;1,400&family=DM+Sans:wght@300;400;500&display=swap" rel="stylesheet" />

  <style>
    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

    :root {
      --cream: #FDF8F3;
      --warm-white: #FFFBF7;
      --coral: #FF6B6B;
      --coral-light: #FFE8E8;
      --peach: #FFAA85;
      --sage: #7DB3A0;
      --sage-light: #E6F2EE;
      --sky: #A8D8EA;
      --sky-light: #EEF7FB;
      --marigold: #F9C74F;
      --marigold-light: #FEF6D8;
      --ink: #2C2C2C;
      --muted: #888880;
      --border: rgba(0,0,0,0.08);
      --shadow: 0 4px 24px rgba(0,0,0,0.07);
    }

    html { scroll-behavior: smooth; }

    body {
      font-family: 'DM Sans', sans-serif;
      background: var(--cream);
      color: var(--ink);
      font-size: 16px;
      line-height: 1.7;
    }

    /* ── NAV ── */
    nav {
      position: sticky; top: 0; z-index: 100;
      background: rgba(253,248,243,0.92);
      backdrop-filter: blur(12px);
      border-bottom: 1px solid var(--border);
      padding: 0 2rem;
      display: flex; align-items: center; justify-content: space-between;
      height: 64px;
    }
    .nav-logo {
      font-family: 'Playfair Display', serif;
      font-size: 1.4rem; font-weight: 700;
      color: var(--ink); text-decoration: none;
      letter-spacing: -0.5px;
    }
    .nav-logo span { color: var(--coral); }
    .nav-links { display: flex; gap: 2rem; list-style: none; }
    .nav-links a {
      text-decoration: none; color: var(--muted);
      font-size: 0.9rem; font-weight: 500;
      transition: color 0.2s;
    }
    .nav-links a:hover { color: var(--coral); }

    /* ── HERO ── */
    .hero {
      max-width: 960px; margin: 0 auto;
      padding: 5rem 2rem 3rem;
      display: grid; grid-template-columns: 1fr 280px; gap: 3rem; align-items: center;
    }
    .hero-eyebrow {
      font-size: 0.8rem; font-weight: 500; letter-spacing: 2px;
      text-transform: uppercase; color: var(--coral);
      margin-bottom: 1rem;
    }
    .hero h1 {
      font-family: 'Playfair Display', serif;
      font-size: clamp(2.2rem, 4vw, 3.2rem);
      font-weight: 700; line-height: 1.15;
      color: var(--ink); margin-bottom: 1.2rem;
    }
    .hero h1 em { font-style: italic; color: var(--coral); }
    .hero-desc {
      color: var(--muted); font-size: 1rem;
      max-width: 420px; margin-bottom: 2rem;
    }
    .hero-cta {
      display: inline-flex; align-items: center; gap: 8px;
      background: var(--coral); color: #fff;
      padding: 0.7rem 1.6rem; border-radius: 999px;
      text-decoration: none; font-weight: 500; font-size: 0.9rem;
      transition: transform 0.2s, box-shadow 0.2s;
      box-shadow: 0 4px 16px rgba(255,107,107,0.35);
    }
    .hero-cta:hover { transform: translateY(-2px); box-shadow: 0 8px 24px rgba(255,107,107,0.4); }
    .hero-avatar-wrap { text-align: center; }
    .hero-avatar {
      width: 220px; height: 220px;
      border-radius: 60% 40% 55% 45% / 50% 55% 45% 50%;
      object-fit: cover;
      background: linear-gradient(135deg, var(--coral-light), var(--marigold-light));
      display: flex; align-items: center; justify-content: center;
      font-family: 'Playfair Display', serif;
      font-size: 5rem; color: var(--coral);
      margin: 0 auto 1rem;
      border: 4px solid #fff;
      box-shadow: var(--shadow);
    }
    .hero-tagline {
      font-size: 0.85rem; color: var(--muted);
      font-style: italic;
    }

    /* ── PILLS / TOPICS ── */
    .topics {
      max-width: 960px; margin: 0 auto;
      padding: 0 2rem 3rem;
      display: flex; flex-wrap: wrap; gap: 10px;
    }
    .pill {
      display: inline-flex; align-items: center; gap: 6px;
      padding: 6px 16px; border-radius: 999px;
      font-size: 0.82rem; font-weight: 500;
      border: 1.5px solid transparent; text-decoration: none;
      transition: transform 0.15s;
    }
    .pill:hover { transform: translateY(-2px); }
    .pill.coral { background: var(--coral-light); color: #cc4444; border-color: #ffcaca; }
    .pill.sage  { background: var(--sage-light);  color: #3d7a66; border-color: #bcd8d1; }
    .pill.sky   { background: var(--sky-light);   color: #3380a0; border-color: #c0dfe8; }
    .pill.gold  { background: var(--marigold-light); color: #a07c10; border-color: #f3d98a; }

    /* ── SECTION TITLES ── */
    .section { max-width: 960px; margin: 0 auto; padding: 2rem 2rem 4rem; }
    .section-header {
      display: flex; align-items: baseline; justify-content: space-between;
      margin-bottom: 2rem; padding-bottom: 1rem;
      border-bottom: 1.5px solid var(--border);
    }
    .section-title {
      font-family: 'Playfair Display', serif;
      font-size: 1.6rem; font-weight: 700;
    }
    .section-link {
      font-size: 0.85rem; color: var(--coral); text-decoration: none; font-weight: 500;
    }
    .section-link:hover { text-decoration: underline; }

    /* ── FEATURED POST ── */
    .featured-post {
      display: grid; grid-template-columns: 1fr 1fr; gap: 2rem;
      background: #fff; border-radius: 20px; overflow: hidden;
      border: 1px solid var(--border); box-shadow: var(--shadow);
      margin-bottom: 2rem;
      text-decoration: none; color: inherit;
      transition: transform 0.25s, box-shadow 0.25s;
    }
    .featured-post:hover { transform: translateY(-4px); box-shadow: 0 12px 40px rgba(0,0,0,0.1); }
    .featured-img {
      background: linear-gradient(135deg, #FFE8E8 0%, #FFD4B8 50%, #FFF0D4 100%);
      min-height: 280px;
      display: flex; align-items: center; justify-content: center;
      font-size: 4rem;
    }
    .featured-body { padding: 2rem; display: flex; flex-direction: column; justify-content: center; }
    .post-tag {
      display: inline-block; font-size: 0.72rem; font-weight: 600;
      letter-spacing: 1.5px; text-transform: uppercase;
      color: var(--coral); margin-bottom: 0.75rem;
    }
    .featured-body h2 {
      font-family: 'Playfair Display', serif;
      font-size: 1.5rem; font-weight: 700; line-height: 1.3;
      margin-bottom: 0.75rem;
    }
    .featured-body p { color: var(--muted); font-size: 0.9rem; margin-bottom: 1.25rem; }
    .post-meta { display: flex; align-items: center; gap: 12px; font-size: 0.8rem; color: var(--muted); }
    .meta-dot { width: 3px; height: 3px; border-radius: 50%; background: var(--muted); }

    /* ── POST GRID ── */
    .post-grid { display: grid; grid-template-columns: repeat(3,1fr); gap: 1.5rem; }
    .post-card {
      background: #fff; border-radius: 16px;
      border: 1px solid var(--border);
      overflow: hidden; text-decoration: none; color: inherit;
      transition: transform 0.2s, box-shadow 0.2s;
      display: flex; flex-direction: column;
    }
    .post-card:hover { transform: translateY(-4px); box-shadow: var(--shadow); }
    .card-img {
      height: 160px;
      display: flex; align-items: center; justify-content: center;
      font-size: 2.5rem;
    }
    .card-img.coral { background: linear-gradient(135deg, #FFE8E8, #FFD4B8); }
    .card-img.sage  { background: linear-gradient(135deg, #E6F2EE, #D4EDE5); }
    .card-img.sky   { background: linear-gradient(135deg, #EEF7FB, #D8EDF5); }
    .card-body { padding: 1.2rem; flex: 1; display: flex; flex-direction: column; }
    .card-body h3 {
      font-family: 'Playfair Display', serif;
      font-size: 1.05rem; font-weight: 700; line-height: 1.35;
      margin-bottom: 0.5rem;
    }
    .card-body p { color: var(--muted); font-size: 0.85rem; flex: 1; }
    .card-footer {
      padding: 0.8rem 1.2rem;
      border-top: 1px solid var(--border);
      font-size: 0.78rem; color: var(--muted);
      display: flex; justify-content: space-between;
    }

    /* ── ABOUT STRIP ── */
    .about-strip {
      background: #fff; border-radius: 20px;
      border: 1px solid var(--border);
      padding: 2.5rem 3rem;
      display: grid; grid-template-columns: 1fr auto; gap: 3rem; align-items: center;
    }
    .about-strip h2 {
      font-family: 'Playfair Display', serif;
      font-size: 1.5rem; margin-bottom: 0.75rem;
    }
    .about-strip p { color: var(--muted); font-size: 0.95rem; max-width: 500px; margin-bottom: 1.25rem; }
    .social-row { display: flex; gap: 10px; }
    .social-btn {
      display: inline-flex; align-items: center; gap: 6px;
      padding: 7px 16px; border-radius: 999px;
      border: 1.5px solid var(--border); background: transparent;
      font-size: 0.82rem; font-weight: 500; color: var(--ink);
      text-decoration: none; transition: background 0.15s, border-color 0.15s;
      cursor: pointer;
    }
    .social-btn:hover { background: var(--coral-light); border-color: #ffcaca; color: var(--coral); }
    .stats { display: flex; flex-direction: column; gap: 1rem; text-align: center; }
    .stat-num {
      font-family: 'Playfair Display', serif;
      font-size: 2rem; font-weight: 700; color: var(--coral);
      line-height: 1;
    }
    .stat-label { font-size: 0.78rem; color: var(--muted); }

    /* ── NEWSLETTER ── */
    .newsletter {
      background: linear-gradient(135deg, #FF6B6B 0%, #FFAA85 100%);
      border-radius: 20px; padding: 3rem;
      text-align: center; color: #fff;
    }
    .newsletter h2 {
      font-family: 'Playfair Display', serif;
      font-size: 1.8rem; margin-bottom: 0.5rem;
    }
    .newsletter p { opacity: 0.88; margin-bottom: 1.5rem; font-size: 0.95rem; }
    .nl-form { display: flex; gap: 10px; max-width: 420px; margin: 0 auto; }
    .nl-form input {
      flex: 1; padding: 0.7rem 1.2rem;
      border-radius: 999px; border: none; outline: none;
      font-family: 'DM Sans', sans-serif; font-size: 0.9rem;
    }
    .nl-form button {
      padding: 0.7rem 1.4rem; border-radius: 999px;
      background: var(--ink); color: #fff; border: none;
      font-family: 'DM Sans', sans-serif; font-weight: 500; font-size: 0.9rem;
      cursor: pointer; transition: opacity 0.2s;
    }
    .nl-form button:hover { opacity: 0.85; }

    /* ── FOOTER ── */
    footer {
      text-align: center; padding: 3rem 2rem;
      font-size: 0.83rem; color: var(--muted);
      border-top: 1px solid var(--border); margin-top: 3rem;
    }
    footer a { color: var(--coral); text-decoration: none; }

    /* ── RESPONSIVE ── */
    @media (max-width: 768px) {
      .hero { grid-template-columns: 1fr; padding: 3rem 1.5rem 2rem; }
      .hero-avatar-wrap { order: -1; }
      .hero-avatar { width: 160px; height: 160px; font-size: 3.5rem; }
      .featured-post { grid-template-columns: 1fr; }
      .featured-img { min-height: 200px; }
      .post-grid { grid-template-columns: 1fr; }
      .about-strip { grid-template-columns: 1fr; }
      .stats { flex-direction: row; justify-content: center; gap: 2rem; }
      nav { padding: 0 1.25rem; }
      .nav-links { display: none; }
      .section { padding: 1.5rem 1.25rem 3rem; }
    }
  </style>
</head>
<body>

<!-- NAV -->
<nav>
  <a href="#" class="nav-logo">Tên<span>.</span></a>
  <ul class="nav-links">
    <li><a href="#bai-viet">Bài viết</a></li>
    <li><a href="#ve-toi">Về tôi</a></li>
    <li><a href="#lien-he">Liên hệ</a></li>
  </ul>
</nav>

<!-- HERO -->
<header class="hero">
  <div>
    <p class="hero-eyebrow">✦ Chào mừng bạn đến blog của mình</p>
    <h1>Chia sẻ cuộc sống qua từng <em>câu chuyện</em></h1>
    <p class="hero-desc">
      Mình là <strong>Tên Của Bạn</strong> — một người yêu thích khám phá, viết lách và trân trọng những khoảnh khắc nhỏ bé của cuộc sống hàng ngày.
    </p>
    <a href="#bai-viet" class="hero-cta">Đọc bài viết mới ↓</a>
  </div>
  <div class="hero-avatar-wrap">
    <!-- Thay src="..." bằng ảnh thật của bạn -->
    <div class="hero-avatar">🌸</div>
    <p class="hero-tagline">"Sống chậm lại, yêu nhiều hơn."</p>
  </div>
</header>

<!-- TOPICS -->
<div class="topics">
  <a href="#" class="pill coral">🌿 Cuộc sống</a>
  <a href="#" class="pill sage">📚 Sách hay</a>
  <a href="#" class="pill sky">✈️ Du lịch</a>
  <a href="#" class="pill gold">☕ Quán cà phê</a>
  <a href="#" class="pill coral">💭 Suy nghĩ</a>
  <a href="#" class="pill sage">🎵 Âm nhạc</a>
  <a href="#" class="pill sky">🍜 Ẩm thực</a>
</div>

<!-- FEATURED POST -->
<section class="section" id="bai-viet">
  <div class="section-header">
    <h2 class="section-title">Bài viết nổi bật</h2>
    <a href="#" class="section-link">Xem tất cả →</a>
  </div>

  <a href="#" class="featured-post">
    <div class="featured-img">🌸</div>
    <div class="featured-body">
      <span class="post-tag">✦ Cuộc sống</span>
      <h2>Tôi đã học cách "sống chậm lại" như thế nào?</h2>
      <p>
        Một buổi sáng tôi ngồi cạnh cửa sổ, ngắm mưa rơi và nhận ra mình đã quá bận rộn để nhận thấy những điều nhỏ bé xung quanh. Bài viết này là hành trình tìm lại sự bình yên...
      </p>
      <div class="post-meta">
        <span>01 tháng 6, 2025</span>
        <span class="meta-dot"></span>
        <span>5 phút đọc</span>
        <span class="meta-dot"></span>
        <span>🤍 128 lượt thích</span>
      </div>
    </div>
  </a>
</section>

<!-- POST GRID -->
<section class="section">
  <div class="section-header">
    <h2 class="section-title">Bài viết gần đây</h2>
    <a href="#" class="section-link">Xem tất cả →</a>
  </div>
  <div class="post-grid">
    <a href="#" class="post-card">
      <div class="card-img coral">☕</div>
      <div class="card-body">
        <span class="post-tag">Quán cà phê</span>
        <h3>5 quán cà phê yên tĩnh nhất Sài Gòn để làm việc và đọc sách</h3>
        <p>Những không gian bình yên, không ồn ào, phù hợp để ngồi cả buổi sáng...</p>
      </div>
      <div class="card-footer">
        <span>28/05/2025</span>
        <span>4 phút đọc</span>
      </div>
    </a>
    <a href="#" class="post-card">
      <div class="card-img sage">📖</div>
      <div class="card-body">
        <span class="post-tag">Sách hay</span>
        <h3>Review sách: "Ikigai – Bí quyết sống trường thọ và hạnh phúc"</h3>
        <p>Người Nhật sống lâu vì họ có một lý do để thức dậy mỗi sáng. Cuốn sách này thay đổi cách mình nhìn cuộc sống...</p>
      </div>
      <div class="card-footer">
        <span>20/05/2025</span>
        <span>6 phút đọc</span>
      </div>
    </a>
    <a href="#" class="post-card">
      <div class="card-img sky">✈️</div>
      <div class="card-body">
        <span class="post-tag">Du lịch</span>
        <h3>Đà Lạt một mình – Hành trình tìm lại bản thân</h3>
        <p>Ba ngày ở Đà Lạt, không có kế hoạch cụ thể, chỉ đi theo cảm xúc và khám phá những góc khuất của thành phố sương mù...</p>
      </div>
      <div class="card-footer">
        <span>12/05/2025</span>
        <span>7 phút đọc</span>
      </div>
    </a>
  </div>
</section>

<!-- ABOUT -->
<section class="section" id="ve-toi">
  <div class="about-strip">
    <div>
      <h2>Xin chào, mình là Tên Của Bạn 👋</h2>
      <p>
        Mình là một người yêu thích viết lách, du lịch và khám phá ẩm thực. Blog này là nơi mình lưu giữ những câu chuyện, trải nghiệm và suy nghĩ của bản thân. Mình tin rằng mỗi ngày đều có điều gì đó đáng để kể lại.
      </p>
      <div class="social-row">
        <a href="https://facebook.com/" class="social-btn">📘 Facebook</a>
        <a href="https://instagram.com/" class="social-btn">📸 Instagram</a>
        <a href="mailto:email@example.com" class="social-btn">✉️ Email</a>
      </div>
    </div>
    <div class="stats">
      <div>
        <div class="stat-num">42</div>
        <div class="stat-label">Bài viết</div>
      </div>
      <div>
        <div class="stat-num">3K+</div>
        <div class="stat-label">Độc giả</div>
      </div>
      <div>
        <div class="stat-num">2</div>
        <div class="stat-label">Năm viết</div>
      </div>
    </div>
  </div>
</section>

<!-- NEWSLETTER -->
<section class="section" id="lien-he">
  <div class="newsletter">
    <h2>Đừng bỏ lỡ bài viết mới! 🌼</h2>
    <p>Đăng ký để nhận thông báo mỗi khi mình có bài viết mới. Không spam, chỉ toàn nội dung hay.</p>
    <div class="nl-form">
      <input type="email" placeholder="email@example.com" />
      <button type="button">Đăng ký</button>
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <p>Làm với 🤍 bởi <a href="#">Tên Của Bạn</a> · 2025</p>
  <p style="margin-top: 6px;">Xây dựng trên <a href="#">GitHub Pages</a></p>
</footer>

</body>
</html>
