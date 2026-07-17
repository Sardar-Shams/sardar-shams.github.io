<html lang="az">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Sərdar &amp; Şəms — Toy Dəvətnaməsi</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Noto+Serif:ital,wght@0,400;0,500;0,600;1,400&family=Cormorant+Garamond:ital,wght@0,400;0,500;0,600;1,500&display=swap" rel="stylesheet">
<style>
  :root{
    --wine: #5C1F2E;
    --wine-deep: #421520;
    --gold: #C6A15B;
    --gold-light: #E4CB94;
    --cream: #F6EFE4;
    --blush: #D9B8A3;
    --ink: #2B211D;
  }
  *{ box-sizing: border-box; }
  html{ scroll-behavior: smooth; }
  body{
    margin:0;
    background: var(--cream);
    color: var(--ink);
    font-family: 'Noto Serif', serif;
    -webkit-font-smoothing: antialiased;
    overflow-x: hidden;
  }
  .accent{ font-family: 'Cormorant Garamond', serif; }

  /* ---------- reveal ---------- */
  .reveal{ opacity:0; transform: translateY(24px); transition: opacity 0.9s ease, transform 0.9s ease; }
  .reveal.in{ opacity:1; transform: translateY(0); }
  @media (prefers-reduced-motion: reduce){
    .reveal{ opacity:1; transform:none; transition:none; }
  }

  /* ---------- buta motif ---------- */
  .buta{ display:block; }

  /* ---------- hero ---------- */
  .hero{
    position: relative;
    min-height: 100svh;
    background: radial-gradient(120% 90% at 50% 15%, var(--wine) 0%, var(--wine-deep) 70%);
    color: var(--gold-light);
    display:flex;
    flex-direction:column;
    align-items:center;
    justify-content:center;
    text-align:center;
    padding: 48px 24px 64px;
    overflow:hidden;
  }
  .hero::before, .hero::after{
    content:"";
    position:absolute;
    width:180px; height:180px;
    background-repeat:no-repeat;
    background-size:contain;
    opacity:0.16;
  }
  .hero .frame-line{
    position:absolute;
    inset: 22px;
    border: 1px solid rgba(198,161,91,0.35);
    pointer-events:none;
  }
  .hero .frame-line::before,.hero .frame-line::after{
    content:"";
    position:absolute;
    width:34px;height:34px;
    border: 1px solid var(--gold);
  }
  .hero .frame-line::before{ top:-1px; left:-1px; border-right:none; border-bottom:none; }
  .hero .frame-line::after{ bottom:-1px; right:-1px; border-left:none; border-top:none; }

  .eyebrow{
    letter-spacing: 0.42em;
    text-transform: uppercase;
    font-size: 11.5px;
    color: var(--gold);
    margin-bottom: 26px;
  }
  .names{
    font-size: clamp(2.6rem, 8vw, 5.2rem);
    line-height: 1.06;
    margin: 0;
    font-weight: 500;
  }
  .names .amp{
    font-family:'Cormorant Garamond', serif;
    font-style: italic;
    color: var(--gold);
    font-size: 0.75em;
    display:inline-block;
    margin: 0 0.12em;
  }
  .hero-sub{
    margin-top: 22px;
    font-family:'Cormorant Garamond', serif;
    font-style: italic;
    font-size: clamp(1.05rem, 2.4vw, 1.35rem);
    color: var(--blush);
    max-width: 520px;
  }
  .hero-date{
    margin-top: 40px;
    display:flex;
    align-items:center;
    gap: 18px;
    font-family:'Cormorant Garamond', serif;
  }
  .hero-date .num{
    font-size: clamp(2.4rem, 6vw, 3.4rem);
    color: var(--gold-light);
    letter-spacing: 0.04em;
  }
  .hero-date .div{ width:1px; height: 46px; background: rgba(198,161,91,0.5); }
  .hero-date .venue{
    text-align:left;
    font-size: 0.95rem;
    letter-spacing: 0.03em;
    color: var(--blush);
    max-width: 160px;
  }
  .scroll-cue{
    position:absolute;
    bottom: 28px;
    font-size: 11px;
    letter-spacing: 0.3em;
    text-transform: uppercase;
    color: var(--gold);
    opacity: 0.75;
    display:flex;
    flex-direction: column;
    align-items:center;
    gap:8px;
  }
  .scroll-cue .line{ width:1px; height: 30px; background: var(--gold); animation: pulse 2.2s ease-in-out infinite; }
  @keyframes pulse{ 0%,100%{ opacity:0.25; } 50%{ opacity:1; } }
  @media (prefers-reduced-motion: reduce){ .scroll-cue .line{ animation:none; } }

  /* ---------- divider ---------- */
  .divider{
    display:flex; align-items:center; justify-content:center; gap:14px;
    margin: 0 auto; padding: 0 24px;
    color: var(--gold);
  }
  .divider .rule{ height:1px; width: 64px; background: var(--gold); opacity:0.55; }

  /* ---------- section base ---------- */
  section{ padding: 96px 24px; }
  .container{ max-width: 720px; margin: 0 auto; text-align:center; }

  .section-title{
    font-size: clamp(1.7rem, 4vw, 2.3rem);
    font-weight: 500;
    color: var(--wine);
    margin: 22px 0 0;
  }

  /* ---------- invite text ---------- */
  .invite-text{
    font-family:'Cormorant Garamond', serif;
    font-style: italic;
    font-size: clamp(1.1rem, 2.6vw, 1.4rem);
    line-height: 1.75;
    color: var(--ink);
    margin-top: 28px;
  }

  /* ---------- details ---------- */
  .details{ background: var(--wine); color: var(--gold-light); }
  .details .section-title{ color: var(--gold-light); }
  .cards{
    display:grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 28px;
    margin-top: 48px;
  }
  .card{
    background: rgba(246,239,228,0.04);
    border: 1px solid rgba(198,161,91,0.35);
    border-radius: 2px;
    padding: 32px 22px;
  }
  .card svg{ width: 34px; height:34px; margin-bottom: 16px; }
  .card h3{
    font-family:'Cormorant Garamond', serif;
    letter-spacing: 0.08em;
    text-transform: uppercase;
    font-size: 0.82rem;
    color: var(--gold);
    margin: 0 0 10px;
  }
  .card p{ margin:0; font-size: 1.02rem; line-height:1.5; color: var(--cream); }
  .card .note{ font-family:'Cormorant Garamond', serif; font-style: italic; font-size:0.85rem; color: var(--blush); margin-top:8px; }

  /* ---------- countdown ---------- */
  .countdown{
    display:flex; justify-content:center; gap: clamp(14px,4vw,34px);
    margin-top: 56px; flex-wrap: wrap;
  }
  .cd-unit{ text-align:center; min-width: 74px; }
  .cd-num{
    font-family:'Cormorant Garamond', serif;
    font-size: clamp(2rem, 5vw, 2.8rem);
    color: var(--gold-light);
    line-height:1;
  }
  .cd-label{
    margin-top: 8px;
    font-size: 10.5px;
    letter-spacing: 0.22em;
    text-transform: uppercase;
    color: var(--blush);
  }

  /* ---------- rsvp ---------- */
  .rsvp{ background: var(--cream); }
  .rsvp-frame{
    margin-top: 42px;
    border: 1px solid var(--blush);
    background: #fff;
    box-shadow: 0 30px 60px -30px rgba(92,31,46,0.35);
    padding: 6px;
  }
  .rsvp-frame iframe{
    width:100%;
    height: 760px;
    border:0;
    display:block;
  }
  @media (max-width: 480px){
    .rsvp-frame iframe{ height: 900px; }
  }

  /* ---------- footer ---------- */
  footer{
    background: var(--wine-deep);
    color: var(--blush);
    text-align:center;
    padding: 56px 24px 44px;
    font-family:'Cormorant Garamond', serif;
    font-style: italic;
  }
  footer .monogram{ color: var(--gold); font-size: 1.4rem; margin-bottom: 14px; }
</style>
</head>
<body>

<!-- HERO -->
<section class="hero">
  <div class="frame-line"></div>
  <svg class="buta" width="86" height="130" viewBox="0 0 86 130" style="margin-bottom:20px;" aria-hidden="true">
    <path d="M43 4 C 74 22, 80 58, 58 86 C 46 101, 46 112, 60 122" fill="none" stroke="#C6A15B" stroke-width="1.4"/>
    <path d="M43 4 C 12 22, 6 58, 28 86 C 40 101, 40 112, 26 122" fill="none" stroke="#C6A15B" stroke-width="1.4"/>
    <circle cx="43" cy="4" r="3" fill="#C6A15B"/>
  </svg>
  <div class="eyebrow reveal">Toy dəvətnaməsi</div>
  <h1 class="names reveal">Sərdar<span class="amp">&amp;</span>Şəms</h1>
  <p class="hero-sub reveal">Bir arzu, iki ürək, sonsuza qədər bir yol&hellip;</p>
  <div class="hero-date reveal">
    <span class="num">09.09</span>
    <span class="div"></span>
    <span class="venue">2026-cı il<br>Ma Donna Şadlıq Sarayı</span>
  </div>
  <div class="scroll-cue"><span>aşağı</span><span class="line"></span></div>
</section>

<!-- INVITATION TEXT -->
<section>
  <div class="container">
    <div class="divider reveal"><span class="rule"></span><svg width="18" height="18" viewBox="0 0 18 18"><path d="M9 1 C15 5,16 12,10 16 C9 17,9 17.5,10.5 18" fill="none" stroke="#C6A15B" stroke-width="1.2"/><path d="M9 1 C3 5,2 12,8 16 C9 17,9 17.5,7.5 18" fill="none" stroke="#C6A15B" stroke-width="1.2"/></svg><span class="rule"></span></div>
    <h2 class="section-title reveal">Sizi dəvət edirik</h2>
    <p class="invite-text reveal">
      Ömrümüzün ən mənalı günündə yanımızda sevdiklərimizin olmasını arzulayırıq.
      Sərdar və Şəms olaraq, sizi toy mərasimimizdə şahid olmağa, bizimlə birgə
      sevinməyə və bu unudulmaz axşamı bölüşməyə dəvət edirik.
    </p>
  </div>
</section>

<!-- DETAILS -->
<section class="details">
  <div class="container">
    <div class="eyebrow reveal" style="color:var(--gold);">Mərasim haqqında</div>
    <h2 class="section-title reveal">Tarix və məkan</h2>
    <div class="cards">
      <div class="card reveal">
        <svg viewBox="0 0 24 24" fill="none" stroke="#C6A15B" stroke-width="1.3"><rect x="3" y="5" width="18" height="16" rx="1"/><path d="M3 9h18M8 3v4M16 3v4"/></svg>
        <h3>Tarix</h3>
        <p>09 Sentyabr 2026<br>Çərşənbə</p>
      </div>
      <div class="card reveal">
        <svg viewBox="0 0 24 24" fill="none" stroke="#C6A15B" stroke-width="1.3"><circle cx="12" cy="12" r="9"/><path d="M12 7v5l3.5 2"/></svg>
        <h3>Vaxt</h3>
        <p>Axşam saat 18:00</p>
        <p class="note">Çox güman ki 19:00</p>
      </div>
      <div class="card reveal">
        <svg viewBox="0 0 24 24" fill="none" stroke="#C6A15B" stroke-width="1.3"><path d="M12 21s7-6.5 7-12a7 7 0 0 0-14 0c0 5.5 7 12 7 12z"/><circle cx="12" cy="9" r="2.4"/></svg>
        <h3>Məkan</h3>
        <p>Ma Donna<br>Şadlıq Sarayı</p>
      </div>
    </div>

    <div class="countdown reveal" id="countdown">
      <div class="cd-unit"><div class="cd-num" data-unit="days">00</div><div class="cd-label">gün</div></div>
      <div class="cd-unit"><div class="cd-num" data-unit="hours">00</div><div class="cd-label">saat</div></div>
      <div class="cd-unit"><div class="cd-num" data-unit="minutes">00</div><div class="cd-label">dəqiqə</div></div>
      <div class="cd-unit"><div class="cd-num" data-unit="seconds">00</div><div class="cd-label">saniyə</div></div>
    </div>
  </div>
</section>

<!-- RSVP -->
<section class="rsvp">
  <div class="container">
    <div class="divider reveal"><span class="rule"></span><svg width="18" height="18" viewBox="0 0 18 18"><path d="M9 1 C15 5,16 12,10 16 C9 17,9 17.5,10.5 18" fill="none" stroke="#C6A15B" stroke-width="1.2"/><path d="M9 1 C3 5,2 12,8 16 C9 17,9 17.5,7.5 18" fill="none" stroke="#C6A15B" stroke-width="1.2"/></svg><span class="rule"></span></div>
    <div class="eyebrow reveal" style="color:var(--gold);">İştirakınızı bildirin</div>
    <h2 class="section-title reveal">Cavabınızı gözləyirik</h2>
    <p class="invite-text reveal" style="font-size:1.05rem;">Aşağıdakı formu doldurmaqla iştirakınızı təsdiq edə bilərsiniz.</p>
    <div class="rsvp-frame reveal">
      <iframe src="https://docs.google.com/forms/d/e/1FAIpQLSdOib1fJG00uGmWhcfUhw5lSw3P8DDMvNca_OM-xaDo1CIdtg/viewform?embedded=true" title="RSVP Formu">Yüklənir…</iframe>
    </div>
  </div>
</section>

<footer>
  <div class="monogram">S &middot; Ş</div>
  <p>Sevginizlə yanımızda olacağınız günü səbirsizliklə gözləyirik.</p>
</footer>

<script>
  // Reveal on scroll
  const els = document.querySelectorAll('.reveal');
  if ('IntersectionObserver' in window){
    const io = new IntersectionObserver((entries)=>{
      entries.forEach(e=>{ if(e.isIntersecting){ e.target.classList.add('in'); io.unobserve(e.target); } });
    }, { threshold: 0.15 });
    els.forEach(el=>io.observe(el));
  } else {
    els.forEach(el=>el.classList.add('in'));
  }

  // Countdown — 09 Sept 2026, 19:00 Baku time (UTC+4)
  const target = new Date('2026-09-09T19:00:00+04:00').getTime();
  function updateCountdown(){
    const now = Date.now();
    const diff = Math.max(0, target - now);
    const d = Math.floor(diff / 86400000);
    const h = Math.floor((diff % 86400000) / 3600000);
    const m = Math.floor((diff % 3600000) / 60000);
    const s = Math.floor((diff % 60000) / 1000);
    const set = (unit, val)=>{ const el = document.querySelector(`[data-unit="${unit}"]`); if(el) el.textContent = String(val).padStart(2,'0'); };
    set('days', d); set('hours', h); set('minutes', m); set('seconds', s);
  }
  updateCountdown();
  setInterval(updateCountdown, 1000);
</script>

</body>
</html>
