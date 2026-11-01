---
# Feel free to add content and custom Front Matter to this file.
layout: home
mathjax: true
---

<style>

/* =================================
   PROFESSIONAL DARK THEME
================================= */

body {
  background: #101114;
  background-attachment: fixed;
  color: #F4F4F5;
}

.page-content {
  padding: 60px 0 40px;
}

.page-content .wrapper {
  max-width: 1100px;
}

.page-heading,
.post-title {
  display: none;
}


/* =================================
   MAIN TWO-COLUMN LAYOUT
================================= */

.home-hero {
  display: grid;
  grid-template-columns: 1.2fr 0.8fr;
  gap: 65px;
  align-items: center;
  min-height: 550px;
  padding: 30px 0 65px;
}


/* =================================
   LEFT: INTRODUCTION
================================= */

.hero-content {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
}

.hero-label {
  color: #10B981;
  font-size: 13px;
  font-weight: 700;
  letter-spacing: 2px;
  text-transform: uppercase;
  margin-bottom: 18px;
}

.hero-name {
  color: #F4F4F5;
  font-size: clamp(42px, 5vw, 60px);
  font-weight: 750;
  line-height: 1.15;
  margin: 0 0 12px;
}

.hero-subtitle {
  color: #A78BFA;
  font-size: 19px;
  font-weight: 600;
  margin-bottom: 25px;
}

.hero-description {
  color: #A1A1AA;
  font-size: 16px;
  line-height: 1.9;
  max-width: 570px;
  margin-bottom: 16px;
}


/* =================================
   RIGHT: PROFILE IMAGE
================================= */

.hero-image {
  position: relative;
  width: 100%;
  max-width: 370px;
  justify-self: end;
}

.hero-image::before {
  content: "";
  position: absolute;
  inset: -12px;
  border: 2px solid #10B981;
  border-radius: 22px;
  opacity: 0.5;
  z-index: 0;
}

.hero-image img {
  position: relative;
  z-index: 1;
  display: block;
  width: 100%;
  aspect-ratio: 4 / 5;
  object-fit: cover;
  object-position: center;
  border-radius: 16px;
  border: none;
}


/* =================================
   SOCIAL ICONS
================================= */

.social-links {
  display: flex;
  align-items: center;
  justify-content: flex-start;
  gap: 18px;
  margin-top: 28px;
}

.social-links a {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 46px;
  height: 46px;
  background: #191B20;
  border: 1px solid #2A2D35;
  border-radius: 12px;
  transition: all 0.25s ease;
}

.social-links a:hover {
  transform: translateY(-4px);
  border-color: #10B981;
  background: #202B27;
}

.social-links img {
  width: 25px;
  height: 25px;
  object-fit: contain;
  border: none;
}


/* =================================
   PUBLICATIONS SECTION
================================= */

.publications-section {
  border-top: 1px solid #2A2D35;
  padding-top: 50px;
  margin-top: 20px;
}

.publications-heading {
  color: #F4F4F5;
  font-size: 36px;
  font-weight: 700;
  margin: 0 0 12px;
}

.publications-heading span {
  color: #10B981;
}

.publications-description {
  color: #A1A1AA;
  font-size: 15px;
  line-height: 1.8;
  margin-bottom: 15px;
}

.publication-note {
  color: #A78BFA;
  font-size: 14px;
  line-height: 1.7;
  margin-bottom: 30px;
}


/* =================================
   PUBLICATION CSS GRID
================================= */

/*
   Jekyll Scholar normally generates:

   <ol class="bibliography">
       <li>Publication 1</li>
       <li>Publication 2</li>
   </ol>

   We turn this list into a two-column grid.
*/

.publications-section .bibliography {
  display: grid !important;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: 20px;

  padding: 0 !important;
  margin: 0 !important;

  list-style: none !important;
  counter-reset: none;
}

/* Individual publication cards */

.publications-section .bibliography > li {
  display: block;

  background: #191B20;
  border: 1px solid #2A2D35;
  border-radius: 14px;

  padding: 22px;
  margin: 0 !important;

  color: #D4D4D8;
  font-size: 14px;
  line-height: 1.8;

  overflow-wrap: anywhere;

  transition:
    border-color 0.25s ease,
    transform 0.25s ease,
    background 0.25s ease;
}

/* Card hover effect */

.publications-section .bibliography > li:hover {
  border-color: #10B981;
  background: #1C201F;
  transform: translateY(-3px);
}


/* =================================
   PUBLICATION TEXT AND LINKS
================================= */

/* Links */

.publications-section .bibliography a {
  color: #10B981;
  text-decoration: none;
  transition: color 0.2s ease;
}

.publications-section .bibliography a:hover {
  color: #A78BFA;
  text-decoration: underline;
}

/* Paper titles */

.publications-section .bibliography em {
  color: #F4F4F5;
}

/* Bold metadata */

.publications-section .bibliography strong {
  color: #A78BFA;
}

/* Author and publication text */

.publications-section .bibliography li {
  overflow-wrap: anywhere;
}


/* =================================
   ABSTRACT AND BIBTEX
================================= */

.publications-section button {
  background: #22242B;
  color: #10B981;

  border: 1px solid #343740;
  border-radius: 7px;

  padding: 6px 12px;
  margin: 8px 5px 0 0;

  cursor: pointer;
  font-size: 12px;

  transition: all 0.2s ease;
}

.publications-section button:hover {
  background: #25342F;
  border-color: #10B981;
}

/* Abstract and BibTeX containers */

.publications-section pre {
  background: #101114;
  color: #D4D4D8;

  border: 1px solid #343740;
  border-radius: 8px;

  padding: 14px;
  margin-top: 10px;

  overflow-x: auto;
  white-space: pre-wrap;
  overflow-wrap: anywhere;
}

.publications-section code {
  color: #A78BFA;
}


/* =================================
   MOBILE RESPONSIVENESS
================================= */

@media screen and (max-width: 768px) {

  .page-content {
    padding-top: 35px;
  }

  .home-hero {
    grid-template-columns: 1fr;
    gap: 40px;
    min-height: auto;
    padding: 20px 0 45px;
  }

  .hero-image {
    order: -1;
    max-width: 260px;
    justify-self: center;
  }

  .hero-name {
    font-size: 42px;
  }

  .hero-subtitle {
    font-size: 17px;
  }

  .hero-description {
    font-size: 15px;
  }

  .social-links {
    gap: 14px;
    flex-wrap: wrap;
  }

  .publications-heading {
    font-size: 30px;
  }

  .publications-section .bibliography {
    grid-template-columns: 1fr;
  }

}

</style>


<!-- =================================
     MATHJAX CONFIGURATION
================================= -->

{% if page.mathjax %}

<script>
  window.MathJax = {
    tex: {
      inlineMath: [['$', '$'], ['\\(', '\\)']],
      displayMath: [['$$', '$$'], ['\\[', '\\]']]
    },
    startup: {
      typeset: true
    }
  };
</script>

<script
  type="text/javascript"
  id="MathJax-script"
  async
  src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js">
</script>

{% endif %}


<div class="home">


  <!-- =================================
       INTRODUCTION
  ================================== -->

  <section class="home-hero">

    <!-- LEFT COLUMN: TEXT -->

    <div class="hero-content">

      <div class="hero-label">
        Welcome to my website
      </div>

      <h1 class="hero-name">
        Keegan Yao
      </h1>

      <div class="hero-subtitle">
        Researcher · Computer Science
      </div>

      <p class="hero-description">
        Hello! I'm Keegan Yao. Welcome to my personal
        academic website.
      </p>

      <p class="hero-description">
        I am a recent Ph.D. graduate in computer science from Duke University, advised by <a href="https://users.cs.duke.edu/~pankaj/">Pankaj K. Agarwal</a>. My research focuses on designing simple and scalable algorithms for the _optimal transport (OT) problem_ and its variants through studying important geometric and structural properties of its solutions. OT is a common method of lifting geometry of points to geometry of distributions across mathematics, statistics, data science and machine learning. The algorithms I design mix together the strengths of both continuous and combinatorial optimization methods, and exploit geometry of the domain space. My research since graduation has focused on various extensions of OT to applications in data science and machine learning, including but not limited to: clustering of distributions, dynamic OT under distributional drift, symmetry-preserving transport plans, flow matchings using semi-discrete OT, and rewiring for graph neural networks.
      </p>

      <p class="hero-description">
        Before attending Duke University, I completed my undergraduate studies in mathematics and computer science at the University of Connecticut. While there, I had the great privilege of exploring many diverse fields across mathematics and computer science. My undergraduate honors thesis, under the supervision of <a href="https://www2.math.uconn.edu/~munteanu/">Ovidiu Munteanu</a>, was an expository paper on the existence of the Ricci flow under negative curvature lower bounds. In addition, I studied geometric data analysis of trajectories under <a href="https://donsheehy.net/">Don Sheehy</a>, comparison of phylogenetic trees with partially overlapping taxa under <a href="https://mukul-bansal.uconn.edu/">Mukul Bansal</a>, and high dimensional entropic uncertainty relations with applications to quantum cryptography under <a href="https://walterkrawec.org/">Walter Krawec</a>.
      </p>


      <!-- SOCIAL ICONS -->

      <div class="social-links">

        <a href="mailto:kyao8686@gmail.com"
           aria-label="Email"
           title="Email">
          <img src="/assets/images/email.png" alt="Email">
        </a>

        <a href="https://scholar.google.com/citations?user=yw2rIKAAAAAJ&hl=en&oi=ao"
           target="_blank"
           rel="noopener"
           aria-label="Google Scholar"
           title="Google Scholar">
          <img src="/assets/images/scholar.png" alt="Google Scholar">
        </a>

        <a href="https://orcid.org/0000-0002-1739-5614"
           target="_blank"
           rel="noopener"
           aria-label="ORCID"
           title="ORCID">
          <img src="/assets/images/orcid.svg" alt="ORCID">
        </a>

        <a href="https://dblp.org/pid/296/1841.html"
           target="_blank"
           rel="noopener"
           aria-label="DBLP"
           title="DBLP">
          <img src="/assets/images/dblp.png" alt="DBLP">
        </a>

        <a href="https://www.linkedin.com/in/keegan-yao-437702170"
           target="_blank"
           rel="noopener"
           aria-label="LinkedIn"
           title="LinkedIn">
          <img src="/assets/images/linkedin.png" alt="LinkedIn">
        </a>

      </div>

    </div>


    <!-- RIGHT COLUMN: PROFILE IMAGE -->

    <div class="hero-image">

      <img
        src="/assets/images/profile1.jpeg"
        alt="Keegan Yao">

    </div>

  </section>


  <!-- =================================
       PUBLICATIONS
  ================================== -->

  <section class="publications-section">

    <h2 class="publications-heading">
      Selected <span>Publications</span>
    </h2>

    <p class="publications-description">
      A collection of my academic publications and research contributions.
    </p>

    <p class="publication-note">
      ($\alpha$-$\beta$): Authors listed in alphabetical order
      (theoretical computer science convention).
    </p>

    {% bibliography %}

  </section>


  <!-- =================================
       ABSTRACT TOGGLE
  ================================== -->

  <script>

  function toggleAbstract(id) {

    var x = document.getElementById('abstract-' + id);

    if (!x) return;

    if (x.style.display === "none" || x.style.display === "") {

      x.style.display = "block";

      setTimeout(function() {

        if (window.MathJax) {

          if (typeof MathJax.typesetPromise === 'function') {

            MathJax.typesetPromise([x])
              .catch(function(err) {
                console.log(err);
              });

          } else if (typeof MathJax.typeset === 'function') {

            MathJax.typeset([x]);

          }

        }

      }, 50);

    } else {

      x.style.display = "none";

    }

  }

  </script>


  <!-- =================================
       BIBTEX TOGGLE
  ================================== -->

  <script>

  function toggleBibtex(key) {

    var element = document.getElementById('bib-' + key);

    if (!element) return;

    if (element.style.display === "none") {

      element.style.display = "block";

    } else {

      element.style.display = "none";

    }

  }

  </script>

</div>
