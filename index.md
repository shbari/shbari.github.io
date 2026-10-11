---
title: "Sheikh Hefzul Bari"
---

<style>
  /* ── LIGHT THEME VARIABLES (PRIMARY DEFAULT) ── */
  :root {
    --bg-color: #ffffff;
    --text-color: #24292e;
    --heading-color: #1f2328;
    --subtext-color: #57606a;
    --link-color: #0366d6;
    --border-color: #e1e4e8;
    --card-bg: #ffffff;
    --card-shadow: 0 4px 12px rgba(0, 0, 0, 0.03);
    --card-hover-border: #0366d6;
    --card-hover-shadow: 0 12px 24px rgba(3, 102, 214, 0.12);
    --footer-text: #666666;
  }

  /* ── AUTO DARK MODE SUPPORT ── */
  @media (prefers-color-scheme: dark) {
    :root {
      --bg-color: #0d1117;
      --text-color: #c9d1d9;
      --heading-color: #f0f6fc;
      --subtext-color: #8b949e;
      --link-color: #58a6ff;
      --border-color: #30363d;
      --card-bg: #161b22;
      --card-shadow: 0 4px 12px rgba(0, 0, 0, 0.3);
      --card-hover-border: #58a6ff;
      --card-hover-shadow: 0 12px 24px rgba(88, 166, 255, 0.2);
      --footer-text: #8b949e;
    }
  }

  /* Base Styles */
  body {
    background-color: var(--bg-color);
    color: var(--text-color);
    transition: background-color 0.3s ease, color 0.3s ease;
  }

  /* ── NAVIGATION BAR ── */
  .navbar { 
    display: flex; 
    align-items: center; 
    justify-content: flex-end; 
    gap: 20px; 
    padding: 10px 0; 
    font-size: 1.0em; 
    flex-wrap: wrap; 
    margin-bottom: 25px; 
  }
  .navbar a { 
    text-decoration: none; 
    color: var(--link-color); 
    font-weight: 600; 
  }
  .navbar a:hover { text-decoration: underline; }
  .nav-toggle, .nav-toggle-label { display: none; }
  .navbar-links { display: flex; gap: 20px; }
  
  /* Mobile Navigation */
  @media (max-width: 768px) {
    .navbar { justify-content: space-between; }
    .nav-toggle-label { 
      display: block; 
      cursor: pointer; 
      padding: 6px 10px; 
      border: 1px solid var(--border-color); 
      border-radius: 4px; 
      margin-left: auto; 
      user-select: none; 
      color: var(--text-color);
    }
    .navbar-links { display: none; flex-direction: column; width: 100%; margin-top: 8px; }
    .nav-toggle:checked + .nav-toggle-label + .navbar-links { display: flex; }
  }

  /* ── INTERACTIVE FLASHCARD GRID (Balanced 2-Card Layout) ── */
  .card-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    gap: 1.5rem;
    width: 100%;
    margin: 2.5rem 0;
  }

  .flashcard {
    background: var(--card-bg);
    border: 1px solid var(--border-color);
    border-radius: 10px;
    padding: 1.5rem;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    min-height: 170px;
    text-decoration: none !important;
    color: var(--text-color) !important;
    box-shadow: var(--card-shadow);
    transition: transform 0.3s cubic-bezier(0.25, 1, 0.5, 1), 
                box-shadow 0.3s cubic-bezier(0.25, 1, 0.5, 1), 
                border-color 0.3s ease,
                background-color 0.3s ease;
    animation: card-float 6s ease-in-out infinite;
    scroll-margin-top: 80px;
  }

  /* Staggered Floating Delays */
  .flashcard:nth-child(1) { animation-delay: 0s; }
  .flashcard:nth-child(2) { animation-delay: 1.5s; }

  .flashcard:hover {
    transform: translateY(-8px) scale(1.01);
    border-color: var(--card-hover-border);
    box-shadow: var(--card-hover-shadow);
    animation-play-state: paused;
  }

  .card-tag {
    align-self: flex-start;
    font-size: 0.7rem;
    font-weight: 700;
    text-transform: uppercase;
    letter-spacing: 0.05em;
    padding: 0.2rem 0.5rem;
    border-radius: 4px;
    margin-bottom: 0.8rem;
  }

  /* Distinct Tags */
  .tag-research { background-color: rgba(3, 102, 214, 0.15); color: #0366d6; }
  .tag-news { background-color: rgba(40, 167, 69, 0.15); color: #28a745; }

  @media (prefers-color-scheme: dark) {
    .tag-research { color: #58a6ff; }
    .tag-news { color: #56d364; }
  }

  .flashcard h3 {
    font-size: 1.25rem;
    font-weight: 700;
    margin: 0 0 0.4rem 0 !important;
    color: var(--heading-color);
    border-bottom: none !important;
  }

  .flashcard p {
    font-size: 0.875rem;
    color: var(--subtext-color);
    line-height: 1.45;
    margin: 0;
  }

  @keyframes card-float {
    0%, 100% { transform: translateY(0px); }
    50% { transform: translateY(-5px); }
  }

  /* Clean Theme Overrides */
  h1, h2, h3 { color: var(--heading-color); border-bottom: none !important; }
  h2 { scroll-margin-top: 80px; }
  hr { display: none !important; }
</style>

<!-- Top Navigation Bar -->
<div class="navbar">
  <input type="checkbox" id="nav-toggle" class="nav-toggle">
  <label for="nav-toggle" class="nav-toggle-label">☰ Menu</label>
  <div class="navbar-links">
    <a href="#about">About</a>
    <a href="Research">Research</a>
    <a href="News">News</a>
    <a href="publications">Publications</a>
    <a href="talks">Talks</a>
    <a href="cv">CV</a>
  </div>
</div>

<!-- Header / Profile Section -->
<div style="text-align: center;">
  <img src="images/profile.jpeg" alt="Sheikh Hefzul Bari" width="160" style="border-radius: 50%; margin-bottom: 10px;">
  
  <h1 style="font-weight: 700; margin-top: -10px;">Sheikh Hefzul Bari</h1>
  
  <p>
    <strong>Specially Appointed Assistant Professor (Research)</strong>, Tohoku University, Japan<br>
    <em>Suspended sediment dynamics &bull; Climate change &bull; Compound flooding &bull; River continuum</em>
  </p>

  <!-- Social & Credentials Badges -->
  <a href="https://orcid.org/0000-0003-2635-2146" target="_blank"><img src="https://img.shields.io/badge/ORCID-A6CE39?style=flat&logo=orcid&logoColor=white" alt="ORCID"></a>
  <a href="https://www.researchgate.net/profile/Sheikh-Hefzul-Bari" target="_blank"><img src="https://img.shields.io/badge/ResearchGate-00CCBB?style=flat&logo=researchgate&logoColor=white" alt="ResearchGate"></a>
  <a href="https://scholar.google.com/citations?user=6c-lCXEAAAAJ&hl=en" target="_blank"><img src="https://img.shields.io/badge/Google_Scholar-4285F4?style=flat&logo=googlescholar&logoColor=white" alt="Google Scholar"></a>
  <a href="https://www.linkedin.com/in/shbari" target="_blank"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=flat&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
  <a href="mailto:bari.sheikh.hefzul.d5@tohoku.ac.jp"><img src="https://img.shields.io/badge/Get_in_touch-EA4335?style=flat&logo=gmail&logoColor=white" alt="Get in touch"></a>
  <a href="cv"><img src="https://img.shields.io/badge/CV-6D28D9?style=flat&logo=document&logoColor=white" alt="Curriculum Vitae"></a>
</div>

---

<!-- About Section -->
<h2 id="about">About</h2>

<div style="text-align: justify;">
I study hydrology and fluvial&ndash;coastal systems in a changing climate, focusing on how hydrological and geomorphological processes shape suspended sediment dynamics from mountain headwaters to river mouths. My research also explores extreme events, with the aim of developing data-driven hazard assessment tools and resilience-oriented adaptation strategies. To achieve this, I use observational and large-ensemble climate simulation data. I am currently working as a <strong>Specially Appointed Assistant Professor at Tohoku University</strong>.
</div>

---

<!-- Directory / Interactive Flashcards Grid (2 Cards) -->
<main class="card-grid">
  <!-- Research Card -->
  <a href="Research" class="flashcard">
    <div>
      <div class="card-tag tag-research">Focus Areas</div>
      <h3>Research</h3>
    </div>
    <p>Hydro-sediment analysis, sediment dynamics, and compound flooding under changing climate.</p>
  </a>

  <!-- News Card -->
  <a href="News" class="flashcard">
    <div>
      <div class="card-tag tag-news">Latest Update</div>
      <h3>News</h3>
    </div>
    <p>
      <span style="
        background-color: #d97706; 
        color: #ffffff; 
        font-size: 0.65rem; 
        font-weight: 700; 
        padding: 2px 6px; 
        border-radius: 3px; 
        text-transform: uppercase; 
        margin-right: 4px;
        vertical-align: middle;
      ">🏆 Honored</span><br>
      Received the <strong>Japan Society of Hydrology and Water Resources (JSHWR) Award</strong>.
    </p>
  </a>
</main>

---

<!-- Footer -->
<div style="text-align: center; margin-top: 40px; font-size: 0.9em; color: var(--footer-text);">
  <p style="margin-bottom: 6px;">
    &copy; 2026 Sheikh Hefzul Bari | Licensed under
    <a href="https://creativecommons.org/licenses/by/4.0/" target="_blank" style="color: var(--link-color);">CC BY 4.0</a>
  </p>
  <p style="margin: 0;">
    <small>Last updated: 29 June 2026</small>
  </p>
</div>
