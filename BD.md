---
layout: page
---

# La progressivité en BD

A la manière du dessinateur Scott McCloud[^1] qui explique la mécanique des bandes dessinées en bande dessinée, je trouve qu'il est aussi plus judicieux d'expliquer la progressivité d'une carte en BD, en mettant en lumière tous leurs liens analogiques.  

[^1]: Scott McCloud. *Understanding Comics : the invisible art*, 1993

# La cohérence

<div id="bd-viewer" style="text-align:center; max-width:800px; margin:auto;">
  <img id="bd-page" src="/assets/bd/coherence/page1.png" style="width:100%; height:auto; border:1px solid #ccc; border-radius:8px;"/>

  <p id="page-number" style="margin-top:0.5rem; font-weight:bold;">Page 1 / 12</p>

  <div style="margin-top:1rem;">
    <button onclick="prevPage()" style="padding:0.5rem 1rem; margin-right:1rem;">⬅ Précédent</button>
    <button onclick="nextPage()" style="padding:0.5rem 1rem;">Suivant ➡</button>
  </div>
</div>

<script>
  const pages = [
    "/assets/bd/coherence/page1.png",
    "/assets/bd/coherence/page2.png",
    "/assets/bd/coherence/page3.png",
    "/assets/bd/coherence/page4.png",
    "/assets/bd/coherence/page5.png",
    "/assets/bd/coherence/page6.png",
    "/assets/bd/coherence/page7.png",
    "/assets/bd/coherence/page8.png",
    "/assets/bd/coherence/page9.png",
    "/assets/bd/coherence/page10.png",
    "/assets/bd/coherence/page11.png",
    "/assets/bd/coherence/page12.png"
  ];
  let current = 0;
  const img = document.getElementById("bd-page");
  const counter = document.getElementById("page-number");

  function showPage(n) {
    current = (n + pages.length) % pages.length;
    img.src = pages[current];
    counter.textContent = `Page ${current + 1} / ${pages.length}`;
  }

  function prevPage() { showPage(current - 1); }
  function nextPage() { showPage(current + 1); }
</script>