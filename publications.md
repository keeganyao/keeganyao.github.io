---
layout: page
title: Publications
mathjax: true
---

<style>
  /* Centers the main page title */
  .page-heading, .post-title {
    text-align: center;
  }

  body {
    /* Change this hex code to your preferred primary text color */
    color: #1f2630;

    /* Creates a smooth gradient from top to bottom */
    background-image: linear-gradient(135deg, #fff1eb, #ffd1ff);
  
    /* Ensures the gradient covers the entire screen even on short pages */
    background-attachment: fixed;
  }
</style>



($\alpha$-$\beta$): Authors listed in alphabetical order (theoretical computer science convention)

{% bibliography %}



<script>
function toggleAbstract(id) {
  var x = document.getElementById('abstract-' + id);
  if (x.style.display === "none" || x.style.display === "") {
    x.style.display = "block";
    
    // Tell MathJax to typeset the newly visible box
    setTimeout(function() {
      if (window.MathJax) {
        if (typeof MathJax.typesetPromise === 'function') {
          MathJax.typesetPromise([x]).catch(function(err) { console.log(err); });
        } else if (typeof MathJax.typeset === 'function') {
          MathJax.typeset([x]);
        }
      }
    }, 50); // Small timeout ensures the DOM has painted the block display first
    
  } else {
    x.style.display = "none";
  }
}
</script>

<script>
function toggleBibtex(key) {
  var element = document.getElementById('bib-' + key);
  if (element.style.display === "none") {
    element.style.display = "block";
  } else {
    element.style.display = "none";
  }
}
</script>