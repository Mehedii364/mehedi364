
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="theme-color" content="#0b0d14">
  <meta name="description" content="Mehedi364 — Web developer and software engineer building practical web applications, Android apps, and digital experiences through Wafa Zone.">
  <meta name="author" content="Md. Mehedi Hasan">
  <title>Wafa Zone — Mehedi364 | Developer Portfolio</title>

  <style>
    :root {
      color-scheme: dark;
      --bg: #0b0d14;
      --surface: #111521;
      --surface-2: #171c2a;
      --text: #f4f6ff;
      --muted: #a2abc0;
      --border: rgba(255,255,255,.09);
      --primary: #9b8cff;
      --secondary: #55e5d0;
      --header: rgba(11,13,20,.82);
      --shadow: 0 24px 70px rgba(0,0,0,.22);
      --radius: 22px;
    }

    body.light {
      color-scheme: light;
      --bg: #f5f6fb;
      --surface: #ffffff;
      --surface-2: #eef0f8;
      --text: #171a29;
      --muted: #626b80;
      --border: rgba(20,25,50,.11);
      --primary: #6853d9;
      --secondary: #087e76;
      --header: rgba(245,246,251,.86);
      --shadow: 0 24px 70px rgba(30,35,70,.09);
    }

    * { box-sizing: border-box; }

    html {
      scroll-behavior: smooth;
      scroll-padding-top: 90px;
    }

    body {
      margin: 0;
      background:
        radial-gradient(ellipse at 12% 0%, rgba(125,100,255,.12), transparent 34%),
        radial-gradient(ellipse at 92% 28%, rgba(53,218,200,.07), transparent 30%),
        var(--bg);
      color: var(--text);
      font-family: Inter, ui-sans-serif, system-ui, -apple-system,
        BlinkMacSystemFont, "Segoe UI", sans-serif;
      line-height: 1.7;
      transition: background .25s, color .25s;
    }

    a { color: inherit; text-decoration: none; }
    button, input, textarea { font: inherit; }
    button { color: inherit; }

    ::selection {
      background: var(--primary);
      color: white;
    }

    .container {
      width: min(1120px, calc(100% - 40px));
      margin-inline: auto;
    }

    .section {
      padding: 100px 0;
    }

    .section-head {
      max-width: 680px;
      margin-bottom: 38px;
    }

    .eyebrow {
      display: inline-flex;
      align-items: center;
      gap: 9px;
      color: var(--secondary);
      font-size: .78rem;
      font-weight: 800;
      letter-spacing: .16em;
      text-transform: uppercase;
    }

    .eyebrow::before {
      content: "";
      width: 22px;
      height: 2px;
      background: currentColor;
    }

    h1, h2, h3, p { margin-top: 0; }

    h1 {
      font-size: clamp(2.8rem, 7vw, 5.8rem);
      line-height: 1.03;
      letter-spacing: -.065em;
      margin: 22px 0;
    }

    h2 {
      font-size: clamp(2rem, 4vw, 3.2rem);
      line-height: 1.15;
      letter-spacing: -.045em;
      margin: 14px 0;
    }

    h3 {
      line-height: 1.3;
      letter-spacing: -.02em;
    }

    .gradient-text {
      background: linear-gradient(105deg, var(--primary), var(--secondary));
      color: transparent;
      background-clip: text;
      -webkit-background-clip: text;
    }

    .muted { color: var(--muted); }

    .section-description {
      max-width: 650px;
      color: var(--muted);
      font-size: 1.04rem;
    }

    .topbar {
      position: sticky;
      z-index: 100;
      top: 0;
      border-bottom: 1px solid var(--border);
      background: var(--header);
      backdrop-filter: blur(18px);
      -webkit-backdrop-filter: blur(18px);
    }

    .nav {
      min-height: 76px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 22px;
    }

    .brand {
      display: flex;
      align-items: center;
      gap: 11px;
      font-weight: 850;
      letter-spacing: -.04em;
      font-size: 1.08rem;
      white-space: nowrap;
    }

    .brand-mark {
      width: 42px;
      height: 42px;
      display: grid;
      place-items: center;
      border-radius: 14px;
      background: linear-gradient(135deg, var(--primary), #6358d9);
      color: white;
      box-shadow: 0 8px 26px rgba(125,100,255,.25);
      font-size: .9rem;
    }

    .nav-links {
      display: flex;
      align-items: center;
      gap: 23px;
    }

    .nav-links a {
      color: var(--muted);
      font-size: .9rem;
      font-weight: 650;
      transition: color .2s;
    }

    .nav-links a:hover,
    .nav-links a.active {
      color: var(--text);
    }

    .nav-actions {
      display: flex;
      align-items: center;
      gap: 9px;
    }

    .icon-button, .menu-button {
      width: 42px;
      height: 42px;
      display: grid;
      place-items: center;
      border: 1px solid var(--border);
      border-radius: 14px;
      background: var(--surface);
      cursor: pointer;
    }

    .menu-button { display: none; }

    .button {
      display: inline-flex;
      justify-content: center;
      align-items: center;
      gap: 9px;
      min-height: 48px;
      padding: 0 20px;
      border: 1px solid var(--border);
      border-radius: 14px;
      font-weight: 750;
      cursor: pointer;
      transition: transform .2s, border-color .2s, opacity .2s;
    }

    .button:hover {
      transform: translateY(-2px);
      border-color: var(--primary);
    }

    .button-primary {
      background: linear-gradient(115deg, #8875ff, #6958d9);
      color: #fff;
      border-color: transparent;
      box-shadow: 0 12px 28px rgba(105,88,217,.2);
    }

    .button-secondary {
      background: var(--surface);
      color: var(--text);
    }

    .hero {
      min-height: 680px;
      display: grid;
      grid-template-columns: 1.3fr .7fr;
      align-items: center;
      gap: 65px;
      padding-top: 85px;
      padding-bottom: 90px;
    }

    .availability {
      display: inline-flex;
      align-items: center;
      gap: 9px;
      border: 1px solid var(--border);
      border-radius: 999px;
      padding: 8px 13px;
      background: var(--surface);
      color: var(--muted);
      font-size: .84rem;
    }

    .availability-dot {
      width: 8px;
      height: 8px;
      border-radius: 50%;
      background: var(--secondary);
      box-shadow: 0 0 13px var(--secondary);
    }

    .hero h1 span { display: block; }

    .hero-description {
      max-width: 610px;
      color: var(--muted);
      font-size: 1.1rem;
      margin-bottom: 27px;
    }

    .hero-buttons {
      display: flex;
      flex-wrap: wrap;
      gap: 12px;
    }

    .social-links {
      display: flex;
      flex-wrap: wrap;
      gap: 18px;
      margin-top: 30px;
    }

    .social-links a {
      color: var(--muted);
      font-size: .9rem;
      font-weight: 700;
    }

    .social-links a:hover { color: var(--secondary); }

    .hero-visual {
      position: relative;
      display: grid;
      place-items: center;
      min-height: 360px;
    }

    .orbit {
      position: absolute;
      width: 320px;
      height: 320px;
      border: 1px solid var(--border);
      border-radius: 50%;
      animation: rotate 25s linear infinite;
    }

    .orbit::before, .orbit::after {
      content: "";
      position: absolute;
      width: 12px;
      height: 12px;
      border-radius: 50%;
      background: var(--secondary);
      box-shadow: 0 0 24px var(--secondary);
    }

    .orbit::before { top: 35px; left: 42px; }
    .orbit::after {
      right: 18px;
      bottom: 85px;
      background: var(--primary);
      box-shadow: 0 0 24px var(--primary);
    }

    .hero-logo {
      width: 220px;
      height: 220px;
      display: grid;
      place-items: center;
      border: 1px solid rgba(155,140,255,.3);
      border-radius: 42px;
      background: linear-gradient(145deg, var(--surface-2), var(--surface));
      box-shadow: var(--shadow), inset 0 1px 0 rgba(255,255,255,.08);
      transform: rotate(-5deg);
    }

    .hero-logo span {
      font-size: 4.2rem;
      font-weight: 950;
      letter-spacing: -.12em;
      background: linear-gradient(135deg, var(--primary), var(--secondary));
      color: transparent;
      background-clip: text;
      -webkit-background-clip: text;
    }

    .floating-label {
      position: absolute;
      padding: 10px 14px;
      border: 1px solid var(--border);
      border-radius: 14px;
      background: var(--surface);
      box-shadow: var(--shadow);
      font-size: .82rem;
      font-weight: 750;
    }

    .floating-one { top: 24px; right: -5px; }
    .floating-two { bottom: 30px; left: -5px; }

    @keyframes rotate {
      to { transform: rotate(360deg); }
    }

    .tech-strip {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 12px;
      padding: 23px 0;
      border-top: 1px solid var(--border);
      border-bottom: 1px solid var(--border);
    }

    .tech-pill, .tag {
      display: inline-flex;
      align-items: center;
      border: 1px solid var(--border);
      border-radius: 999px;
      padding: 7px 12px;
      color: var(--muted);
      background: var(--surface);
      font-size: .82rem;
      font-weight: 700;
    }

    .grid-2 {
      display: grid;
      grid-template-columns: repeat(2, minmax(0,1fr));
      gap: 22px;
    }

    .grid-3 {
      display: grid;
      grid-template-columns: repeat(3, minmax(0,1fr));
      gap: 20px;
    }

    .card {
      padding: 27px;
      border: 1px solid var(--border);
      border-radius: var(--radius);
      background: linear-gradient(145deg, var(--surface), var(--surface-2));
      box-shadow: 0 10px 40px rgba(0,0,0,.035);
      transition: transform .22s, border-color .22s;
    }

    .card:hover {
      transform: translateY(-5px);
      border-color: rgba(155,140,255,.45);
    }

    .card p:last-child { margin-bottom: 0; }

    .feature-icon {
      width: 48px;
      height: 48px;
      display: grid;
      place-items: center;
      border-radius: 15px;
      background: rgba(155,140,255,.12);
      color: var(--primary);
      font-size: 1.25rem;
      margin-bottom: 20px;
    }

    .about-copy p { color: var(--muted); }

    .check-list {
      display: grid;
      gap: 12px;
      margin: 22px 0 0;
      padding: 0;
      list-style: none;
    }

    .check-list li {
      display: flex;
      gap: 10px;
      color: var(--muted);
    }

    .check-list li::before {
      content: "✓";
      color: var(--secondary);
      font-weight: 900;
    }

    .skill-card h3 { margin-bottom: 18px; }

    .skill-tags {
      display: flex;
      flex-wrap: wrap;
      gap: 9px;
    }

    .project-tools {
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
      margin-bottom: 25px;
    }

    .filter-button {
      padding: 9px 15px;
      border: 1px solid var(--border);
      border-radius: 999px;
      background: var(--surface);
      color: var(--muted);
      cursor: pointer;
    }

    .filter-button.active {
      background: var(--primary);
      color: #fff;
      border-color: transparent;
    }

    .project-card {
      display: flex;
      flex-direction: column;
      min-height: 275px;
    }

    .project-top {
      display: flex;
      justify-content: space-between;
      gap: 12px;
      align-items: center;
      margin-bottom: 18px;
    }

    .project-icon {
      width: 46px;
      height: 46px;
      display: grid;
      place-items: center;
      border-radius: 14px;
      background: var(--surface-2);
      font-size: 1.35rem;
    }

    .project-status {
      font-size: .72rem;
      font-weight: 800;
      color: var(--secondary);
      text-transform: uppercase;
      letter-spacing: .07em;
    }

    .project-card p {
      color: var(--muted);
      font-size: .94rem;
    }

    .project-card .skill-tags { margin-top: auto; padding-top: 12px; }

    .project-card[hidden] { display: none; }

    .process-number {
      color: var(--primary);
      font-size: 2.1rem;
      font-weight: 900;
      letter-spacing: -.06em;
    }

    .contact-panel {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 32px;
      padding: clamp(24px, 5vw, 50px);
      border: 1px solid var(--border);
      border-radius: 30px;
      background: linear-gradient(135deg, var(--surface), var(--surface-2));
      box-shadow: var(--shadow);
    }

    .contact-method {
      display: flex;
      align-items: flex-start;
      gap: 13px;
      margin-top: 22px;
    }

    .contact-method strong { display: block; }
    .contact-method a, .contact-method span {
      color: var(--muted);
      overflow-wrap: anywhere;
    }

    .contact-form {
      display: grid;
      gap: 14px;
    }

    .field label {
      display: block;
      margin-bottom: 7px;
      font-size: .87rem;
      font-weight: 750;
    }

    .field input, .field textarea {
      width: 100%;
      border: 1px solid var(--border);
      border-radius: 13px;
      background: var(--bg);
      color: var(--text);
      padding: 13px 14px;
      outline: none;
    }

    .field input:focus, .field textarea:focus {
      border-color: var(--primary);
      box-shadow: 0 0 0 3px rgba(155,140,255,.12);
    }

    .field textarea {
      resize: vertical;
      min-height: 120px;
    }

    .form-note {
      color: var(--muted);
      font-size: .8rem;
      margin: 0;
    }

    footer {
      padding: 27px 0;
      border-top: 1px solid var(--border);
    }

    .footer-inner {
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 20px;
      flex-wrap: wrap;
    }

    .footer-inner p {
      color: var(--muted);
      font-size: .87rem;
      margin: 0;
    }

    .back-top {
      position: fixed;
      right: 20px;
      bottom: 20px;
      z-index: 50;
      width: 46px;
      height: 46px;
      border: 1px solid var(--border);
      border-radius: 15px;
      background: var(--surface);
      box-shadow: var(--shadow);
      cursor: pointer;
      opacity: 0;
      pointer-events: none;
      transform: translateY(10px);
      transition: .2s;
    }

    .back-top.visible {
      opacity: 1;
      pointer-events: auto;
      transform: translateY(0);
    }

    .reveal {
      opacity: 0;
      transform: translateY(18px);
      transition: opacity .6s ease, transform .6s ease;
    }

    .reveal.show {
      opacity: 1;
      transform: translateY(0);
    }

    @media (prefers-reduced-motion: reduce) {
      *, *::before, *::after {
        scroll-behavior: auto !important;
        animation-duration: .01ms !important;
        transition-duration: .01ms !important;
      }
      .reveal { opacity: 1; transform: none; }
    }

    @media (max-width: 900px) {
      .nav-links { gap: 14px; }
      .nav-links a { font-size: .82rem; }
      .hero { gap: 25px; }
      .hero-visual { transform: scale(.88); }
      .grid-3 { grid-template-columns: repeat(2, minmax(0,1fr)); }
    }

    @media (max-width: 720px) {
      .container { width: min(100% - 30px, 560px); }
      .section { padding: 72px 0; }
      .nav { min-height: 68px; }
      .menu-button { display: grid; }
      .nav-links {
        position: absolute;
        top: calc(100% + 1px);
        left: 0;
        right: 0;
        display: none;
        flex-direction: column;
        align-items: stretch;
        gap: 0;
        padding: 12px 20px 20px;
        border-bottom: 1px solid var(--border);
        background: var(--bg);
      }

      .nav-links.open { display: flex; }
      .nav-links a { padding: 12px 4px; font-size: .95rem; }
      .hero {
        grid-template-columns: 1fr;
        min-height: auto;
        padding-top: 65px;
        gap: 8px;
      }

      .hero h1 { font-size: clamp(2.8rem, 12vw, 4.5rem); }
      .hero-visual { min-height: 300px; transform: scale(.84); }
      .grid-2, .grid-3, .contact-panel { grid-template-columns: 1fr; }
      .contact-panel { padding: 23px; }
      .floating-one { right: 0; }
      .floating-two { left: 0; }
      .footer-inner { align-items: flex-start; flex-direction: column; }
    }

    @media (max-width: 380px) {
      .brand { font-size: .93rem; }
      .brand-mark { width: 37px; height: 37px; }
      .hero-buttons .button { width: 100%; }
    }
  </style>
</head>

<body>
  <header class="topbar">
    <div class="container nav">
      <a class="brand" href="#home" aria-label="Wafa Zone home">
        <span class="brand-mark">WZ</span>
        <span>Wafa Zone <span class="gradient-text">.</span></span>
      </a>

      <nav class="nav-links" id="navLinks" aria-label="Main navigation">
        <a href="#home">Home</a>
        <a href="#about">About</a>
        <a href="#skills">Skills</a>
        <a href="#projects">Projects</a>
        <a href="#process">Process</a>
        <a href="#contact">Contact</a>
      </nav>

      <div class="nav-actions">
        <button class="icon-button" id="themeButton" aria-label="Switch theme" title="Switch theme">☼</button>
        <a class="button button-primary desktop-contact" href="#contact">Let's Talk ↗</a>
        <button class="menu-button" id="menuButton" aria-label="Open navigation" aria-expanded="false">☰</button>
      </div>
    </div>
  </header>

  <main>
    <!-- HERO -->
    <section class="container hero" id="home">
      <div class="hero-copy reveal">
        <div class="availability">
          <span class="availability-dot"></span>
          Developer portfolio · Wafa Zone
        </div>

        <h1>
          Building ideas<br>
          into <span class="gradient-text">digital reality.</span>
        </h1>

        <p class="hero-description">
          I'm <strong>Md. Mehedi Hasan</strong>, known as <strong>Mehedi364</strong>.
          I build web applications, software projects and practical digital tools
          with a focus on usability, performance and thoughtful design.
        </p>

        <div class="hero-buttons">
          <a class="button button-primary" href="#projects">Explore Projects ↗</a>
          <a class="button button-secondary" href="#contact">Contact Me</a>
        </div>

        <div class="social-links">
          <a href="https://github.com/Mehedi364" target="_blank" rel="noopener noreferrer">GitHub ↗</a>
          <a href="https://facebook.com/mehedi3643" target="_blank" rel="noopener noreferrer">Facebook ↗</a>
          <a href="mailto:useable.me2@gmail.com">Email ↗</a>
        </div>
      </div>

      <div class="hero-visual reveal" aria-label="Wafa Zone monogram illustration">
        <div class="orbit"></div>
        <div class="hero-logo"><span>WZ</span></div>
        <div class="floating-label floating-one">✦ Build with purpose</div>
        <div class="floating-label floating-two">⌘ Code · Design · Improve</div>
      </div>
    </section>

    <!-- TECHNOLOGIES -->
    <div class="container">
      <div class="tech-strip" aria-label="Technology areas">
        <span class="tech-pill">HTML & CSS</span>
        <span class="tech-pill">JavaScript</span>
        <span class="tech-pill">PHP</span>
        <span class="tech-pill">MySQL</span>
        <span class="tech-pill">Android</span>
        <span class="tech-pill">PWA</span>
        <span class="tech-pill">REST APIs</span>
      </div>
    </div>

    <!-- ABOUT -->
    <section class="section" id="about">
      <div class="container">
        <div class="section-head reveal">
          <span class="eyebrow">About Me</span>
          <h2>Technology with a <span class="gradient-text">purpose.</span></h2>
          <p class="section-description">
            I enjoy turning practical problems into clear, useful and accessible
            software experiences.
          </p>
        </div>

        <div class="grid-2">
          <article class="card about-copy reveal">
            <div class="feature-icon">⌘</div>
            <h3>Who I Am</h3>
            <p>
              I'm Md. Mehedi Hasan, a developer working under the
              <strong>Mehedi364</strong> identity and the <strong>Wafa Zone</strong>
              project ecosystem.
            </p>
            <p>
              My interests include web development, software engineering,
              Android applications, responsive interfaces and practical digital tools.
            </p>
          </article>

          <article class="card reveal">
            <div class="feature-icon">✧</div>
            <h3>What I Focus On</h3>
            <ul class="check-list">
              <li>Responsive and accessible user interfaces</li>
              <li>PHP and MySQL application development</li>
              <li>Progressive Web Apps and REST API integration</li>
              <li>Performance, security and maintainability</li>
              <li>Practical projects built around real user needs</li>
            </ul>
          </article>
        </div>
      </div>
    </section>

    <!-- SKILLS -->
    <section class="section" id="skills">
      <div class="container">
        <div class="section-head reveal">
          <span class="eyebrow">Skills & Tools</span>
          <h2>My development <span class="gradient-text">toolkit.</span></h2>
          <p class="section-description">
            Technologies and development areas used across my project work.
            Specific experience can vary by project.
          </p>
        </div>

        <div class="grid-3">
          <article class="card skill-card reveal">
            <div class="feature-icon">⌘</div>
            <h3>Web Development</h3>
            <div class="skill-tags">
              <span class="tag">HTML5</span>
              <span class="tag">CSS3</span>
              <span class="tag">JavaScript</span>
              <span class="tag">Responsive UI</span>
              <span class="tag">Accessibility</span>
            </div>
          </article>

          <article class="card skill-card reveal">
            <div class="feature-icon">▤</div>
            <h3>Backend & Data</h3>
            <div class="skill-tags">
              <span class="tag">PHP</span>
              <span class="tag">MySQL</span>
              <span class="tag">PDO</span>
              <span class="tag">REST APIs</span>
              <span class="tag">Web Security</span>
            </div>
          </article>

          <article class="card skill-card reveal">
            <div class="feature-icon">▣</div>
            <h3>Apps & Workflow</h3>
            <div class="skill-tags">
              <span class="tag">PWA</span>
              <span class="tag">Android Projects</span>
              <span class="tag">Git</span>
              <span class="tag">GitHub</span>
              <span class="tag">Deployment</span>
            </div>
          </article>
        </div>
      </div>
    </section>

    <!-- PROJECTS -->
    <section class="section" id="projects">
      <div class="container">
        <div class="section-head reveal">
          <span class="eyebrow">Selected Projects</span>
          <h2>Ideas becoming <span class="gradient-text">products.</span></h2>
          <p class="section-description">
            A selection of projects associated with the Wafa Zone ecosystem.
            Project links can be added as each public repository or live release is verified.
          </p>
        </div>

        <div class="project-tools reveal" role="group" aria-label="Filter projects">
          <button class="filter-button active" data-filter="all" aria-pressed="true">All Projects</button>
          <button class="filter-button" data-filter="web" aria-pressed="false">Web</button>
          <button class="filter-button" data-filter="android" aria-pressed="false">Android</button>
          <button class="filter-button" data-filter="platform" aria-pressed="false">Platforms</button>
        </div>

        <div class="grid-3" id="projectGrid">
          <article class="card project-card reveal" data-category="platform">
            <div class="project-top">
              <span class="project-icon">✦</span>
              <span class="project-status">Ecosystem</span>
            </div>
            <h3>Wafa Zone</h3>
            <p>
              A project ecosystem focused on useful digital products,
              web applications and software experiments.
            </p>
            <div class="skill-tags">
              <span class="tag">Web</span>
              <span class="tag">Product Design</span>
            </div>
          </article>

          <article class="card project-card reveal" data-category="web">
            <div class="project-top">
              <span class="project-icon">▤</span>
              <span class="project-status">Web App</span>
            </div>
            <h3>Hisab</h3>
            <p>
              A personal finance and expense-management project designed
              to help organize everyday financial records.
            </p>
            <div class="skill-tags">
              <span class="tag">PHP</span>
              <span class="tag">MySQL</span>
            </div>
          </article>

          <article class="card project-card reveal" data-category="android">
            <div class="project-top">
              <span class="project-icon">◉</span>
              <span class="project-status">Android</span>
            </div>
            <h3>Wafa Camera Pro</h3>
            <p>
              An Android camera application concept with camera tools,
              OCR and other planned productivity features.
            </p>
            <div class="skill-tags">
              <span class="tag">Kotlin</span>
              <span class="tag">CameraX</span>
            </div>
          </article>

          <article class="card project-card reveal" data-category="platform">
            <div class="project-top">
              <span class="project-icon">🌐</span>
              <span class="project-status">Platform</span>
            </div>
            <h3>ONEBD</h3>
            <p>
              A Bangladesh-focused platform concept for organizing
              useful services and public information in one place.
            </p>
            <div class="skill-tags">
              <span class="tag">Web Platform</span>
              <span class="tag">Bangladesh</span>
            </div>
          </article>

          <article class="card project-card reveal" data-category="android">
            <div class="project-top">
              <span class="project-icon">⌁</span>
              <span class="project-status">Android</span>
            </div>
            <h3>Wafa Device Intelligence</h3>
            <p>
              A device-information project exploring useful hardware,
              battery and device-status information.
            </p>
            <div class="skill-tags">
              <span class="tag">Android</span>
              <span class="tag">Device APIs</span>
            </div>
          </article>

          <article class="card project-card reveal" data-category="web">
            <div class="project-top">
              <span class="project-icon">⇄</span>
              <span class="project-status">Web App</span>
            </div>
            <h3>Wafa One-Time Share</h3>
            <p>
              A temporary sharing service concept for content with
              expiry and one-time access controls.
            </p>
            <div class="skill-tags">
              <span class="tag">PHP</span>
              <span class="tag">MySQL</span>
              <span class="tag">Privacy</span>
            </div>
          </article>
        </div>

        <p class="muted" style="margin-top:24px;font-size:.88rem">
          Note: The cards describe project goals and areas. They do not claim
          that every feature is completed or currently deployed.
        </p>

        <div style="margin-top:28px">
          <a class="button button-secondary"
             href="https://github.com/Mehedi364"
             target="_blank" rel="noopener noreferrer">
            Browse GitHub ↗
          </a>
        </div>
      </div>
    </section>

    <!-- PROCESS -->
    <section class="section" id="process">
      <div class="container">
        <div class="section-head reveal">
          <span class="eyebrow">My Approach</span>
          <h2>Think. Build. <span class="gradient-text">Improve.</span></h2>
          <p class="section-description">
            A practical workflow that prioritizes useful features,
            clear requirements and honest testing.
          </p>
        </div>

        <div class="grid-3">
          <article class="card reveal">
            <div class="process-number">01</div>
            <h3>Understand</h3>
            <p class="muted">
              Define the user problem, requirements, constraints and success criteria.
            </p>
          </article>

          <article class="card reveal">
            <div class="process-number">02</div>
            <h3>Design & Build</h3>
            <p class="muted">
              Create a usable interface and implement the features that matter.
            </p>
          </article>

          <article class="card reveal">
            <div class="process-number">03</div>
            <h3>Test & Improve</h3>
            <p class="muted">
              Check mobile layouts, errors, security basics and real functionality.
            </p>
          </article>
        </div>
      </div>
    </section>

    <!-- CONTACT -->
    <section class="section" id="contact">
      <div class="container">
        <div class="contact-panel reveal">
          <div>
            <span class="eyebrow">Get In Touch</span>
            <h2>Have an idea?<br><span class="gradient-text">Let's discuss it.</span></h2>
            <p class="muted">
              Have a project, collaboration idea or useful feedback?
              Send a message and let's talk about the requirements.
            </p>

            <div class="contact-method">
              <div class="feature-icon">✉</div>
              <div>
                <strong>Email</strong>
                <a href="mailto:useable.me2@gmail.com">useable.me2@gmail.com</a>
              </div>
            </div>

            <div class="contact-method">
              <div class="feature-icon">⌘</div>
              <div>
                <strong>GitHub</strong>
                <a href="https://github.com/Mehedi364"
                   target="_blank" rel="noopener noreferrer">
                  github.com/Mehedi364 ↗
                </a>
              </div>
            </div>

            <div class="contact-method">
              <div class="feature-icon">f</div>
              <div>
                <strong>Facebook</strong>
                <a href="https://facebook.com/mehedi3643"
                   target="_blank" rel="noopener noreferrer">
                  facebook.com/mehedi3643 ↗
                </a>
              </div>
            </div>
          </div>

          <form class="contact-form" id="contactForm">
            <div class="field">
              <label for="name">Your name</label>
              <input id="name" name="name" autocomplete="name"
                     placeholder="Enter your name" required maxlength="100">
            </div>

            <div class="field">
              <label for="email">Your email</label>
              <input id="email" name="email" type="email"
                     autocomplete="email" placeholder="you@example.com"
                     required maxlength="254">
            </div>

            <div class="field">
              <label for="message">Message</label>
              <textarea id="message" name="message"
                        placeholder="Tell me about your idea..."
                        required maxlength="5000"></textarea>
            </div>

            <button class="button button-primary" type="submit">
              Prepare Email ↗
            </button>
            <p class="form-note">
              This form opens your email app. It does not send or store
              messages on this website.
            </p>
          </form>
        </div>
      </div>
    </section>
  </main>

  <footer>
    <div class="container footer-inner">
      <a class="brand" href="#home">
        <span class="brand-mark">WZ</span>
        <span>Wafa Zone</span>
      </a>

      <p>© <span id="year"></span> Md. Mehedi Hasan · Mehedi364</p>

      <p>Built with purpose. Improved with care.</p>
    </div>
  </footer>

  <button class="back-top" id="backTop" aria-label="Back to top">↑</button>

  <script>
    (() => {
      "use strict";

      const body = document.body;
      const themeButton = document.getElementById("themeButton");
      const menuButton = document.getElementById("menuButton");
      const navLinks = document.getElementById("navLinks");
      const backTop = document.getElementById("backTop");

      // Theme preference: saved when browser storage is available.
      try {
        const savedTheme = localStorage.getItem("wafa-theme");
        if (savedTheme === "light") body.classList.add("light");
      } catch (_) {}

      function updateThemeButton() {
        const isLight = body.classList.contains("light");
        themeButton.textContent = isLight ? "☾" : "☼";
        themeButton.setAttribute(
          "aria-label",
          isLight ? "Switch to dark theme" : "Switch to light theme"
        );
      }

      updateThemeButton();

      themeButton.addEventListener("click", () => {
        body.classList.toggle("light");
        const theme = body.classList.contains("light") ? "light" : "dark";

        try {
          localStorage.setItem("wafa-theme", theme);
        } catch (_) {}

        updateThemeButton();
      });

      // Mobile navigation.
      menuButton.addEventListener("click", () => {
        const isOpen = navLinks.classList.toggle("open");
        menuButton.setAttribute("aria-expanded", String(isOpen));
        menuButton.setAttribute(
          "aria-label",
          isOpen ? "Close navigation" : "Open navigation"
        );
        menuButton.textContent = isOpen ? "✕" : "☰";
      });

      navLinks.querySelectorAll("a").forEach(link => {
        link.addEventListener("click", () => {
          navLinks.classList.remove("open");
          menuButton.setAttribute("aria-expanded", "false");
          menuButton.setAttribute("aria-label", "Open navigation");
          menuButton.textContent = "☰";
        });
      });

      // Project category filters.
      const filterButtons = document.querySelectorAll("[data-filter]");
      const projectCards = document.querySelectorAll(".project-card");

      filterButtons.forEach(button => {
        button.addEventListener("click", () => {
          const filter = button.dataset.filter;

          filterButtons.forEach(item => {
            const active = item === button;
            item.classList.toggle("active", active);
            item.setAttribute("aria-pressed", String(active));
          });

          projectCards.forEach(card => {
            const matches =
              filter === "all" || card.dataset.category === filter;
            card.hidden = !matches;
          });
        });
      });

      // Contact form: prepare a message in the visitor's email application.
      document.getElementById("contactForm").addEventListener("submit", event => {
        event.preventDefault();

        const name = document.getElementById("name").value.trim();
        const email = document.getElementById("email").value.trim();
        const message = document.getElementById("message").value.trim();

        if (!name || !email || !message) {
          alert("Please complete all fields.");
          return;
        }

        const subject = encodeURIComponent("Portfolio inquiry from " + name);
        const bodyText = encodeURIComponent(
          "Name: " + name + "\n" +
          "Email: " + email + "\n\n" +
          "Message:\n" + message
        );

        window.location.href =
          "mailto:useable.me2@gmail.com?subject=" +
          subject + "&body=" + bodyText;
      });

      // Scroll-to-top control.
      function updateBackTop() {
        backTop.classList.toggle("visible", window.scrollY > 450);
      }

      window.addEventListener("scroll", updateBackTop, { passive: true });
      updateBackTop();

      backTop.addEventListener("click", () => {
        window.scrollTo({ top: 0, behavior: "smooth" });
      });

      // Reveal sections as they enter the viewport.
      const revealElements = document.querySelectorAll(".reveal");

      if ("IntersectionObserver" in window) {
        const observer = new IntersectionObserver(entries => {
          entries.forEach(entry => {
            if (entry.isIntersecting) {
              entry.target.classList.add("show");
              observer.unobserve(entry.target);
            }
          });
        }, { threshold: 0.08 });

        revealElements.forEach(element => observer.observe(element));
      } else {
        revealElements.forEach(element => element.classList.add("show"));
      }

      // Current year.
      document.getElementById("year").textContent = new Date().getFullYear();

      // Highlight the navigation item for the current section.
      const sections = document.querySelectorAll("main section[id]");
      if ("IntersectionObserver" in window) {
        const sectionObserver = new IntersectionObserver(entries => {
          entries.forEach(entry => {
            if (!entry.isIntersecting) return;

            navLinks.querySelectorAll("a").forEach(link => {
              const active = link.getAttribute("href") === "#" + entry.target.id;
              link.classList.toggle("active", active);
            });
          });
        }, { rootMargin: "-25% 0px -60% 0px" });

        sections.forEach(section => sectionObserver.observe(section));
      }
    })();
  </script>
</body>
</html>
