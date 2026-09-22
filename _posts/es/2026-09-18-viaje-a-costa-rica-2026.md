---
ref: trip-to-costa-rica-2026
lang: es
title: "Viaje a Costa Rica 2026"
date: 2026-09-18
permalink: /es/posts/2026/09/viaje-a-costa-rica-2026/
excerpt: "Bosques nubosos en Monteverde, el bosque húmedo del Caribe en Puerto Viejo, quetzales, trogones y un esquivo pájaro campana."
tags:
  - Costa Rica
  - bosque nuboso
  - viajes
---

<style>
.fw-wrap{display:flex;gap:2em;align-items:flex-start;flex-wrap:wrap-reverse;}
.fw-text{flex:1 1 280px;min-width:0;}
.fw-gallery{flex:0 0 340px;max-width:100%;position:relative;}
.fw-track{display:flex;overflow-x:auto;scroll-snap-type:x mandatory;scroll-behavior:smooth;border-radius:10px;scrollbar-width:none;}
.fw-track::-webkit-scrollbar{display:none;}
.fw-track img{flex:0 0 100%;width:100%;aspect-ratio:3/4;object-fit:cover;scroll-snap-align:center;display:block;}
.fw-btn{position:absolute;top:50%;transform:translateY(-50%);background:rgba(0,0,0,.45);color:#fff;border:0;border-radius:50%;width:36px;height:36px;font-size:20px;line-height:36px;padding:0;cursor:pointer;}
.fw-btn:hover{background:rgba(0,0,0,.7);}
.fw-prev{left:8px;} .fw-next{right:8px;}
.fw-dots{text-align:center;margin-top:.5em;}
.fw-dots span{display:inline-block;width:8px;height:8px;border-radius:50%;background:#bbb;margin:0 4px;cursor:pointer;}
.fw-dots span.on{background:#2e7d32;}
@media (max-width: 700px){.fw-gallery{flex:1 1 100%;}}
</style>

<div class="fw-wrap">
  <div class="fw-text">
    <p>Tuve la oportunidad de viajar de vacaciones a Costa Rica. En la grata compañía de mi novia, pasamos tres días en el bosque nuboso de Monteverde, un bosque montano tropical muy bien conservado donde muchos ecólogos brillantes han trabajado antes. En los meses previos al viaje leí sobre cómo investigadores como Daniel Janzen y Leslie Holdridge hicieron grandes aportes a la ecología de los bosques tropicales recorriendo los senderos de los bosques de Costa Rica, justo como los que yo recorrí. Vimos muchísimos paisajes hermosos, quetzales, trogones collarejos y colibríes, y escuchamos muchas veces al pájaro campana sin lograr verlo nunca.</p>
    <p>Después fuimos a Puerto Viejo a disfrutar unos días en la costa caribe de Centroamérica. Aunque Puerto Viejo no ha sido objeto de tanta investigación como otros bosques de Costa Rica, pudimos disfrutar de la belleza de su bosque húmedo.</p>
    <p>Me gusta mucho Costa Rica y “la cultura tica”, y espero volver algún día a hacer ciencia, como lo han hecho tantos grandes científicos.</p>
  </div>
  <div class="fw-gallery">
    <div class="fw-track" id="crTrack">
      <img src="/images/bloc6.jpeg" alt="Costa Rica 2026, foto 1" loading="lazy">
      <img src="/images/bloc7.jpeg" alt="Costa Rica 2026, foto 2" loading="lazy">
      <img src="/images/bloc8.jpeg" alt="Costa Rica 2026, foto 3" loading="lazy">
      <img src="/images/bloc9.jpeg" alt="Costa Rica 2026, foto 4" loading="lazy">
      <img src="/images/bloc10.jpeg" alt="Costa Rica 2026, foto 5" loading="lazy" style="object-fit:contain;background:#111;">
      <img src="/images/bloc11.JPG" alt="Costa Rica 2026, foto 6" loading="lazy">
      <img src="/images/bloc12.jpeg" alt="Costa Rica 2026, foto 7" loading="lazy">
    </div>
    <button class="fw-btn fw-prev" aria-label="Foto anterior" onclick="crGo(-1)">&#8249;</button>
    <button class="fw-btn fw-next" aria-label="Foto siguiente" onclick="crGo(1)">&#8250;</button>
    <div class="fw-dots" id="crDots"></div>
  </div>
</div>

<script>
(function(){
  var t=document.getElementById('crTrack'), d=document.getElementById('crDots'), n=t.children.length;
  for(var i=0;i<n;i++){var s=document.createElement('span');s.dataset.i=i;s.onclick=function(){t.scrollTo({left:this.dataset.i*t.clientWidth});};d.appendChild(s);}
  function cur(){return Math.round(t.scrollLeft/t.clientWidth);}
  function upd(){var k=cur();for(var j=0;j<n;j++){d.children[j].className=(j===k?'on':'');}}
  window.crGo=function(step){var k=(cur()+step+n)%n;t.scrollTo({left:k*t.clientWidth});};
  t.addEventListener('scroll',function(){window.requestAnimationFrame(upd);});
  upd();
})();
</script>
