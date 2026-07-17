<html lang="az">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover">
<meta name="format-detection" content="telephone=no, date=no, address=no, email=no">
<meta name="theme-color" content="#EFE3CB">
<title>Sərdar &amp; Şəms — Toy Dəvətnaməsi</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Noto+Serif:ital,wght@0,400;0,500;0,600;1,400;1,500&family=Cormorant+Garamond:ital,wght@0,400;0,500;0,600;1,400;1,500;1,600&display=swap" rel="stylesheet">
<style>
  :root{
    --page: #EFE3CB;
    --card: #F8F0DC;
    --gold: #A9803F;
    --gold-light: #C9A24B;
    --gold-deep: #7C5B26;
    --ink: #3E3123;
    --ink-soft: #6B5A42;
    --blush: #E7D3C9;
  }
  *{ box-sizing: border-box; }
  header, footer, section, div{ display:block; }
  html{
    scroll-behavior: smooth;
    -webkit-text-size-adjust: 100%;
    text-size-adjust: 100%;
  }
  body{
    margin:0;
    background: var(--page);
    color: var(--ink);
    font-family: 'Noto Serif', Georgia, 'Times New Roman', serif;
    -webkit-font-smoothing: antialiased;
    text-rendering: optimizeLegibility;
    -webkit-tap-highlight-color: transparent;
    overflow-x: hidden;
    width: 100%;
  }
  a{ color: inherit; text-decoration: none; }
  .accent{ font-family: 'Cormorant Garamond', serif; }

  .reveal{ opacity:0; transform: translateY(24px); transition: opacity 0.9s ease, transform 0.9s ease; }
  .reveal.in{ opacity:1; transform: translateY(0); }
  @media (prefers-reduced-motion: reduce){ .reveal{ opacity:1; transform:none; transition:none; } }

  /* ================= HERO / INVITATION CARD ================= */
  .hero-wrap{
    min-height: 100vh;
    padding: 64px 16px;
    text-align: center;
    background:
      radial-gradient(140% 100% at 50% 0%, #F5EAD3 0%, #EFE3CB 55%, #E7D8B9 100%);
  }
  .invite-card{
    position: relative;
    width: 100%;
    max-width: 620px;
    margin: 0 auto;
    background: var(--card);
    padding: 56px 34px 60px;
    text-align:center;
    box-shadow: 0 40px 80px -40px rgba(124,91,38,0.35);
  }
  /* outer + inner hairline border, arched top like the reference */
  .card-border{
    position:absolute; top:14px; right:14px; bottom:14px; left:14px;
    border: 1px solid var(--gold);
    pointer-events:none;
  }
  .card-border::before{
    content:"";
    position:absolute; top:7px; right:7px; bottom:7px; left:7px;
    border: 1px solid rgba(169,128,63,0.55);
  }
  .card-border .corner{
    position:absolute; width:26px; height:26px; border: 1px solid var(--gold);
  }
  .card-border .corner.tl{ top:-1px; left:-1px; border-right:none; border-bottom:none; }
  .card-border .corner.tr{ top:-1px; right:-1px; border-left:none; border-bottom:none; }
  .card-border .corner.bl{ bottom:-1px; left:-1px; border-right:none; border-top:none; }
  .card-border .corner.br{ bottom:-1px; right:-1px; border-left:none; border-top:none; }

  /* floral corner ornaments (hand-drawn line art, not photographic) */
  .floral{ position:absolute; width: 120px; height:120px; opacity: 0.9; }
  .floral.c-tl{ top:-18px; left:-18px; }
  .floral.c-br{ bottom:-18px; right:-18px; transform: rotate(180deg); }

  @media (max-width: 380px){
    .invite-card{ padding: 44px 20px 48px; }
    .floral{ width: 84px; height: 84px; }
    .floral.c-tl{ top:-10px; left:-10px; }
    .floral.c-br{ bottom:-10px; right:-10px; }
  }

  .eyebrow{
    letter-spacing: 0.28em;
    text-transform: uppercase;
    font-size: 11.5px;
    color: var(--gold-deep);
    margin: 8px 0 22px;
  }
  .flourish{ margin: 0 auto 22px; display:block; }

  .names{
    margin: 4px 0 0;
    font-family: 'Cormorant Garamond', 'Times New Roman', serif;
    font-style: italic;
    font-weight: 600;
    line-height: 1.05;
    color: var(--gold-deep); /* solid-color fallback if gradient text isn't supported */
  }
  @supports ((-webkit-background-clip: text) or (background-clip: text)){
    .names{
      background: linear-gradient(180deg, #C9A24B 0%, #8C6B32 100%);
      -webkit-background-clip: text;
      background-clip: text;
      -webkit-text-fill-color: transparent;
      color: transparent;
    }
  }
  .names .n1{ font-size: clamp(3.2rem, 12vw, 4.6rem); display:block; }
  .names .n2{ font-size: clamp(3.2rem, 12vw, 4.6rem); display:block; margin-top: -6px; }
  .name-divider{ margin: 6px auto 10px; }

  .invite-line{
    margin-top: 20px;
    font-size: 1.02rem;
    color: var(--ink-soft);
  }
  .small-rule{ width:70px; height:1px; background: var(--gold); opacity:0.6; margin: 16px auto; }

  .hero-date-big{
    font-family: 'Cormorant Garamond', serif;
    font-weight: 600;
    font-size: clamp(2.2rem, 7vw, 3rem);
    letter-spacing: 0.06em;
    color: var(--gold-deep);
    margin-top: 4px;
  }
  .hero-time{ margin-top: 14px; font-size: 1.05rem; color: var(--ink); }
  .venue-name{
    margin-top: 16px;
    font-weight: 600;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    font-size: 1.15rem;
    color: var(--ink);
  }
  .venue-sub{ font-size: 1rem; color: var(--ink-soft); margin-top: 2px; }
  .venue-address{
    margin-top: 16px;
    font-family: 'Cormorant Garamond', serif;
    font-style: italic;
    font-size: 1.02rem;
    color: var(--ink-soft);
  }

  /* ================= divider between sections ================= */
  .divider{
    display:flex; align-items:center; justify-content:center; gap:14px;
    margin: 0 auto; padding: 0 24px;
    color: var(--gold);
  }
  .divider .rule{ height:1px; width: 64px; background: var(--gold); opacity:0.55; }

  section{ padding: 88px 24px; }
  .container{ max-width: 720px; margin: 0 auto; text-align:center; }

  .section-title{
    font-size: clamp(1.6rem, 4vw, 2.1rem);
    font-weight: 500;
    color: var(--gold-deep);
    margin: 18px 0 0;
    font-family: 'Cormorant Garamond', serif;
    font-style: italic;
  }

  .invite-text{
    font-family:'Cormorant Garamond', serif;
    font-style: italic;
    font-size: clamp(1.1rem, 2.6vw, 1.4rem);
    line-height: 1.75;
    color: var(--ink);
    margin-top: 26px;
  }

  /* ================= details ================= */
  .details{ background: #F3E7CC; border-top: 1px solid var(--blush); border-bottom: 1px solid var(--blush); }
  .cards{
    display:grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 26px;
    margin-top: 46px;
  }
  .card{
    background: var(--card);
    border: 1px solid rgba(169,128,63,0.35);
    padding: 30px 20px;
  }
  .card svg{ width: 32px; height:32px; margin-bottom: 14px; }
  .card h3{
    font-family:'Cormorant Garamond', serif;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    font-size: 0.8rem;
    color: var(--gold-deep);
    margin: 0 0 8px;
  }
  .card p{ margin:0; font-size: 1rem; line-height:1.5; color: var(--ink); }

  /* ================= countdown ================= */
  .countdown{
    display:flex; justify-content:center; gap: clamp(14px,4vw,32px);
    margin-top: 52px; flex-wrap: wrap;
  }
  .cd-unit{ text-align:center; min-width: 70px; }
  .cd-num{
    font-family:'Cormorant Garamond', serif;
    font-size: clamp(1.9rem, 5vw, 2.6rem);
    color: var(--gold-deep);
    line-height:1;
  }
  .cd-label{
    margin-top: 8px;
    font-size: 10px;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    color: var(--ink-soft);
  }
  @media (max-width: 380px){
    section{ padding: 64px 18px; }
    .cards{ gap: 18px; margin-top: 36px; }
    .card{ padding: 24px 16px; }
    .countdown{ gap: 12px; margin-top: 38px; }
    .cd-unit{ min-width: 60px; }
  }

  /* ================= rsvp ================= */
  .rsvp-frame{
    margin-top: 40px;
    border: 1px solid var(--gold);
    background: #fff;
    box-shadow: 0 30px 60px -30px rgba(124,91,38,0.3);
    padding: 6px;
  }
  .rsvp-frame iframe{ width:100%; height: 760px; border:0; display:block; -webkit-overflow-scrolling: touch; }
  @media (max-width: 480px){ .rsvp-frame iframe{ height: 900px; } }
  .rsvp-fallback{
    margin-top: 16px;
    font-family:'Cormorant Garamond', serif;
    font-style: italic;
    font-size: 0.95rem;
    color: var(--ink-soft);
  }
  .rsvp-fallback a{ color: var(--gold-deep); text-decoration: underline; }

  /* ================= footer ================= */
  footer{
    background: var(--gold-deep);
    color: #F3E7CC;
    text-align:center;
    padding: 50px 24px 40px;
    font-family:'Cormorant Garamond', serif;
    font-style: italic;
  }
  footer .monogram{ color: #F3E7CC; font-size: 1.3rem; margin-bottom: 12px; letter-spacing: 0.1em; }
  @media (max-width: 380px){
    footer{ padding: 40px 18px 32px; }
  }
</style>
</head>
<body>

<!-- HERO INVITATION CARD -->
<div class="hero-wrap">
  <div class="invite-card">
    <div class="card-border">
      <span class="corner tl"></span><span class="corner tr"></span>
      <span class="corner bl"></span><span class="corner br"></span>
    </div>

    <!-- floral line-art ornaments, top-left / bottom-right -->
    <svg class="floral c-tl" viewBox="0 0 120 120" aria-hidden="true">
      <g fill="none" stroke="#A9803F" stroke-width="1.1">
        <path d="M14 70 C 10 50, 20 30, 40 20 C 55 12, 70 14, 78 22"/>
        <path d="M20 62 C 30 55, 34 44, 30 34"/>
        <path d="M28 76 C 40 70, 46 58, 42 46"/>
        <circle cx="30" cy="30" r="9"/>
        <circle cx="44" cy="20" r="6.5"/>
        <circle cx="18" cy="46" r="5.5"/>
        <path d="M56 16 C 62 20, 66 26, 64 34"/>
        <path d="M62 12 C 68 16, 72 22, 70 30"/>
      </g>
    </svg>
    <svg class="floral c-br" viewBox="0 0 120 120" aria-hidden="true">
      <g fill="none" stroke="#A9803F" stroke-width="1.1">
        <path d="M14 70 C 10 50, 20 30, 40 20 C 55 12, 70 14, 78 22"/>
        <path d="M20 62 C 30 55, 34 44, 30 34"/>
        <path d="M28 76 C 40 70, 46 58, 42 46"/>
        <circle cx="30" cy="30" r="9"/>
        <circle cx="44" cy="20" r="6.5"/>
        <circle cx="18" cy="46" r="5.5"/>
        <path d="M56 16 C 62 20, 66 26, 64 34"/>
        <path d="M62 12 C 68 16, 72 22, 70 30"/>
      </g>
    </svg>

    <div class="eyebrow">Birlikdə bir ömür, sevgi ilə&hellip;</div>

    <svg class="flourish" width="120" height="20" viewBox="0 0 120 20" aria-hidden="true">
      <path d="M4 10 H44" stroke="#A9803F" stroke-width="1"/>
      <path d="M76 10 H116" stroke="#A9803F" stroke-width="1"/>
      <path d="M50 10 C 54 4, 60 4, 60 10 C 60 4, 66 4, 70 10 C 66 12, 64 16, 60 14 C 56 16, 54 12, 50 10 Z" fill="#A9803F"/>
    </svg>

    <h1 class="names">
      <span class="n1">Sərdar</span>
      <svg class="name-divider" width="18" height="18" viewBox="0 0 18 18" aria-hidden="true"><path d="M9 3 C 12 0, 17 3, 17 7 C 17 11, 12 13, 9 16 C 6 13, 1 11, 1 7 C 1 3, 6 0, 9 3 Z" fill="#A9803F"/></svg>
      <span class="n2">Şəms</span>
    </h1>

    <p class="invite-line accent">Sizi toy mərasimimizə dəvət edirik</p>
    <div class="small-rule"></div>

    <div class="hero-date-big">09.09.2026</div>
    <div class="hero-time">Saat: 18:00</div>

    <div class="small-rule"></div>
    <div class="venue-name">Ma Donna</div>
    <div class="venue-sub">Şadlıq Sarayı</div>
    <div class="venue-address">Ünvan: 24 Mehdi Abbasov, Baku</div>
  </div>
</div>

<!-- INVITATION TEXT -->
<section>
  <div class="container">
    <div class="divider reveal"><span class="rule"></span><svg width="18" height="18" viewBox="0 0 18 18"><path d="M9 1 C15 5,16 12,10 16 C9 17,9 17.5,10.5 18" fill="none" stroke="#A9803F" stroke-width="1.2"/><path d="M9 1 C3 5,2 12,8 16 C9 17,9 17.5,7.5 18" fill="none" stroke="#A9803F" stroke-width="1.2"/></svg><span class="rule"></span></div>
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
    <div class="eyebrow reveal" style="color:var(--gold-deep);">Mərasim haqqında</div>
    <h2 class="section-title reveal">Tarix və məkan</h2>
    <div class="cards">
      <div class="card reveal">
        <svg viewBox="0 0 24 24" fill="none" stroke="#A9803F" stroke-width="1.3"><rect x="3" y="5" width="18" height="16" rx="1"/><path d="M3 9h18M8 3v4M16 3v4"/></svg>
        <h3>Tarix</h3>
        <p>09 Sentyabr 2026<br>Çərşənbə</p>
      </div>
      <div class="card reveal">
        <svg viewBox="0 0 24 24" fill="none" stroke="#A9803F" stroke-width="1.3"><circle cx="12" cy="12" r="9"/><path d="M12 7v5l3.5 2"/></svg>
        <h3>Vaxt</h3>
        <p>Saat 18:00</p>
      </div>
      <div class="card reveal">
        <svg viewBox="0 0 24 24" fill="none" stroke="#A9803F" stroke-width="1.3"><path d="M12 21s7-6.5 7-12a7 7 0 0 0-14 0c0 5.5 7 12 7 12z"/><circle cx="12" cy="9" r="2.4"/></svg>
        <h3>Məkan</h3>
        <p>Ma Donna Şadlıq Sarayı<br>24 Mehdi Abbasov, Baku</p>
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
    <div class="divider reveal"><span class="rule"></span><svg width="18" height="18" viewBox="0 0 18 18"><path d="M9 1 C15 5,16 12,10 16 C9 17,9 17.5,10.5 18" fill="none" stroke="#A9803F" stroke-width="1.2"/><path d="M9 1 C3 5,2 12,8 16 C9 17,9 17.5,7.5 18" fill="none" stroke="#A9803F" stroke-width="1.2"/></svg><span class="rule"></span></div>
    <div class="eyebrow reveal" style="color:var(--gold-deep);">İştirakınızı bildirin</div>
    <h2 class="section-title reveal">Cavabınızı gözləyirik</h2>
    <p class="invite-text reveal" style="font-size:1.05rem;">Aşağıdakı formu doldurmaqla iştirakınızı təsdiq edə bilərsiniz.</p>
    <div class="rsvp-frame reveal">
      <iframe src="https://docs.google.com/forms/d/e/1FAIpQLSdOib1fJG00uGmWhcfUhw5lSw3P8DDMvNca_OM-xaDo1CIdtg/viewform?embedded=true" title="RSVP Formu" loading="lazy" referrerpolicy="no-referrer-when-downgrade">Yüklənir…</iframe>
    </div>
    <p class="rsvp-fallback reveal">
      Form açılmırsa,
      <a href="https://forms.gle/pB8bmvZjFLZdc6y37" target="_blank" rel="noopener">bura klikləyin</a>.
    </p>
  </div>
</section>

<footer>
  <div class="monogram">S &middot; Ş</div>
  <p>Sevginizlə yanımızda olacağınız günü səbirsizliklə gözləyirik.</p>
</footer>

<script>
  const els = document.querySelectorAll('.reveal');
  if ('IntersectionObserver' in window){
    const io = new IntersectionObserver((entries)=>{
      entries.forEach(e=>{ if(e.isIntersecting){ e.target.classList.add('in'); io.unobserve(e.target); } });
    }, { threshold: 0.15 });
    els.forEach(el=>io.observe(el));
  } else { els.forEach(el=>el.classList.add('in')); }

  // Countdown — 09 Sept 2026, 18:00 Baku time (UTC+4)
  const target = new Date('2026-09-09T18:00:00+04:00').getTime();
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
