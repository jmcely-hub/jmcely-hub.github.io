---
title: "Trip to Costa Rica 2026"
date: 2026-09-18
permalink: /posts/2026/09/trip-to-costa-rica-2026/
excerpt: "Cloud forests in Monteverde, the Caribbean rainforest of Puerto Viejo, quetzals, trogons, and an elusive bellbird."
tags:
  - Costa Rica
  - cloud forest
  - travel
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
    <p>I had the opportunity to travel to Costa Rica on vacation. While enjoying the great company of my girlfriend, we spent three days in the cloud forest of Monteverde, a well-conserved tropical montane forest where many brilliant ecologists have worked before. In the months before the trip, I read about how researchers like Daniel Janzen and Leslie Holdridge made major contributions to the ecology of tropical forests by walking the trails of Costa Rica's forests, just like the ones I walked. We saw so many beautiful landscapes, quetzals, collared trogons, and hummingbirds, and we heard the bellbird many times without ever managing to see it.</p>
    <p>We then went to Puerto Viejo to enjoy a few days on the Caribbean coast of Central America. Although Puerto Viejo has not been the subject of as much research as other forests in Costa Rica, we got to enjoy the beauty of its rainforest.</p>
    <p>I really like Costa Rica and "la cultura tica," and I hope I can go back one day to do science, just like so many great scientists have.</p>
  </div>
  <div class="fw-gallery">
    <div class="fw-track" id="crTrack">
      <img src="/images/bloc6.jpeg" alt="Costa Rica 2026, photo 1" loading="lazy">
      <img src="/images/bloc7.jpeg" alt="Costa Rica 2026, photo 2" loading="lazy">
      <img src="/images/bloc8.jpeg" alt="Costa Rica 2026, photo 3" loading="lazy">
      <img src="/images/bloc9.jpeg" alt="Costa Rica 2026, photo 4" loading="lazy">
      <img src="/images/bloc10.jpeg" alt="Costa Rica 2026, photo 5" loading="lazy" style="object-fit:contain;background:#111;">
      <img src="/images/bloc11.JPG" alt="Costa Rica 2026, photo 6" loading="lazy">
      <img src="/images/bloc12.jpeg" alt="Costa Rica 2026, photo 7" loading="lazy">
    </div>
    <button class="fw-btn fw-prev" aria-label="Previous photo" onclick="crGo(-1)">&#8249;</button>
    <button class="fw-btn fw-next" aria-label="Next photo" onclick="crGo(1)">&#8250;</button>
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
