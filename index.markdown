
---
# Main homepage
layout: home
mathjax: true
---

<style>

  /* =================================
     GLOBAL THEME
  ================================= */

  body {
    background: #101114;
    background-attachment: fixed;
    color: #F4F4F5;
  }

  .page-content {
    padding: 60px 0 50px;
  }

  .page-content .wrapper {
    max-width: 1100px;
  }

  .page-heading,
  .post-title {
    display: none;
  }


  /* =================================
     HOMEPAGE HERO
  ================================= */

  .home-hero {
    display: grid;
    grid-template-columns: 1.2fr 0.8fr;
    gap: 65px;
    align-items: center;
    min-height: 550px;
    padding: 30px 0 65px;
  }

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
     PROFILE IMAGE
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
  margin-top: 30px;
}

.publications-heading {
  color: #F4F4F5;
  font-size: 36px;
  font-weight: 700;
}

.publications-heading span {
  color: #10B981;
}

.publications-description {
  color: #A1A1AA;
  line-height: 1.8;
}

.publication-note {
  color: #A78BFA;
  font-size: 14px;
  margin-bottom: 30px;
}

/* Style individual entries without changing their structure */

.publications-section li {
  background: #191B20;
  border: 1px solid #2A2D35;
  border-radius: 12px;
  padding: 22px;
  margin-bottom: 16px;
  color: #D4D4D8;
  line-height: 1.8;
}

.publications-section li:hover {
  border-color: #10B981;
}

.publications-section a {
  color: #10B981;
}

.publications-section a:hover {
  color: #A78BFA;
}

.publications-section button {
  background: #22242B;
  color: #10B981;
  border: 1px solid #343740;
  border-radius: 6px;
  padding: 6px 12px;
  cursor: pointer;
}

.publications-section pre {
  background: #101114;
  color: #D4D4D8;
  padding: 12px;
  overflow-x: auto;
}

/* Responsive grid, if the plugin uses a list */

.publications-section ol.bibliography,
.publications-section ul.bibliography {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: 18px;
  padding: 0;
  list-style: none;
}

@media (max-width: 768px) {
  .publications-section ol.bibliography,
  .publications-section ul.bibliography {
    grid-template-columns: 1fr;
  }
}


  /* =================================
     BIBLIOGRAPHY GRID
  ================================= */

  /* The bibliography plugin generates
     the publication entries. */

  .publications-section ol,
  .publications-section ul {
    list-style: none;
    padding: 0;
    margin: 0;

    display: grid;
    grid-template-columns: repeat(2, minmax(0, 1fr));
    gap: 20px;
  }

  /* Individual publication cards */

  .publications-section li {
    background: #191B20;
    border: 1px solid #2A2D35;
    border-radius: 14px;
    padding: 24px;
    color: #D4D4D8;
    font-size: 14px;
    line-height: 1.8;
    transition: all 0.25s ease;
    overflow-wrap: anywhere;
  }

  .publications-section li:hover {
    border-color: #10B981;
    transform: translateY(-3px);
  }

  /* Publication links */

  .publications-section a {
    color: #10B981;
    text-decoration: none;
    transition: color 0.2s ease;
  }

  .publications-section a:hover {
    color: #A78BFA;
    text-decoration: underline;
  }

  /* Publication titles */

  .publications-section em {
    color: #F4F4F5;
    font-style: italic;
  }

  /* Publication year / metadata */

  .publications-section strong {
    color: #A78BFA;
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

  .publications-section pre {
    background: #101114;
    color: #D4D4D8;
    border: 1px solid #343740;
    border-radius: 8px;
    padding: 14px;
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

    .publications-section ol,
    .publications-section ul {
      grid-template-columns: 1fr;
    }
  }

</style>


<div class="home">

  <!-- =================================
       INTRODUCTION
  ================================= -->

  <section class="home-hero">

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
        My research interests include [Research Area 1],
        [Research Area 2], and [Research Area 3].
        I am passionate about exploring innovative solutions
        to challenging problems in computer science.
      </p>

      <p class="hero-description">
        Here, you can find information about my research,
        academic publications, and professional activities.
        Feel free to explore my work or get in touch!
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


    <!-- PROFILE IMAGE -->

    <div class="hero-image">

      <img src="/assets/images/profile1.jpeg"
           alt="Keegan Yao">

    </div>

  </section>


  <!-- =================================
       PUBLICATIONS
  ================================= -->

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

</div>


<!-- =================================
     ABSTRACT TOGGLE
================================= -->

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
