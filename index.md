---
layout: default
title: "Home"
---

<style>
/* -------------------------------------------------------
   Modern, clean homepage styling (works well on GitHub Pages)
   - Responsive layout
   - Better typography + spacing
   - Card-based sections
   - Subtle hover effects
   - Dark-mode support via prefers-color-scheme
-------------------------------------------------------- */

:root{
  --bg: #ffffff;
  --text: #111827;
  --muted: #4b5563;
  --card: rgba(255,255,255,0.85);
  --border: rgba(17,24,39,0.10);
  --shadow: 0 10px 30px rgba(0,0,0,0.08);
  --shadow-sm: 0 6px 16px rgba(0,0,0,0.08);
  --radius: 16px;

  --brand1: #6ea8fe;
  --brand2: #ff7ac8;
  --brand3: #7c3aed;
  --link: #1f5eff;

  --chip-bg: rgba(17,24,39,0.06);
  --chip-border: rgba(17,24,39,0.10);

  --btn: rgba(17,24,39,0.08);
  --btn-hover: rgba(17,24,39,0.12);
}

@media (prefers-color-scheme: dark) {
  :root{
    --bg: #0b1220;
    --text: #e5e7eb;
    --muted: #a5b4fc;
    --card: rgba(17,24,39,0.70);
    --border: rgba(229,231,235,0.12);
    --shadow: 0 12px 36px rgba(0,0,0,0.35);
    --shadow-sm: 0 10px 26px rgba(0,0,0,0.35);
    --link: #8ab4ff;

    --chip-bg: rgba(229,231,235,0.07);
    --chip-border: rgba(229,231,235,0.12);

    --btn: rgba(229,231,235,0.10);
    --btn-hover: rgba(229,231,235,0.16);
  }
}

/* Page wrapper */
.home-wrap{
  max-width: 1050px;
  margin: 0 auto;
  padding: 18px 14px 30px;
  color: var(--text);
}

/* Make links consistent */
.home-wrap a{
  color: var(--link);
  text-decoration: none;
}
.home-wrap a:hover{
  text-decoration: underline;
}

/* Shared card styling */
.card{
  background: var(--card);
  border: 1px solid var(--border);
  border-radius: var(--radius);
  box-shadow: var(--shadow-sm);
  padding: 18px;
  backdrop-filter: blur(8px);
}

/* HERO */
.hero{
  position: relative;
  overflow: hidden;
  border-radius: calc(var(--radius) + 6px);
  background: radial-gradient(1200px 500px at 15% 10%, rgba(110,168,254,0.55), transparent 60%),
              radial-gradient(900px 450px at 80% 20%, rgba(255,122,200,0.45), transparent 60%),
              radial-gradient(900px 450px at 60% 120%, rgba(124,58,237,0.35), transparent 60%),
              linear-gradient(135deg, rgba(110,168,254,0.35), rgba(255,122,200,0.25));
  border: 1px solid var(--border);
  box-shadow: var(--shadow);
  padding: 26px 18px;
  margin-bottom: 18px;
}

/* subtle “grain” overlay */
.hero:before{
  content:"";
  position:absolute;
  inset:0;
  background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='180' height='180'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='.9' numOctaves='3' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='180' height='180' filter='url(%23n)' opacity='.10'/%3E%3C/svg%3E");
  opacity: .25;
  pointer-events:none;
}

.hero-inner{
  position: relative;
  display: grid;
  grid-template-columns: 220px 1fr;
  gap: 18px;
  align-items: center;
}

@media (max-width: 720px){
  .hero-inner{
    grid-template-columns: 1fr;
    text-align: center;
  }
}

/* Avatar */
.avatar{
  width: 200px;
  height: 200px;
  border-radius: 999px;
  border: 3px solid rgba(255,255,255,0.75);
  box-shadow: 0 10px 24px rgba(0,0,0,0.18);
  object-fit: cover;
  margin: 0 auto;
}

/* Hero text */
.hero h1{
  margin: 0;
  font-size: 2.2rem;
  letter-spacing: -0.02em;
  line-height: 1.15;
}

.subtitle{
  margin: 8px 0 0;
  font-size: 1.05rem;
  color: rgba(255,255,255,0.92);
}

.tagline{
  margin: 10px 0 0;
  font-size: 0.98rem;
  color: rgba(255,255,255,0.90);
}

/* CTA buttons */
.hero-actions{
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
  margin-top: 14px;
}
@media (max-width: 720px){
  .hero-actions{
    justify-content: center;
  }
}

.btn{
  display: inline-flex;
  align-items: center;
  gap: 10px;
  padding: 10px 14px;
  border-radius: 999px;
  border: 1px solid rgba(255,255,255,0.35);
  background: rgba(255,255,255,0.14);
  color: #ffffff !important;
  font-weight: 600;
  text-decoration: none !important;
  transition: transform .2s ease, background .2s ease, border-color .2s ease;
  box-shadow: 0 8px 18px rgba(0,0,0,0.12);
}

.btn:hover{
  transform: translateY(-1px);
  background: rgba(255,255,255,0.18);
  border-color: rgba(255,255,255,0.55);
}

.btn.primary{
  background: rgba(255,255,255,0.22);
  border-color: rgba(255,255,255,0.55);
}

/* Hero “micro links” */
.hero-links{
  margin-top: 12px;
  display: flex;
  flex-wrap: wrap;
  gap: 12px;
  font-size: 0.95rem;
}
@media (max-width: 720px){
  .hero-links{ justify-content: center; }
}
.hero-links a{
  color: rgba(255,255,255,0.92) !important;
  text-decoration: none !important;
  border-bottom: 1px solid rgba(255,255,255,0.35);
}
.hero-links a:hover{
  border-bottom-color: rgba(255,255,255,0.80);
}

/* ABOUT */
.section-title{
  margin: 0 0 10px;
  font-size: 1.15rem;
  letter-spacing: -0.01em;
}
.about p{
  margin: 0 0 12px;
  color: var(--text);
  line-height: 1.7;
}
.about p:last-child{ margin-bottom: 0; }

/* Two-column row */
.row{
  display: grid;
  grid-template-columns: 1.1fr 0.9fr;
  gap: 16px;
  margin-top: 16px;
}
@media (max-width: 900px){
  .row{ grid-template-columns: 1fr; }
}

/* Contact list */
.contact ul{
  list-style: none;
  padding-left: 0;
  margin: 0;
}
.contact li{
  padding: 8px 0;
  border-bottom: 1px dashed var(--border);
}
.contact li:last-child{ border-bottom: none; }
.contact strong{ color: var(--text); }

/* Chips */
.chips{
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
  margin-top: 10px;
}
.chip{
  display: inline-flex;
  align-items: center;
  padding: 8px 12px;
  border-radius: 999px;
  background: var(--chip-bg);
  border: 1px solid var(--chip-border);
  color: var(--text);
  font-size: 0.92rem;
}

/* QUICK LINKS */
.quick{
  margin-top: 16px;
}
.quick-grid{
  display: grid;
  grid-template-columns: repeat(4, minmax(0, 1fr));
  gap: 14px;
}
@media (max-width: 980px){
  .quick-grid{ grid-template-columns: repeat(2, minmax(0, 1fr)); }
}
@media (max-width: 520px){
  .quick-grid{ grid-template-columns: 1fr; }
}

.link-card{
  display: block;
  padding: 14px 14px;
  border-radius: var(--radius);
  border: 1px solid var(--border);
  background: var(--card);
  box-shadow: var(--shadow-sm);
  transition: transform .2s ease, box-shadow .2s ease, border-color .2s ease;
  text-decoration: none !important;
  color: var(--text) !important;
}
.link-card:hover{
  transform: translateY(-2px);
  box-shadow: var(--shadow);
  border-color: rgba(31,94,255,0.28);
}
.link-title{
  font-weight: 700;
  margin: 0 0 6px;
  letter-spacing: -0.01em;
}
.link-sub{
  margin: 0;
  color: var(--muted);
  font-size: 0.93rem;
  line-height: 1.4;
}

/* Footer note */
.footer-note{
  margin-top: 14px;
  color: var(--muted);
  line-height: 1.6;
}
</style>

<div class="home-wrap">

  <!-- HERO -->
  <div class="hero">
    <div class="hero-inner">
      <img class="avatar" src="/assets/images/sharkawy.jpg" alt="Mohamed Elsharkawy profile photo" />

      <div>
        <h1>Mohamed Elsharkawy, MSc</h1>
        <div class="subtitle">PhD Student @ University of Louisville</div>
        <div class="tagline">Medical Image Analysis • Machine Learning • Computer Vision</div>

        <div class="hero-actions">
          <a class="btn primary" href="/publications/">Browse Publications</a>
          <a class="btn" href="/assets/files/elsharkawycv.pdf" target="_blank" rel="noopener">Download CV (PDF)</a>
          <a class="btn" href="/cv/">Preview CV</a>
        </div>

        <div class="hero-links" aria-label="External links">
          <a href="https://scholar.google.com/citations?user=IknnHU4AAAAJ&hl=en" target="_blank" rel="noopener">Google Scholar</a>
          <!-- Add more if you want:
          <a href="https://github.com/USERNAME" target="_blank" rel="noopener">GitHub</a>
          <a href="https://www.linkedin.com/in/USERNAME/" target="_blank" rel="noopener">LinkedIn</a>
          -->
        </div>
      </div>
    </div>
  </div>

  <!-- ABOUT -->
  <div class="card about">
    <h2 class="section-title">About</h2>
    <p>
      I’m Mohamed Elsharkawy, a PhD student in Computer Science and Engineering and a Graduate Teaching Assistant at the
      University of Louisville. I also serve as an Assistant Lecturer in the Information Technology Department at
      Mansoura University.
    </p>
    <p>
      My research focuses on developing reliable and explainable AI methods for medical imaging, with a strong interest
      in ophthalmic applications (e.g., retinal disease diagnosis) using deep learning and computer vision.
    </p>
    <p>
      <strong>Research interests:</strong> medical image analysis, deep learning, vision transformers, explainable AI (XAI),
      segmentation & classification.
    </p>
  </div>

  <!-- ROW: Contact + Focus -->
  <div class="row">
    <div class="card contact">
      <h2 class="section-title">Contact</h2>
      <ul>
        <li><strong>Email:</strong> <a href="mailto:mohamed.elsharkawy@louisville.edu">mohamed.elsharkawy@louisville.edu</a></li>
        <li><strong>Phone (USA):</strong> +1 502-885-0800</li>
        <li><strong>Phone (Egypt):</strong> +20 1069662911</li>
      </ul>
      <p style="margin:12px 0 0; color: var(--muted); line-height:1.6;">
        Feel free to reach out for research collaboration, academic opportunities, or project discussions.
      </p>
    </div>

    <div class="card">
      <h2 class="section-title">Focus Areas</h2>
      <div class="chips">
        <span class="chip">Fundus / OCT / OCTA</span>
        <span class="chip">Classification</span>
        <span class="chip">Segmentation</span>
        <span class="chip">Transformers (ViT/Swin)</span>
        <span class="chip">Graph Neural Networks</span>
        <span class="chip">Explainability (XAI)</span>
      </div>
      <p style="margin:12px 0 0; color: var(--muted); line-height:1.6;">
        I build end-to-end pipelines (data → models → evaluation → visual explanations) and aim for strong reproducibility.
      </p>
    </div>
  </div>

  <!-- QUICK LINKS -->
  <div class="quick">
    <h2 class="section-title">Quick Links</h2>
    <div class="quick-grid">
      <a class="link-card" href="/assets/files/elsharkawycv.pdf" target="_blank" rel="noopener">
        <div class="link-title">Download Full CV (PDF)</div>
        <p class="link-sub">Latest PDF version of my CV.</p>
      </a>

      <a class="link-card" href="/cv/">
        <div class="link-title">Preview CV</div>
        <p class="link-sub">Web version (easy to read on mobile).</p>
      </a>

      <a class="link-card" href="/publications/">
        <div class="link-title">Publications</div>
        <p class="link-sub">Papers, journals, and conference work.</p>
      </a>

      <a class="link-card" href="https://scholar.google.com/citations?user=IknnHU4AAAAJ&hl=en" target="_blank" rel="noopener">
        <div class="link-title">Google Scholar</div>
        <p class="link-sub">Citation metrics + complete publication list.</p>
      </a>
    </div>

    <p class="footer-note">
      Thanks for visiting — explore my publications and feel free to connect.
    </p>
  </div>

</div>
