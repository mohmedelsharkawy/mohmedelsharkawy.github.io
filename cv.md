---
layout: default
title: "CV"
permalink: /cv/
---

<style>
/* ============================
   CV Page – Clean + Modern (Teal/Orange/Indigo)
   - Responsive
   - Dark-mode support
   - Sticky table-of-contents on desktop
   - Collapsible long lists (Teaching, Reviewing)
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

  /* Theme */
  --accent1:#14b8a6; /* teal */
  --accent2:#f97316; /* orange */
  --accent3:#6366f1; /* indigo */
  --link:#0ea5e9;

  --chip-bg:rgba(15,23,42,0.05);
  --chip-border:rgba(15,23,42,0.10);
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

    --chip-bg:rgba(229,231,235,0.07);
    --chip-border:rgba(229,231,235,0.12);
  }
}

.cv-wrap{
  max-width: 1100px;
  margin: 0 auto;
  padding: 18px 14px 34px;
  color: var(--text);
}

.cv-wrap a{ color: var(--link); text-decoration: none; }
.cv-wrap a:hover{ text-decoration: underline; }

.card{
  background: var(--card);
  border: 1px solid var(--border);
  border-radius: var(--radius);
  box-shadow: var(--shadow-sm);
  padding: 16px;
  backdrop-filter: blur(8px);
}

/* HERO */
.cv-hero{
  position: relative;
  overflow: hidden;
  border-radius: calc(var(--radius) + 8px);
  padding: 22px 18px;
  border: 1px solid var(--border);
  box-shadow: var(--shadow);
  background:
    radial-gradient(1100px 520px at 15% 10%, rgba(20,184,166,0.40), transparent 60%),
    radial-gradient(900px 480px at 85% 20%, rgba(249,115,22,0.28), transparent 60%),
    radial-gradient(900px 480px at 60% 120%, rgba(99,102,241,0.25), transparent 60%),
    linear-gradient(135deg, rgba(20,184,166,0.12), rgba(249,115,22,0.10));
}

.cv-hero:before{
  content:"";
  position:absolute;
  inset:0;
  background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='180' height='180'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='.9' numOctaves='3' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='180' height='180' filter='url(%23n)' opacity='.10'/%3E%3C/svg%3E");
  opacity: .16;
  pointer-events:none;
}

.cv-hero-inner{
  position: relative;
  display: grid;
  grid-template-columns: 1fr;
  gap: 12px;
}

.cv-hero h1{
  margin: 0;
  font-size: 2.05rem;
  letter-spacing: -0.02em;
  line-height: 1.15;
}

.cv-hero .subtitle{
  color: var(--muted);
  font-size: 1.02rem;
  line-height: 1.6;
  margin-top: 2px;
}

/* ACTION BUTTONS */
.actions{
  display:flex;
  flex-wrap: wrap;
  gap: 10px;
  margin-top: 6px;
}

.btn{
  display:inline-flex;
  align-items:center;
  gap: 10px;
  padding: 10px 14px;
  border-radius: 999px;
  border: 1px solid var(--border);
  background: rgba(127,127,127,0.06);
  box-shadow: var(--shadow-sm);
  color: var(--text) !important;
  text-decoration: none !important;
  font-weight: 700;
  transition: transform .2s ease, box-shadow .2s ease, border-color .2s ease;
}
.btn:hover{
  transform: translateY(-2px);
  box-shadow: var(--shadow);
  border-color: rgba(20,184,166,0.35);
}
.btn.primary{
  background: rgba(20,184,166,0.12);
  border-color: rgba(20,184,166,0.35);
}

/* LAYOUT */
.cv-layout{
  display:grid;
  grid-template-columns: 1fr 320px;
  gap: 16px;
  margin-top: 16px;
}
@media (max-width: 980px){
  .cv-layout{ grid-template-columns: 1fr; }
}

/* TOC */
.toc{
  position: sticky;
  top: 14px;
  align-self: start;
}
.toc h2{
  margin: 0 0 10px;
  font-size: 1.05rem;
}
.toc a{
  display:block;
  padding: 9px 10px;
  border-radius: 12px;
  border: 1px solid var(--border);
  background: rgba(127,127,127,0.04);
  text-decoration: none !important;
  color: var(--text) !important;
  margin-bottom: 8px;
  transition: transform .2s ease, border-color .2s ease;
}
.toc a:hover{
  transform: translateY(-1px);
  border-color: rgba(99,102,241,0.35);
}

/* SECTION HEADERS */
.section-head{
  display:flex;
  align-items: baseline;
  justify-content: space-between;
  gap: 12px;
  padding-bottom: 10px;
  border-bottom: 1px solid var(--border);
  margin-bottom: 12px;
}
.section-head h2{
  margin: 0;
  font-size: 1.18rem;
  letter-spacing: -0.01em;
}
.badge{
  font-size: 0.85rem;
  color: var(--muted);
  padding: 6px 10px;
  border-radius: 999px;
  border: 1px solid var(--border);
  background: rgba(127,127,127,0.06);
}

/* CONTACT GRID */
.contact-grid{
  display:grid;
  grid-template-columns: 1fr 1fr;
  gap: 10px 14px;
  margin-top: 10px;
}
@media (max-width: 720px){
  .contact-grid{ grid-template-columns: 1fr; }
}
.kv{
  border: 1px solid var(--border);
  background: rgba(127,127,127,0.04);
  border-radius: 14px;
  padding: 10px 12px;
}
.kv .k{ font-weight: 800; }
.kv .v{ color: var(--muted); margin-top: 4px; line-height: 1.5; }

/* CHIPS */
.chips{
  display:flex;
  flex-wrap:wrap;
  gap: 10px;
  margin-top: 10px;
}
.chip{
  display:inline-flex;
  align-items:center;
  padding: 8px 12px;
  border-radius: 999px;
  background: var(--chip-bg);
  border: 1px solid var(--chip-border);
  color: var(--text);
  font-size: 0.92rem;
}

/* TIMELINE ITEM */
.item{
  border: 1px solid var(--border);
  background: rgba(127,127,127,0.04);
  border-radius: 14px;
  padding: 12px 12px;
  margin-top: 10px;
}
.item .top{
  display:flex;
  flex-wrap:wrap;
  gap: 10px;
  align-items: baseline;
  justify-content: space-between;
}
.item .role{
  font-weight: 900;
  letter-spacing: -0.01em;
}
.item .dates{
  color: var(--muted);
  font-weight: 700;
}
.item .meta{
  color: var(--muted);
  line-height: 1.6;
  margin-top: 6px;
}
.item ul{
  margin: 10px 0 0 18px;
}
.item li{ margin: 6px 0; line-height: 1.55; }

/* DETAILS */
details{
  border: 1px solid var(--border);
  border-radius: 14px;
  background: rgba(127,127,127,0.04);
  padding: 10px 12px;
  margin-top: 10px;
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
.note{
  color: var(--muted);
  line-height: 1.7;
  margin: 10px 0 0;
}

/* PRINT (optional) */
@media print{
  .toc, .actions{ display:none !important; }
  .card{ box-shadow:none !important; }
  a{ text-decoration: none !important; color: #000 !important; }
}
</style>

<div class="cv-wrap">

  <!-- HERO -->
  <section class="cv-hero">
    <div class="cv-hero-inner">
      <div>
        <h1>Mohamed Elsharkawy, MSc</h1>
        <div class="subtitle">
          PhD Student (Computer Science & Engineering) • Graduate Teaching Assistant (Bioengineering) • University of Louisville
        </div>

        <div class="actions">
          <a class="btn primary" href="/assets/files/elsharkawycv.pdf" target="_blank" rel="noopener">Download CV (PDF)</a>
          <a class="btn" href="/publications/">Publications</a>
          <a class="btn" href="https://scholar.google.com/citations?user=IknnHU4AAAAJ&hl=en" target="_blank" rel="noopener">Google Scholar</a>
        </div>

        <div class="contact-grid" style="margin-top:14px;">
          <div class="kv">
            <div class="k">Address</div>
            <div class="v">2301 S. Third St. Paul C. Lutz Hall, Room 419, University of Louisville, KY, USA</div>
          </div>
          <div class="kv">
            <div class="k">Email</div>
            <div class="v">
              <a href="mailto:mohamed.elsharkawy@louisville.edu">mohamed.elsharkawy@louisville.edu</a><br/>
              <a href="mailto:mohmed.elsharkawy@mans.edu.eg">mohmed.elsharkawy@mans.edu.eg</a>
            </div>
          </div>
          <div class="kv">
            <div class="k">Phone (USA)</div>
            <div class="v">+1 502-885-0800</div>
          </div>
          <div class="kv">
            <div class="k">Phone (Egypt)</div>
            <div class="v">+20 1069662911</div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- CONTENT + TOC -->
  <div class="cv-layout">

    <!-- MAIN CONTENT -->
    <main>

      <!-- Research Interests -->
      <section class="card" id="interests">
        <div class="section-head">
          <h2>Research Interests</h2>
          <span class="badge">areas</span>
        </div>
        <div class="chips">
          <span class="chip">Medical Image Analysis</span>
          <span class="chip">Machine Learning</span>
          <span class="chip">Deep Learning</span>
          <span class="chip">Image Segmentation</span>
          <span class="chip">Computer Vision</span>
        </div>
      </section>

      <!-- Education -->
      <section class="card" id="education" style="margin-top:16px;">
        <div class="section-head">
          <h2>Education</h2>
          <span class="badge">degrees</span>
        </div>

        <div class="item">
          <div class="top">
            <div class="role">Ph.D. • University of Louisville</div>
            <div class="dates">2023 – Present</div>
          </div>
          <div class="meta">Thesis Advisors: Profs. Ayman El-Baz, Adel Elmaghraby</div>
        </div>

        <div class="item">
          <div class="top">
            <div class="role">M.Sc. • University of Louisville (USA) + Mansoura University (Egypt)</div>
            <div class="dates">2016 – 2022</div>
          </div>
          <div class="meta">
            Thesis: <em>“Role of Machine Learning in Early Detection of Retinal Diseases”</em><br/>
            Advisors: Profs. Ayman El-Baz, Ahmed Atwan, Eman Eldaydamoni
          </div>
        </div>

        <div class="item">
          <div class="top">
            <div class="role">B.S. • Information Technology • Mansoura University</div>
            <div class="dates">2011 – 2015</div>
          </div>
          <div class="meta">
            Senior Project: <em>“Smart Intensive Care Unit”</em><br/>
            Cumulative Grade: Distinction with Degree of Honor (90.2%), GPA = 3.7<br/>
            Department Rank: 1st among 160 students
          </div>
        </div>
      </section>

      <!-- Teaching -->
      <section class="card" id="teaching" style="margin-top:16px;">
        <div class="section-head">
          <h2>Teaching Experience</h2>
          <span class="badge">GTA / Lecturer</span>
        </div>

        <div class="item">
          <div class="top">
            <div class="role">Mansoura University, Egypt • Assistant Lecturer</div>
            <div class="dates">Mar 2015 – Present</div>
          </div>
          <ul>
            <li>Prepared, delivered, and organized laboratory/tutorial sessions</li>
            <li>Graded quizzes and mid-term exams</li>
          </ul>

          <details>
            <summary>Courses assisted</summary>
            <ul>
              <li>Logic Circuits</li>
              <li>Electronic Fundamentals</li>
              <li>Network Programming</li>
              <li>Object-Oriented Programming</li>
              <li>Mobile Computing</li>
              <li>Fundamentals of Programming</li>
              <li>Fundamentals of Statistics</li>
            </ul>
          </details>
        </div>

        <div class="item">
          <div class="top">
            <div class="role">University of Louisville, USA • Graduate Teaching Assistant</div>
            <div class="dates">Jan 2023 – Present</div>
          </div>
          <ul>
            <li>Prepared, delivered, and organized lab/tutorial sessions</li>
            <li>Graded quizzes and mid-term exams</li>
          </ul>

          <details>
            <summary>Undergraduate courses assisted</summary>
            <ul>
              <li>Bioengineering Measurements and Biosystems & Signals</li>
              <li>Computer Tools for Medical Image Analysis</li>
            </ul>
          </details>
        </div>
      </section>

      <!-- Honors -->
      <section class="card" id="honors" style="margin-top:16px;">
        <div class="section-head">
          <h2>Honors & Awards</h2>
          <span class="badge">highlights</span>
        </div>
        <ul style="margin:0 0 0 18px;">
          <li><strong>Exemplary Research Scholarship Award</strong>, University of Louisville (Apr 2024)</li>
          <li><strong>Second Place</strong>, Doctoral Engineering Student Awards, Research! Louisville (Oct 2023)</li>
          <li><strong>Best Dissertation Award</strong> (Master’s), Mansoura University (Jul 2023)</li>
          <li><strong>Second Place</strong>, Master Engineering Student Awards, Research! Louisville (Sep 2021)</li>
          <li><strong>Exemplary Research Scholarship Award</strong>, University of Louisville (Apr 2023)</li>
          <li>Finalist, <strong>3-Minute Thesis (3MT)</strong>, University of Louisville (2023)</li>
          <li><strong>Ranked first (Honors)</strong> in B.Sc. (2015), Mansoura University</li>
          <li><strong>College excellence award</strong> for all four undergraduate years (2011–2015)</li>
        </ul>
      </section>

      <!-- Profiles / Identifiers -->
      <section class="card" id="profiles" style="margin-top:16px;">
        <div class="section-head">
          <h2>Research Profiles</h2>
          <span class="badge">identifiers</span>
        </div>

        <div class="chips">
          <a class="chip" href="https://scholar.google.com/citations?user=IknnHU4AAAAJ&hl=en" target="_blank" rel="noopener">Google Scholar</a>
          <a class="chip" href="https://publons.com/researcher/2993425/mohamed-elsharkawy/" target="_blank" rel="noopener">Web of Science / Publons</a>
          <a class="chip" href="https://www.scopus.com/authid/detail.uri?authorId=57217217044" target="_blank" rel="noopener">Scopus</a>
          <a class="chip" href="https://www.researchgate.net/profile/Mohamed-Elsharkawy-11" target="_blank" rel="noopener">ResearchGate</a>
          <a class="chip" href="https://mymans.mans.edu.eg/cv/4ce56d50-10b2-11ec-8d2b-a1fabb74302b/2" target="_blank" rel="noopener">Mansoura Univ. Profile</a>
          <a class="chip" href="https://loop.frontiersin.org/people/1018324/overview" target="_blank" rel="noopener">Loop</a>
          <a class="chip" href="https://orcid.org/0000-0001-9242-9709" target="_blank" rel="noopener">ORCID</a>
        </div>

        <p class="note">
          For a full breakdown (journals, conferences, chapters), see the <a href="/publications/">Publications</a> page.
        </p>
      </section>

      <!-- Patents -->
      <section class="card" id="patents" style="margin-top:16px;">
        <div class="section-head">
          <h2>Patents & Disclosures</h2>
          <span class="badge">IP</span>
        </div>
        <div class="item">
          <div class="top">
            <div class="role">Assessment of Pulmonary Function in Coronavirus Patient</div>
            <div class="dates">U.S. Patent Application #63/156,171</div>
          </div>
          <div class="meta">
            <strong>M. Elsharkawy</strong>, A. El-Baz, A. Shalaby, A. Soliman, A. Sharafeldeen, A. Mahmoud, H. Sandhu, G. Giridharan. <br/>
            <em>Status:</em> In Progress
          </div>
        </div>
      </section>

      <!-- Service -->
      <section class="card" id="service" style="margin-top:16px;">
        <div class="section-head">
          <h2>Professional Service</h2>
          <span class="badge">reviewing</span>
        </div>

        <p class="note" style="margin-top:0;">
          Reviewer for journals and conferences in medical imaging and AI.
        </p>

        <details>
          <summary>Reviewer list (expand)</summary>
          <ul style="margin:10px 0 0 18px;">
            <li>IEEE Journal of Biomedical and Health Informatics</li>
            <li><em>Scientific Reports</em></li>
            <li><em>Artificial Intelligence in Medicine</em></li>
            <li><em>Artificial Intelligence Review</em></li>
            <li><em>Computers in Biology and Medicine</em></li>
            <li><em>PLOS ONE</em></li>
            <li><em>ISA Transactions</em></li>
            <li><em>IEEE Access</em></li>
            <li><em>Diagnostics</em></li>
            <li>ICPR, MICCAI, ISBI (and related venues)</li>
          </ul>
        </details>
      </section>

      <!-- Skills -->
      <section class="card" id="skills" style="margin-top:16px;">
        <div class="section-head">
          <h2>Software & Skills</h2>
          <span class="badge">tools</span>
        </div>

        <div class="chips">
          <span class="chip"><strong>Programming:</strong>&nbsp;Python, MATLAB, R</span>
          <span class="chip"><strong>Tooling:</strong>&nbsp;LaTeX, Overleaf, Microsoft Office</span>
          <span class="chip"><strong>OS:</strong>&nbsp;Windows</span>
        </div>
      </section>

      <!-- Languages -->
      <section class="card" id="languages" style="margin-top:16px;">
        <div class="section-head">
          <h2>Languages</h2>
          <span class="badge">fluency</span>
        </div>
        <div class="chips">
          <span class="chip"><strong>Arabic:</strong>&nbsp;Native</span>
          <span class="chip"><strong>English:</strong>&nbsp;Very Good</span>
        </div>
      </section>

      <!-- Hobbies -->
      <section class="card" id="hobbies" style="margin-top:16px;">
        <div class="section-head">
          <h2>Activities & Hobbies</h2>
          <span class="badge">personal</span>
        </div>
        <div class="chips">
          <span class="chip">Tennis</span>
          <span class="chip">Soccer</span>
          <span class="chip">Traveling</span>
          <span class="chip">Social relationships</span>
        </div>
      </section>

      <!-- References -->
      <section class="card" id="references" style="margin-top:16px;">
        <div class="section-head">
          <h2>References</h2>
          <span class="badge">available</span>
        </div>
        <p class="note" style="margin-top:0;">Available upon request.</p>
      </section>

    </main>

    <!-- TOC -->
    <aside class="card toc">
      <h2>On this page</h2>
      <a href="#interests">Research Interests</a>
      <a href="#education">Education</a>
      <a href="#teaching">Teaching</a>
      <a href="#honors">Honors & Awards</a>
      <a href="#profiles">Research Profiles</a>
      <a href="#patents">Patents</a>
      <a href="#service">Professional Service</a>
      <a href="#skills">Software & Skills</a>
      <a href="#languages">Languages</a>
      <a href="#hobbies">Activities & Hobbies</a>
      <a href="#references">References</a>
    </aside>

  </div>
</div>
