<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Build Your Remote PMO | Greater Ambitions LLC</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,700;0,900;1,700&family=DM+Sans:wght@300;400;500&family=DM+Mono:wght@400;500&display=swap" rel="stylesheet">
<style>
  :root {
    --burgundy: #52211A;
    --burgundy-light: #7a342a;
    --gold: #A87605;
    --gold-light: #c99b2a;
    --cream: #F5EFE6;
    --warm-white: #FAF7F3;
    --charcoal: #1C1C1C;
    --mid: #4A4035;
    --muted: #8a7c6e;
    --border: #e0d6c8;
  }

  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  html { scroll-behavior: smooth; }

  body {
    font-family: 'DM Sans', sans-serif;
    background: var(--warm-white);
    color: var(--charcoal);
    line-height: 1.7;
    overflow-x: hidden;
  }

  /* ── COVER ── */
  .cover {
    min-height: 100vh;
    background: var(--charcoal);
    display: grid;
    grid-template-rows: auto 1fr auto;
    position: relative;
    overflow: hidden;
  }

  .cover::before {
    content: '';
    position: absolute;
    inset: 0;
    background:
      radial-gradient(ellipse 60% 50% at 80% 20%, rgba(168,118,5,0.12) 0%, transparent 60%),
      radial-gradient(ellipse 40% 60% at 10% 80%, rgba(82,33,26,0.35) 0%, transparent 55%);
    pointer-events: none;
  }

  .cover-grid {
    position: absolute;
    inset: 0;
    background-image:
      linear-gradient(rgba(168,118,5,0.06) 1px, transparent 1px),
      linear-gradient(90deg, rgba(168,118,5,0.06) 1px, transparent 1px);
    background-size: 60px 60px;
    pointer-events: none;
  }

  .cover-header {
    padding: 40px 60px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    position: relative;
    z-index: 2;
  }

  .logo-block {
    display: flex;
    flex-direction: column;
  }

  .logo-name {
    font-family: 'Playfair Display', serif;
    font-size: 1.1rem;
    color: var(--gold);
    letter-spacing: 0.03em;
  }

  .logo-sub {
    font-family: 'DM Mono', monospace;
    font-size: 0.58rem;
    color: var(--muted);
    letter-spacing: 0.18em;
    text-transform: uppercase;
    margin-top: 2px;
  }

  .cover-badge {
    font-family: 'DM Mono', monospace;
    font-size: 0.62rem;
    color: var(--gold);
    border: 1px solid rgba(168,118,5,0.4);
    padding: 6px 14px;
    letter-spacing: 0.14em;
    text-transform: uppercase;
  }

  .cover-body {
    display: flex;
    flex-direction: column;
    justify-content: center;
    padding: 60px 60px 40px;
    position: relative;
    z-index: 2;
    max-width: 900px;
  }

  .cover-eyebrow {
    font-family: 'DM Mono', monospace;
    font-size: 0.68rem;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    color: var(--gold);
    margin-bottom: 28px;
    display: flex;
    align-items: center;
    gap: 14px;
  }

  .cover-eyebrow::before {
    content: '';
    display: block;
    width: 40px;
    height: 1px;
    background: var(--gold);
  }

  .cover-title {
    font-family: 'Playfair Display', serif;
    font-size: clamp(3rem, 7vw, 6.5rem);
    font-weight: 900;
    line-height: 1.0;
    color: var(--cream);
    margin-bottom: 30px;
  }

  .cover-title em {
    font-style: italic;
    color: var(--gold);
  }

  .cover-subtitle {
    font-size: 1.15rem;
    color: rgba(245,239,230,0.65);
    font-weight: 300;
    max-width: 560px;
    line-height: 1.75;
    margin-bottom: 48px;
  }

  .cover-cta-row {
    display: flex;
    gap: 20px;
    align-items: center;
    flex-wrap: wrap;
  }

  .btn-primary {
    background: var(--gold);
    color: var(--charcoal);
    font-family: 'DM Mono', monospace;
    font-size: 0.72rem;
    font-weight: 500;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    padding: 16px 32px;
    border: none;
    cursor: pointer;
    text-decoration: none;
    display: inline-block;
    transition: background 0.2s, transform 0.15s;
  }

  .btn-primary:hover { background: var(--gold-light); transform: translateY(-1px); }

  .btn-ghost {
    color: var(--cream);
    font-family: 'DM Mono', monospace;
    font-size: 0.68rem;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    text-decoration: none;
    opacity: 0.6;
    display: flex;
    align-items: center;
    gap: 8px;
    transition: opacity 0.2s;
  }

  .btn-ghost:hover { opacity: 1; }

  .cover-footer {
    padding: 30px 60px;
    position: relative;
    z-index: 2;
    display: flex;
    justify-content: space-between;
    align-items: flex-end;
    border-top: 1px solid rgba(168,118,5,0.15);
  }

  .cover-stat-row {
    display: flex;
    gap: 48px;
  }

  .cover-stat-num {
    font-family: 'Playfair Display', serif;
    font-size: 1.8rem;
    font-weight: 700;
    color: var(--gold);
    display: block;
  }

  .cover-stat-label {
    font-family: 'DM Mono', monospace;
    font-size: 0.58rem;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    color: var(--muted);
  }

  .cover-author {
    font-size: 0.78rem;
    color: rgba(245,239,230,0.4);
    text-align: right;
    line-height: 1.5;
  }

  .cover-author strong { color: rgba(245,239,230,0.75); display: block; }

  /* ── MAIN CONTENT ── */
  .page { max-width: 1100px; margin: 0 auto; padding: 0 40px; }

  /* ── INTRO STRIP ── */
  .intro-strip {
    background: var(--burgundy);
    color: var(--cream);
    padding: 72px 0;
  }

  .intro-strip .page {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 80px;
    align-items: center;
  }

  .intro-tag {
    font-family: 'DM Mono', monospace;
    font-size: 0.62rem;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    color: var(--gold);
    margin-bottom: 20px;
  }

  .intro-heading {
    font-family: 'Playfair Display', serif;
    font-size: 2.4rem;
    font-weight: 700;
    line-height: 1.2;
    margin-bottom: 20px;
  }

  .intro-body {
    font-size: 0.95rem;
    color: rgba(245,239,230,0.75);
    font-weight: 300;
    line-height: 1.85;
  }

  .stat-cards {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 16px;
  }

  .stat-card {
    background: rgba(245,239,230,0.07);
    border: 1px solid rgba(168,118,5,0.25);
    padding: 24px 20px;
  }

  .stat-card-num {
    font-family: 'Playfair Display', serif;
    font-size: 2.2rem;
    font-weight: 700;
    color: var(--gold);
    line-height: 1;
  }

  .stat-card-label {
    font-size: 0.8rem;
    color: rgba(245,239,230,0.55);
    margin-top: 8px;
    font-weight: 300;
  }

  /* ── SECTION STYLES ── */
  .section {
    padding: 88px 0;
  }

  .section-alt { background: var(--cream); }

  .section-dark {
    background: var(--charcoal);
    color: var(--cream);
  }

  .section-label {
    font-family: 'DM Mono', monospace;
    font-size: 0.62rem;
    letter-spacing: 0.22em;
    text-transform: uppercase;
    color: var(--gold);
    margin-bottom: 14px;
    display: flex;
    align-items: center;
    gap: 12px;
  }

  .section-label::before {
    content: '';
    display: block;
    width: 28px;
    height: 1px;
    background: var(--gold);
  }

  .section-title {
    font-family: 'Playfair Display', serif;
    font-size: clamp(1.8rem, 3.5vw, 2.8rem);
    font-weight: 700;
    line-height: 1.2;
    margin-bottom: 20px;
    color: var(--charcoal);
  }

  .section-dark .section-title { color: var(--cream); }

  .section-desc {
    font-size: 1rem;
    color: var(--mid);
    max-width: 620px;
    font-weight: 300;
    line-height: 1.8;
    margin-bottom: 56px;
  }

  .section-dark .section-desc { color: rgba(245,239,230,0.6); }

  /* ── WHY IT MATTERS ── */
  .pillars-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 2px;
    background: var(--border);
  }

  .pillar {
    background: var(--warm-white);
    padding: 40px 32px;
    position: relative;
    overflow: hidden;
    transition: background 0.2s;
  }

  .section-alt .pillar { background: var(--cream); }

  .pillar::after {
    content: '';
    position: absolute;
    bottom: 0;
    left: 0;
    width: 100%;
    height: 3px;
    background: var(--gold);
    transform: scaleX(0);
    transform-origin: left;
    transition: transform 0.3s;
  }

  .pillar:hover::after { transform: scaleX(1); }

  .pillar-num {
    font-family: 'DM Mono', monospace;
    font-size: 0.65rem;
    color: var(--gold);
    letter-spacing: 0.15em;
    margin-bottom: 20px;
    display: block;
  }

  .pillar-icon {
    font-size: 1.6rem;
    margin-bottom: 16px;
    display: block;
  }

  .pillar-title {
    font-family: 'Playfair Display', serif;
    font-size: 1.15rem;
    font-weight: 700;
    margin-bottom: 12px;
    color: var(--charcoal);
  }

  .pillar-body {
    font-size: 0.88rem;
    color: var(--mid);
    font-weight: 300;
    line-height: 1.75;
  }

  /* ── ROLES ── */
  .roles-list {
    display: flex;
    flex-direction: column;
    gap: 2px;
  }

  .role-card {
    background: var(--warm-white);
    border-left: 4px solid transparent;
    padding: 0;
    overflow: hidden;
    transition: border-color 0.25s;
  }

  .role-card:hover { border-left-color: var(--gold); }

  .role-header {
    display: grid;
    grid-template-columns: 56px 1fr auto;
    align-items: center;
    gap: 24px;
    padding: 28px 32px;
    cursor: pointer;
  }

  .role-num {
    font-family: 'DM Mono', monospace;
    font-size: 1.4rem;
    font-weight: 500;
    color: var(--gold);
    opacity: 0.5;
  }

  .role-name {
    font-family: 'Playfair Display', serif;
    font-size: 1.2rem;
    font-weight: 700;
    color: var(--charcoal);
  }

  .role-level {
    font-family: 'DM Mono', monospace;
    font-size: 0.6rem;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    color: var(--muted);
    background: var(--cream);
    padding: 5px 12px;
    white-space: nowrap;
  }

  .role-body {
    padding: 0 32px 28px 112px;
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 24px;
  }

  .role-section-label {
    font-family: 'DM Mono', monospace;
    font-size: 0.6rem;
    letter-spacing: 0.18em;
    text-transform: uppercase;
    color: var(--gold);
    margin-bottom: 10px;
  }

  .role-list {
    list-style: none;
    display: flex;
    flex-direction: column;
    gap: 6px;
  }

  .role-list li {
    font-size: 0.84rem;
    color: var(--mid);
    font-weight: 300;
    padding-left: 16px;
    position: relative;
    line-height: 1.55;
  }

  .role-list li::before {
    content: '—';
    position: absolute;
    left: 0;
    color: var(--gold);
    font-size: 0.7rem;
  }

  /* ── GOVERNANCE FRAMEWORK ── */
  .framework-grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 24px;
  }

  .fw-card {
    border: 1px solid var(--border);
    padding: 36px 32px;
    position: relative;
    background: var(--warm-white);
  }

  .fw-card-accent {
    position: absolute;
    top: 0;
    left: 0;
    width: 40px;
    height: 3px;
    background: var(--gold);
  }

  .fw-card-title {
    font-family: 'Playfair Display', serif;
    font-size: 1.1rem;
    font-weight: 700;
    margin-bottom: 16px;
    color: var(--charcoal);
    margin-top: 12px;
  }

  .fw-card-body {
    font-size: 0.86rem;
    color: var(--mid);
    font-weight: 300;
    line-height: 1.75;
  }

  .fw-tag-row {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
    margin-top: 16px;
  }

  .fw-tag {
    font-family: 'DM Mono', monospace;
    font-size: 0.6rem;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    color: var(--burgundy);
    background: rgba(82,33,26,0.08);
    padding: 4px 10px;
  }

  /* ── TECH STACK ── */
  .tech-cols {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 2px;
    background: rgba(168,118,5,0.15);
  }

  .tech-col {
    background: var(--charcoal);
    padding: 32px 24px;
  }

  .tech-col-label {
    font-family: 'DM Mono', monospace;
    font-size: 0.6rem;
    letter-spacing: 0.18em;
    text-transform: uppercase;
    color: var(--gold);
    margin-bottom: 20px;
    padding-bottom: 12px;
    border-bottom: 1px solid rgba(168,118,5,0.2);
  }

  .tech-list {
    list-style: none;
    display: flex;
    flex-direction: column;
    gap: 10px;
  }

  .tech-list li {
    font-size: 0.84rem;
    color: rgba(245,239,230,0.7);
    font-weight: 300;
    display: flex;
    align-items: baseline;
    gap: 8px;
  }

  .tech-list li::before {
    content: '▸';
    color: var(--gold);
    font-size: 0.65rem;
    flex-shrink: 0;
  }

  /* ── IMPLEMENTATION ROADMAP ── */
  .roadmap {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 0;
    position: relative;
  }

  .roadmap::before {
    content: '';
    position: absolute;
    top: 36px;
    left: 10%;
    width: 80%;
    height: 2px;
    background: linear-gradient(90deg, var(--gold), rgba(168,118,5,0.3));
    z-index: 0;
  }

  .roadmap-phase {
    padding: 0 20px;
    position: relative;
    z-index: 1;
  }

  .phase-dot {
    width: 72px;
    height: 72px;
    background: var(--charcoal);
    border: 2px solid var(--gold);
    display: flex;
    align-items: center;
    justify-content: center;
    margin-bottom: 24px;
    position: relative;
  }

  .section-alt .phase-dot { background: var(--cream); }

  .phase-dot-inner {
    font-family: 'DM Mono', monospace;
    font-size: 0.7rem;
    color: var(--gold);
    text-align: center;
    font-weight: 500;
  }

  .phase-timeline {
    font-family: 'DM Mono', monospace;
    font-size: 0.6rem;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    color: var(--gold);
    margin-bottom: 10px;
  }

  .phase-title {
    font-family: 'Playfair Display', serif;
    font-size: 1.05rem;
    font-weight: 700;
    margin-bottom: 14px;
    color: var(--charcoal);
  }

  .phase-list {
    list-style: none;
    display: flex;
    flex-direction: column;
    gap: 7px;
  }

  .phase-list li {
    font-size: 0.82rem;
    color: var(--mid);
    font-weight: 300;
    padding-left: 14px;
    position: relative;
    line-height: 1.5;
  }

  .phase-list li::before {
    content: '·';
    position: absolute;
    left: 0;
    color: var(--gold);
    font-size: 1rem;
    line-height: 1.2;
  }

  /* ── CERTIFICATIONS ── */
  .cert-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 16px;
  }

  .cert-card {
    background: rgba(245,239,230,0.05);
    border: 1px solid rgba(168,118,5,0.2);
    padding: 28px 24px;
  }

  .cert-badge {
    font-family: 'DM Mono', monospace;
    font-size: 1.1rem;
    font-weight: 500;
    color: var(--gold);
    margin-bottom: 10px;
    display: block;
  }

  .cert-name {
    font-size: 0.88rem;
    font-weight: 500;
    color: var(--cream);
    margin-bottom: 8px;
  }

  .cert-body {
    font-size: 0.78rem;
    color: rgba(245,239,230,0.5);
    font-weight: 300;
    line-height: 1.65;
  }

  /* ── COMMON MISTAKES ── */
  .mistakes-grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 16px;
  }

  .mistake-card {
    border: 1px solid var(--border);
    padding: 28px 28px 28px 56px;
    position: relative;
  }

  .mistake-x {
    position: absolute;
    left: 20px;
    top: 26px;
    width: 22px;
    height: 22px;
    background: rgba(82,33,26,0.12);
    color: var(--burgundy);
    font-size: 0.75rem;
    font-weight: 700;
    display: flex;
    align-items: center;
    justify-content: center;
  }

  .mistake-title {
    font-family: 'Playfair Display', serif;
    font-size: 0.95rem;
    font-weight: 700;
    color: var(--charcoal);
    margin-bottom: 8px;
  }

  .mistake-body {
    font-size: 0.83rem;
    color: var(--mid);
    font-weight: 300;
    line-height: 1.7;
  }

  /* ── CTA SECTION ── */
  .cta-section {
    background: var(--burgundy);
    padding: 100px 0;
    text-align: center;
    position: relative;
    overflow: hidden;
  }

  .cta-section::before {
    content: '';
    position: absolute;
    inset: 0;
    background:
      radial-gradient(ellipse 70% 70% at 50% -10%, rgba(168,118,5,0.18) 0%, transparent 60%);
    pointer-events: none;
  }

  .cta-eyebrow {
    font-family: 'DM Mono', monospace;
    font-size: 0.65rem;
    letter-spacing: 0.22em;
    text-transform: uppercase;
    color: var(--gold);
    margin-bottom: 24px;
  }

  .cta-title {
    font-family: 'Playfair Display', serif;
    font-size: clamp(2rem, 4vw, 3.2rem);
    font-weight: 700;
    color: var(--cream);
    line-height: 1.2;
    max-width: 680px;
    margin: 0 auto 20px;
  }

  .cta-title em { font-style: italic; color: var(--gold); }

  .cta-sub {
    font-size: 0.95rem;
    color: rgba(245,239,230,0.6);
    max-width: 480px;
    margin: 0 auto 40px;
    font-weight: 300;
    line-height: 1.8;
  }

  .cta-btn {
    display: inline-block;
    background: var(--gold);
    color: var(--charcoal);
    font-family: 'DM Mono', monospace;
    font-size: 0.7rem;
    font-weight: 500;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    padding: 18px 44px;
    text-decoration: none;
    transition: background 0.2s, transform 0.15s;
  }

  .cta-btn:hover { background: var(--gold-light); transform: translateY(-2px); }

  .cta-secondary {
    display: block;
    margin-top: 20px;
    font-size: 0.78rem;
    color: rgba(245,239,230,0.35);
    font-weight: 300;
  }

  /* ── FOOTER ── */
  .footer {
    background: var(--charcoal);
    padding: 48px 0;
    border-top: 1px solid rgba(168,118,5,0.15);
  }

  .footer .page {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  .footer-brand {
    font-family: 'Playfair Display', serif;
    font-size: 1rem;
    color: var(--gold);
  }

  .footer-brand span {
    font-family: 'DM Mono', monospace;
    font-size: 0.58rem;
    letter-spacing: 0.16em;
    text-transform: uppercase;
    color: var(--muted);
    display: block;
    margin-top: 4px;
  }

  .footer-copy {
    font-family: 'DM Mono', monospace;
    font-size: 0.6rem;
    color: var(--muted);
    letter-spacing: 0.08em;
    text-align: right;
    line-height: 1.8;
  }

  /* ── DIVIDER ── */
  .gold-divider {
    width: 48px;
    height: 3px;
    background: var(--gold);
    margin-bottom: 40px;
  }

  /* ── PRINT / download ── */
  @media print {
    .cover { min-height: auto; }
    .btn-primary, .btn-ghost, .cta-btn { display: none; }
  }

  @media (max-width: 900px) {
    .cover-header, .cover-body, .cover-footer { padding-left: 28px; padding-right: 28px; }
    .cover-stat-row { gap: 24px; }
    .intro-strip .page { grid-template-columns: 1fr; gap: 40px; }
    .pillars-grid { grid-template-columns: 1fr; }
    .roles-grid { grid-template-columns: 1fr; }
    .tech-cols { grid-template-columns: 1fr 1fr; }
    .roadmap { grid-template-columns: 1fr 1fr; }
    .roadmap::before { display: none; }
    .cert-grid { grid-template-columns: 1fr 1fr; }
    .mistakes-grid { grid-template-columns: 1fr; }
    .framework-grid { grid-template-columns: 1fr; }
    .page { padding: 0 24px; }
    .role-body { grid-template-columns: 1fr; padding-left: 56px; }
    .footer .page { flex-direction: column; gap: 20px; text-align: center; }
    .footer-copy { text-align: center; }
  }
</style>
</head>
<body>

<!-- ══════════ COVER ══════════ -->
<section class="cover">
  <div class="cover-grid"></div>
  <header class="cover-header">
    <div class="logo-block">
      <span class="logo-name">Greater Ambitions LLC</span>
      <span class="logo-sub">PM + Operations Consultancy</span>
    </div>
    <span class="cover-badge">Free Digital Guide</span>
  </header>

  <div class="cover-body">
    <div class="cover-eyebrow">Execution Architecture Series</div>
    <h1 class="cover-title">Build Your<br><em>Remote PMO</em><br>From the Ground Up</h1>
    <p class="cover-subtitle">A practitioner's field guide to designing, staffing, and operationalizing a high-performing Project Management Office — built for the modern distributed enterprise.</p>
    <div class="cover-cta-row">
      <a href="#start" class="btn-primary">Read the Guide ↓</a>
      <a href="#cta" class="btn-ghost">Book a Strategy Call →</a>
    </div>
  </div>

  <footer class="cover-footer">
    <div class="cover-stat-row">
      <div>
        <span class="cover-stat-num">$500M+</span>
        <span class="cover-stat-label">Program Value Led</span>
      </div>
      <div>
        <span class="cover-stat-num">20+</span>
        <span class="cover-stat-label">Years of Execution</span>
      </div>
      <div>
        <span class="cover-stat-num">100%</span>
        <span class="cover-stat-label">Practitioner-Built</span>
      </div>
    </div>
    <div class="cover-author">
      <strong>Dr. Minina Johnson, DBA, PMP, CSM</strong>
      Founder & Principal Strategist
    </div>
  </footer>
</section>

<!-- ══════════ WHY REMOTE PMO MATTERS ══════════ -->
<section class="intro-strip" id="start">
  <div class="page">
    <div>
      <div class="intro-tag">The Case for Remote PMOs</div>
      <h2 class="intro-heading">Why This Matters Now More Than Ever</h2>
      <p class="intro-body">Companies scaling from 50 to 500 employees accumulate execution debt faster than they can clear it. A remote PMO isn't a luxury — it's the control tower that separates organizations that scale strategically from those that firefight constantly.<br><br>Without one, strategy documents gather dust while teams operate in silos, deadlines shift silently, and leadership loses visibility. With one, your distributed workforce executes with the same rigor and accountability as a co-located team.</p>
    </div>
    <div class="stat-cards">
      <div class="stat-card">
        <span class="stat-card-num">77%</span>
        <p class="stat-card-label">of high-performing projects use a formal PMO structure</p>
      </div>
      <div class="stat-card">
        <span class="stat-card-num">38%</span>
        <p class="stat-card-label">more projects delivered on time with PMO governance in place</p>
      </div>
      <div class="stat-card">
        <span class="stat-card-num">$97M</span>
        <p class="stat-card-label">wasted per $1B spent due to poor project performance (PMI)</p>
      </div>
      <div class="stat-card">
        <span class="stat-card-num">3×</span>
        <p class="stat-card-label">faster strategic alignment with centralized PMO oversight</p>
      </div>
    </div>
  </div>
</section>

<!-- ══════════ SECTION 1: IMPORTANCE ══════════ -->
<section class="section">
  <div class="page">
    <div class="section-label">Section 01</div>
    <h2 class="section-title">Why a Remote PMO Is a Strategic Imperative</h2>
    <p class="section-desc">A well-structured remote PMO is the execution engine of your organization — providing visibility, standardization, and strategic alignment across every distributed team.</p>
    <div class="pillars-grid">
      <div class="pillar">
        <span class="pillar-num">01 —</span>
        <span class="pillar-icon">🏗️</span>
        <div class="pillar-title">Execution Infrastructure</div>
        <p class="pillar-body">Creates the frameworks, tools, and standards that allow distributed teams to operate with consistency. Eliminates the chaos of "every PM doing it differently."</p>
      </div>
      <div class="pillar">
        <span class="pillar-num">02 —</span>
        <span class="pillar-icon">🎯</span>
        <div class="pillar-title">Strategic Alignment</div>
        <p class="pillar-body">Bridges the gap between boardroom strategy and day-to-day execution. Every project is tied to a business objective — no orphan work, no wasted resources.</p>
      </div>
      <div class="pillar">
        <span class="pillar-num">03 —</span>
        <span class="pillar-icon">📊</span>
        <div class="pillar-title">Portfolio Visibility</div>
        <p class="pillar-body">Gives leadership a real-time view of project health, risk exposure, and capacity — without needing to chase status updates across Slack channels.</p>
      </div>
      <div class="pillar">
        <span class="pillar-num">04 —</span>
        <span class="pillar-icon">⚡</span>
        <div class="pillar-title">Velocity at Scale</div>
        <p class="pillar-body">Enables the organization to take on more strategic work by eliminating duplicate effort, resolving blockers proactively, and optimizing resource allocation.</p>
      </div>
      <div class="pillar">
        <span class="pillar-num">05 —</span>
        <span class="pillar-icon">🔒</span>
        <div class="pillar-title">Risk & Governance</div>
        <p class="pillar-body">Establishes the guardrails — escalation paths, change control protocols, and compliance checkpoints — that prevent costly surprises and scope chaos.</p>
      </div>
      <div class="pillar">
        <span class="pillar-num">06 —</span>
        <span class="pillar-icon">🧠</span>
        <div class="pillar-title">Institutional Knowledge</div>
        <p class="pillar-body">Captures lessons learned, process improvements, and team intelligence in a central hub — so the organization doesn't restart from zero with every new project.</p>
      </div>
    </div>
  </div>
</section>

<!-- ══════════ SECTION 2: KEY ROLES ══════════ -->
<section class="section section-alt">
  <div class="page">
    <div class="section-label">Section 02</div>
    <h2 class="section-title">The Core Remote PMO Team:<br>Roles & Responsibilities</h2>
    <p class="section-desc">Every role in your remote PMO serves a distinct function. Build for the work you have today — then scale as complexity demands.</p>

    <div class="roles-list">

      <div class="role-card">
        <div class="role-header">
          <span class="role-num">01</span>
          <div>
            <div class="role-name">PMO Director / VP of PMO</div>
            <div style="font-size:0.8rem;color:var(--muted);font-weight:300;margin-top:3px;">Strategic leadership · Executive-facing</div>
          </div>
          <span class="role-level">Senior Leadership</span>
        </div>
        <div class="role-body">
          <div>
            <div class="role-section-label">Core Responsibilities</div>
            <ul class="role-list">
              <li>Define and champion the PMO's vision, mission, and strategic roadmap</li>
              <li>Align portfolio priorities with executive leadership and board objectives</li>
              <li>Govern PMO budget, headcount, and resource allocation</li>
              <li>Represent PMO in C-suite and stakeholder forums</li>
              <li>Drive organizational change and PMO maturity advancement</li>
            </ul>
          </div>
          <div>
            <div class="role-section-label">Key Qualifications</div>
            <ul class="role-list">
              <li>10+ years in program or portfolio management</li>
              <li>PMP, PgMP, or equivalent advanced certification</li>
              <li>Experience managing distributed or global teams</li>
              <li>Executive presence and cross-functional influence skills</li>
              <li>Proficiency in enterprise PPM platforms (Smartsheet, Planview)</li>
            </ul>
          </div>
        </div>
      </div>

      <div class="role-card">
        <div class="role-header">
          <span class="role-num">02</span>
          <div>
            <div class="role-name">Senior Program Manager</div>
            <div style="font-size:0.8rem;color:var(--muted);font-weight:300;margin-top:3px;">Multi-project orchestration · Cross-functional leadership</div>
          </div>
          <span class="role-level">Mid-Senior</span>
        </div>
        <div class="role-body">
          <div>
            <div class="role-section-label">Core Responsibilities</div>
            <ul class="role-list">
              <li>Manage interdependencies and risks across a portfolio of projects</li>
              <li>Facilitate executive steering committees and governance reviews</li>
              <li>Develop and maintain program-level roadmaps and integrated schedules</li>
              <li>Resolve escalated blockers and cross-team resource conflicts</li>
              <li>Ensure program benefits realization and ROI tracking</li>
            </ul>
          </div>
          <div>
            <div class="role-section-label">Key Qualifications</div>
            <ul class="role-list">
              <li>7–10 years of project/program management experience</li>
              <li>PMP required; PgMP or MBA preferred</li>
              <li>Strong stakeholder management and facilitation skills</li>
              <li>Experience with Agile and waterfall delivery models</li>
              <li>Budget management experience ($1M+)</li>
            </ul>
          </div>
        </div>
      </div>

      <div class="role-card">
        <div class="role-header">
          <span class="role-num">03</span>
          <div>
            <div class="role-name">Project Manager (PM)</div>
            <div style="font-size:0.8rem;color:var(--muted);font-weight:300;margin-top:3px;">Tactical delivery · Day-to-day execution</div>
          </div>
          <span class="role-level">Mid-Level</span>
        </div>
        <div class="role-body">
          <div>
            <div class="role-section-label">Core Responsibilities</div>
            <ul class="role-list">
              <li>Own full project lifecycle from initiation through closeout</li>
              <li>Develop and maintain project charters, WBS, and RACI matrices</li>
              <li>Facilitate daily standups, sprint reviews, and retrospectives</li>
              <li>Manage project budget, schedule, scope, and quality baselines</li>
              <li>Produce status reports and escalate risks to program leadership</li>
            </ul>
          </div>
          <div>
            <div class="role-section-label">Key Qualifications</div>
            <ul class="role-list">
              <li>3–7 years of project management experience</li>
              <li>PMP or CAPM certification preferred</li>
              <li>Proficiency in Jira, Asana, Monday.com, or MS Project</li>
              <li>Strong written and async communication skills (critical for remote)</li>
              <li>CSM (Certified ScrumMaster) a strong plus</li>
            </ul>
          </div>
        </div>
      </div>

      <div class="role-card">
        <div class="role-header">
          <span class="role-num">04</span>
          <div>
            <div class="role-name">PMO Analyst / Business Analyst</div>
            <div style="font-size:0.8rem;color:var(--muted);font-weight:300;margin-top:3px;">Data · Reporting · Process intelligence</div>
          </div>
          <span class="role-level">Mid-Level</span>
        </div>
        <div class="role-body">
          <div>
            <div class="role-section-label">Core Responsibilities</div>
            <ul class="role-list">
              <li>Build and maintain PMO dashboards, KPI reports, and health metrics</li>
              <li>Conduct process analysis and identify operational improvement areas</li>
              <li>Document requirements, workflows, and standard operating procedures</li>
              <li>Support project intake and prioritization scoring models</li>
              <li>Analyze project data for portfolio-level trends and insights</li>
            </ul>
          </div>
          <div>
            <div class="role-section-label">Key Qualifications</div>
            <ul class="role-list">
              <li>2–5 years in business or data analysis</li>
              <li>CBAP, PMI-PBA, or Lean Six Sigma Green Belt preferred</li>
              <li>Advanced Excel, Power BI, or Tableau proficiency</li>
              <li>Ability to translate data into executive-level narrative</li>
              <li>Experience with process mapping tools (Lucidchart, Visio)</li>
            </ul>
          </div>
        </div>
      </div>

      <div class="role-card">
        <div class="role-header">
          <span class="role-num">05</span>
          <div>
            <div class="role-name">Scrum Master / Agile Coach</div>
            <div style="font-size:0.8rem;color:var(--muted);font-weight:300;margin-top:3px;">Agile delivery · Team velocity · Continuous improvement</div>
          </div>
          <span class="role-level">Specialist</span>
        </div>
        <div class="role-body">
          <div>
            <div class="role-section-label">Core Responsibilities</div>
            <ul class="role-list">
              <li>Facilitate all Agile ceremonies in a remote-first format</li>
              <li>Coach teams on Agile principles, Scrum rituals, and Kanban flow</li>
              <li>Remove impediments and shield teams from organizational noise</li>
              <li>Track velocity, sprint health, and team well-being metrics</li>
              <li>Evangelize continuous improvement across PMO delivery teams</li>
            </ul>
          </div>
          <div>
            <div class="role-section-label">Key Qualifications</div>
            <ul class="role-list">
              <li>3–6 years in Agile delivery roles</li>
              <li>CSM, PSM, or SAFe Scrum Master certification required</li>
              <li>Experience with Jira, ClickUp, or Azure DevOps</li>
              <li>Strong facilitation skills for virtual environments</li>
              <li>Coaching or organizational change background preferred</li>
            </ul>
          </div>
        </div>
      </div>

      <div class="role-card">
        <div class="role-header">
          <span class="role-num">06</span>
          <div>
            <div class="role-name">PMO Coordinator / Project Coordinator</div>
            <div style="font-size:0.8rem;color:var(--muted);font-weight:300;margin-top:3px;">Administrative backbone · Logistics · Knowledge management</div>
          </div>
          <span class="role-level">Entry–Mid</span>
        </div>
        <div class="role-body">
          <div>
            <div class="role-section-label">Core Responsibilities</div>
            <ul class="role-list">
              <li>Maintain project documentation, meeting minutes, and action logs</li>
              <li>Coordinate cross-team scheduling, calendar management, and logistics</li>
              <li>Support onboarding of new project team members</li>
              <li>Manage the PMO knowledge repository and templates library</li>
              <li>Track action items and follow up on open deliverables</li>
            </ul>
          </div>
          <div>
            <div class="role-section-label">Key Qualifications</div>
            <ul class="role-list">
              <li>1–3 years of coordination or administrative project support</li>
              <li>CAPM or PMI entry-level cert preferred</li>
              <li>Highly organized with exceptional async communication skills</li>
              <li>Proficiency in Notion, Confluence, SharePoint, or Google Workspace</li>
              <li>Self-directed and comfortable in autonomous remote environments</li>
            </ul>
          </div>
        </div>
      </div>

    </div>
  </div>
</section>

<!-- ══════════ SECTION 3: GOVERNANCE ══════════ -->
<section class="section">
  <div class="page">
    <div class="section-label">Section 03</div>
    <h2 class="section-title">Governance Frameworks for Remote PMOs</h2>
    <p class="section-desc">Remote PMOs require explicit governance that co-located teams take for granted. Build these structures before you need them.</p>
    <div class="framework-grid">
      <div class="fw-card">
        <div class="fw-card-accent"></div>
        <div class="fw-card-title">Project Intake & Prioritization</div>
        <p class="fw-card-body">Establish a formal intake process with scoring criteria aligned to strategic objectives. Every request enters a funnel — not a Slack message. Use weighted scoring models (strategic value, resource feasibility, risk, ROI) to maintain a live priority stack visible to all stakeholders.</p>
        <div class="fw-tag-row">
          <span class="fw-tag">Intake Form</span>
          <span class="fw-tag">Scoring Matrix</span>
          <span class="fw-tag">Prioritization Board</span>
          <span class="fw-tag">Governance Gate</span>
        </div>
      </div>
      <div class="fw-card">
        <div class="fw-card-accent"></div>
        <div class="fw-card-title">Change Control Protocol</div>
        <p class="fw-card-body">Define what constitutes a change request, the approval threshold by impact level, and who holds authority at each tier. Document it. Train every PM on it. A remote team without change control is one undocumented Zoom conversation away from major scope creep.</p>
        <div class="fw-tag-row">
          <span class="fw-tag">CCB Charter</span>
          <span class="fw-tag">Impact Thresholds</span>
          <span class="fw-tag">Approval Tiers</span>
          <span class="fw-tag">Change Log</span>
        </div>
      </div>
      <div class="fw-card">
        <div class="fw-card-accent"></div>
        <div class="fw-card-title">Risk & Issue Management</div>
        <p class="fw-card-body">Build a tiered risk register protocol with defined probability/impact scoring, response strategies (accept, mitigate, transfer, avoid), and clear escalation paths. Remote teams need structured channels for risk surfacing — not just a shared spreadsheet that nobody updates.</p>
        <div class="fw-tag-row">
          <span class="fw-tag">Risk Register</span>
          <span class="fw-tag">Escalation Matrix</span>
          <span class="fw-tag">Response Plans</span>
          <span class="fw-tag">RAID Log</span>
        </div>
      </div>
      <div class="fw-card">
        <div class="fw-card-accent"></div>
        <div class="fw-card-title">Communication Cadence</div>
        <p class="fw-card-body">Over-communicate intentionally. Establish a tiered communication framework: daily async standups, weekly project status reports, bi-weekly portfolio reviews, and monthly executive briefings. Define the medium, format, and owner for each. Silence in a remote PMO is never golden.</p>
        <div class="fw-tag-row">
          <span class="fw-tag">Async Standups</span>
          <span class="fw-tag">Status Templates</span>
          <span class="fw-tag">Comms Plan</span>
          <span class="fw-tag">Stakeholder Map</span>
        </div>
      </div>
      <div class="fw-card">
        <div class="fw-card-accent"></div>
        <div class="fw-card-title">Resource Capacity Planning</div>
        <p class="fw-card-body">Maintain a real-time resource capacity map that shows allocation across all active projects. Remote teams are especially susceptible to invisible overloading — when you can't see someone's desk piling up, the data must tell you. Build bi-weekly capacity check-ins into the PMO rhythm.</p>
        <div class="fw-tag-row">
          <span class="fw-tag">Capacity Matrix</span>
          <span class="fw-tag">Utilization Reports</span>
          <span class="fw-tag">Demand Forecasting</span>
        </div>
      </div>
      <div class="fw-card">
        <div class="fw-card-accent"></div>
        <div class="fw-card-title">Lessons Learned & Continuous Improvement</div>
        <p class="fw-card-body">Close every project with a structured retrospective. Archive findings in a searchable PMO knowledge base. Create quarterly "PMO Improvement Sprints" to systematically upgrade your frameworks, templates, and tools based on real delivery data — not gut feel.</p>
        <div class="fw-tag-row">
          <span class="fw-tag">Retro Template</span>
          <span class="fw-tag">Knowledge Base</span>
          <span class="fw-tag">Improvement Log</span>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ══════════ SECTION 4: TECH STACK ══════════ -->
<section class="section section-dark">
  <div class="page">
    <div class="section-label">Section 04</div>
    <h2 class="section-title">The Remote PMO Technology Stack</h2>
    <p class="section-desc">Tools don't create execution discipline — but the right stack makes discipline easier to sustain. Choose tools that fit your team's maturity and scale with your complexity.</p>
    <div class="tech-cols">
      <div class="tech-col">
        <div class="tech-col-label">Project & Portfolio Mgmt</div>
        <ul class="tech-list">
          <li>Smartsheet (enterprise-grade)</li>
          <li>Microsoft Project / Planner</li>
          <li>Monday.com</li>
          <li>Asana (mid-market)</li>
          <li>ClickUp (all-in-one)</li>
          <li>Planview (large enterprise)</li>
          <li>Wrike</li>
        </ul>
      </div>
      <div class="tech-col">
        <div class="tech-col-label">Communication & Collaboration</div>
        <ul class="tech-list">
          <li>Slack (async-first culture)</li>
          <li>Microsoft Teams</li>
          <li>Zoom + Loom (async video)</li>
          <li>Notion (wiki + docs)</li>
          <li>Confluence (documentation)</li>
          <li>Miro (virtual whiteboarding)</li>
          <li>Google Workspace</li>
        </ul>
      </div>
      <div class="tech-col">
        <div class="tech-col-label">Agile & Dev-Adjacent</div>
        <ul class="tech-list">
          <li>Jira (Agile boards)</li>
          <li>Azure DevOps</li>
          <li>Linear (modern teams)</li>
          <li>Trello (visual boards)</li>
          <li>GitHub Projects</li>
          <li>Shortcut (formerly Clubhouse)</li>
          <li>ProductBoard</li>
        </ul>
      </div>
      <div class="tech-col">
        <div class="tech-col-label">Reporting & Analytics</div>
        <ul class="tech-list">
          <li>Power BI (enterprise dashboards)</li>
          <li>Tableau</li>
          <li>Datadog (tech PMOs)</li>
          <li>Google Looker Studio</li>
          <li>Klipfolio</li>
          <li>Smartsheet Dashboards</li>
          <li>Excel / Google Sheets</li>
        </ul>
      </div>
    </div>
    <div style="margin-top:32px;padding:24px 28px;border:1px solid rgba(168,118,5,0.25);background:rgba(168,118,5,0.05);">
      <p style="font-family:'DM Mono',monospace;font-size:0.68rem;letter-spacing:0.1em;color:var(--gold);margin-bottom:8px;">⚡ EXECUTION TIP</p>
      <p style="font-size:0.88rem;color:rgba(245,239,230,0.65);font-weight:300;line-height:1.75;">Don't let tool selection stall your PMO launch. Pick one tool per category, deploy it consistently, and optimize later. A team using Trello religiously outperforms a team that has Planview licenses nobody opens.</p>
    </div>
  </div>
</section>

<!-- ══════════ SECTION 5: IMPLEMENTATION ROADMAP ══════════ -->
<section class="section section-alt">
  <div class="page">
    <div class="section-label">Section 05</div>
    <h2 class="section-title">Your 90-Day Remote PMO Launch Roadmap</h2>
    <p class="section-desc">Stand up your PMO with intention, not improvisation. This phased approach builds the foundation before adding complexity.</p>
    <div class="roadmap">
      <div class="roadmap-phase">
        <div class="phase-dot">
          <div class="phase-dot-inner">Day<br>1–30</div>
        </div>
        <div class="phase-timeline">Phase 01</div>
        <div class="phase-title">Foundation &amp; Charter</div>
        <ul class="phase-list">
          <li>Define PMO type (supportive, controlling, directive)</li>
          <li>Draft PMO charter with scope and authority levels</li>
          <li>Conduct stakeholder analysis and alignment sessions</li>
          <li>Identify core team roles and begin hiring/assignment</li>
          <li>Select and configure PPM tool stack</li>
          <li>Audit current project inventory</li>
        </ul>
      </div>
      <div class="roadmap-phase">
        <div class="phase-dot">
          <div class="phase-dot-inner">Day<br>31–60</div>
        </div>
        <div class="phase-timeline">Phase 02</div>
        <div class="phase-title">Infrastructure Build</div>
        <ul class="phase-list">
          <li>Deploy project intake and prioritization process</li>
          <li>Build standard PM templates and documentation library</li>
          <li>Establish governance cadences and meeting rhythms</li>
          <li>Create RACI templates and communication plans</li>
          <li>Stand up reporting dashboards for leadership</li>
          <li>Develop onboarding playbook for new projects</li>
        </ul>
      </div>
      <div class="roadmap-phase">
        <div class="phase-dot">
          <div class="phase-dot-inner">Day<br>61–75</div>
        </div>
        <div class="phase-timeline">Phase 03</div>
        <div class="phase-title">Pilot &amp; Calibrate</div>
        <ul class="phase-list">
          <li>Run 2–3 projects through new PMO processes</li>
          <li>Collect PM and stakeholder feedback in real time</li>
          <li>Identify friction points in tools and workflows</li>
          <li>Refine templates based on pilot learnings</li>
          <li>Calibrate reporting frequency and format</li>
          <li>Validate governance gates with leadership</li>
        </ul>
      </div>
      <div class="roadmap-phase">
        <div class="phase-dot">
          <div class="phase-dot-inner">Day<br>76–90</div>
        </div>
        <div class="phase-timeline">Phase 04</div>
        <div class="phase-title">Scale &amp; Formalize</div>
        <ul class="phase-list">
          <li>Officially onboard all active projects to PMO oversight</li>
          <li>Publish PMO standards and playbook organization-wide</li>
          <li>Launch first executive portfolio review</li>
          <li>Establish quarterly PMO maturity assessment cadence</li>
          <li>Define PMO OKRs for the next 12 months</li>
          <li>Document lessons learned from launch phase</li>
        </ul>
      </div>
    </div>
  </div>
</section>

<!-- ══════════ SECTION 6: CERTIFICATIONS ══════════ -->
<section class="section section-dark">
  <div class="page">
    <div class="section-label">Section 06</div>
    <h2 class="section-title">Certifications That Build Remote PMO Credibility</h2>
    <p class="section-desc">The right credentials signal that your team has internalized industry standards — not just learned the vocabulary. Prioritize these for your PMO hires and existing team development.</p>
    <div class="cert-grid">
      <div class="cert-card">
        <span class="cert-badge">PMP</span>
        <div class="cert-name">Project Management Professional</div>
        <p class="cert-body">The gold standard for project managers. Required for senior PMO roles. Covers predictive, Agile, and hybrid delivery approaches. Issued by PMI.</p>
      </div>
      <div class="cert-card">
        <span class="cert-badge">PgMP</span>
        <div class="cert-name">Program Management Professional</div>
        <p class="cert-body">For Program Managers and PMO Directors managing interdependent projects. Validates strategic alignment and benefits management competency. Issued by PMI.</p>
      </div>
      <div class="cert-card">
        <span class="cert-badge">PfMP</span>
        <div class="cert-name">Portfolio Management Professional</div>
        <p class="cert-body">Senior-level cert for portfolio governance and strategic prioritization. Ideal for PMO Directors and VPs managing a large project portfolio. Issued by PMI.</p>
      </div>
      <div class="cert-card">
        <span class="cert-badge">CSM</span>
        <div class="cert-name">Certified ScrumMaster</div>
        <p class="cert-body">Entry point to Agile leadership. Ensures foundational Scrum knowledge. Essential for any PMO running Agile or hybrid delivery. Issued by Scrum Alliance.</p>
      </div>
      <div class="cert-card">
        <span class="cert-badge">SAFe</span>
        <div class="cert-name">Scaled Agile Framework</div>
        <p class="cert-body">For PMOs scaling Agile across multiple teams and value streams. Particularly valuable in tech or product-led organizations. Multiple role-specific certifications available.</p>
      </div>
      <div class="cert-card">
        <span class="cert-badge">CBAP</span>
        <div class="cert-name">Certified Business Analysis Professional</div>
        <p class="cert-body">For PMO Analysts and BAs responsible for requirements, process analysis, and data-driven decision support. Issued by IIBA.</p>
      </div>
      <div class="cert-card">
        <span class="cert-badge">LSS</span>
        <div class="cert-name">Lean Six Sigma (Green/Black Belt)</div>
        <p class="cert-body">Validates process improvement and waste-reduction expertise. Highly valuable for PMO analysts and operations-focused team members. Available from ASQ and others.</p>
      </div>
      <div class="cert-card">
        <span class="cert-badge">PMI-ACP</span>
        <div class="cert-name">Agile Certified Practitioner</div>
        <p class="cert-body">Broad Agile certification covering Scrum, Kanban, XP, and more. Ideal for PMs transitioning into or deepening Agile practice. Issued by PMI.</p>
      </div>
      <div class="cert-card">
        <span class="cert-badge">CAPM</span>
        <div class="cert-name">Certified Associate in Project Mgmt</div>
        <p class="cert-body">Entry-level PMI certification. Strong signal for PMO Coordinators and early-career PMs demonstrating commitment to the profession. Issued by PMI.</p>
      </div>
    </div>
  </div>
</section>

<!-- ══════════ SECTION 7: COMMON MISTAKES ══════════ -->
<section class="section">
  <div class="page">
    <div class="section-label">Section 07</div>
    <h2 class="section-title">7 Mistakes That Sink Remote PMOs</h2>
    <p class="section-desc">Most remote PMO failures aren't caused by bad PMs — they're caused by bad architecture. Recognize these patterns before they become your reality.</p>
    <div class="mistakes-grid">
      <div class="mistake-card">
        <div class="mistake-x">✕</div>
        <div class="mistake-title">Confusing Activity with Accountability</div>
        <p class="mistake-body">Long status meetings and crowded Slack channels create the illusion of control. Remote PMOs need outcomes-based accountability — not performative busyness. Measure what moves the needle.</p>
      </div>
      <div class="mistake-card">
        <div class="mistake-x">✕</div>
        <div class="mistake-title">Launching Without a Charter</div>
        <p class="mistake-body">Skipping the PMO charter is like building a house without a foundation permit. Without documented authority, scope, and mandate, the PMO will spend more time defending its existence than delivering value.</p>
      </div>
      <div class="mistake-card">
        <div class="mistake-x">✕</div>
        <div class="mistake-title">Tool Overload Before Process Clarity</div>
        <p class="mistake-body">Buying five PM tools before establishing standard processes guarantees chaos in multiple platforms. Process first. Tools second. Always. The platform should reinforce the process — not define it.</p>
      </div>
      <div class="mistake-card">
        <div class="mistake-x">✕</div>
        <div class="mistake-title">Hiring Only for Technical PM Skills</div>
        <p class="mistake-body">Remote PMOs demand exceptional async communication, self-management, and digital fluency. A PM with perfect PMBOK knowledge who can't write a clear Slack update or run a virtual stakeholder session will struggle.</p>
      </div>
      <div class="mistake-card">
        <div class="mistake-x">✕</div>
        <div class="mistake-title">Neglecting Culture and Team Cohesion</div>
        <p class="mistake-body">Remote teams don't build culture by accident. Without intentional investment in virtual team rituals, recognition, and psychological safety, your PMO will suffer from isolation, disengagement, and attrition.</p>
      </div>
      <div class="mistake-card">
        <div class="mistake-x">✕</div>
        <div class="mistake-title">No Escalation Path for Blockers</div>
        <p class="mistake-body">Remote teams lose days waiting for approvals that would take minutes in a hallway conversation. Pre-define escalation paths, authority levels, and response SLAs before the first blocker hits your board.</p>
      </div>
      <div class="mistake-card">
        <div class="mistake-x">✕</div>
        <div class="mistake-title">Treating the PMO as a Cost Center</div>
        <p class="mistake-body">PMOs that can't articulate their ROI get defunded. From day one, track value delivered: projects completed on time, budget variance reduced, execution debt eliminated. Speak the language of the business — not just project management.</p>
      </div>
      <div class="mistake-card">
        <div class="mistake-x">✕</div>
        <div class="mistake-title">One-Size-Fits-All Methodology</div>
        <p class="mistake-body">Forcing waterfall methodology on Agile delivery teams (or vice versa) creates resentment and workarounds. The most effective remote PMOs are methodology-agnostic — standardizing on governance and reporting, not delivery approach.</p>
      </div>
    </div>
  </div>
</section>

<!-- ══════════ CTA ══════════ -->
<section class="cta-section" id="cta">
  <div class="page">
    <div class="cta-eyebrow">Ready to Build Your Execution Engine?</div>
    <h2 class="cta-title">Your PMO Is Only as Strong as Its <em>Architect</em></h2>
    <p class="cta-sub">Greater Ambitions LLC helps growth-stage companies build the execution infrastructure that turns strategy into results — remotely, at scale, without chaos.</p>
    <a href="https://greaterambitionsllc.com" class="cta-btn">I'm Available. Book Your Execution Strategy Consultation.</a>
    <span class="cta-secondary">greaterambitionsllc.com · Tucson, AZ · Dr. Minina Johnson, DBA, PMP, CSM</span>
  </div>
</section>

<footer class="footer">
  <div class="page">
    <div class="footer-brand">
      Greater Ambitions LLC
      <span>PM + Operations Consultancy</span>
    </div>
    <div class="footer-copy">
      © 2025 Greater Ambitions LLC. All Rights Reserved.<br>
      Dr. Minina Johnson, DBA, PMP, CSM · Founder & Principal Strategist<br>
      Diversity-Owned · Tucson, AZ
    </div>
  </div>
</footer>

</body>
</html>
