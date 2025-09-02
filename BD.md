---
layout: page
---

# La progressivité en BD

A la manière du dessinateur Scott McCloud[^1] qui explique la mécanique des bandes dessinées en bande dessinée, je trouve qu'il est aussi plus judicieux d'expliquer la progressivité d'une carte en BD, en mettant en lumière tous leurs liens analogiques.  

[^1]: Scott McCloud. *Understanding Comics : the invisible art*, 1993

# La cohérence

<div id="bd-viewer-coherence" style="text-align:center; max-width:800px; margin:auto;">
  <img id="bd-page-coherence" src="/assets/bd/coherence/page1.png" style="width:100%; height:auto; border:1px solid #ccc; border-radius:8px;"/>

  <p id="page-number-coherence" style="margin-top:0.5rem; font-weight:bold;">Page 1 / 12</p>

  <div style="margin-top:1rem;">
    <button onclick="prevPageCoherence()" style="padding:0.5rem 1rem; margin-right:1rem;">⬅ Précédent</button>
    <button onclick="nextPageCoherence()" style="padding:0.5rem 1rem;">Suivant ➡</button>
  </div>
</div>

<script>
  const pagesCoherence = [
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
  let currentCoherence = 0;
  const imgCoherence = document.getElementById("bd-page-coherence");
  const counterCoherence = document.getElementById("page-number-coherence");

  function showPageCoherence(n) {
    currentCoherence = (n + pagesCoherence.length) % pagesCoherence.length;
    imgCoherence.src = pagesCoherence[currentCoherence];
    counterCoherence.textContent = `Page ${currentCoherence + 1} / ${pagesCoherence.length}`;
  }

  function prevPageCoherence() { showPageCoherence(currentCoherence - 1); }
  function nextPageCoherence() { showPageCoherence(currentCoherence + 1); }
</script>

# Le rythme

<div id="bd-viewer-rythme" style="text-align:center; max-width:800px; margin:auto;">
  <img id="bd-page-rythme" src="/assets/bd/rythme/page1.png" style="width:100%; height:auto; border:1px solid #ccc; border-radius:8px;"/>

  <p id="page-number-rythme" style="margin-top:0.5rem; font-weight:bold;">Page 1 / 23</p>

  <div style="margin-top:1rem;">
    <button onclick="prevPageRythme()" style="padding:0.5rem 1rem; margin-right:1rem;">⬅ Précédent</button>
    <button onclick="nextPageRythme()" style="padding:0.5rem 1rem;">Suivant ➡</button>
  </div>
</div>

<script>
  const pagesRythme = [
    "/assets/bd/rythme/page1.png",
    "/assets/bd/rythme/page2.png",
    "/assets/bd/rythme/page3.png",
    "/assets/bd/rythme/page4.png",
    "/assets/bd/rythme/page5.png",
    "/assets/bd/rythme/page6.png",
    "/assets/bd/rythme/page7.png",
    "/assets/bd/rythme/page8.png",
    "/assets/bd/rythme/page9.png",
    "/assets/bd/rythme/page10.png",
    "/assets/bd/rythme/page11.png",
    "/assets/bd/rythme/page12.png",
    "/assets/bd/rythme/page13.png",
    "/assets/bd/rythme/page14.png",
    "/assets/bd/rythme/page15.png",
    "/assets/bd/rythme/page16.png",
    "/assets/bd/rythme/page17.png",
    "/assets/bd/rythme/page18.png",
    "/assets/bd/rythme/page19.png",
    "/assets/bd/rythme/page20.png",
    "/assets/bd/rythme/page21.png",
    "/assets/bd/rythme/page22.png",
    "/assets/bd/rythme/page23.png"
  ];
  let currentRythme = 0;
  const imgRythme = document.getElementById("bd-page-rythme");
  const counterRythme = document.getElementById("page-number-rythme");

  function showPageRythme(n) {
    currentRythme = (n + pagesRythme.length) % pagesRythme.length;
    imgRythme.src = pagesRythme[currentRythme];
    counterRythme.textContent = `Page ${currentRythme + 1} / ${pagesRythme.length}`;
  }

  function prevPageRythme() { showPageRythme(currentRythme - 1); }
  function nextPageRythme() { showPageRythme(currentRythme + 1); }
</script>