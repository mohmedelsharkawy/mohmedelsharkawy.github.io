---
layout: default
title: "Publications"
permalink: /publications/
---

<style>
/* ============================
   Publications Page – Modern UI
   ============================ */

:root{
  --bg:#ffffff;
  --text:#0f172a;
  --muted:#475569;
  --card:rgba(255,255,255,0.9);
  --border:rgba(15,23,42,0.10);
  --shadow:0 12px 30px rgba(0,0,0,0.08);
  --shadow-sm:0 6px 16px rgba(0,0,0,0.07);
  --radius:16px;
  --link:#2563eb;

  --accent1:#60a5fa;
  --accent2:#f472b6;
  --accent3:#a78bfa;

  --chip-bg:rgba(15,23,42,0.05);
  --chip-border:rgba(15,23,42,0.10);
}

@media (prefers-color-scheme: dark){
  :root{
    --bg:#0b1220;
    --text:#e5e7eb;
    --muted:#a1a1aa;
    --card:rgba(17,24,39,0.72);
    --border:rgba(229,231,235,0.12);
    --shadow:0 16px 42px rgba(0,0,0,0.35);
    --shadow-sm:0 10px 26px rgba(0,0,0,0.35);
    --link:#8ab4ff;

    --chip-bg:rgba(229,231,235,0.07);
    --chip-border:rgba(229,231,235,0.12);
  }
}

.pub-wrap{
  max-width: 1100px;
  margin: 0 auto;
  padding: 18px 14px 34px;
  color: var(--text);
}

/* Global link style inside this page */
.pub-wrap a{
  color: var(--link);
  text-decoration: none;
}
.pub-wrap a:hover{ text-decoration: underline; }

/* HERO */
.pub-hero{
  position: relative;
  overflow: hidden;
  border-radius: calc(var(--radius) + 8px);
  padding: 26px 18px;
  border: 1px solid var(--border);
  box-shadow: var(--shadow);
  background:
    radial-gradient(1100px 520px at 15% 10%, rgba(96,165,250,0.45), transparent 60%),
    radial-gradient(900px 480px at 80% 20%, rgba(244,114,182,0.35), transparent 60%),
    radial-gradient(900px 480px at 60% 120%, rgba(167,139,250,0.30), transparent 60%),
    linear-gradient(135deg, rgba(96,165,250,0.18), rgba(244,114,182,0.14));
}

.pub-hero:before{
  content:"";
  position:absolute;
  inset:0;
  background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='180' height='180'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='.9' numOctaves='3' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='180' height='180' filter='url(%23n)' opacity='.10'/%3E%3C/svg%3E");
  opacity: .22;
  pointer-events:none;
}

.pub-hero-inner{
  position: relative;
  display: grid;
  grid-template-columns: 1fr;
  gap: 10px;
  text-align: center;
}

.pub-hero h1{
  margin: 0;
  font-size: 2.2rem;
  letter-spacing: -0.02em;
  line-height: 1.15;
}

.pub-hero p{
  margin: 0;
  color: rgba(255,255,255,0.92);
  font-size: 1.05rem;
  line-height: 1.6;
}

/* Chips row */
.pub-chips{
  margin-top: 14px;
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
  justify-content: center;
}

.chip{
  display: inline-flex;
  align-items: center;
  gap: 8px;
  padding: 8px 12px;
  border-radius: 999px;
  border: 1px solid rgba(255,255,255,0.25);
  background: rgba(255,255,255,0.14);
  color: rgba(255,255,255,0.95);
  font-size: 0.92rem;
  backdrop-filter: blur(8px);
}

/* Layout row */
.pub-row{
  display: grid;
  grid-template-columns: 1fr 320px;
  gap: 16px;
  margin-top: 16px;
}

@media (max-width: 980px){
  .pub-row{ grid-template-columns: 1fr; }
}

/* Cards */
.card{
  background: var(--card);
  border: 1px solid var(--border);
  border-radius: var(--radius);
  box-shadow: var(--shadow-sm);
  padding: 16px;
  backdrop-filter: blur(8px);
}

.card h2{
  margin: 0 0 12px;
  font-size: 1.1rem;
  letter-spacing: -0.01em;
}

/* Sidebar */
.sidebar .mini{
  color: var(--muted);
  line-height: 1.6;
  margin: 0 0 12px;
}

.side-links{
  display: grid;
  gap: 10px;
}

.side-btn{
  display: block;
  padding: 10px 12px;
  border-radius: 12px;
  border: 1px solid var(--border);
  background: var(--card);
  box-shadow: var(--shadow-sm);
  text-decoration: none !important;
  color: var(--text) !important;
  transition: transform .2s ease, box-shadow .2s ease, border-color .2s ease;
}
.side-btn:hover{
  transform: translateY(-2px);
  box-shadow: var(--shadow);
  border-color: rgba(37,99,235,0.25);
}
.side-btn small{
  display:block;
  color: var(--muted);
  margin-top: 3px;
}

/* Publication sections */
.pub-section{
  margin-top: 16px;
}

.section-head{
  display:flex;
  align-items: baseline;
  justify-content: space-between;
  gap: 12px;
  padding-bottom: 10px;
  border-bottom: 1px solid var(--border);
  margin-bottom: 12px;
}

.section-head h3{
  margin: 0;
  font-size: 1.15rem;
  letter-spacing: -0.01em;
}

.section-badge{
  font-size: 0.85rem;
  color: var(--muted);
  padding: 6px 10px;
  border-radius: 999px;
  border: 1px solid var(--border);
  background: rgba(127,127,127,0.06);
}

/* Publication list */
.pub-list{
  list-style: none;
  padding-left: 0;
  margin: 0;
  display: grid;
  gap: 12px;
}

.pub-item{
  padding: 12px 12px;
  border-radius: 14px;
  border: 1px solid var(--border);
  background: rgba(127,127,127,0.04);
}

.pub-item:hover{
  border-color: rgba(37,99,235,0.22);
}

.pub-title{
  font-weight: 800;
}

.me{
  font-weight: 800;
  text-decoration: underline;
  text-decoration-thickness: 2px;
  text-underline-offset: 3px;
}

/* Small actions under a publication (DOI, PDF, etc.) */
.pub-actions{
  margin-top: 8px;
  display: flex;
  flex-wrap: wrap;
  gap: 8px;
}

.pill{
  display:inline-flex;
  align-items:center;
  gap:8px;
  padding: 6px 10px;
  border-radius: 999px;
  border: 1px solid var(--border);
  background: var(--card);
  box-shadow: var(--shadow-sm);
  font-size: 0.88rem;
  text-decoration: none !important;
  color: var(--text) !important;
}
.pill:hover{
  border-color: rgba(37,99,235,0.25);
}

/* Note */
.note{
  margin-top: 16px;
  color: var(--muted);
  line-height: 1.7;
}
</style>

<div class="pub-wrap">

  <!-- HERO -->
  <section class="pub-hero">
    <div class="pub-hero-inner">
      <h1>Publications</h1>
      <p>
        A curated list of my <strong>peer-reviewed journal articles, conference papers, book chapters, and abstracts</strong>.
        (For the most up-to-date record, please see Google Scholar.)
      </p>

      <div class="pub-chips" aria-label="Highlights">
        <span class="chip">Medical Imaging AI</span>
        <span class="chip">Fundus / OCT / OCTA</span>
        <span class="chip">Classification & Segmentation</span>
        <span class="chip">Explainable AI (XAI)</span>
      </div>
    </div>
  </section>

  <div class="pub-row">

    <!-- MAIN -->
    <main>

      <!-- Patents -->
      <section class="card pub-section" id="patents">
        <div class="section-head">
          <h3>Patents and Disclosures</h3>
          <span class="section-badge">1 item</span>
        </div>

        <ul class="pub-list">
          <li class="pub-item">
            <strong class="me">M. Elsharkawy</strong>, A. El-Baz, A. Shalaby, A. Soliman, A. Sharafeldeen, A. Mahmoud, H. Sandhu, G. Giridharan<br/>
            <em>"ASSESSMENT OF PULMONARY FUNCTION IN CORONAVIRUS PATIENT,"</em> U.S. Patent Application 12,217,432 (Active)
          </li>
        </ul>
      </section>

      <!-- Journals -->
      <section class="card pub-section" id="journals">
        <div class="section-head">
          <h3>Peer-Reviewed Journal Articles</h3>
          <span class="section-badge">selected list</span>
        </div>

        <ul class="pub-list">
          <li class="pub-item">
            [1] El-Den, N.N., <span class="me">Elsharkawy, M.</span>, Saleh, I., Ghazal, M., Khalil, A., Haq, M.Z., Sewelam, A., Mahdi, H. and El-Baz, A., 2024.
            <span class="pub-title">AI-based methods for detecting and classifying age-related macular degeneration: a comprehensive review.</span>
            <em>Artificial Intelligence Review</em>, 57(9), p.237.
          </li>

          <li class="pub-item">
            [2] Abdelhalim, I., Nadmid, N., <span class="me">Elsharkawy, M.</span>, Ghazal, M., Mahmoud, A. and El-Baz, A., 2025.
            <span class="pub-title">Mask-UnMask Regions (MUMR) Framework for Classifying AMD Grades Using Inter-Regional Interaction Analysis.</span>
            <em>IEEE Access</em>.
          </li>

          <li class="pub-item">
            [3] <span class="me">Elsharkawy, M.</span>, Sharafeldeen A., Khalifa, F., Soliman, A., Elnakib, A., Ghazal, M., Sewelam, A., Thanos, A., Sandhu, H.S., El-Baz, A.
            <span class="pub-title">A Clinically Explainable AI-Based Grading System for Age-Related Macular Degeneration Using Optical Coherence Tomography.</span>
            <em>IEEE Journal of Biomedical Health Informatics.</em> 2024 Jan 17;PP. doi: 10.1109/JBHI.2024.3355329.
            <div class="pub-actions">
              <a class="pill" href="https://doi.org/10.1109/JBHI.2024.3355329" target="_blank" rel="noopener">DOI</a>
            </div>
          </li>

          <li class="pub-item">
            [4] El-Den, N.N., Naglah, A., <span class="me">Elsharkawy, M.</span>, Ghazal, M., Alghamdi, N.S., Sandhu, H., Mahdi, H. and El-Baz, A., 2023.
            <span class="pub-title">Scale-adaptive model for detection and grading of age-related macular degeneration from color retinal fundus images.</span>
            <em>Scientific Reports</em>, 13(1), p.9590.
          </li>

          <li class="pub-item">
            [5] Haggag, S.; Elnakib, A.; Sharafeldeen, A.; <span class="me">Elsharkawy, M.</span>, Khalifa, F.; Farag, R.K.; Mohamed, M.A.; Sandhu, H.S.; Mansoor, W.; Sewelam, A.; El-Baz, A.
            <span class="pub-title">A Computer-Aided Diagnostic System for Diabetic Retinopathy Based on Local and Global Extracted Features.</span>
            <em>Appl. Sci.</em> 2022, 12, 8326.
            <div class="pub-actions">
              <a class="pill" href="https://doi.org/10.3390/app12168326" target="_blank" rel="noopener">DOI</a>
            </div>
          </li>
        </ul>

        <p class="note">
          Tip: You can keep adding the rest of your journal list in the same <code>&lt;li class="pub-item"&gt;</code> format.
        </p>
      </section>

      <!-- Conferences -->
      <section class="card pub-section" id="conferences">
        <div class="section-head">
          <h3>Peer-Reviewed Conference Proceedings</h3>
          <span class="section-badge">selected list</span>
        </div>

        <ul class="pub-list">
          <li class="pub-item">
            [1] <span class="me">M. Elsharkawy</span>, Abdelhalim, I., Ghazal, M., Haq, M.Z., Haq, R., Mahmoud, A., Sandhu, H.S., Thanos, A. and El-Baz, A., 2025.
            <span class="pub-title">TransNetOCT: An Efficient Transformer-Based Model for 3D-OCT Segmentation Using Prior Shape.</span>
            In <em>International Conference on Pattern Recognition</em> (pp. 301–315). Springer Nature Switzerland.
          </li>

          <li class="pub-item">
            [2] Abdelhalim, I., <span class="me">M. Elsharkawy</span>, Nadmid, N., Ghazal, M., Mahmoud, A. and El-Baz, A., 2024, December.
            <span class="pub-title">MUMR: Mask-UnMask Regions Framework for AMD Grades Classification Based on Inter-regional Interactions.</span>
            In <em>International Conference on Pattern Recognition</em> (pp. 213–223). Springer Nature Switzerland.
          </li>

          <li class="pub-item">
            [3] Abdelhalim, I., Almalki, Y., Abbas, A., <span class="me">M. Elsharkawy</span>, Karam, R., Alduraibi, S., Ghazal, M., Mahmoud, A., Contractor, S. and El-Baz, A., 2024, May.
            <span class="pub-title">Twoviewdensity-Pvt: A Vision Transformer System for Accurate Bi-Rads Classification in Breast Cancer Grading From Mammogram Images.</span>
            In <em>2024 IEEE International Symposium on Biomedical Imaging (ISBI)</em> (pp. 1–4). IEEE.
          </li>
        </ul>
      </section>

      <!-- Book Chapters -->
      <section class="card pub-section" id="chapters">
        <div class="section-head">
          <h3>Book Chapters</h3>
          <span class="section-badge">2 items</span>
        </div>

        <ul class="pub-list">
          <li class="pub-item">
            [1] <span class="me">Elsharkawy, M.</span>, Soliman, A., Mahmoud, A., Ghazal, M., Alhalabi, M., El-Baz, A., Thanos, A., Sandhu, H.S., Giridharan, G. and El-Baz, A., 2023.
            <span class="pub-title">Prevention of age-related macular degeneration disease: current strategies and future directions.</span>
            In <em>Photo Acoustic and Optical Coherence Tomography Imaging, Volume 1: Diabetic retinopathy</em> (pp. 13-1). IOP Publishing.
          </li>

          <li class="pub-item">
            [2] <span class="me">Elsharkawy, M.</span>, Sharafeldeen, A., Soliman, A., Khalifa, F., Mahmoud, A., El-Baz, A., Ghazal, M., Sandhu, H.S. and El-Baz, A., 2023.
            <span class="pub-title">Early identification of diabetic retinopathy through a computer-assisted diagnostic system and a higher-order spatial appearance model of 3D-OCT.</span>
            In <em>Photo Acoustic and Optical Coherence Tomography Imaging, Volume 1: Diabetic retinopathy</em> (pp. 12-1). IOP Publishing.
          </li>
        </ul>
      </section>

      <!-- Abstracts -->
      <section class="card pub-section" id="abstracts">
        <div class="section-head">
          <h3>Abstracts in Published Proceedings</h3>
          <span class="section-badge">selected list</span>
        </div>

        <ul class="pub-list">
          <li class="pub-item">
            [1] Haq, M.Z., El-Den, N.N., <span class="me">Elsharkawy, M.</span>, Ghazal, M., Mahmoud, A., Sandhu, H., Mahdi, H. and El-Baz, A., 2024.
            <span class="pub-title">A Novel AI Approach with Scale-Adaptive Integrated BiT-Autoencoder for Diagnosing Age-Related Macular Degeneration Using Fundus Images.</span>
            <em>Investigative Ophthalmology & Visual Science</em>, 65(7), pp.5663–5663.
          </li>
        </ul>
      </section>

      <p class="note">
        <strong>Note:</strong> For a complete overview, please see my
        <a href="https://scholar.google.com/citations?user=IknnHU4AAAAJ&hl=en" target="_blank" rel="noopener">Google Scholar</a>
        and
        <a href="https://publons.com/researcher/2993425/mohamed-elsharkawy/" target="_blank" rel="noopener">Web of Science</a>.
      </p>

    </main>

    <!-- SIDEBAR -->
    <aside class="card sidebar">
      <h2>Quick Navigation</h2>
      <p class="mini">
        Jump to a section, or use the external profiles for the most up-to-date list.
      </p>

      <div class="side-links">
        <a class="side-btn" href="#patents">
          Patents & Disclosures
          <small>U.S. patent application(s)</small>
        </a>
        <a class="side-btn" href="#journals">
          Journal Articles
          <small>Peer-reviewed journals</small>
        </a>
        <a class="side-btn" href="#conferences">
          Conference Papers
          <small>ICPR / ISBI / ICIP …</small>
        </a>
        <a class="side-btn" href="#chapters">
          Book Chapters
          <small>IOP Publishing chapters</small>
        </a>
        <a class="side-btn" href="#abstracts">
          Abstracts
          <small>IOVS / BMES …</small>
        </a>

        <a class="side-btn" href="https://scholar.google.com/citations?user=IknnHU4AAAAJ&hl=en" target="_blank" rel="noopener">
          Google Scholar
          <small>Most complete & updated</small>
        </a>
      </div>
    </aside>

  </div>
</div>
