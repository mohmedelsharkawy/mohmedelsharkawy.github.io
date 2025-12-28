---
layout: default
title: "Publications"
permalink: /publications/
---

<style>
/* ============================
   Publications Page – Teal/Orange Theme
   ============================ */

:root{
  --bg:#ffffff;
  --text:#0f172a;
  --muted:#475569;

  --card:rgba(255,255,255,0.92);
  --border:rgba(15,23,42,0.10);

  --shadow:0 14px 34px rgba(0,0,0,0.09);
  --shadow-sm:0 7px 18px rgba(0,0,0,0.08);
  --radius:16px;

  /* NEW COLORS */
  --accent1:#14b8a6; /* teal */
  --accent2:#f97316; /* orange */
  --accent3:#6366f1; /* indigo */
  --link:#0ea5e9;

  --pill-bg:rgba(15,23,42,0.04);
  --pill-border:rgba(15,23,42,0.10);
}

@media (prefers-color-scheme: dark){
  :root{
    --bg:#0b1220;
    --text:#e5e7eb;
    --muted:#a1a1aa;

    --card:rgba(17,24,39,0.74);
    --border:rgba(229,231,235,0.12);

    --shadow:0 18px 48px rgba(0,0,0,0.40);
    --shadow-sm:0 12px 28px rgba(0,0,0,0.38);

    --link:#7dd3fc;

    --pill-bg:rgba(229,231,235,0.07);
    --pill-border:rgba(229,231,235,0.12);
  }
}

.pub-wrap{
  max-width: 1100px;
  margin: 0 auto;
  padding: 18px 14px 34px;
  color: var(--text);
}

.pub-wrap a{ color: var(--link); text-decoration: none; }
.pub-wrap a:hover{ text-decoration: underline; }

/* HERO */
.pub-hero{
  position: relative;
  overflow: hidden;
  border-radius: calc(var(--radius) + 8px);
  padding: 28px 18px;
  border: 1px solid var(--border);
  box-shadow: var(--shadow);
  background:
    radial-gradient(1100px 520px at 15% 10%, color-mix(in srgb, var(--accent1) 55%, transparent), transparent 60%),
    radial-gradient(900px 480px at 85% 20%, color-mix(in srgb, var(--accent2) 45%, transparent), transparent 60%),
    radial-gradient(900px 480px at 60% 120%, color-mix(in srgb, var(--accent3) 40%, transparent), transparent 60%),
    linear-gradient(135deg, rgba(20,184,166,0.18), rgba(249,115,22,0.12));
}

.pub-hero:before{
  content:"";
  position:absolute;
  inset:0;
  background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='180' height='180'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='.9' numOctaves='3' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='180' height='180' filter='url(%23n)' opacity='.10'/%3E%3C/svg%3E");
  opacity: .18;
  pointer-events:none;
}

.pub-hero-inner{
  position: relative;
  text-align: center;
  display: grid;
  gap: 10px;
}

.pub-hero h1{
  margin: 0;
  font-size: 2.25rem;
  letter-spacing: -0.02em;
  line-height: 1.12;
  color: #ffffff;
}

.pub-hero p{
  margin: 0;
  color: rgba(255,255,255,0.92);
  font-size: 1.05rem;
  line-height: 1.65;
}

.pub-chips{
  margin-top: 14px;
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
  justify-content: center;
}

.chip{
  display:inline-flex;
  align-items:center;
  gap:8px;
  padding: 8px 12px;
  border-radius: 999px;
  border: 1px solid rgba(255,255,255,0.26);
  background: rgba(255,255,255,0.13);
  color: rgba(255,255,255,0.95);
  font-size: 0.92rem;
  backdrop-filter: blur(8px);
}

/* Layout */
.pub-row{
  display: grid;
  grid-template-columns: 1fr 320px;
  gap: 16px;
  margin-top: 16px;
}
@media (max-width: 980px){ .pub-row{ grid-template-columns: 1fr; } }

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
  font-size: 1.05rem;
  letter-spacing: -0.01em;
}

/* Section head */
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
  font-size: 1.18rem;
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

/* Venue subheaders */
.venue{
  margin: 14px 0 10px;
  padding-left: 12px;
  border-left: 4px solid var(--accent1);
  font-size: 1.02rem;
  letter-spacing: -0.01em;
}
.venue.orange{ border-left-color: var(--accent2); }
.venue.indigo{ border-left-color: var(--accent3); }
.venue.gray{ border-left-color: rgba(100,116,139,0.7); }

.venue small{
  color: var(--muted);
  font-weight: 600;
  margin-left: 6px;
}

/* Publication items */
.pub-list{
  list-style:none;
  padding-left:0;
  margin:0;
  display:grid;
  gap: 12px;
}

.pub-item{
  padding: 12px 12px;
  border-radius: 14px;
  border: 1px solid var(--border);
  background: rgba(127,127,127,0.04);
}
.pub-item:hover{
  border-color: color-mix(in srgb, var(--accent1) 35%, var(--border));
}

.pub-title{ font-weight: 800; }

/* Your name highlight */
.me{
  font-weight: 900;
  color: color-mix(in srgb, var(--accent1) 75%, var(--text));
  text-decoration: underline;
  text-decoration-thickness: 2px;
  text-underline-offset: 3px;
}

/* First-author badge */
.badge{
  display:inline-flex;
  align-items:center;
  gap:8px;
  padding: 5px 10px;
  border-radius: 999px;
  border: 1px solid var(--pill-border);
  background: var(--pill-bg);
  font-size: 0.85rem;
  color: var(--text);
  margin-left: 8px;
}
.badge.fa{
  border-color: color-mix(in srgb, var(--accent2) 40%, var(--pill-border));
}

/* Actions */
.pub-actions{
  margin-top: 8px;
  display:flex;
  flex-wrap: wrap;
  gap: 8px;
}
.pill{
  display:inline-flex;
  align-items:center;
  gap:8px;
  padding: 6px 10px;
  border-radius: 999px;
  border: 1px solid var(--pill-border);
  background: var(--card);
  box-shadow: var(--shadow-sm);
  font-size: 0.88rem;
  text-decoration: none !important;
  color: var(--text) !important;
}
.pill:hover{ border-color: color-mix(in srgb, var(--accent3) 30%, var(--pill-border)); }

/* Sidebar */
.sidebar .mini{
  color: var(--muted);
  line-height: 1.6;
  margin: 0 0 12px;
}
.side-links{ display:grid; gap: 10px; }
.side-btn{
  display:block;
  padding: 10px 12px;
  border-radius: 12px;
  border: 1px solid var(--border);
  background: var(--card);
  box-shadow: var(--shadow-sm);
  text-decoration:none !important;
  color: var(--text) !important;
  transition: transform .2s ease, box-shadow .2s ease, border-color .2s ease;
}
.side-btn:hover{
  transform: translateY(-2px);
  box-shadow: var(--shadow);
  border-color: color-mix(in srgb, var(--accent1) 35%, var(--border));
}
.side-btn small{ display:block; color: var(--muted); margin-top: 3px; }

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
        Selected peer-reviewed journal articles, conference papers, book chapters, and abstracts.
        For the most up-to-date record, please see Google Scholar.
      </p>
      <div class="pub-chips" aria-label="Highlights">
        <span class="chip">Medical Imaging AI</span>
        <span class="chip">Fundus / OCT / OCTA</span>
        <span class="chip">Classification & Segmentation</span>
        <span class="chip">Explainable AI (XAI)</span>
        <span class="chip">First-author highlights</span>
      </div>
    </div>
  </section>

  <div class="pub-row">

    <!-- MAIN -->
    <main>

      <!-- FIRST-AUTHOR HIGHLIGHTS (ORDERED AS REQUESTED) -->
      <section class="card pub-section" id="first-author">
        <div class="section-head">
          <h3>First-Author Journal Highlights</h3>
          <span class="section-badge">ordered by venue</span>
        </div>

        <!-- 1) JBHI -->
        <div class="venue indigo">IEEE JBHI <small>(first author)</small></div>
        <ul class="pub-list">
          <li class="pub-item">
            <span class="me">Elsharkawy, M.</span>, Sharafeldeen A., Khalifa, F., Soliman, A., Elnakib, A., Ghazal, M., Sewelam, A., Thanos, A., Sandhu, H.S., El-Baz, A.
            <span class="pub-title">A Clinically Explainable AI-Based Grading System for Age-Related Macular Degeneration Using Optical Coherence Tomography.</span>
            <em>IEEE Journal of Biomedical and Health Informatics</em>, 2024.
            <span class="badge fa">First Author</span>
            <div class="pub-actions">
              <a class="pill" href="https://doi.org/10.1109/JBHI.2024.3355329" target="_blank" rel="noopener">DOI</a>
            </div>
          </li>
        </ul>

        <!-- 2) Diagnostics -->
        <div class="venue orange">Diagnostics <small>(first author)</small></div>
        <ul class="pub-list">
          <li class="pub-item">
            <span class="me">Elsharkawy, M.</span>, Sharafeldeen, A., Soliman, A., Khalifa, F., Ghazal, M., El-Daydamony, E., Atwan, A., Sandhu, H.S., El-Baz, A.
            <span class="pub-title">A Novel Computer-Aided Diagnostic System for Early Detection of Diabetic Retinopathy Using 3D-OCT Higher-Order Spatial Appearance Model.</span>
            <em>Diagnostics</em>, 12(2), 461, 2022.
            <span class="badge fa">First Author</span>
          </li>
          <li class="pub-item">
            <span class="me">Elsharkawy, M.</span>, Elrazzaz, M., Ghazal, M., Alhalabi, M., Soliman, A., Mahmoud, A., et al., El-Baz, A.
            <span class="pub-title">Role of Optical Coherence Tomography Imaging in Predicting Progression of Age-Related Macular Disease: A Survey.</span>
            <em>Diagnostics</em>, 11(12), 2313, 2021.
            <span class="badge fa">First Author</span>
          </li>
        </ul>

        <!-- 3) IEEE Access -->
        <div class="venue">IEEE Access <small>(co-author listed in CV)</small></div>
        <ul class="pub-list">
          <li class="pub-item">
            Abdelhalim, I., Nadmid, N., <span class="me">Elsharkawy, M.</span>, Ghazal, M., Mahmoud, A., El-Baz, A.
            <span class="pub-title">Mask-UnMask Regions (MUMR) Framework for Classifying AMD Grades Using Inter-Regional Interaction Analysis.</span>
            <em>IEEE Access</em>, 2025.
            <span class="badge">Co-author</span>
          </li>
          <li class="pub-item">
            El-Den, N.N., <span class="me">Elsharkawy, M.</span>, Saleh, I., et al.
            <span class="pub-title">Seg-Swin: A Dual-Attention Transformer Model for Advanced AMD Classification and Lesion Detection Using Color Fundus Imaging.</span>
            <em>IEEE Access</em>, 2025.
            <span class="badge">Co-author</span>
          </li>
        </ul>

        <!-- 4) Scientific Reports -->
        <div class="venue gray">Scientific Reports <small>(first author)</small></div>
        <ul class="pub-list">
          <li class="pub-item">
            <span class="me">Elsharkawy, M.</span>, Sharafeldeen, A., Taher, F., Shalaby, A., Soliman, A., Mahmoud, A., et al., El-Baz, A.
            <span class="pub-title">Early Assessment of Lung Function in Coronavirus Patients Using Invariant Markers from Chest X-Rays Images.</span>
            <em>Scientific Reports</em>, 11(1), 2021.
            <span class="badge fa">First Author</span>
          </li>
        </ul>
      </section>

      <!-- Patents -->
      <section class="card pub-section" id="patents">
        <div class="section-head">
          <h3>Patents and Disclosures</h3>
          <span class="section-badge">1 item</span>
        </div>
        <ul class="pub-list">
          <li class="pub-item">
            A. S. El-Baz, A. Shalaby, <span class="me">M. Elsharkawy</span>, et al.<br/>
            <em>"ASSESSMENT OF PULMONARY FUNCTION IN CORONAVIRUS PATIENT,"</em> U.S. Patent 12,217,432 (Feb. 2025).
          </li>
        </ul>
      </section>

      <!-- FULL JOURNAL LIST (keep extending) -->
      <section class="card pub-section" id="journals">
        <div class="section-head">
          <h3>Peer-Reviewed Journal Articles</h3>
          <span class="section-badge">extendable list</span>
        </div>

        <p class="note" style="margin-top:0;">
          First-author papers are visually emphasized by underlining my name.
        </p>

        <ul class="pub-list">
          <!-- You can paste your full journal list here exactly like before -->
          <li class="pub-item">
            El-Den, N.N., <span class="me">Elsharkawy, M.</span>, Saleh, I., Ghazal, M., Khalil, A., Haq, M.Z., Sewelam, A., Mahdi, H., El-Baz, A., 2024.
            <span class="pub-title">AI-based methods for detecting and classifying age-related macular degeneration: a comprehensive review.</span>
            <em>Artificial Intelligence Review</em>, 57(9), 237.
          </li>
          <!-- ... add the rest ... -->
        </ul>
      </section>

      <p class="note">
        <strong>Note:</strong> For the complete and updated record, please see my
        <a href="https://scholar.google.com/citations?user=IknnHU4AAAAJ&hl=en" target="_blank" rel="noopener">Google Scholar</a>
        and
        <a href="https://publons.com/researcher/2993425/mohamed-elsharkawy/" target="_blank" rel="noopener">Web of Science</a>.
      </p>

    </main>

    <!-- SIDEBAR -->
    <aside class="card sidebar">
      <h2>Quick Navigation</h2>
      <p class="mini">
        Jump to a section, or use external profiles for the most up-to-date list.
      </p>

      <div class="side-links">
        <a class="side-btn" href="#first-author">First-Author Highlights
          <small>JBHI → Diagnostics → Access → Sci Rep</small>
        </a>
        <a class="side-btn" href="#patents">Patents & Disclosures
          <small>U.S. patent</small>
        </a>
        <a class="side-btn" href="#journals">Journal Articles
          <small>Full list (extendable)</small>
        </a>

        <a class="side-btn" href="https://scholar.google.com/citations?user=IknnHU4AAAAJ&hl=en" target="_blank" rel="noopener">
          Google Scholar
          <small>Most complete & updated</small>
        </a>
      </div>
    </aside>

  </div>
</div>
