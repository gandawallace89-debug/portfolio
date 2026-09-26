<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Wallace Ganda | Portfolio</title>
    <meta
      name="description"
      content="Portfolio website for Wallace Ganda, a KCA University student passionate about software development."
    />
    <style>
      :root {
        --bg: #f5f0ea;
        --panel: #fffdfb;
        --primary: #1b2a3a;
        --secondary: #d07a5a;
        --text: #202b36;
        --muted: #5b6977;
        --accent: #f3d7c5;
        --shadow: rgba(23, 33, 42, 0.14);
      }

      * {
        box-sizing: border-box;
      }

      html {
        scroll-behavior: smooth;
      }

      body {
        margin: 0;
        font-family: Arial, Helvetica, sans-serif;
        background: var(--bg);
        color: var(--text);
        line-height: 1.7;
      }

      a {
        text-decoration: none;
        color: inherit;
      }

      img {
        max-width: 100%;
        display: block;
      }

      .container {
        width: min(1100px, calc(100% - 32px));
        margin: 0 auto;
      }

      header {
        background: rgba(245, 240, 234, 0.95);
        backdrop-filter: blur(10px);
        position: sticky;
        top: 0;
        z-index: 10;
        border-bottom: 1px solid rgba(27, 42, 58, 0.08);
      }

      nav {
        display: flex;
        align-items: center;
        justify-content: space-between;
        padding: 18px 0;
      }

      .brand {
        font-size: 1.8rem;
        font-weight: 700;
        letter-spacing: 0.04em;
      }

      .nav-links {
        display: flex;
        gap: 28px;
        align-items: center;
        font-weight: 600;
      }

      .nav-links a {
        color: var(--muted);
        transition: color 0.2s ease;
      }

      .nav-links a:hover {
        color: var(--secondary);
      }

      .nav-links .button-link {
        background: var(--primary);
        color: #fff;
        padding: 11px 18px;
        border-radius: 999px;
      }

      section {
        padding: 90px 0;
      }

      .hero {
        display: grid;
        grid-template-columns: 1.2fr 0.8fr;
        gap: 48px;
        align-items: center;
        min-height: 80vh;
      }

      .eyebrow {
        display: inline-block;
        padding: 8px 16px;
        border-radius: 999px;
        background: var(--accent);
        color: var(--primary);
        font-size: 0.8rem;
        font-weight: 700;
        letter-spacing: 0.08em;
        text-transform: uppercase;
      }

      h1, h2, h3 {
        margin-top: 0;
        line-height: 1.15;
      }

      h1 {
        font-size: clamp(2.8rem, 5vw, 5.2rem);
        margin: 20px 0 18px;
      }

      .highlight {
        color: var(--secondary);
      }

      .hero p {
        font-size: 1.1rem;
        color: var(--muted);
        max-width: 620px;
      }

      .actions {
        display: flex;
        flex-wrap: wrap;
        gap: 14px;
        margin-top: 26px;
      }

      .button {
        display: inline-block;
        background: var(--primary);
        color: #fff;
        padding: 14px 24px;
        border-radius: 999px;
        font-weight: 700;
        transition: transform 0.2s ease, box-shadow 0.2s ease;
      }

      .button:hover {
        transform: translateY(-2px);
        box-shadow: 0 14px 30px rgba(27, 42, 58, 0.15);
      }

      .button.secondary {
        background: transparent;
        border: 2px solid var(--primary);
        color: var(--primary);
      }

      .profile-box {
        background: var(--panel);
        border-radius: 28px;
        box-shadow: 0 20px 40px var(--shadow);
        padding: 18px;
      }

      .profile-box img {
        width: 100%;
        height: 560px;
        object-fit: cover;
        border-radius: 20px;
      }

      .section-title {
        text-align: center;
        margin-bottom: 40px;
      }

      .section-title h2 {
        font-size: clamp(2.2rem, 4vw, 3.5rem);
        margin-bottom: 10px;
      }

      .section-title p {
        color: var(--muted);
        margin: 0;
      }

      .about {
        background: #f0e9e2;
      }

      .about-grid {
        display: grid;
        grid-template-columns: 0.9fr 1.1fr;
        gap: 42px;
        align-items: center;
      }

      .about-grid p {
        color: var(--muted);
        margin: 0 0 14px;
      }

      .about-image {
        background: var(--panel);
        border-radius: 28px;
        padding: 18px;
        box-shadow: 0 18px 32px var(--shadow);
      }

      .about-image img {
        width: 100%;
        height: 420px;
        object-fit: cover;
        border-radius: 18px;
      }

      .services-grid {
        display: grid;
        grid-template-columns: repeat(3, minmax(0, 1fr));
        gap: 24px;
      }

      .service-card {
        background: var(--panel);
        border-radius: 22px;
        padding: 28px 22px;
        box-shadow: 0 14px 26px rgba(17, 25, 33, 0.06);
      }

      .service-card h3 {
        font-size: 1.5rem;
        margin-bottom: 12px;
      }

      .service-card p {
        color: var(--muted);
        margin: 0;
      }

      .contact-wrap {
        display: grid;
        grid-template-columns: 1fr 1fr;
        gap: 30px;
        align-items: center;
      }

      .contact-card {
        background: var(--panel);
        padding: 32px;
        border-radius: 22px;
        box-shadow: 0 14px 26px rgba(17, 25, 33, 0.07);
      }

      .contact-card p {
        margin: 0 0 12px;
        color: var(--muted);
      }

      footer {
        background: var(--primary);
        color: rgba(255,255,255,0.8);
        text-align: center;
        padding: 28px 0;
      }

      @media (max-width: 760px) {
        .nav-links {
          gap: 12px;
          font-size: 0.9rem;
        }

        .hero,
        .about-grid,
        .services-grid,
        .contact-wrap {
          grid-template-columns: 1fr;
        }

        .profile-box img {
          height: 440px;
        }

        nav {
          flex-wrap: wrap;
          gap: 12px;
        }
      }
    </style>
  </head>
  <body>
    <header>
      <div class="container">
        <nav>
          <a href="#home" class="brand">Wallace Ganda</a>
          <div class="nav-links">
            <a href="#home">Home</a>
            <a href="#about">About</a>
            <a href="#services">Services</a>
            <a href="#contact">Contact</a>
            <a href="#contact" class="button-link">Hire Me</a>
          </div>
        </nav>
      </div>
    </header>

    <main>
      <section id="home" class="container hero">
        <div>
          <span class="eyebrow">Student Portfolio</span>
          <h1>Hello, I'm <span class="highlight">Wallace Ganda</span></h1>
          <h3>Welcome to my autobiography</h3>
          <p>
            This website tells a little story about who I am, my interests, my skills,
            and my goals. I am a student at KCA University with a growing passion for
            software development and web design.
          </p>
          <div class="actions">
            <a href="#about" class="button">Learn More</a>
            <a href="#contact" class="button secondary">Contact Me</a>
          </div>
        </div>

        <div class="profile-box">
          <img src="WhatsApp Image 2026-09-26 at 4.42.52 PM.jpeg" alt="Wallace Ganda profile photo" />
        </div>
      </section>

      <section id="about" class="about">
        <div class="container about-grid">
          <div class="about-image">
            <img src="WhatsApp Image 2026-09-26 at 4.42.52 PM.jpeg" alt="Wallace Ganda portrait" />
          </div>

          <div>
            <div class="section-title" style="text-align: left; margin-bottom: 18px;">
              <h2>About Me</h2>
            </div>
            <p>
              My name is Wallace Ganda. I am a student at KCA University, and I am
              passionate about software development. I enjoy learning new things and
              building my skills in coding and digital technology.
            </p>
            <p>
              I started learning programming because I wanted to understand how websites
              and applications are created. I am especially interested in creating useful,
              well-designed digital solutions and growing into a skilled software developer.
            </p>
            <p>
              My goal is to keep improving my technical knowledge, develop practical
              problem-solving skills, and one day contribute meaningfully to the world of
              technology.
            </p>
          </div>
        </div>
      </section>

      <section id="services">
        <div class="container">
          <div class="section-title">
            <h2>My Services</h2>
            <p>Skills and areas I am developing as part of my journey.</p>
          </div>

          <div class="services-grid">
            <div class="service-card">
              <h3>Web Design</h3>
              <p>
                Creating simple, modern, and attractive websites using HTML and CSS
                to make digital experiences more engaging.
              </p>
            </div>

            <div class="service-card">
              <h3>Programming</h3>
              <p>
                Learning and developing basic programs using different programming
                languages and improving logical thinking through code.
              </p>
            </div>

            <div class="service-card">
              <h3>Computer Skills</h3>
              <p>
                Supporting basic computer operations, software installation, and general
                digital assistance for everyday productivity.
              </p>
            </div>
          </div>
        </div>
      </section>

      <section id="contact">
        <div class="container">
          <div class="section-title">
            <h2>Contact Me</h2>
            <p>Let's connect and grow together.</p>
          </div>

          <div class="contact-wrap">
            <div class="contact-card">
              <p><strong>Email:</strong> wallaceganda@gmail.com</p>
              <p><strong>Phone:</strong> +254 727 577 390</p>
              <p><strong>Location:</strong> Kisumu, Kenya</p>
            </div>

            <div class="contact-card">
              <p>
                I am open to learning opportunities, collaborations, and projects that help
                me build my skills in technology and software development.
              </p>
              <a href="mailto:wallaceganda@gmail.com" class="button">Send Email</a>
            </div>
          </div>
        </div>
      </section>
    </main>

    <footer>
      <div class="container">
        &copy; 2026 Wallace Ganda. All Rights Reserved.
      </div>
    </footer>
  </body>
</html>
