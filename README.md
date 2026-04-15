# portfolio[index.html](https://github.com/user-attachments/files/26758952/index.html)
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Aditya Vaish — Research & Analytics</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=DM+Serif+Display:ital@0;1&family=DM+Sans:wght@300;400;500;600&family=JetBrains+Mono:wght@400;600&display=swap" rel="stylesheet">
<style>
  :root {
    --ink: #0d1117;
    --paper: #f5f0e8;
    --gold: #c9922a;
    --gold-light: #e8b84b;
    --muted: #6b6357;
    --border: #ddd8ce;
    --accent-bg: #1a1410;
  }

  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  html { scroll-behavior: smooth; }

  body {
    background: var(--paper);
    color: var(--ink);
    font-family: 'DM Sans', sans-serif;
    font-size: 16px;
    line-height: 1.6;
    overflow-x: hidden;
  }

  /* ── NAV ── */
  nav {
    position: fixed; top: 0; left: 0; right: 0; z-index: 100;
    display: flex; justify-content: space-between; align-items: center;
    padding: 1rem 3rem;
    background: rgba(245, 240, 232, 0.92);
    backdrop-filter: blur(10px);
    border-bottom: 1px solid var(--border);
  }
  .nav-logo {
    font-family: 'JetBrains Mono', monospace;
    font-size: 0.8rem; font-weight: 600;
    color: var(--gold); letter-spacing: 0.15em; text-transform: uppercase;
  }
  .nav-links { display: flex; gap: 2rem; list-style: none; }
  .nav-links a {
    text-decoration: none; color: var(--muted);
    font-size: 0.85rem; font-weight: 500; letter-spacing: 0.05em;
    transition: color 0.2s;
  }
  .nav-links a:hover { color: var(--gold); }

  /* ── HERO ── */
  .hero {
    min-height: 100vh;
    display: grid; grid-template-columns: 1fr 1fr;
    align-items: center;
    padding: 8rem 3rem 4rem;
    gap: 4rem;
    position: relative;
    overflow: hidden;
  }
  .hero::before {
    content: '';
    position: absolute; top: -20%; right: -10%;
    width: 600px; height: 600px;
    background: radial-gradient(circle, rgba(201,146,42,0.08) 0%, transparent 70%);
    pointer-events: none;
  }

  .hero-label {
    font-family: 'JetBrains Mono', monospace;
    font-size: 0.75rem; color: var(--gold);
    letter-spacing: 0.2em; text-transform: uppercase;
    margin-bottom: 1.5rem;
    display: flex; align-items: center; gap: 0.75rem;
  }
  .hero-label::before {
    content: '';
    display: inline-block; width: 30px; height: 1px; background: var(--gold);
  }
  h1 {
    font-family: 'DM Serif Display', serif;
    font-size: clamp(3rem, 6vw, 5.5rem);
    line-height: 1.05;
    letter-spacing: -0.02em;
    margin-bottom: 1.5rem;
  }
  h1 em {
    font-style: italic; color: var(--gold);
  }
  .hero-sub {
    font-size: 1.1rem; color: var(--muted);
    max-width: 420px; line-height: 1.75;
    margin-bottom: 2.5rem;
  }
  .hero-cta {
    display: flex; gap: 1rem; flex-wrap: wrap;
  }
  .btn {
    padding: 0.75rem 1.75rem; border-radius: 2px;
    font-size: 0.85rem; font-weight: 600;
    letter-spacing: 0.08em; text-transform: uppercase;
    text-decoration: none; cursor: pointer; border: none;
    transition: all 0.25s;
  }
  .btn-primary {
    background: var(--accent-bg); color: var(--gold-light);
    border: 1px solid var(--accent-bg);
  }
  .btn-primary:hover { background: var(--gold); color: var(--ink); }
  .btn-outline {
    background: transparent; color: var(--ink);
    border: 1.5px solid var(--ink);
  }
  .btn-outline:hover { background: var(--ink); color: var(--paper); }

  .hero-stats {
    display: grid; grid-template-columns: 1fr 1fr; gap: 1.5rem;
  }
  .stat-card {
    background: white;
    border: 1px solid var(--border);
    padding: 1.5rem;
    border-radius: 4px;
    position: relative;
    overflow: hidden;
    transition: transform 0.25s, box-shadow 0.25s;
  }
  .stat-card:hover {
    transform: translateY(-3px);
    box-shadow: 0 12px 40px rgba(0,0,0,0.08);
  }
  .stat-card::before {
    content: '';
    position: absolute; top: 0; left: 0; right: 0; height: 3px;
    background: var(--gold);
  }
  .stat-num {
    font-family: 'DM Serif Display', serif;
    font-size: 2.2rem; color: var(--ink);
    line-height: 1.1;
  }
  .stat-desc {
    font-size: 0.8rem; color: var(--muted);
    margin-top: 0.25rem; line-height: 1.4;
  }
  .stat-card.dark {
    background: var(--accent-bg); border-color: var(--accent-bg);
  }
  .stat-card.dark .stat-num { color: var(--gold-light); }
  .stat-card.dark .stat-desc { color: #a09080; }

  /* ── SECTION COMMONS ── */
  section { padding: 6rem 3rem; }
  .section-label {
    font-family: 'JetBrains Mono', monospace;
    font-size: 0.7rem; color: var(--gold);
    letter-spacing: 0.25em; text-transform: uppercase;
    margin-bottom: 0.75rem;
  }
  h2 {
    font-family: 'DM Serif Display', serif;
    font-size: clamp(2rem, 4vw, 3rem);
    line-height: 1.15; margin-bottom: 3rem;
  }

  /* ── PROJECTS ── */
  .projects { background: white; }
  .projects-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 2rem; }
  .project-card {
    border: 1px solid var(--border);
    padding: 2rem;
    border-radius: 4px;
    transition: all 0.3s;
    position: relative;
  }
  .project-card:hover {
    box-shadow: 0 16px 48px rgba(0,0,0,0.1);
    transform: translateY(-4px);
    border-color: var(--gold);
  }
  .project-tag {
    display: inline-block;
    font-family: 'JetBrains Mono', monospace;
    font-size: 0.65rem; font-weight: 600;
    letter-spacing: 0.15em; text-transform: uppercase;
    padding: 0.3rem 0.75rem;
    border-radius: 20px;
    margin-bottom: 1rem;
  }
  .tag-finance { background: #fff3e0; color: #c9922a; }
  .tag-analytics { background: #e8f5e9; color: #2e7d32; }
  .tag-research { background: #e3f2fd; color: #1565c0; }
  .tag-market { background: #fce4ec; color: #c62828; }

  .project-title {
    font-family: 'DM Serif Display', serif;
    font-size: 1.3rem; margin-bottom: 0.75rem;
  }
  .project-desc { color: var(--muted); font-size: 0.9rem; line-height: 1.65; margin-bottom: 1.25rem; }
  .project-highlights { list-style: none; display: flex; flex-direction: column; gap: 0.4rem; }
  .project-highlights li {
    font-size: 0.82rem; color: var(--ink);
    display: flex; align-items: flex-start; gap: 0.5rem;
  }
  .project-highlights li::before { content: '→'; color: var(--gold); flex-shrink: 0; margin-top: 1px; }

  /* ── MARKET SECTION ── */
  .market { background: var(--accent-bg); color: var(--paper); }
  .market h2 { color: var(--paper); }
  .market .section-label { color: var(--gold); }
  .market-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 3rem; align-items: start; }
  .market-text p { color: #b0a090; line-height: 1.8; margin-bottom: 1rem; font-size: 0.95rem; }
  .market-text strong { color: var(--gold-light); }
  .ticker-list { display: flex; flex-direction: column; gap: 0.75rem; }
  .ticker {
    display: flex; justify-content: space-between; align-items: center;
    padding: 1rem 1.25rem;
    background: rgba(255,255,255,0.04);
    border: 1px solid rgba(201,146,42,0.2);
    border-radius: 4px;
    transition: border-color 0.2s;
  }
  .ticker:hover { border-color: var(--gold); }
  .ticker-name { font-weight: 600; font-size: 0.9rem; }
  .ticker-sector { font-size: 0.75rem; color: #a09080; margin-top: 2px; }
  .ticker-badge {
    font-family: 'JetBrains Mono', monospace;
    font-size: 0.7rem; padding: 0.2rem 0.6rem;
    border-radius: 3px; background: rgba(201,146,42,0.15);
    color: var(--gold-light);
  }

  /* ── SKILLS ── */
  .skills-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(240px, 1fr)); gap: 1.5rem; }
  .skill-group {
    padding: 1.75rem;
    border: 1px solid var(--border);
    border-radius: 4px;
    background: white;
  }
  .skill-group-title {
    font-size: 0.75rem; font-weight: 600;
    letter-spacing: 0.1em; text-transform: uppercase;
    color: var(--gold); margin-bottom: 1rem;
  }
  .skill-pills { display: flex; flex-wrap: wrap; gap: 0.5rem; }
  .pill {
    padding: 0.3rem 0.8rem;
    background: var(--paper);
    border: 1px solid var(--border);
    border-radius: 20px;
    font-size: 0.8rem; color: var(--ink);
    transition: all 0.2s;
  }
  .pill:hover { background: var(--gold); color: white; border-color: var(--gold); }

  /* ── CERTS ── */
  .certs { background: white; }
  .certs-list { display: grid; grid-template-columns: repeat(auto-fit, minmax(260px, 1fr)); gap: 1.25rem; }
  .cert-item {
    display: flex; gap: 1rem; align-items: flex-start;
    padding: 1.25rem; border: 1px solid var(--border); border-radius: 4px;
  }
  .cert-icon {
    width: 40px; height: 40px; flex-shrink: 0;
    background: var(--accent-bg);
    border-radius: 8px; display: flex; align-items: center; justify-content: center;
    font-size: 1.1rem;
  }
  .cert-name { font-weight: 600; font-size: 0.9rem; margin-bottom: 0.2rem; }
  .cert-org { font-size: 0.78rem; color: var(--muted); }

  /* ── CONTACT ── */
  .contact { text-align: center; padding: 5rem 3rem; }
  .contact h2 { margin-bottom: 1rem; }
  .contact p { color: var(--muted); margin-bottom: 2rem; }
  .contact-links { display: flex; gap: 1rem; justify-content: center; flex-wrap: wrap; }
  .contact-link {
    display: flex; align-items: center; gap: 0.5rem;
    padding: 0.7rem 1.5rem; border: 1.5px solid var(--border);
    border-radius: 4px; text-decoration: none; color: var(--ink);
    font-size: 0.85rem; font-weight: 500;
    transition: all 0.2s;
  }
  .contact-link:hover { border-color: var(--gold); color: var(--gold); }

  /* ── FOOTER ── */
  footer {
    text-align: center; padding: 2rem;
    border-top: 1px solid var(--border);
    font-family: 'JetBrains Mono', monospace;
    font-size: 0.72rem; color: var(--muted);
    letter-spacing: 0.1em;
  }

  /* ── ANIMATIONS ── */
  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(24px); }
    to { opacity: 1; transform: translateY(0); }
  }
  .hero-text > * { animation: fadeUp 0.7s ease both; }
  .hero-text > *:nth-child(1) { animation-delay: 0.1s; }
  .hero-text > *:nth-child(2) { animation-delay: 0.2s; }
  .hero-text > *:nth-child(3) { animation-delay: 0.3s; }
  .hero-text > *:nth-child(4) { animation-delay: 0.4s; }
  .hero-stats > * { animation: fadeUp 0.7s ease both; }
  .hero-stats > *:nth-child(1) { animation-delay: 0.3s; }
  .hero-stats > *:nth-child(2) { animation-delay: 0.4s; }
  .hero-stats > *:nth-child(3) { animation-delay: 0.5s; }
  .hero-stats > *:nth-child(4) { animation-delay: 0.6s; }

  /* ── RESPONSIVE ── */
  @media (max-width: 768px) {
    nav { padding: 1rem 1.5rem; }
    .nav-links { display: none; }
    .hero { grid-template-columns: 1fr; padding: 7rem 1.5rem 3rem; gap: 2.5rem; }
    .hero-stats { grid-template-columns: 1fr 1fr; }
    .market-grid { grid-template-columns: 1fr; }
    section { padding: 4rem 1.5rem; }
  }
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <div class="nav-logo">Aditya Vaish</div>
  <ul class="nav-links">
    <li><a href="#projects">Projects</a></li>
    <li><a href="#market">Market</a></li>
    <li><a href="#skills">Skills</a></li>
    <li><a href="#certs">Credentials</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
</nav>

<!-- HERO -->
<section class="hero">
  <div class="hero-text">
    <div class="hero-label">Research · Analytics · Finance</div>
    <h1>Aditya<br><em>Vaish</em></h1>
    <p class="hero-sub">
      PGDM student at IB Institute, Noida — specializing in Business Analytics and Finance.
      I research markets, dissect data, and build tools that turn economic complexity into clear decisions.
    </p>
    <div class="hero-cta">
      <a href="#projects" class="btn btn-primary">View Work</a>
      <a href="https://linkedin.com/in/aditya-vaish-b85b052b4" target="_blank" class="btn btn-outline">LinkedIn ↗</a>
    </div>
  </div>
  <div class="hero-stats">
    <div class="stat-card">
      <div class="stat-num">500+</div>
      <div class="stat-desc">SKUs analysed in Retail Pareto Study</div>
    </div>
    <div class="stat-card dark">
      <div class="stat-num">78%</div>
      <div class="stat-desc">Revenue concentration identified — findings adopted by management</div>
    </div>
    <div class="stat-card">
      <div class="stat-num">3+</div>
      <div class="stat-desc">Sectors tracked via fundamental analysis</div>
    </div>
    <div class="stat-card dark">
      <div class="stat-num">IIM</div>
      <div class="stat-desc">Business Intelligence certified — IIM Bangalore</div>
    </div>
  </div>
</section>

<!-- PROJECTS -->
<section class="projects" id="projects">
  <div class="section-label">// Featured Work</div>
  <h2>Research &amp; Analytics Projects</h2>
  <div class="projects-grid">

    <div class="project-card">
      <span class="project-tag tag-analytics">Retail Analytics</span>
      <div class="project-title">Pareto Analysis — Reliance Smart Bazaar</div>
      <p class="project-desc">Conducted a structured 80/20 analysis on 500+ SKUs across product categories to identify revenue concentration patterns and surface actionable assortment decisions.</p>
      <ul class="project-highlights">
        <li>Identified that ~78% of revenue was driven by a focused SKU cluster</li>
        <li>Recommendations presented to store management and formally adopted</li>
        <li>Tools: Excel, data segmentation, visualisation</li>
        <li>Demonstrates applied economic thinking in a commercial context</li>
      </ul>
    </div>

    <div class="project-card">
      <span class="project-tag tag-research">Academic Research</span>
      <div class="project-title">SLR: AI-Driven Credit Risk Analytics</div>
      <p class="project-desc">Co-authored a Systematic Literature Review submitted to MERC 2026, IIM Kashipur — examining how AI models are reshaping credit risk assessment in financial institutions.</p>
      <ul class="project-highlights">
        <li>Framework: ADO (Antecedent–Decision–Outcome)</li>
        <li>Theoretical anchors: Information Asymmetry Theory + Technology Acceptance Model</li>
        <li>Reviewed peer-reviewed literature across fintech and BFSI sectors</li>
        <li>Submitted to a national management research conference</li>
      </ul>
    </div>

    <div class="project-card">
      <span class="project-tag tag-finance">Finance Analytics</span>
      <div class="project-title">Personal Finance Tracker — Power BI</div>
      <p class="project-desc">Built an end-to-end personal finance dashboard using Power BI — covering income, expense categorisation, KPI reporting, and trend analysis with custom DAX measures.</p>
      <ul class="project-highlights">
        <li>Power Query transformations + correct month-sort logic</li>
        <li>KPI cards: total income, total expenses, savings rate</li>
        <li>Monthly expense trend chart with category drill-down</li>
        <li>Demonstrates self-initiated applied analytics beyond coursework</li>
      </ul>
    </div>

    <div class="project-card">
      <span class="project-tag tag-market">Market Research</span>
      <div class="project-title">Equity Research — Sector-Level Study</div>
      <p class="project-desc">Self-directed equity research across multiple sectors focusing on fundamental analysis — covering growth drivers, competitive dynamics, and macro-economic linkages.</p>
      <ul class="project-highlights">
        <li>Sectors: Power/Energy, FMCG (mid-cap), Conglomerate (Adani Group)</li>
        <li>Analysis: industry trends, company financials, valuation context</li>
        <li>Diversified mutual fund investing alongside direct equity</li>
        <li>Tata Data Visualisation Virtual Experience (Forage)</li>
      </ul>
    </div>

  </div>
</section>

<!-- MARKET -->
<section class="market" id="market">
  <div class="section-label">// Market Experience</div>
  <h2>Investing &amp; Market Research</h2>
  <div class="market-grid">
    <div class="market-text">
      <p>
        I have actively tracked and invested in Indian equities since my undergraduate years —
        a practice that has fundamentally shaped how I think about <strong>economic cycles, sector dynamics,</strong> and <strong>capital allocation.</strong>
      </p>
      <p>
        My approach is grounded in <strong>fundamental analysis</strong>: studying industry trends,
        understanding business models, reading financial results, and identifying what macro signals
        mean for individual companies and sectors.
      </p>
      <p>
        Alongside direct equity, I manage a <strong>diversified mutual fund portfolio</strong>,
        which has reinforced my understanding of risk-adjusted returns, fund categories, and
        long-term wealth creation frameworks.
      </p>
      <p>
        This market experience directly informs my research orientation —
        I approach economics not as an abstraction but as something with real stakes and measurable outcomes.
      </p>
    </div>
    <div class="ticker-list">
      <div class="ticker">
        <div>
          <div class="ticker-name">Adani Group</div>
          <div class="ticker-sector">Conglomerate · Infrastructure · Energy</div>
        </div>
        <div class="ticker-badge">Tracked</div>
      </div>
      <div class="ticker">
        <div>
          <div class="ticker-name">Power Sector Companies</div>
          <div class="ticker-sector">Energy · Utilities · Renewable Transition</div>
        </div>
        <div class="ticker-badge">Tracked</div>
      </div>
      <div class="ticker">
        <div>
          <div class="ticker-name">LT Foods</div>
          <div class="ticker-sector">FMCG · Mid-Cap · Consumer Staples</div>
        </div>
        <div class="ticker-badge">Tracked</div>
      </div>
      <div class="ticker">
        <div>
          <div class="ticker-name">Diversified Mutual Funds</div>
          <div class="ticker-sector">Equity Funds · SIP · Long-Term Allocation</div>
        </div>
        <div class="ticker-badge">Active</div>
      </div>
    </div>
  </div>
</section>

<!-- SKILLS -->
<section id="skills">
  <div class="section-label">// Toolkit</div>
  <h2>Skills &amp; Tools</h2>
  <div class="skills-grid">
    <div class="skill-group">
      <div class="skill-group-title">Data & Analytics</div>
      <div class="skill-pills">
        <span class="pill">Power BI</span>
        <span class="pill">Excel</span>
        <span class="pill">SQL (Fundamentals)</span>
        <span class="pill">Power Query</span>
        <span class="pill">KPI Reporting</span>
        <span class="pill">Pareto Analysis</span>
      </div>
    </div>
    <div class="skill-group">
      <div class="skill-group-title">Finance & Research</div>
      <div class="skill-pills">
        <span class="pill">Fundamental Analysis</span>
        <span class="pill">Equity Research</span>
        <span class="pill">Mutual Funds</span>
        <span class="pill">Financial Modelling</span>
        <span class="pill">Literature Review</span>
        <span class="pill">Credit Risk</span>
      </div>
    </div>
    <div class="skill-group">
      <div class="skill-group-title">Communication</div>
      <div class="skill-pills">
        <span class="pill">Research Writing</span>
        <span class="pill">Data Storytelling</span>
        <span class="pill">Presentations</span>
        <span class="pill">ADO Framework</span>
      </div>
    </div>
    <div class="skill-group">
      <div class="skill-group-title">Programming (Learning)</div>
      <div class="skill-pills">
        <span class="pill">Python (Fundamentals)</span>
        <span class="pill">GitHub</span>
        <span class="pill">AI / ML Basics</span>
      </div>
    </div>
  </div>
</section>

<!-- CERTS -->
<section class="certs" id="certs">
  <div class="section-label">// Credentials</div>
  <h2>Certifications &amp; Programmes</h2>
  <div class="certs-list">
    <div class="cert-item">
      <div class="cert-icon">🏛️</div>
      <div>
        <div class="cert-name">Business Intelligence Programme</div>
        <div class="cert-org">IIM Bangalore</div>
      </div>
    </div>
    <div class="cert-item">
      <div class="cert-icon">💻</div>
      <div>
        <div class="cert-name">AI Technical Foundations</div>
        <div class="cert-org">Qualcomm</div>
      </div>
    </div>
    <div class="cert-item">
      <div class="cert-icon">📊</div>
      <div>
        <div class="cert-name">Data Visualisation Virtual Experience</div>
        <div class="cert-org">Tata Group / Forage</div>
      </div>
    </div>
    <div class="cert-item">
      <div class="cert-icon">🚀</div>
      <div>
        <div class="cert-name">Entrepreneurship Training</div>
        <div class="cert-org">Skill India / NSDC</div>
      </div>
    </div>
    <div class="cert-item">
      <div class="cert-icon">📚</div>
      <div>
        <div class="cert-name">PGDM — Business Analytics & Finance</div>
        <div class="cert-org">IB Institute, Noida (2025–2027)</div>
      </div>
    </div>
    <div class="cert-item">
      <div class="cert-icon">📝</div>
      <div>
        <div class="cert-name">Paper Submission — MERC 2026</div>
        <div class="cert-org">IIM Kashipur · AI Credit Risk SLR</div>
      </div>
    </div>
  </div>
</section>

<!-- CONTACT -->
<section class="contact" id="contact">
  <div class="section-label">// Get In Touch</div>
  <h2>Let's Connect</h2>
  <p>Open to research internships, analytics roles, and collaborative projects in Finance &amp; Economics.</p>
  <div class="contact-links">
    <a class="contact-link" href="https://linkedin.com/in/aditya-vaish-b85b052b4" target="_blank">
      🔗 LinkedIn
    </a>
    <a class="contact-link" href="https://github.com/adityavaish06-star" target="_blank">
      🐱 GitHub
    </a>
    <a class="contact-link" href="mailto:adityavaish06@gmail.com">
      ✉️ Email
    </a>
  </div>
</section>

<footer>
  ADITYA VAISH &nbsp;·&nbsp; RESEARCH & ANALYTICS &nbsp;·&nbsp; DELHI NCR
</footer>

</body>
</html>
