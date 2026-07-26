<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Abhijeet Pathak · Digital Marketing & Dev</title>
  <!-- Font Awesome 6 (free) -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
  <!-- Google Fonts: Inter & Space Grotesk -->
  <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,400;14..32,500;14..32,600;14..32,700&family=Space+Grotesk:wght@400;500;600;700&display=swap" rel="stylesheet">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      background: #f6f9fc;
      font-family: 'Inter', sans-serif;
      color: #0b1a2e;
      padding: 2rem 1.5rem;
      display: flex;
      justify-content: center;
      align-items: center;
      min-height: 100vh;
    }

    .card {
      max-width: 1200px;
      width: 100%;
      background: #ffffff;
      border-radius: 2.5rem;
      box-shadow: 0 25px 50px -12px rgba(0, 0, 0, 0.15);
      padding: 2.5rem 2.8rem;
      transition: all 0.2s ease;
    }

    /* ----- header & profile ----- */
    .profile-head {
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
      align-items: flex-start;
      margin-bottom: 2.5rem;
      border-bottom: 2px solid #eef3f7;
      padding-bottom: 1.8rem;
    }

    .title-group h1 {
      font-family: 'Space Grotesk', sans-serif;
      font-size: 2.6rem;
      font-weight: 700;
      letter-spacing: -0.02em;
      color: #0b1a2e;
      margin-bottom: 0.3rem;
    }

    .title-group h1 i {
      color: #2563eb;
      margin-right: 8px;
    }

    .title-group .subhead {
      font-size: 1.15rem;
      font-weight: 500;
      color: #1e3a5f;
      background: #eaf2fb;
      display: inline-block;
      padding: 0.3rem 1.2rem;
      border-radius: 40px;
      letter-spacing: -0.01em;
    }

    .badge-links {
      display: flex;
      gap: 0.9rem;
      margin-top: 0.6rem;
      flex-wrap: wrap;
    }

    .badge-links a {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      background: #f0f5fa;
      padding: 0.5rem 1.2rem;
      border-radius: 40px;
      text-decoration: none;
      font-weight: 500;
      font-size: 0.95rem;
      color: #1a3149;
      transition: 0.2s;
      border: 1px solid transparent;
    }

    .badge-links a:hover {
      background: #e3edf7;
      border-color: #2563eb30;
      color: #0b1a2e;
      transform: translateY(-2px);
    }

    .badge-links a i {
      font-size: 1.2rem;
      color: #2563eb;
    }

    /* ----- about section ----- */
    .about-grid {
      display: grid;
      grid-template-columns: 1.2fr 0.8fr;
      gap: 2rem;
      margin: 2rem 0 2.8rem 0;
    }

    .about-text p {
      font-size: 1rem;
      line-height: 1.6;
      color: #1f3a57;
      margin-bottom: 0.8rem;
    }

    .about-text strong {
      color: #0b1a2e;
      font-weight: 600;
    }

    .highlight-tag {
      display: inline-block;
      background: #dbeafe;
      padding: 0.2rem 0.9rem;
      border-radius: 30px;
      font-size: 0.85rem;
      font-weight: 600;
      color: #1e4b8a;
      margin-right: 5px;
    }

    .stats-mini {
      background: #f8fafc;
      border-radius: 2rem;
      padding: 1.5rem 1.8rem;
      border: 1px solid #e7edf3;
    }

    .stats-mini .stat-item {
      display: flex;
      align-items: center;
      gap: 12px;
      font-size: 0.95rem;
      padding: 0.5rem 0;
      border-bottom: 1px dashed #dde6ef;
    }

    .stats-mini .stat-item:last-child {
      border-bottom: 0;
    }

    .stats-mini i {
      width: 28px;
      color: #2563eb;
      font-size: 1.2rem;
    }

    /* ----- tech stack (skill icons) ----- */
    .tech-stack {
      margin: 2rem 0 2.8rem 0;
    }

    .tech-stack h3 {
      font-size: 1.2rem;
      font-weight: 600;
      letter-spacing: -0.01em;
      color: #1a3149;
      margin-bottom: 1rem;
      display: flex;
      align-items: center;
      gap: 8px;
    }

    .tech-stack h3 i {
      color: #2563eb;
    }

    .icon-grid {
      display: flex;
      flex-wrap: wrap;
      gap: 0.8rem 1.2rem;
      background: #f9fcff;
      padding: 1.2rem 1.8rem;
      border-radius: 60px;
      border: 1px solid #eaf0f5;
      align-items: center;
    }

    .icon-grid img {
      height: 40px;
      width: auto;
      filter: grayscale(0.1);
      transition: 0.2s;
    }

    .icon-grid img:hover {
      transform: scale(1.08);
      filter: grayscale(0);
    }

    /* fallback text for skill icons (if image fails) */
    .icon-grid span {
      font-size: 0.9rem;
      font-weight: 500;
      color: #1e3a5f;
      background: #eef3f8;
      padding: 0.2rem 1rem;
      border-radius: 30px;
    }

    /* ----- projects ----- */
    .projects h3 {
      font-size: 1.3rem;
      font-weight: 600;
      margin-bottom: 1.2rem;
      display: flex;
      align-items: center;
      gap: 8px;
    }

    .projects h3 i {
      color: #2563eb;
    }

    .project-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 1.8rem;
    }

    .project-card {
      background: #fafcfe;
      border-radius: 1.8rem;
      padding: 1.6rem 1.8rem;
      border: 1px solid #e7edf5;
      transition: 0.2s;
    }

    .project-card:hover {
      border-color: #b8cee8;
      box-shadow: 0 10px 20px -8px rgba(0, 20, 50, 0.08);
      transform: translateY(-4px);
    }

    .project-card h4 {
      font-size: 1.1rem;
      font-weight: 600;
      color: #0b1a2e;
      margin-bottom: 0.3rem;
    }

    .project-card .tech-badge {
      font-size: 0.7rem;
      background: #dce6f0;
      padding: 0.2rem 0.8rem;
      border-radius: 30px;
      display: inline-block;
      font-weight: 600;
      color: #1a3e66;
      margin: 0.3rem 0 0.6rem 0;
      letter-spacing: 0.3px;
    }

    .project-card p {
      font-size: 0.95rem;
      line-height: 1.5;
      color: #26415e;
    }

    .project-card .tech-stack-sm {
      margin-top: 0.8rem;
      font-size: 0.8rem;
      color: #3d5f83;
      font-weight: 500;
    }

    /* ----- github stats ----- */
    .github-stats {
      display: flex;
      flex-wrap: wrap;
      align-items: center;
      justify-content: center;
      gap: 1.8rem;
      margin: 2.8rem 0 1.5rem 0;
      background: #f4f9ff;
      padding: 1.5rem 1.8rem;
      border-radius: 3rem;
      border: 1px solid #e2ecf6;
    }

    .github-stats img {
      height: 165px;
      width: auto;
      border-radius: 20px;
      background: white;
      box-shadow: 0 4px 10px rgba(0,0,0,0.02);
    }

    .github-stats .placeholder-stat {
      display: flex;
      align-items: center;
      gap: 20px;
    }

    /* footer */
    .footer-note {
      text-align: center;
      margin-top: 2.2rem;
      font-size: 0.95rem;
      color: #3d5f83;
      border-top: 1px solid #e6eef6;
      padding-top: 1.8rem;
      letter-spacing: -0.2px;
    }

    .footer-note i {
      color: #2563eb;
      margin: 0 4px;
    }

    /* responsiveness */
    @media (max-width: 800px) {
      .card {
        padding: 1.8rem;
      }
      .about-grid {
        grid-template-columns: 1fr;
        gap: 1rem;
      }
      .profile-head {
        flex-direction: column;
      }
      .badge-links {
        margin-top: 1rem;
      }
      .title-group h1 {
        font-size: 2rem;
      }
      .icon-grid {
        border-radius: 30px;
        padding: 0.8rem 1.5rem;
        gap: 0.6rem 1rem;
      }
      .github-stats {
        flex-direction: column;
        align-items: center;
        border-radius: 2rem;
      }
      .github-stats img {
        height: 140px;
      }
    }

    @media (max-width: 480px) {
      .badge-links a {
        padding: 0.4rem 1rem;
        font-size: 0.8rem;
      }
      .project-grid {
        grid-template-columns: 1fr;
      }
    }

    /* small tweaks */
    .text-muted {
      color: #3b5e7e;
    }
    .inline-icon {
      margin-right: 6px;
    }
    .fa-chevron-right {
      font-size: 0.7rem;
      color: #2563eb;
    }
  </style>
</head>
<body>
<div class="card">

  <!-- header -->
  <div class="profile-head">
    <div class="title-group">
      <h1><i class="fas fa-code"></i> Abhijeet Pathak</h1>
      <div class="subhead">
        <i class="fas fa-bullhorn" style="margin-right: 6px;"></i> Digital Marketing Manager · WordPress Dev · Full-Stack (Java + React)
      </div>
      <div class="badge-links">
        <a href="#"><i class="fab fa-linkedin-in"></i> LinkedIn</a>
        <a href="#"><i class="fas fa-envelope"></i> Email</a>
      </div>
    </div>
    <div style="display: flex; gap: 12px; flex-wrap: wrap; margin-top: 0.5rem;">
      <span style="background: #e2ecf6; padding: 0.3rem 1.2rem; border-radius: 40px; font-weight: 500; font-size: 0.9rem;"><i class="fas fa-map-pin" style="color: #2563eb;"></i> SMB · Growth</span>
      <span style="background: #e2ecf6; padding: 0.3rem 1.2rem; border-radius: 40px; font-weight: 500; font-size: 0.9rem;"><i class="fas fa-rocket" style="color: #2563eb;"></i> 3+ years</span>
    </div>
  </div>

  <!-- about + mini stats -->
  <div class="about-grid">
    <div class="about-text">
      <p><i class="fas fa-user-tie" style="color: #2563eb; margin-right: 6px;"></i> <strong>Digital Marketing Manager</strong> with 3+ years in SEO, Meta Ads, and content strategy for SMBs. I bridge marketing and technical execution by building WordPress sites, CRM tools, and web apps.</p>
      <p><i class="fas fa-cogs" style="color: #2563eb; margin-right: 6px;"></i> Built an internal CRM system (lead & client management) at WitQualis Technologies. Currently upgrading full-stack skills: <span class="highlight-tag">Core/Advanced Java</span> <span class="highlight-tag">React.js</span> <span class="highlight-tag">GenAI</span> <span class="highlight-tag">Backend</span></p>
      <p><i class="fas fa-lightbulb" style="color: #2563eb; margin-right: 6px;"></i> I enjoy building practical digital products that support growth, automation, and better user experience.</p>
    </div>
    <div class="stats-mini">
      <div class="stat-item"><i class="fas fa-globe"></i> <span><strong>SEO + Meta Ads</strong> · SMB growth</span></div>
      <div class="stat-item"><i class="fas fa-wordpress"></i> <span><strong>WordPress</strong> · custom themes & plugins</span></div>
      <div class="stat-item"><i class="fas fa-database"></i> <span><strong>CRM system</strong> · PHP · MySQL</span></div>
      <div class="stat-item"><i class="fas fa-code"></i> <span><strong>Full-stack</strong> Java + React + GenAI</span></div>
    </div>
  </div>

  <!-- Tech stack (skill icons) -->
  <div class="tech-stack">
    <h3><i class="fas fa-laptop-code"></i> Tech Stack</h3>
    <div class="icon-grid">
      <!-- using skill icons from CDN (simulated) -->
      <img src="https://skillicons.dev/icons?i=html" alt="HTML5" title="HTML5">
      <img src="https://skillicons.dev/icons?i=css" alt="CSS3" title="CSS3">
      <img src="https://skillicons.dev/icons?i=js" alt="JavaScript" title="JavaScript">
      <img src="https://skillicons.dev/icons?i=php" alt="PHP" title="PHP">
      <img src="https://skillicons.dev/icons?i=mysql" alt="MySQL" title="MySQL">
      <img src="https://skillicons.dev/icons?i=wordpress" alt="WordPress" title="WordPress">
      <img src="https://skillicons.dev/icons?i=java" alt="Java" title="Java">
      <img src="https://skillicons.dev/icons?i=react" alt="React" title="React">
      <img src="https://skillicons.dev/icons?i=git" alt="Git" title="Git">
      <img src="https://skillicons.dev/icons?i=github" alt="GitHub" title="GitHub">
      <img src="https://skillicons.dev/icons?i=vscode" alt="VSCode" title="VSCode">
      <!-- fallback text for any missing -->
      <span><i class="fas fa-brain" style="margin-right: 4px;"></i> GenAI</span>
    </div>
  </div>

  <!-- Featured Projects -->
  <div class="projects">
    <h3><i class="fas fa-folder-open"></i> Featured Projects</h3>
    <div class="project-grid">
      <div class="project-card">
        <h4>WitQualis Internal CRM</h4>
        <span class="tech-badge">PHP · MySQL · HTML5 · CSS3 · JS</span>
        <p>Streamlined lead tracking & client communication for sales & marketing teams. Built from scratch.</p>
        <div class="tech-stack-sm"><i class="fas fa-tag"></i> custom dashboard · automation</div>
      </div>
      <div class="project-card">
        <h4>Planwise — Productivity & Travel</h4>
        <span class="tech-badge">WordPress · PHP · MySQL</span>
        <p>Custom WordPress theme with multi-user dashboard, custom post types, and automated email reminders.</p>
        <div class="tech-stack-sm"><i class="fas fa-tag"></i> ecosystem · travel</div>
      </div>
      <div class="project-card">
        <h4>Portfolio Animated Website</h4>
        <span class="tech-badge">Three.js · GSAP · JavaScript</span>
        <p>7‑page, zero‑plugin portfolio with Three.js particle backgrounds and GSAP parallax scrolling.</p>
        <div class="tech-stack-sm"><i class="fas fa-tag"></i> creative · immersive</div>
      </div>
      <div class="project-card">
        <h4>FinanceBharat Magazine</h4>
        <span class="tech-badge">WordPress · Elementor · Structured Data</span>
        <p>SEO‑optimized digital magazine theme built for AdSense monetization with live market ticker.</p>
        <div class="tech-stack-sm"><i class="fas fa-tag"></i> AdSense · structured data</div>
      </div>
      <div class="project-card">
        <h4>E‑commerce Interface</h4>
        <span class="tech-badge">HTML5 · CSS3 · JavaScript</span>
        <p>Responsive front‑end with dynamic filtering and cart logic. Clean UI, smooth interactions.</p>
        <div class="tech-stack-sm"><i class="fas fa-tag"></i> front‑end · cart logic</div>
      </div>
    </div>
  </div>

  <!-- GitHub Stats -->
  <div class="github-stats">
    <div class="placeholder-stat">
      <img src="https://github-readme-stats.vercel.app/api?username=abhijeetpathak&show_icons=true&theme=default&hide_border=true&bg_color=f4f9ff&title_color=0b1a2e&text_color=1f3a57" alt="GitHub Stats" />
      <img src="https://github-readme-streak-stats.herokuapp.com/?user=abhijeetpathak&theme=default&hide_border=true&background=f4f9ff&stroke=2563eb&ring=2563eb&fire=2563eb&currStreakLabel=0b1a2e" alt="GitHub Streak" />
    </div>
  </div>

  <!-- footer -->
  <div class="footer-note">
    <i class="fas fa-handshake"></i> Open to connecting with SMB founders, marketing teams, and fellow developers <i class="fas fa-arrow-right"></i> 
    <span style="background: #e6f0fa; padding: 0.1rem 1.2rem; border-radius: 30px; font-weight: 500;">Let's build something great</span>
  </div>

</div>
</body>
</html>
