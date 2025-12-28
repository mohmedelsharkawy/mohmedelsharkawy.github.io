---
layout: default
title: "Publications"
permalink: /publications/
---

<style>
/* ============================
   Publications – Modern, Fast, Filterable
   Theme: Teal / Orange / Indigo
   ============================ */
:root{
  --text:#0f172a;
  --muted:#475569;

  --card:rgba(255,255,255,0.92);
  --border:rgba(15,23,42,0.10);
  --shadow:0 14px 34px rgba(0,0,0,0.09);
  --shadow-sm:0 7px 18px rgba(0,0,0,0.08);
  --radius:16px;

  --teal:#14b8a6;
  --orange:#f97316;
  --indigo:#6366f1;
  --link:#0ea5e9;

  --chip-bg:rgba(15,23,42,0.05);
  --chip-border:rgba(15,23,42,0.10);
}
@media (prefers-color-scheme: dark){
  :root{
    --text:#e5e7eb;
    --muted:#a1a1aa;

    --card:rgba(17,24,39,0.74);
    --border:rgba(229,231,235,0.12);
    --shadow:0 18px 48px rgba(0,0,0,0.40);
    --shadow-sm:0 12px 28px rgba(0,0,0,0.38);
    --link:#7dd3fc;

    --chip-bg:rgba(229,231,235,0.07);
    --chip-border:rgba(229,231,235,0.12);
  }
}

.pub-wrap{
  max-width: 1120px;
  margin: 0 auto;
  padding: 18px 14px 34px;
  color: var(--text);
}
.pub-wrap a{ color: var(--link); text-decoration:none; }
.pub-wrap a:hover{ text-decoration:underline; }

/* HERO */
.hero{
  position: relative;
  overflow: hidden;
  border-radius: calc(var(--radius) + 10px);
  padding: 28px 18px;
  border: 1px solid var(--border);
  box-shadow: var(--shadow);
  background:
    radial-gradient(1100px 520px at 15% 10%, rgba(20,184,166,0.42), transparent 60%),
    radial-gradient(900px 480px at 85% 20%, rgba(249,115,22,0.30), transparent 60%),
    radial-gradient(900px 480px at 60% 120%, rgba(99,102,241,0.28), transparent 60%),
    linear-gradient(135deg, rgba(20,184,166,0.12), rgba(249,115,22,0.10));
}
.hero:before{
  content:"";
  position:absolute; inset:0;
  background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='180' height='180'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='.9' numOctaves='3' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='180' height='180' filter='url(%23n)' opacity='.10'/%3E%3C/svg%3E");
  opacity: .16; pointer-events:none;
}
.hero-inner{ position:relative; text-align:center; display:grid; gap:10px; }
.hero h1{ margin:0; font-size:2.15rem; letter-spacing:-0.02em; line-height:1.1; color:#fff; }
.hero p{ margin:0; color:rgba(255,255,255,0.93); font-size:1.05rem; line-height:1.65; }

.actions{
  margin-top: 10px;
  display:flex; flex-wrap:wrap; gap:10px;
  justify-content:center;
}
.btn{
  display:inline-flex; align-items:center; gap:10px;
  padding: 10px 14px;
  border-radius: 999px;
  border: 1px solid rgba(255,255,255,0.26);
  background: rgba(255,255,255,0.13);
  color: rgba(255,255,255,0.95) !important;
  text-decoration:none !important;
  font-weight:800;
  backdrop-filter: blur(8px);
  transition: transform .2s ease, box-shadow .2s ease;
}
.btn:hover{ transform: translateY(-2px); box-shadow: var(--shadow); }

/* FILTER BAR */
.filterbar{
  margin-top: 14px;
  display:flex;
  flex-wrap:wrap;
  gap:10px;
  justify-content:center;
}
.input, .select{
  border-radius: 999px;
  border: 1px solid rgba(255,255,255,0.28);
  background: rgba(255,255,255,0.14);
  color: rgba(255,255,255,0.95);
  padding: 10px 12px;
  font-weight: 700;
  outline: none;
  backdrop-filter: blur(8px);
}
.input::placeholder{ color: rgba(255,255,255,0.85); }
.select option{ color:#111; }

/* LAYOUT */
.grid{
  display:grid;
  grid-template-columns: 1fr 1fr;
  gap: 16px;
  margin-top: 16px;
}
@media (max-width: 980px){ .grid{ grid-template-columns: 1fr; } }

/* CARDS */
.card{
  background: var(--card);
  border: 1px solid var(--border);
  border-radius: var(--radius);
  box-shadow: var(--shadow-sm);
  padding: 16px;
  backdrop-filter: blur(8px);
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
.section-head h2{ margin:0; font-size: 1.18rem; letter-spacing:-0.01em; }
.badge{
  font-size: 0.85rem;
  color: var(--muted);
  padding: 6px 10px;
  border-radius: 999px;
  border: 1px solid var(--border);
  background: rgba(127,127,127,0.06);
}

/* LIST ITEMS */
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
.pub-item:hover{ border-color: rgba(20,184,166,0.35); }

.tagrow{
  margin-top: 10px;
  display:flex;
  flex-wrap:wrap;
  gap: 8px;
}
.tag{
  display:inline-flex;
  align-items:center;
  gap: 8px;
  padding: 6px 10px;
  border-radius: 999px;
  border: 1px solid var(--chip-border);
  background: var(--chip-bg);
  font-size: 0.86rem;
  color: var(--text);
}
.tag.fa{ border-color: color-mix(in srgb, var(--orange) 42%, var(--chip-border)); }
.tag.j{ border-color: color-mix(in srgb, var(--indigo) 42%, var(--chip-border)); }
.tag.c{ border-color: color-mix(in srgb, var(--teal) 50%, var(--chip-border)); }
.tag.b{ border-color: rgba(100,116,139,0.35); }

.me{
  font-weight: 900;
  color: color-mix(in srgb, var(--teal) 75%, var(--text));
  text-decoration: underline;
  text-decoration-thickness: 2px;
  text-underline-offset: 3px;
}

.note{
  margin-top: 14px;
  color: var(--muted);
  line-height: 1.7;
}

/* DETAILS */
details{
  border: 1px solid var(--border);
  border-radius: 14px;
  background: rgba(127,127,127,0.04);
  padding: 10px 12px;
  margin-top: 12px;
}
details summary{
  cursor: pointer;
  font-weight: 900;
  list-style: none;
}
details summary::-webkit-details-marker{ display:none; }
details summary:after{
  content:"▾";
  float:right;
  color: var(--muted);
}
details[open] summary:after{ content:"▴"; }
</style>

<div class="pub-wrap">

  <!-- HERO -->
  <section class="hero">
    <div class="hero-inner">
      <h1>Publications</h1>
      <p>
        A curated, high-impact selection of my work. <strong>First-author papers are emphasized</strong>.
        (Full record is on Google Scholar / CV.)
      </p>

      <div class="actions">
        <a class="btn" href="/assets/files/elsharkawycv.pdf" target="_blank" rel="noopener">Download CV (PDF)</a>
        <a class="btn" href="https://scholar.google.com/citations?user=IknnHU4AAAAJ&hl=en" target="_blank" rel="noopener">Google Scholar</a>
        <a class="btn" href="/cv/">CV</a>
      </div>

      <div class="filterbar">
        <input id="pubSearch" class="input" type="text" placeholder="Search (e.g., OCT, AMD, transformer, review)..." />
        <select id="yearFilter" class="select">
          <option value="all">All years</option>
          <option value="2025">2025</option>
          <option value="2024">2024</option>
          <option value="2023">2023</option>
          <option value="2022">2022</option>
          <option value="2021">2021</option>
          <option value="2020">2020</option>
        </select>
        <select id="typeFilter" class="select">
          <option value="all">All types</option>
          <option value="journal">Journal</option>
          <option value="conference">Conference</option>
          <option value="review">Review</option>
          <option value="chapter">Book chapter</option>
          <option value="patent">Patent</option>
          <option value="abstract">Abstract</option>
        </select>
        <label style="display:flex; align-items:center; gap:8px; color:#fff; font-weight:800;">
          <input id="firstOnly" type="checkbox" />
          First-author only
        </label>
      </div>
    </div>
  </section>

  <div class="grid">

    <!-- =========================
         FIRST-AUTHOR JOURNALS (ORDER YOU REQUESTED)
         JBHI → Diagnostics → IEEE Access → Scientific Reports → (then Sensors)
         ========================= -->
    <section class="card" id="first-journals">
      <div class="section-head">
        <h2>Journal Articles (First Author • Selected)</h2>
        <span class="badge">priority order</span>
      </div>

      <ul class="pub-list">

        <!-- JBHI 2024 -->
        <li class="pub-item" data-year="2024" data-type="journal" data-first="yes">
          <div>
            <span class="me">Elsharkawy, M.</span>, Sharafeldeen A., Khalifa F., Soliman A., et al.
            <strong>A clinically explainable AI-based grading system for age-related macular degeneration using optical coherence tomography.</strong>
            <em>IEEE Journal of Biomedical and Health Informatics (JBHI)</em>, 28(4):2079–2090, 2024.
          </div>
          <div class="tagrow">
            <span class="tag fa">First Author</span>
            <span class="tag j">Top Journal</span>
            <span class="tag">OCT</span>
            <a class="tag" href="https://doi.org/10.1109/JBHI.2024.3355329" target="_blank" rel="noopener">DOI</a>
          </div>
        </li>

        <!-- Diagnostics 2022 -->
        <li class="pub-item" data-year="2022" data-type="journal" data-first="yes">
          <div>
            <span class="me">Elsharkawy, M.</span>, Sharafeldeen A., Soliman A., Khalifa F., et al.
            <strong>A novel computer-aided diagnostic system for early detection of diabetic retinopathy using 3D-OCT higher-order spatial appearance model.</strong>
            <em>Diagnostics</em>, 12(2):461, 2022.
          </div>
          <div class="tagrow">
            <span class="tag fa">First Author</span>
            <span class="tag j">Journal</span>
            <span class="tag">3D-OCT</span>
            <span class="tag">DR</span>
          </div>
        </li>

        <!-- Diagnostics 2021 (Survey) -->
        <li class="pub-item" data-year="2021" data-type="journal" data-first="yes">
          <div>
            <span class="me">Elsharkawy, M.</span>, Elrazzaz M., Ghazal M., et al.
            <strong>Role of optical coherence tomography imaging in predicting progression of age-related macular disease: A survey.</strong>
            <em>Diagnostics</em>, 11(12):2313, 2021.
          </div>
          <div class="tagrow">
            <span class="tag fa">First Author</span>
            <span class="tag j">Journal</span>
            <span class="tag">Survey</span>
            <span class="tag">AMD</span>
          </div>
        </li>

        <!-- IEEE Access 2025 -->
        <li class="pub-item" data-year="2025" data-type="journal" data-first="yes">
          <div>
            <span class="me">Elsharkawy, M.</span>, Abdelhalim I., Mahmoud A., Gamal A., et al.
            <strong>Fused-AETNet: A variational transformer-based framework for diabetic retinopathy classification using OCT biomarkers.</strong>
            <em>IEEE Access</em>, 2025.
          </div>
          <div class="tagrow">
            <span class="tag fa">First Author</span>
            <span class="tag j">Journal</span>
            <span class="tag">Transformer</span>
            <span class="tag">OCT biomarkers</span>
          </div>
        </li>

        <!-- Scientific Reports 2021 -->
        <li class="pub-item" data-year="2021" data-type="journal" data-first="yes">
          <div>
            <span class="me">Elsharkawy, M.</span>, Sharafeldeen A., Taher F., et al.
            <strong>Early assessment of lung function in coronavirus patients using invariant markers from chest X-rays images.</strong>
            <em>Scientific Reports</em>, 11(1):12095, 2021.
          </div>
          <div class="tagrow">
            <span class="tag fa">First Author</span>
            <span class="tag j">High-Visibility Journal</span>
            <span class="tag">CXR</span>
            <span class="tag">COVID-19</span>
          </div>
        </li>

        <!-- Sensors 2022 -->
        <li class="pub-item" data-year="2022" data-type="journal" data-first="yes">
          <div>
            <span class="me">Elsharkawy, M.</span>, Elrazzaz M., Sharafeldeen A., et al.
            <strong>The role of different retinal imaging modalities in predicting progression of diabetic retinopathy: A survey.</strong>
            <em>Sensors</em>, 22(9):3490, 2022.
          </div>
          <div class="tagrow">
            <span class="tag fa">First Author</span>
            <span class="tag j">Journal</span>
            <span class="tag">Survey</span>
            <span class="tag">DR</span>
          </div>
        </li>

      </ul>

      <p class="note">
        (This section is intentionally “selected + ordered”. The complete list is on Google Scholar.)
      </p>
    </section>

    <!-- =========================
         FIRST-AUTHOR CONFERENCES (SELECTED)
         ========================= -->
    <section class="card" id="first-conferences">
      <div class="section-head">
        <h2>Conference Proceedings (First Author • Selected)</h2>
        <span class="badge">top venues first</span>
      </div>

      <ul class="pub-list">

        <!-- ICIP 2025 CrossDR -->
        <li class="pub-item" data-year="2025" data-type="conference" data-first="yes">
          <div>
            <span class="me">Elsharkawy, M.</span>, Abdelhalim I., Taher F., et al.
            <strong>CrossDR: Bridging 2D and 3D features for diabetic retinopathy classification using context-aware cross-attention.</strong>
            <em>IEEE International Conference on Image Processing (ICIP)</em>, 2025.
          </div>
          <div class="tagrow">
            <span class="tag fa">First Author</span>
            <span class="tag c">Major IEEE Conf</span>
            <span class="tag">Cross-attention</span>
            <span class="tag">2D+3D</span>
          </div>
        </li>

        <!-- ICPR 2024 TransNetOCT -->
        <li class="pub-item" data-year="2024" data-type="conference" data-first="yes">
          <div>
            <span class="me">Elsharkawy, M.</span>, Abdelhalim I., Ghazal M., et al.
            <strong>TransNetOCT: An efficient transformer-based model for 3D-OCT segmentation using prior shape.</strong>
            <em>International Conference on Pattern Recognition (ICPR)</em>, 2024.
          </div>
          <div class="tagrow">
            <span class="tag fa">First Author</span>
            <span class="tag c">Major PR Conf</span>
            <span class="tag">Segmentation</span>
            <span class="tag">3D-OCT</span>
          </div>
        </li>

        <!-- ISBI 2025 ISGM-DR -->
        <li class="pub-item" data-year="2025" data-type="conference" data-first="yes">
          <div>
            <span class="me">Elsharkawy, M.</span>, Abdelhalim I., Ghazal M., Mahmoud A., Sandhu H.S., El-Baz A.
            <strong>ISGM-DR: Important slice-guided model for diabetic retinopathy diagnosis using 3D-OCT images.</strong>
            <em>IEEE ISBI</em>, 2025.
          </div>
          <div class="tagrow">
            <span class="tag fa">First Author</span>
            <span class="tag c">Top Biomedical Imaging</span>
            <span class="tag">3D-OCT</span>
          </div>
        </li>

        <!-- ISBI 2025 OCT-Trans -->
        <li class="pub-item" data-year="2025" data-type="conference" data-first="yes">
          <div>
            <span class="me">Elsharkawy, M.</span>, Abdelhalim I., Ghazal M., Mahmoud A., et al.
            <strong>OCT-Trans: A novel transformer backbone with multimodal feature extraction in OCT-based retinal disease classification.</strong>
            <em>IEEE ISBI</em>, 2025.
          </div>
          <div class="tagrow">
            <span class="tag fa">First Author</span>
            <span class="tag c">Top Biomedical Imaging</span>
            <span class="tag">Transformer</span>
            <span class="tag">OCT</span>
          </div>
        </li>

        <!-- ISBI 2022 -->
        <li class="pub-item" data-year="2022" data-type="conference" data-first="yes">
          <div>
            <span class="me">Elsharkawy, M.</span>, Sharafeldeen A., Soliman A., et al.
            <strong>Diabetic retinopathy diagnostic CAD system using 3D-OCT higher-order spatial appearance model.</strong>
            <em>IEEE ISBI</em>, 2022.
          </div>
          <div class="tagrow">
            <span class="tag fa">First Author</span>
            <span class="tag c">Top Biomedical Imaging</span>
            <span class="tag">3D-OCT</span>
          </div>
        </li>

      </ul>
    </section>

    <!-- =========================
         REVIEW PAPERS (HIGH-IMPACT)
         ========================= -->
    <section class="card" id="reviews">
      <div class="section-head">
        <h2>Review Papers (Selected)</h2>
        <span class="badge">high-impact</span>
      </div>

      <ul class="pub-list">

        <li class="pub-item" data-year="2025" data-type="review" data-first="no">
          <div>
            Saleh I., El-Den N.N., <span class="me">Elsharkawy, M.</span>, et al.
            <strong>AI-based methods for diagnosing and grading diabetic retinopathy: A comprehensive review.</strong>
            <em>Artificial Intelligence in Medicine</em>, 2025.
          </div>
          <div class="tagrow">
            <span class="tag j">Top Review Venue</span>
            <span class="tag">DR</span>
            <span class="tag">Survey</span>
          </div>
        </li>

        <li class="pub-item" data-year="2024" data-type="review" data-first="no">
          <div>
            El-Den N.N., <span class="me">Elsharkawy, M.</span>, Saleh I., et al.
            <strong>AI-based methods for detecting and classifying age-related macular degeneration: A comprehensive review.</strong>
            <em>Artificial Intelligence Review</em>, 57(9):237, 2024.
          </div>
          <div class="tagrow">
            <span class="tag j">High-Impact Review</span>
            <span class="tag">AMD</span>
            <span class="tag">Survey</span>
          </div>
        </li>

      </ul>
    </section>

    <!-- =========================
         BOOK CHAPTERS (FIRST AUTHOR)
         ========================= -->
    <section class="card" id="chapters">
      <div class="section-head">
        <h2>Book Chapters (First Author)</h2>
        <span class="badge">IOP Publishing</span>
      </div>

      <ul class="pub-list">

        <li class="pub-item" data-year="2023" data-type="chapter" data-first="yes">
          <div>
            <span class="me">Elsharkawy, M.</span>, Sharafeldeen A., Soliman A., et al.
            <strong>Early identification of diabetic retinopathy through a computer-assisted diagnostic system and a higher-order spatial appearance model of 3D-OCT.</strong>
            <em>Photo Acoustic and Optical Coherence Tomography Imaging (Vol. 1)</em>, IOP Publishing, 2023.
          </div>
          <div class="tagrow">
            <span class="tag fa">First Author</span>
            <span class="tag b">Book Chapter</span>
            <span class="tag">DR</span>
            <span class="tag">3D-OCT</span>
          </div>
        </li>

        <li class="pub-item" data-year="2023" data-type="chapter" data-first="yes">
          <div>
            <span class="me">Elsharkawy, M.</span>, Soliman A., Mahmoud A., et al.
            <strong>Prevention of age-related macular degeneration disease: current strategies and future directions.</strong>
            <em>Photo Acoustic and Optical Coherence Tomography Imaging (Vol. 1)</em>, IOP Publishing, 2023.
          </div>
          <div class="tagrow">
            <span class="tag fa">First Author</span>
            <span class="tag b">Book Chapter</span>
            <span class="tag">AMD</span>
          </div>
        </li>

      </ul>
    </section>

    <!-- =========================
         PATENT
         ========================= -->
    <section class="card" id="patent">
      <div class="section-head">
        <h2>Patent</h2>
        <span class="badge">selected</span>
      </div>

      <ul class="pub-list">
        <li class="pub-item" data-year="2025" data-type="patent" data-first="no">
          <div>
            El-Baz A.S., Shalaby A., <span class="me">Elsharkawy, M.</span>, et al.
            <strong>Assessment of pulmonary function in coronavirus patients.</strong>
            <em>US Patent 12,217,432</em>, Feb 2025.
          </div>
          <div class="tagrow">
            <span class="tag b">Patent</span>
            <span class="tag">Inventor</span>
          </div>
        </li>
      </ul>

      <p class="note">
        If you want: I can add the patent number as a clickable link to the USPTO page.
      </p>
    </section>

    <!-- =========================
         SELECTED CO-AUTHORED HIGH-IMPACT (COLLAPSIBLE)
         ========================= -->
    <section class="card" id="coauthored">
      <div class="section-head">
        <h2>Selected Co-Authored (High-Impact)</h2>
        <span class="badge">optional</span>
      </div>

      <details>
        <summary>Show selected co-authored journal + conference papers</summary>

        <ul class="pub-list" style="margin-top:12px;">

          <!-- AJO -->
          <li class="pub-item" data-year="2020" data-type="journal" data-first="no">
            <div>
              Sandhu H.S., Elmogy M., Sharafeldeen A.T., <span class="me">Elsharkawy, M.</span>, et al.
              <strong>Automated diagnosis of diabetic retinopathy using clinical biomarkers, OCT, and OCT angiography.</strong>
              <em>American Journal of Ophthalmology</em>, 2020.
            </div>
            <div class="tagrow">
              <span class="tag j">Top Clinical Journal</span>
              <span class="tag">OCT/OCTA</span>
              <span class="tag">DR</span>
            </div>
          </li>

          <!-- Medical Physics retinal layers -->
          <li class="pub-item" data-year="2021" data-type="journal" data-first="no">
            <div>
              Sleman A.A., Soliman A., <span class="me">Elsharkawy, M.</span>, et al.
              <strong>A novel 3D segmentation approach for extracting retinal layers from OCT images.</strong>
              <em>Medical Physics</em>, 48(4):1584–1595, 2021.
            </div>
            <div class="tagrow">
              <span class="tag j">Top Journal</span>
              <span class="tag">Segmentation</span>
              <span class="tag">OCT</span>
            </div>
          </li>

          <!-- Scientific Reports DR (Sharafeldeen first) -->
          <li class="pub-item" data-year="2021" data-type="journal" data-first="no">
            <div>
              Sharafeldeen A., <span class="me">Elsharkawy, M.</span>, et al.
              <strong>Precise higher-order reflectivity and morphology models for early diagnosis of diabetic retinopathy using OCT images.</strong>
              <em>Scientific Reports</em>, 11:4730, 2021.
            </div>
            <div class="tagrow">
              <span class="tag j">High-Visibility Journal</span>
              <span class="tag">OCT</span>
              <span class="tag">DR</span>
            </div>
          </li>

          <!-- ICIP 2023 -->
          <li class="pub-item" data-year="2023" data-type="conference" data-first="no">
            <div>
              Aboudessouki A., Ali K.M., <span class="me">Elsharkawy, M.</span>, et al.
              <strong>Automated diagnosis of breast cancer using deep learning-based whole slide image analysis of molecular biomarkers.</strong>
              <em>IEEE ICIP</em>, 2023.
            </div>
            <div class="tagrow">
              <span class="tag c">Major IEEE Conf</span>
              <span class="tag">WSI</span>
              <span class="tag">Breast cancer</span>
            </div>
          </li>

          <!-- IEEE Access 2025 Seg-Swin (coauthored) -->
          <li class="pub-item" data-year="2025" data-type="journal" data-first="no">
            <div>
              El-Den N.N., <span class="me">Elsharkawy, M.</span>, et al.
              <strong>Seg-Swin: A dual-attention transformer model for advanced AMD classification and lesion detection using color fundus imaging.</strong>
              <em>IEEE Access</em>, 2025.
            </div>
            <div class="tagrow">
              <span class="tag j">Journal</span>
              <span class="tag">Fundus</span>
              <span class="tag">AMD</span>
            </div>
          </li>

        </ul>
      </details>

      <p class="note">
        I kept this section short (only higher-impact / representative items).
      </p>
    </section>

    <!-- =========================
         ABSTRACTS (COLLAPSIBLE)
         ========================= -->
    <section class="card" id="abstracts">
      <div class="section-head">
        <h2>Abstracts / Proceedings</h2>
        <span class="badge">ARVO / IOVS</span>
      </div>

      <details>
        <summary>Show abstracts</summary>

        <ul class="pub-list" style="margin-top:12px;">

          <li class="pub-item" data-year="2021" data-type="abstract" data-first="yes">
            <div>
              <span class="me">Elsharkawy, M.</span>, et al.
              <strong>Automated diagnosis and grading of dry AMD using OCT imaging.</strong>
              <em>Investigative Ophthalmology & Visual Science (IOVS)</em>, 62(8):107–107, 2021.
            </div>
            <div class="tagrow">
              <span class="tag fa">First Author</span>
              <span class="tag">Abstract</span>
              <span class="tag">OCT</span>
              <span class="tag">AMD</span>
            </div>
          </li>

          <li class="pub-item" data-year="2024" data-type="abstract" data-first="no">
            <div>
              Haq M.Z., El-Den N.N., <span class="me">Elsharkawy, M.</span>, et al.
              <strong>Scale-adaptive integrated BiT-autoencoder for diagnosing AMD using fundus images.</strong>
              <em>IOVS</em>, 65(7):5663–5663, 2024.
            </div>
            <div class="tagrow">
              <span class="tag">Abstract</span>
              <span class="tag">Fundus</span>
              <span class="tag">AMD</span>
            </div>
          </li>

          <li class="pub-item" data-year="2025" data-type="abstract" data-first="no">
            <div>
              Saleh I., <span class="me">Elsharkawy, M.</span>, et al.
              <strong>Explainable automated framework for diagnosing DR and AMD using OCT scans.</strong>
              <em>IOVS</em>, 66(10):PB0022–PB0022, 2025.
            </div>
            <div class="tagrow">
              <span class="tag">Abstract</span>
              <span class="tag">OCT</span>
              <span class="tag">DR + AMD</span>
            </div>
          </li>

        </ul>
      </details>

      <p class="note">
        If you prefer, we can hide this whole section to keep the page “very high-impact only”.
      </p>
    </section>

  </div>
</div>

<script>
(function(){
  const search = document.getElementById('pubSearch');
  const year = document.getElementById('yearFilter');
  const type = document.getElementById('typeFilter');
  const firstOnly = document.getElementById('firstOnly');
  const items = Array.from(document.querySelectorAll('.pub-item'));

  function norm(s){ return (s || '').toLowerCase(); }

  function apply(){
    const q = norm(search.value);
    const y = year.value;
    const t = type.value;
    const f = firstOnly.checked;

    items.forEach(it => {
      const text = norm(it.innerText);
      const itY = it.getAttribute('data-year') || '';
      const itT = it.getAttribute('data-type') || '';
      const itF = it.getAttribute('data-first') || 'no';

      const okQ = !q || text.includes(q);
      const okY = (y === 'all') || (itY === y);
      const okT = (t === 'all') || (itT === t);
      const okF = !f || (itF === 'yes');

      it.style.display = (okQ && okY && okT && okF) ? '' : 'none';
    });
  }

  [search, year, type, firstOnly].forEach(el => el.addEventListener('input', apply));
  apply();
})();
</script>
