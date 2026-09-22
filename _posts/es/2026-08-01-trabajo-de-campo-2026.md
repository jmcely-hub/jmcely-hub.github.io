---
ref: field-work-2026
lang: es
title: "Trabajo de campo 2026"
date: 2026-08-01
permalink: /es/posts/2026/08/trabajo-de-campo-2026/
excerpt: "De vuelta en Colombia para el sexto censo de plántulas en los bosques secos tropicales, con muchísima fauna y flora maravillosa en el camino."
tags:
  - trabajo de campo
  - Colombia
  - bosque seco tropical
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
    <p>Durante el verano de 2026 viajé a mi país, Colombia, para realizar el sexto censo de un programa de monitoreo a largo plazo de la dinámica de plántulas en los bosques secos tropicales, liderado por mi asesora, la Dra. María Natalia Umaña. Esta vez me acompañó Larissa Lotti, ecóloga brasileña y compañera de nuestro laboratorio.</p>
    <p>¡Nos divertimos muchísimo y vimos una fauna y una flora maravillosas en el camino!</p>
    <p>Si le interesa hacer investigación en Colombia, no dude en escribirme a mi correo: ¡seguro encontramos la manera!</p>
  </div>
  <div class="fw-gallery">
    <div class="fw-track" id="fwTrack">
      <img src="/images/blog1.jpg" alt="Trabajo de campo 2026, foto 1" loading="lazy">
      <img src="/images/blog2.jpeg" alt="Trabajo de campo 2026, foto 2" loading="lazy">
      <img src="/images/blog3.jpeg" alt="Trabajo de campo 2026, foto 3" loading="lazy">
      <img src="/images/blog4.jpeg" alt="Trabajo de campo 2026, foto 4" loading="lazy">
      <img src="/images/blog5.jpeg" alt="Trabajo de campo 2026, foto 5" loading="lazy">
    </div>
    <button class="fw-btn fw-prev" aria-label="Foto anterior" onclick="fwGo(-1)">&#8249;</button>
    <button class="fw-btn fw-next" aria-label="Foto siguiente" onclick="fwGo(1)">&#8250;</button>
    <div class="fw-dots" id="fwDots"></div>
  </div>
</div>

<script>
(function(){
  var t=document.getElementById('fwTrack'), d=document.getElementById('fwDots'), n=t.children.length;
  for(var i=0;i<n;i++){var s=document.createElement('span');s.dataset.i=i;s.onclick=function(){t.scrollTo({left:this.dataset.i*t.clientWidth});};d.appendChild(s);}
  function cur(){return Math.round(t.scrollLeft/t.clientWidth);}
  function upd(){var k=cur();for(var j=0;j<n;j++){d.children[j].className=(j===k?'on':'');}}
  window.fwGo=function(step){var k=(cur()+step+n)%n;t.scrollTo({left:k*t.clientWidth});};
  t.addEventListener('scroll',function(){window.requestAnimationFrame(upd);});
  upd();
})();
</script>
