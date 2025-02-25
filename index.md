---
layout: default
title: "Home"
---

<style>
/* Inline styles to enhance the homepage look */

/* HERO SECTION: gradient background, centered content */
.hero {
  position: relative;
  background: linear-gradient(135deg, #a9c9ff 0%, #ffbbec 100%);
  color: #fff;
  text-align: center;
  padding: 40px 20px;
  border-radius: 8px;
  margin-bottom: 30px;
}

/* 
   Updated: 
   - Removed fixed 'height: 250px;'
   - Removed 'object-fit: cover;'
   - Now uses height: auto to avoid cropping
*/
.hero img {
  display: block;
  margin: 0 auto;
  border: 2px solid #fff;
  border-radius: 50%;
  width: 250px;
  height: auto;
}

/* Adjusted font sizes slightly */
.hero h1 {
  font-size: 2rem;
  margin-top: 20px;
}

.hero h2 {
  font-size: 1.2rem;
  margin-top: 10px;
  font-weight: 400;
}

/* INTRO SECTION */
.intro {
  background-color: #fdfdfd;
  padding: 20px;
  border-radius: 8px;
  margin-bottom: 20px;
  box-shadow: 0 3px 10px rgba(0,0,0,0.05);
}

/* CONTACT CARD */
.contact-card {
  background-color: #f7f7f7;
  padding: 20px;
  border-left: 4px solid #334;
  border-radius: 8px;
  margin-bottom: 20px;
}

/* QUICK LINKS GRID */
.quick-links {
  display: flex;
  flex-wrap: wrap;
  gap: 20px;
  margin-bottom: 20px;
}

.quick-link-item {
  flex: 1 1 calc(25% - 20px); /* 4 items per row if space allows */
  min-width: 180px;
  background: #eee;
  text-align: center;
  padding: 15px;
  border-radius: 8px;
  transition: background 0.3s, transform 0.3s;
}

.quick-link-item:hover {
  background: #ddd;
  transform: translateY(-2px);
}

.quick-link-item a {
  text-decoration: none;
  color: #333;
  font-weight: 600;
}
</style>

<!-- HERO SECTION -->
<div class="hero">
  <img
    src="/assets/images/sharkawy.jpg"
    alt="Profile Photo"
  />
  <h1>Mohamed Elsharkawy, MSc</h1>
  <h2>PhD Student @ University of Louisville</h2>
</div>

<!-- INTRO / ABOUT SECTION -->
<div class="intro">
  <p>
    Mohamed Elsharkawy was born in Egypt in 1993. He is currently a Ph.D. student in Computer Science and Engineering and a Graduate Teaching Assistant (GTA) at the Bioengineering Department, Speed School of Engineering, University of Louisville, USA. He is also an assistant lecturer in the Information Technology Department, Faculty of Computer and Information Sciences, at Mansoura University.
  </p>
  <p>
    He received his B.Sc. and M.Sc. degrees from the same faculty at Mansoura University and worked as a visiting researcher from August 2019 to May 2022 at the University of Louisville. He has authored or co-authored more than 20 research publications in peer-reviewed journals and conferences and serves as a reviewer for several international journals, including <em>Scientific Reports</em>, <em>IEEE Journal of Biomedical and Health Informatics</em>, <em>IEEE Access</em>, <em>Diagnostics</em>, and <em>Artificial Intelligence Review</em>.
  </p>
  <p>
    His research primarily focuses on <strong>Medical Image Analysis, Machine Learning, and Computer Vision</strong>.
  </p>
</div>

<!-- CONTACT CARD -->
<div class="contact-card">
  <h3>Contact Info</h3>
  <ul style="list-style:none; padding-left:0;">
    <li><strong>Email:</strong> <a href="mailto:mohamed.elsharkawy@louisville.edu">mohamed.elsharkawy@louisville.edu</a></li>
    <li><strong>Phone (USA):</strong> +1 502-885-0800</li>
    <li><strong>Phone (Egypt):</strong> +20 1069662911</li>
  </ul>
</div>

<!-- QUICK LINKS -->
<div class="quick-links">
  <div class="quick-link-item">
    <a href="/assets/files/elsharkawycv.pdf" target="_blank">
      Download Full CV (PDF)
    </a>
  </div>
  <div class="quick-link-item">
    <a href="/cv/">
      Preview CV
    </a>
  </div>
  <div class="quick-link-item">
    <a href="/publications/">
      Browse Publications
    </a>
  </div>
  <div class="quick-link-item">
    <a href="https://scholar.google.com/citations?user=IknnHU4AAAAJ&hl=en" target="_blank" rel="noopener">
      Google Scholar Profile
    </a>
  </div>
</div>

<p>
  Please feel free to explore my background and publications, and reach out if you’d like to connect!
</p>
