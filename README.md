<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Giri Stores | Since 1978</title>
    <style>
      :root {
        --green: #174f36;
        --green-2: #0d3626;
        --sage: #eaf4ee;
        --cream: #fffaf2;
        --gold: #d7a64f;
        --gold-soft: #f4dfb5;
        --text: #1b2a22;
        --muted: #58675d;
        --card: #ffffff;
        --border: #e9e0d1;
        --shadow: 0 18px 45px rgba(19, 40, 30, 0.12);
      }

      * {
        box-sizing: border-box;
        margin: 0;
        padding: 0;
      }

      html {
        scroll-behavior: smooth;
      }

      body {
        font-family: Georgia, "Times New Roman", serif;
        background: linear-gradient(180deg, #fffaf3 0%, #f8f1e7 100%);
        color: var(--text);
        line-height: 1.65;
      }

      img {
        max-width: 100%;
        display: block;
      }

      a {
        text-decoration: none;
      }

      .container {
        width: min(1120px, calc(100% - 32px));
        margin: 0 auto;
      }

      .section-tag {
        display: inline-block;
        font: 700 12px/1 Arial, sans-serif;
        letter-spacing: 0.18em;
        text-transform: uppercase;
        color: var(--gold);
        margin-bottom: 12px;
      }

      .section-title {
        color: var(--green);
        font-size: clamp(2.2rem, 4vw, 3.5rem);
        line-height: 1.1;
        letter-spacing: -0.03em;
      }

      nav {
        position: sticky;
        top: 0;
        z-index: 1000;
        background: rgba(255, 250, 242, 0.9);
        backdrop-filter: blur(12px);
        border-bottom: 1px solid rgba(23, 79, 54, 0.08);
      }

      .nav-wrap {
        display: flex;
        align-items: center;
        justify-content: space-between;
        min-height: 78px;
      }

      .brand {
        color: var(--green);
        text-decoration: none;
        letter-spacing: 0.12em;
        font-size: 1.45rem;
        font-weight: 700;
      }

      .brand small {
        display: block;
        color: var(--gold);
        font-size: 0.62rem;
        letter-spacing: 0.28em;
        margin-top: 4px;
        font-family: Arial, sans-serif;
      }

      .nav-links {
        display: flex;
        align-items: center;
        gap: 28px;
      }

      .nav-links a {
        color: var(--text);
        font: 700 14px/1 Arial, sans-serif;
        transition: color 0.2s ease;
      }

      .nav-links a:hover,
      .nav-links a:focus-visible {
        color: var(--gold);
      }

      .primary-btn,
      .secondary-btn,
      .cta-btn {
        display: inline-flex;
        align-items: center;
        justify-content: center;
        gap: 8px;
        padding: 16px 24px;
        border-radius: 12px;
        font: 700 14px/1 Arial, sans-serif;
        transition: transform 0.2s ease, box-shadow 0.2s ease, background 0.2s ease;
      }

      .primary-btn {
        background: var(--green);
        color: var(--white, #fff);
        box-shadow: 0 12px 24px rgba(23, 79, 54, 0.18);
      }

      .secondary-btn {
        background: transparent;
        color: var(--green);
        border: 1px solid rgba(23, 79, 54, 0.35);
      }

      .primary-btn:hover,
      .secondary-btn:hover,
      .cta-btn:hover {
        transform: translateY(-2px);
      }

      .hero {
        padding: 72px 0 58px;
        background:
          radial-gradient(circle at top, rgba(215, 166, 79, 0.18), transparent 26%),
          linear-gradient(135deg, #fffdf9 0%, #f3ead6 100%);
      }

      .hero-grid {
        display: grid;
        grid-template-columns: 1.2fr 0.8fr;
        align-items: center;
        gap: 32px;
      }

      .hero-copy {
        max-width: 700px;
      }

      .eyebrow {
        color: var(--gold);
        font: 700 13px/1.5 Arial, sans-serif;
        letter-spacing: 0.22em;
        text-transform: uppercase;
      }

      h1 {
        margin-top: 16px;
        color: var(--green);
        font-size: clamp(3rem, 6vw, 6rem);
        line-height: 0.94;
        letter-spacing: 0.06em;
      }

      .hero-sub {
        margin-top: 18px;
        max-width: 620px;
        color: var(--muted);
        font-family: Arial, sans-serif;
        font-size: clamp(1.05rem, 2vw, 1.3rem);
      }

      .hero-badges {
        margin-top: 26px;
        display: flex;
        flex-wrap: wrap;
        gap: 12px;
      }

      .badge {
        display: inline-flex;
        padding: 10px 16px;
        border-radius: 999px;
        border: 1px solid rgba(23, 79, 54, 0.18);
        background: rgba(255, 255, 255, 0.5);
        color: var(--green);
        font: 700 11px/1 Arial, sans-serif;
        letter-spacing: 0.08em;
        text-transform: uppercase;
      }

      .hero-actions {
        margin-top: 30px;
        display: flex;
        flex-wrap: wrap;
        gap: 14px;
      }

      .hero-panel {
        position: relative;
        background: linear-gradient(180deg, rgba(23, 79, 54, 0.96) 0%, rgba(15, 52, 39, 0.98) 100%);
        border-radius: 26px;
        overflow: hidden;
        box-shadow: var(--shadow);
        border: 1px solid rgba(255, 255, 255, 0.1);
      }

      .panel-inner {
        padding: 24px;
      }

      .mini-card {
        background: rgba(255, 255, 255, 0.08);
        border: 1px solid rgba(255, 255, 255, 0.12);
        border-radius: 18px;
        padding: 18px;
        color: #ecf0ec;
        margin-bottom: 16px;
      }

      .mini-card:last-child {
        margin-bottom: 0;
      }

      .mini-label {
        display: block;
        font: 700 11px/1 Arial, sans-serif;
        letter-spacing: 0.12em;
        text-transform: uppercase;
        opacity: 0.72;
        color: var(--gold-soft);
        margin-bottom: 10px;
      }

      .mini-card strong {
        display: block;
        font-size: clamp(1.6rem, 3vw, 2.2rem);
        line-height: 1.1;
        letter-spacing: 0.02em;
      }

      .mini-card span {
        font-family: Arial, sans-serif;
        font-size: 0.92rem;
        color: rgba(255, 255, 255, 0.8);
      }

      .trust-bar {
        display: grid;
        grid-template-columns: repeat(3, minmax(0, 1fr));
        gap: 16px;
        margin-top: 32px;
        padding: 18px 20px;
        background: rgba(255, 255, 255, 0.65);
        border: 1px solid rgba(23, 79, 54, 0.08);
        border-radius: 18px;
      }

      .stat {
        text-align: center;
      }

      .stat strong {
        display: block;
        font-size: clamp(1.5rem, 3vw, 2.1rem);
        color: var(--green);
      }

      .stat span {
        display: block;
        font: 700 11px/1 Arial, sans-serif;
        letter-spacing: 0.12em;
        text-transform: uppercase;
        color: var(--muted);
      }

      section {
        padding: 90px 0;
      }

      .intro {
        display: grid;
        grid-template-columns: 1.1fr 0.9fr;
        gap: 28px;
        align-items: center;
      }

      .story-card {
        background: var(--card);
        border-radius: 22px;
        border: 1px solid var(--border);
        box-shadow: var(--shadow);
        padding: 28px;
      }

      .story-card p {
        color: var(--muted);
        font-family: Arial, sans-serif;
        font-size: 1.03rem;
        margin-bottom: 16px;
      }

      .story-card p:last-child {
        margin-bottom: 0;
      }

      .quote-box {
        background: linear-gradient(135deg, #f9f0df 0%, #fffaf5 100%);
        border: 1px solid rgba(215, 166, 79, 0.3);
        border-radius: 20px;
        padding: 28px;
        font-size: clamp(1.5rem, 2.7vw, 2.1rem);
        line-height: 1.4;
        color: var(--green);
        font-style: italic;
      }

      .cards {
        margin-top: 42px;
        display: grid;
        grid-template-columns: repeat(4, minmax(0, 1fr));
        gap: 20px;
      }

      .info-card {
        background: var(--card);
        border: 1px solid var(--border);
        border-radius: 18px;
        padding: 26px 22px;
        box-shadow: 0 12px 24px rgba(29, 45, 36, 0.04);
      }

      .icon {
        width: 52px;
        height: 52px;
        display: grid;
        place-items: center;
        border-radius: 14px;
        background: #edf6ef;
        font-size: 1.7rem;
        margin-bottom: 16px;
      }

      .info-card h3 {
        color: var(--green);
        margin-bottom: 8px;
        font-size: 1.28rem;
      }

      .info-card p {
        color: var(--muted);
        font-family: Arial, sans-serif;
        font-size: 0.96rem;
      }

      .products {
        background: linear-gradient(180deg, rgba(23, 79, 54, 0.04) 0%, rgba(255, 255, 255, 0) 100%);
      }

      .products-grid {
        margin-top: 34px;
        display: grid;
        grid-template-columns: repeat(3, minmax(0, 1fr));
        gap: 22px;
      }

      .product-card {
        position: relative;
        overflow: hidden;
        background: var(--card);
        border: 1px solid var(--border);
        border-radius: 22px;
        padding: 22px;
        box-shadow: 0 12px 22px rgba(19, 40, 30, 0.04);
      }

      .product-visual {
        height: 170px;
        border-radius: 16px;
        display: flex;
        align-items: center;
        justify-content: center;
        font-size: 4rem;
        margin-bottom: 18px;
        background: linear-gradient(135deg, #ebf5ee 0%, #f8f0df 100%);
      }

      .product-card h3 {
        color: var(--green);
        font-size: 1.7rem;
        margin-bottom: 10px;
      }

      .product-card p {
        color: var(--muted);
        font-family: Arial, sans-serif;
      }

      .tag-row {
        margin-top: 16px;
        display: flex;
        flex-wrap: wrap;
        gap: 8px;
      }

      .tag {
        padding: 8px 10px;
        border-radius: 999px;
        font: 700 11px/1 Arial, sans-serif;
        letter-spacing: 0.06em;
        text-transform: uppercase;
        background: var(--sage);
        color: var(--green);
      }

      .visit-wrap {
        display: grid;
        grid-template-columns: 1.1fr 0.9fr;
        gap: 24px;
      }

      .visit-card,
      .contact-card {
        background: var(--card);
        border: 1px solid var(--border);
        border-radius: 24px;
        padding: 28px;
        box-shadow: var(--shadow);
      }

      .visit-card p,
      .contact-card p,
      .contact-card li {
        color: var(--muted);
        font-family: Arial, sans-serif;
      }

      .contact-list {
        list-style: none;
        margin-top: 18px;
        display: grid;
        gap: 14px;
      }

      .contact-list li {
        display: flex;
        gap: 12px;
        align-items: flex-start;
      }

      .bullet {
        width: 30px;
        height: 30px;
        border-radius: 10px;
        display: grid;
        place-items: center;
        background: #edf6ef;
        color: var(--green);
        font-size: 1rem;
      }

      .callout {
        margin-top: 36px;
        background: linear-gradient(135deg, var(--green) 0%, var(--green-2) 100%);
        border-radius: 26px;
        padding: 24px 28px;
        display: flex;
        align-items: center;
        justify-content: space-between;
        gap: 18px;
        color: white;
      }

      .callout strong {
        display: block;
        font-size: clamp(1.5rem, 2.5vw, 2.1rem);
      }

      .cta-btn {
        background: #f3d28b;
        color: var(--green-2);
        border: none;
      }

      footer {
        padding: 28px 0 36px;
        background: var(--green-2);
        color: rgba(255, 255, 255, 0.8);
        text-align: center;
        font-family: Arial, sans-serif;
        letter-spacing: 0.08em;
        text-transform: uppercase;
      }

      @media (max-width: 900px) {
        .hero-grid,
        .intro,
        .visit-wrap,
        .products-grid {
          grid-template-columns: 1fr;
        }

        .cards {
          grid-template-columns: repeat(2, minmax(0, 1fr));
        }
      }

      @media (max-width: 700px) {
        .nav-links {
          display: none;
        }

        .hero {
          padding-top: 52px;
        }

        .hero-actions,
        .callout {
          flex-direction: column;
          align-items: stretch;
        }

        .trust-bar,
        .cards {
          grid-template-columns: 1fr;
        }

        .product-card {
          padding: 18px;
        }
      }
    </style>
  </head>
  <body>
    <nav>
      <div class="container nav-wrap">
        <a href="#home" class="brand">
          GIRI STORES
          <small>SINCE 1978</small>
        </a>

        <div class="nav-links">
          <a href="#store">Store</a>
          <a href="#about">About</a>
          <a href="#services">Offers</a>
          <a href="#contact">Contact</a>
        </div>
      </div>
    </nav>

    <header class="hero" id="home">
      <div class="container hero-grid">
        <div class="hero-copy">
          <div class="eyebrow">A family legacy of trust</div>
          <h1>GIRI<br />STORES</h1>
          <p class="hero-sub">
            Fresh groceries, vegetables, and daily essentials delivered with the warmth of a neighborhood shop you can always rely on.
          </p>

          <div class="hero-badges">
            <span class="badge">Trusted Since 1978</span>
            <span class="badge">Fresh Daily</span>
            <span class="badge">Local Service</span>
          </div>

          <div class="hero-actions">
            <a class="primary-btn" href="tel:+919791620813">📞 Call 9791620813</a>
            <a class="secondary-btn" href="https://wa.me/919791620813" target="_blank" rel="noreferrer">💬 WhatsApp Us</a>
          </div>

          <div class="trust-bar">
            <div class="stat">
              <strong>45+</strong>
              <span>Years</span>
            </div>
            <div class="stat">
              <strong>Daily</strong>
              <span>Fresh Stock</span>
            </div>
            <div class="stat">
              <strong>Local</strong>
              <span>Community First</span>
            </div>
          </div>
        </div>

        <div class="hero-panel" aria-label="Store highlight cards">
          <div class="panel-inner">
            <div class="mini-card">
              <span class="mini-label">Popular</span>
              <strong>Groceries</strong>
              <span>Everyday essentials for your home and family.</span>
            </div>

            <div class="mini-card">
              <span class="mini-label">Fresh picks</span>
              <strong>Vegetables</strong>
              <span>Clean, fresh, and carefully selected each day.</span>
            </div>

            <div class="mini-card">
              <span class="mini-label">Our promise</span>
              <strong>Honest Service</strong>
              <span>Friendly guidance, fair pricing, and trusted quality.</span>
            </div>
          </div>
        </div>
      </div>
    </header>

    <main>
      <section id="about">
        <div class="container intro">
          <div>
            <div class="section-tag">Our heritage</div>
            <h2 class="section-title">A neighborhood store built on trust.</h2>
          </div>

          <div class="quote-box">
            “A neighborhood grocery store should be built on trust, quality, and deep family values.”
          </div>
        </div>

        <div class="container">
          <div class="story-card" style="margin-top: 30px;">
            <p>
              At <strong>Giri Stores</strong>, we believe that a neighborhood grocery shop should be more than just a place to buy essentials — it should be a place people can depend on.
            </p>
            <p>
              Our journey began in <strong>1978</strong>, when our founder, <strong>Muniyappa</strong>, opened our doors with a simple and powerful vision: to provide the local community with high-quality daily essentials, fair pricing, and honest service.
            </p>
            <p>
              Today, that same spirit continues under the care of <strong>Muniyappa’s sons</strong>, who carry forward the values of integrity, warmth, and dedication that have shaped the store for generations.
            </p>
          </div>
        </div>

        <div class="container cards">
          <div class="info-card">
            <div class="icon">🤝</div>
            <h3>Trusted Service</h3>
            <p>Built on honest guidance and relationships that last beyond the purchase.</p>
          </div>

          <div class="info-card">
            <div class="icon">🌿</div>
            <h3>Fresh Daily</h3>
            <p>Vegetables and daily essentials handpicked to keep your kitchen stocked with quality.</p>
          </div>

          <div class="info-card">
            <div class="icon">💬</div>
            <h3>Family Values</h3>
            <p>Warm, personal service that feels like shopping with a trusted neighbor.</p>
          </div>

          <div class="info-card">
            <div class="icon">🏡</div>
            <h3>Local Legacy</h3>
            <p>For over four decades, we have proudly served homes across Hosur and nearby areas.</p>
          </div>
        </div>
      </section>

      <section id="services" class="products">
        <div class="container">
          <div class="section-tag">Everyday essentials</div>
          <h2 class="section-title">What we offer</h2>

          <div class="products-grid">
            <article class="product-card">
              <div class="product-visual">🛒</div>
              <h3>Groceries</h3>
              <p>Daily household essentials and a wide range of grocery products for home, family, and routine living.</p>
              <div class="tag-row">
                <span class="tag">Rice</span>
                <span class="tag">Spices</span>
                <span class="tag">Staples</span>
              </div>
            </article>

            <article class="product-card">
              <div class="product-visual">🥦</div>
              <h3>Fresh Vegetables</h3>
              <p>Fresh vegetables for daily cooking, healthy meals, and every family table.</p>
              <div class="tag-row">
                <span class="tag">Fresh</span>
                <span class="tag">Seasonal</span>
                <span class="tag">Aromatic</span>
              </div>
            </article>

            <article class="product-card">
              <div class="product-visual">🤝</div>
              <h3>Trusted Service</h3>
              <p>A family-run store built on genuine service, fair prices, and lasting local relationships.</p>
              <div class="tag-row">
                <span class="tag">Honest</span>
                <span class="tag">Friendly</span>
                <span class="tag">Reliable</span>
              </div>
            </article>
          </div>
        </div>
      </section>

      <section id="store">
        <div class="container">
          <div class="section-tag">Our store</div>
          <h2 class="section-title">Inside Giri Stores</h2>

          <div class="visit-wrap" style="margin-top: 32px;">
            <div class="visit-card">
              <img src="store.jpg" alt="Inside Giri Stores" style="border-radius: 18px; border: 1px solid var(--border);" />
            </div>

            <div class="contact-card">
              <p style="font-size: 1.05rem; margin-bottom: 12px;">
                We proudly serve the local community at a convenient location in Nanjapuram, Hosur—bringing everyday essentials closer to home.
              </p>
              <ul class="contact-list">
                <li>
                  <span class="bullet">📍</span>
                  <div>
                    <strong style="display:block; color: var(--green);">Store Address</strong>
                    Nanjapuram, TVS Main Road,<br />
                    Kothagondapalli PO, Hosur TK,<br />
                    Krishnagiri DT, Tamil Nadu – 635109
                  </div>
                </li>
                <li>
                  <span class="bullet">🕘</span>
                  <div>
                    <strong style="display:block; color: var(--green);">Store Hours</strong>
                    Open daily with friendly, local service.
                  </div>
                </li>
              </ul>
            </div>
          </div>
        </div>
      </section>

      <section id="contact">
        <div class="container">
          <div class="section-tag">Visit or contact us</div>
          <h2 class="section-title">Let’s shop local together.</h2>

          <div class="visit-wrap" style="margin-top: 28px;">
            <div class="contact-card">
              <h3 style="font-size: 1.6rem; color: var(--green); margin-bottom: 14px;">Get in touch</h3>
              <ul class="contact-list">
                <li>
                  <span class="bullet">📞</span>
                  <div>
                    <strong style="display:block; color: var(--green);">Phone / WhatsApp</strong>
                    <a href="tel:+919791620813" style="color: var(--green); font-weight: 700;">9791620813</a>
                  </div>
                </li>
                <li>
                  <span class="bullet">✉️</span>
                  <div>
                    <strong style="display:block; color: var(--green);">Email</strong>
                    <a href="mailto:kaligiri1997@gmail.com" style="color: var(--green); font-weight: 700;">kaligiri1997@gmail.com</a>
                  </div>
                </li>
              </ul>
            </div>

            <div class="contact-card">
              <h3 style="font-size: 1.6rem; color: var(--green); margin-bottom: 14px;">Why choose us?</h3>
              <p>
                With a legacy of trust, an unwavering commitment to quality, and service rooted in family values, Giri Stores continues to be the reliable neighborhood choice for your daily needs.
              </p>
              <div class="hero-actions" style="margin-top: 22px;">
                <a class="primary-btn" href="https://wa.me/919791620813" target="_blank" rel="noreferrer">💬 Message on WhatsApp</a>
              </div>
            </div>
          </div>

          <div class="callout">
            <div>
              <span style="font: 700 12px/1 Arial, sans-serif; letter-spacing: 0.18em; text-transform: uppercase; opacity: 0.8;">Fresh, local, reliable</span>
              <strong>Visit Giri Stores today.</strong>
            </div>
            <a class="cta-btn" href="tel:+919791620813">📞 Call Now</a>
          </div>
        </div>
      </section>
    </main>

    <footer>
      Giri Stores · Since 1978 · Nanjapuram, Hosur
    </footer>
  </body>
</html>
