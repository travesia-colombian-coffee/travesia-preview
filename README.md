
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Travesía — A story in every cup</title>
<meta name="description" content="Specialty Colombian coffee born between Santander and New York. Crafted to bring you back.">
<meta property="og:title" content="Travesía — A story in every cup">
<meta property="og:description" content="Specialty Colombian coffee born between Santander and New York. Crafted to bring you back.">
<meta property="og:type" content="website">
<link rel="icon" type="image/png" href="assets/symbol-color.png">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,500;0,600;1,300;1,400;1,500&family=DM+Sans:wght@300;400;500&display=swap" rel="stylesheet">
<style>
/* ===========================================================
   TRAVESÍA — Home · Paleta oficial de marca · Editorial/cinematográfico
   Dos fases (Early Access / Preventa): ver SITE_PHASE en el script.
   =========================================================== */
:root{
  --coffee:#473224; --coffee-deep:#3d2a1c; --night:#3d2a1c;
  --teal:#018E86; --teal-deep:#09685F;
  --gold:#BE9F56; --gold-soft:#cdb877;
  --beige:#E1D6C0; --paper:#F2EADB; --cream:#FAF8F4; --ink:#2e2014;
  --font-hero:'Cormorant Garamond',serif;
  --font-display:'Cormorant Garamond',serif;
  --font-serif:'Cormorant Garamond',serif;
  --font-sans:'DM Sans',system-ui,sans-serif;
}
*{margin:0;padding:0;box-sizing:border-box;}
html{scroll-behavior:smooth;}
body{background:var(--paper);color:var(--ink);font-family:var(--font-serif);-webkit-font-smoothing:antialiased;overflow-x:hidden;}
img{display:block;max-width:100%;}a{color:inherit;text-decoration:none;}
button{font-family:inherit;cursor:pointer;border:none;background:none;}
a:focus-visible,button:focus-visible,input:focus-visible,select:focus-visible{outline:2px solid var(--gold);outline-offset:3px;}
.only-ea,.only-po{display:none;}
/* Grano cinematográfico */
body::after{content:"";position:fixed;inset:0;z-index:9999;pointer-events:none;opacity:.03;mix-blend-mode:overlay;background-image:url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='120' height='120'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.85' numOctaves='2'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)'/%3E%3C/svg%3E");}
.eyebrow{font-family:var(--font-sans);font-size:11px;font-weight:400;text-transform:uppercase;letter-spacing:.30em;color:var(--gold);}
.chapter{font-family:var(--font-sans);font-size:11px;text-transform:uppercase;letter-spacing:.34em;color:var(--teal-deep);display:inline-flex;align-items:center;gap:14px;}
.chapter::before{content:"";width:36px;height:1px;background:var(--teal-deep);}
.seam{height:1px;background:linear-gradient(90deg,transparent,var(--gold),transparent);}
.reveal{opacity:1;transform:none;}
.reveal.in{opacity:1;transform:none;}
/* ===== Navbar ===== */
.nav{position:fixed;top:0;left:0;right:0;z-index:100;height:72px;display:grid;grid-template-columns:auto 1fr auto;align-items:center;padding:0 24px;background:transparent;transition:background .35s ease,backdrop-filter .35s ease;}
.nav.scrolled{background:rgba(58,39,25,.94);backdrop-filter:blur(8px);-webkit-backdrop-filter:blur(8px);}
.nav__logo{justify-self:center;line-height:0;}
.nav__logo img{height:34px;width:auto;max-width:170px;object-fit:contain;}
.nav__links{display:none;gap:36px;justify-content:center;list-style:none;}
.nav__links a{font-family:var(--font-sans);font-size:13px;text-transform:uppercase;letter-spacing:.12em;color:var(--cream);transition:color .2s;}
.nav__links a:hover{color:var(--gold);}
.nav__right{display:flex;align-items:center;gap:20px;justify-self:end;}
.lang{display:flex;align-items:center;gap:6px;font-family:var(--font-sans);font-size:13px;text-transform:uppercase;letter-spacing:.12em;}
.lang button{color:var(--cream);transition:color .2s;}.lang button.active{color:var(--gold);}
.lang span{color:var(--beige);opacity:.5;}
.cart{color:var(--cream);width:22px;height:22px;}
.burger{color:var(--cream);justify-self:start;display:flex;flex-direction:column;gap:5px;padding:6px 0;}
.burger span{width:24px;height:1.5px;background:currentColor;display:block;}
.mobile-menu{position:fixed;inset:0;z-index:99;background:var(--coffee-deep);display:flex;flex-direction:column;justify-content:center;align-items:center;gap:32px;transform:translateX(-100%);transition:transform .35s;}
.mobile-menu.open{transform:translateX(0);}
.mobile-menu a{font-family:var(--font-sans);font-size:15px;text-transform:uppercase;letter-spacing:.12em;color:var(--cream);}
.mobile-menu .mm-social{display:flex;gap:24px;margin-top:24px;color:var(--beige);}
.mobile-menu .mm-close{position:absolute;top:24px;right:24px;color:var(--cream);font-size:28px;}
@media(min-width:980px){.nav{height:80px;padding:0 80px;}.nav__logo{justify-self:start;}.nav__logo img{height:42px;max-width:230px;}.nav__links{display:flex;}.burger{display:none;}.mobile-menu{display:none;}}
/* ===== Hero — title card cinematográfico ===== */
.hero{position:relative;min-height:100vh;display:flex;flex-direction:column;align-items:center;justify-content:center;text-align:center;padding:120px 24px;overflow:hidden;
  background:radial-gradient(120% 80% at 50% 30%,rgba(1,142,134,0) 30%,rgba(58,39,25,.28) 100%),radial-gradient(140% 110% at 50% 8%,#15a89d 0%,var(--teal) 30%,var(--teal-deep) 62%,#0b5d54 100%);}
.hero__bar{display:none;}
.hero__bar.top{top:0;border-bottom:1px solid rgba(190,159,86,.4);}
.hero__bar.bottom{bottom:0;border-top:1px solid rgba(190,159,86,.4);}
.hero__inner{position:relative;z-index:2;max-width:640px;}
.hero__eyebrow{color:var(--gold-soft);margin-bottom:24px;opacity:0;animation:rise 1.4s ease .5s forwards;}
.hero h1{font-family:var(--font-hero);font-weight:400;color:var(--cream);font-size:clamp(46px,9.5vw,104px);line-height:1.0;opacity:0;animation:rise 1.6s ease .8s forwards;}
.hero__sub{font-family:var(--font-serif);font-style:italic;font-weight:300;color:rgba(250,248,244,.82);font-size:clamp(16px,2.3vw,21px);margin:22px auto 0;max-width:36ch;opacity:0;animation:rise 1.6s ease 1.3s forwards;}
.hero__actions{display:flex;flex-wrap:wrap;gap:16px;justify-content:center;margin-top:34px;opacity:0;animation:rise 1.6s ease 1.7s forwards;}
@keyframes rise{to{opacity:1;transform:none;}}
.btn-primary{font-family:var(--font-sans);font-size:12px;font-weight:500;text-transform:uppercase;letter-spacing:.16em;background:var(--gold);color:var(--coffee);padding:16px 38px;border-radius:0;display:inline-block;transition:background .25s;}
.btn-primary:hover{background:var(--gold-soft);}
.btn-secondary{font-family:var(--font-sans);font-size:12px;font-weight:500;text-transform:uppercase;letter-spacing:.16em;background:transparent;color:var(--cream);padding:16px 38px;border-radius:0;border:1px solid rgba(250,248,244,.45);display:inline-block;transition:border-color .25s;}
.btn-secondary:hover{border-color:var(--cream);}
@media(min-width:980px){.hero h1{font-size:clamp(70px,8vw,104px);}}
/* ===== Capítulo I — Creencia (papel) ===== */
.belief{padding:clamp(96px,15vh,190px) 24px;text-align:center;background:var(--beige);}
.belief .chapter{margin-bottom:38px;}
.belief .chapter,.belief blockquote,.belief .rule{position:relative;z-index:2;}
.belief blockquote{font-family:var(--font-serif);font-weight:300;font-size:clamp(24px,4vw,40px);line-height:1.32;color:var(--ink);max-width:760px;margin:0 auto;}
.belief blockquote .accent{color:var(--teal-deep);font-style:italic;}
.belief .rule{width:54px;height:1px;background:var(--teal-deep);border:0;margin:46px auto 0;}
/* ===== Capítulo II — Raíces (café, cinematográfico) ===== */
.origin{position:relative;background:var(--coffee);color:var(--beige);padding:clamp(90px,12vh,150px) 24px;overflow:hidden;}
.origin::before{content:"";position:absolute;inset:0;background:radial-gradient(80% 80% at 30% 30%,rgba(0,0,0,0) 40%,rgba(58,39,25,.28) 100%);pointer-events:none;}
.origin__grid{position:relative;max-width:1140px;margin:0 auto;display:grid;grid-template-columns:1fr;gap:50px;align-items:center;}
.origin__still{aspect-ratio:3/4;background:radial-gradient(70% 60% at 50% 38%,#5e4230,var(--coffee-deep));border:1px solid rgba(190,159,86,.3);display:flex;align-items:flex-end;padding:24px;}
.lowerthird{font-family:var(--font-sans);font-size:11px;letter-spacing:.2em;text-transform:uppercase;color:var(--gold-soft);display:flex;align-items:center;gap:12px;}
.lowerthird::before{content:"";width:18px;height:1px;background:var(--gold);}
.origin__info .chapter{color:var(--gold);margin-bottom:22px;}
.origin__info .chapter::before{background:var(--gold);}
.origin__info h2{font-family:var(--font-display);font-size:clamp(36px,5.5vw,58px);color:var(--cream);margin-bottom:22px;line-height:1.04;}
.origin__info p{font-family:var(--font-serif);font-size:clamp(18px,2vw,21px);line-height:1.55;color:rgba(225,214,192,.9);max-width:44ch;}
.origin__info p .dropcap{float:left;font-family:var(--font-hero);font-size:3.2em;line-height:.8;color:var(--gold-soft);padding:6px 14px 0 0;}
.origin__notes{font-family:var(--font-sans);font-size:12px;letter-spacing:.06em;color:var(--gold-soft);margin:26px 0;}
.ea-note{font-family:var(--font-serif);font-style:italic;font-size:17px;color:rgba(225,214,192,.85);margin-bottom:22px;max-width:46ch;}
.price-line{margin-bottom:6px;}
.price-line .now{font-family:var(--font-serif);font-size:23px;color:var(--cream);}
.price-line .later{display:block;font-family:var(--font-sans);font-size:12px;font-weight:300;color:rgba(225,214,192,.6);letter-spacing:.04em;margin-top:6px;}
@media(min-width:920px){.origin__grid{grid-template-columns:.85fr 1.15fr;gap:90px;}}
/* ===== Interludio — tributo (teal inmersión) ===== */
.tribute{position:relative;padding:clamp(120px,18vh,210px) 24px;text-align:center;color:var(--cream);overflow:hidden;background:radial-gradient(120% 100% at 50% 40%,var(--teal) 0%,var(--teal-deep) 55%,#0b5d54 100%);}
.tribute::before{content:"";position:absolute;inset:0;background:radial-gradient(70% 70% at 50% 50%,rgba(0,0,0,0) 45%,rgba(11,93,84,.3) 100%);pointer-events:none;}
.tribute p{position:relative;max-width:660px;margin:0 auto;font-family:var(--font-serif);font-style:italic;font-weight:300;font-size:clamp(21px,3.2vw,32px);line-height:1.42;}
.tribute p .accent{font-style:normal;font-weight:500;color:var(--gold-soft);}
/* ===== Capítulo III — Film (papel) ===== */
.film{padding:clamp(90px,12vh,150px) 24px;text-align:center;background:var(--paper);}
.film .chapter{justify-content:center;margin-bottom:24px;}
.film__title{font-family:var(--font-display);font-size:clamp(28px,4vw,44px);color:var(--ink);max-width:600px;margin:0 auto 44px;line-height:1.15;}
.film__player{position:relative;aspect-ratio:16/9;max-width:880px;margin:0 auto;background:linear-gradient(135deg,#018E86,#0b5d54);display:flex;align-items:center;justify-content:center;border:1px solid rgba(190,159,86,.3);}
.film__play{width:74px;height:74px;border-radius:50%;border:1px solid rgba(250,248,244,.7);display:flex;align-items:center;justify-content:center;color:var(--cream);transition:background .25s;}
.film__play:hover{background:rgba(250,248,244,.12);}
.film .btn-secondary{margin-top:34px;border-color:var(--teal-deep);color:var(--teal-deep);}
.film .btn-secondary:hover{border-color:var(--coffee);color:var(--coffee);}
/* ===== Early Access (solo EA) ===== */
.ea{position:relative;background:var(--coffee-deep);color:var(--beige);padding:clamp(90px,12vh,150px) 24px;}
.ea__wrap{max-width:560px;margin:0 auto;text-align:center;}
.ea .chapter{justify-content:center;color:var(--gold);margin-bottom:18px;}
.ea .chapter::before{background:var(--gold);}
.ea h2{font-family:var(--font-display);font-size:clamp(28px,4vw,42px);color:var(--cream);margin-bottom:16px;}
.ea__lead{font-family:var(--font-serif);font-size:18px;color:rgba(225,214,192,.85);margin-bottom:34px;}
.ea form{display:grid;gap:14px;text-align:left;}
.ea label{font-family:var(--font-sans);font-size:11px;text-transform:uppercase;letter-spacing:.12em;color:var(--gold-soft);display:block;margin-bottom:6px;}
.ea input,.ea select{width:100%;background:rgba(0,0,0,.22);border:1px solid rgba(190,159,86,.3);color:var(--cream);padding:13px 14px;font-family:var(--font-sans);font-size:14px;}
.ea input::placeholder{color:rgba(225,214,192,.5);}
.ea select{appearance:none;}
.ea .row2{display:grid;grid-template-columns:1fr 1fr;gap:14px;}
.ea .consent{display:flex;gap:10px;align-items:flex-start;font-family:var(--font-sans);font-size:11px;color:rgba(225,214,192,.7);line-height:1.4;}
.ea .consent input{width:auto;margin-top:2px;}
.ea button[type=submit]{margin-top:8px;background:var(--gold);color:var(--coffee);padding:15px;font-family:var(--font-sans);font-size:12px;font-weight:500;text-transform:uppercase;letter-spacing:.16em;}
.ea button[type=submit]:hover{background:var(--gold-soft);}
.ea__thanks{display:none;}
.ea__thanks h2{margin-bottom:12px;}
.ea__thanks p{font-family:var(--font-serif);font-size:18px;color:rgba(225,214,192,.85);}
/* ===== Newsletter (papel) ===== */
.newsletter{background:var(--beige);padding:clamp(80px,10vh,120px) 24px;text-align:center;}
.newsletter h2{font-family:var(--font-display);font-size:clamp(26px,3.5vw,36px);color:var(--ink);margin-bottom:16px;}
.newsletter p{font-family:var(--font-serif);font-size:18px;color:var(--coffee);margin:0 auto 28px;max-width:520px;}
.newsletter__form{display:flex;gap:12px;max-width:480px;margin:0 auto;flex-wrap:wrap;justify-content:center;}
.newsletter__form input{flex:1;min-width:200px;background:transparent;border:1px solid rgba(71,50,36,.35);color:var(--ink);padding:14px 16px;font-family:var(--font-sans);font-size:14px;}
.newsletter__form input::placeholder{color:rgba(71,50,36,.5);}
.newsletter__form button{background:var(--teal-deep);color:var(--cream);padding:14px 28px;font-family:var(--font-sans);font-size:12px;font-weight:500;text-transform:uppercase;letter-spacing:.14em;}
.newsletter__form button:hover{background:var(--teal);}
.consent-inline{display:block;margin-top:16px;font-family:var(--font-sans);font-size:11px;color:var(--coffee);}
/* ===== Footer ===== */
.footer{background:var(--coffee-deep);color:var(--beige);padding:72px 24px 56px;}
.footer__grid{display:grid;grid-template-columns:1fr;gap:40px;max-width:1100px;margin:0 auto;}
.footer__brand .logo img{height:34px;width:auto;}
.footer__brand .tagline{font-family:var(--font-hero);font-size:17px;letter-spacing:.02em;color:rgba(225,214,192,.82);margin:16px 0 16px;}
.footer__social{display:flex;gap:18px;color:var(--beige);}
.footer__col h4{font-family:var(--font-sans);font-size:13px;text-transform:uppercase;letter-spacing:.12em;color:var(--gold);margin-bottom:16px;font-weight:500;}
.footer__col a{display:block;font-family:var(--font-sans);font-size:13px;font-weight:300;color:rgba(225,214,192,.8);margin-bottom:10px;transition:color .2s;}
.footer__col a:hover{color:var(--cream);}
.footer__copy{text-align:center;margin-top:48px;font-family:var(--font-sans);font-size:11px;color:rgba(225,214,192,.5);}
@media(min-width:980px){.footer{padding:80px 80px 56px;}.footer__grid{grid-template-columns:1.4fr 1fr 1fr;gap:64px;}}
@media(prefers-reduced-motion:reduce){.reveal{opacity:1;transform:none;transition:none;}.hero__eyebrow,.hero h1,.hero__sub,.hero__actions{animation:none;opacity:1;transform:none;}html{scroll-behavior:auto;}}
.origin__info h2,.film__title,.ea h2,.newsletter h2{font-weight:600;letter-spacing:-0.01em;}
</style>
</head>
<body>
<nav class="nav" id="nav">
  <button class="burger" id="burger" aria-label="Open menu"><span></span><span></span><span></span></button>
  <a href="index.html" class="nav__logo"><img src="assets/logo-horizontal-white.png" alt="Travesía — A Story in Every Cup"></a>
  <ul class="nav__links">
    <li><a href="#raices">Raíces</a></li>
    <li><a href="our-story.html" data-en="Our Story" data-es="Nuestra Historia">Our Story</a></li>
    <li><a href="#film">Film</a></li>
    <li><a href="#contact" data-en="Contact" data-es="Contacto">Contact</a></li>
  </ul>
  <div class="nav__right">
    <div class="lang"><button data-lang="en" class="active">EN</button><span>/</span><button data-lang="es">ES</button></div>
    <a href="raices.html" aria-label="Raices"><svg class="cart" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.4"><path d="M6 6h15l-1.5 9h-12z"/><circle cx="9" cy="20" r="1"/><circle cx="18" cy="20" r="1"/><path d="M6 6 5 3H2"/></svg></a>
  </div>
</nav>
<div class="mobile-menu" id="mobileMenu">
  <button class="mm-close" id="mmClose" aria-label="Close menu">&times;</button>
  <a href="#raices">Raíces</a>
  <a href="our-story.html" data-en="Our Story" data-es="Nuestra Historia">Our Story</a>
  <a href="#film">Film</a>
  <a href="#contact" data-en="Contact" data-es="Contacto">Contact</a>
  <div class="lang"><button data-lang="en" class="active">EN</button><span>/</span><button data-lang="es">ES</button></div>
  <div class="mm-social">Instagram · Facebook · Twitter</div>
</div>
<!-- HERO -->
<header class="hero">
  <div class="hero__bar top"></div>
  <div class="hero__inner">
    <p class="eyebrow hero__eyebrow">Colombia · New York</p>
    <h1 data-en="A story<br>in every cup." data-es="Una historia<br>en cada taza.">A story<br>in every cup.</h1>
    <p class="hero__sub" data-en="Specialty coffee born between Santander and New York. Crafted to bring you back." data-es="Café de especialidad entre Santander y New York. Hecho para traerte de vuelta.">Specialty coffee born between Santander and New York. Crafted to bring you back.</p>
    <div class="hero__actions">
      <a href="#early-access" class="btn-primary cta-main" data-track="PreorderClick" data-ea-en="Join Early Access" data-ea-es="Unirme al Early Access" data-po-en="Preorder Raíces" data-po-es="Reservar Raíces">Join Early Access</a>
      <a href="#film" class="btn-secondary" data-track="VideoClick" data-en="Watch the Film" data-es="Ver el Film">Watch the Film</a>
    </div>
  </div>
  <div class="hero__bar bottom"></div>
</header>
<!-- CAPÍTULO I — CREENCIA -->
<section class="belief">
  <span class="chapter" data-en="Chapter I — The Belief" data-es="Capítulo I — La Creencia">Chapter I — The Belief</span>
  <blockquote data-en='We believe the aroma of a cup can <span class="accent">awaken memories</span>, shorten distances, and remind us of who we are.' data-es='Creemos que el aroma de una taza puede <span class="accent">despertar memorias</span>, acortar distancias y recordarnos quiénes somos.'>We believe the aroma of a cup can <span class="accent">awaken memories</span>, shorten distances, and remind us of who we are.</blockquote>
  <hr class="rule">
</section>
<!-- CAPÍTULO II — RAÍCES -->
<section class="origin" id="raices">
  <div class="origin__grid">
    <div class="origin__still reveal"><span class="lowerthird">Raíces · 250g · Santander</span></div>
    <div class="origin__info reveal">
      <span class="chapter" data-en="Chapter II — The Origin" data-es="Capítulo II — El Origen">Chapter II — The Origin</span>
      <h2>Raíces</h2>
      <p data-en='<span class="dropcap">N</span>ot just the name of an edition. It is the point from which Travesía began to move — the first chapter of a longer journey.' data-es='<span class="dropcap">N</span>o es solo el nombre de una edición. Es el punto desde donde Travesía empezó a navegar — el primer capítulo de un viaje más largo.'><span class="dropcap">N</span>ot just the name of an edition. It is the point from which Travesía began to move — the first chapter of a longer journey.</p>
      <p class="origin__notes" data-en="Chocolate · Panela · Red fruits · Almond" data-es="Chocolate · Panela · Frutos rojos · Almendra">Chocolate · Panela · Red fruits · Almond</p>
      <p class="ea-note only-ea" data-en="The first edition is in preparation. Join the priority list for early access to the official preorder." data-es="La primera edición está en preparación. Únete a la lista prioritaria para recibir acceso anticipado a la preventa oficial.">The first edition is in preparation. Join the priority list for early access to the official preorder.</p>
      <div class="price-line only-po">
        <span class="now" data-en="Raíces — First Edition · $20.99" data-es="Raíces — Primera Edición · $20.99">Raíces — First Edition · $20.99</span>
        <span class="later" data-en="Editorial Edition · $24.50 after first release" data-es="Edición Editorial · $24.50 después del primer lanzamiento">Editorial Edition · $24.50 after first release</span>
      </div>
      <a href="#early-access" class="btn-primary cta-main" data-track="PreorderClick" data-ea-en="Join Early Access" data-ea-es="Unirme al Early Access" data-po-en="Preorder Raíces" data-po-es="Reservar Raíces" style="margin-top:30px">Join Early Access</a>
    </div>
  </div>
</section>
<!-- INTERLUDIO — TRIBUTO -->
<section class="tribute reveal">
  <p data-en='Travesía is <span class="accent">not just coffee</span>. It is a tribute to those who migrate, to those who dream, to those who love from afar.' data-es='Travesía <span class="accent">no es solo café</span>. Es un tributo a quienes migran, a quienes sueñan, a quienes aman desde lejos.'>Travesía is <span class="accent">not just coffee</span>. It is a tribute to those who migrate, to those who dream, to those who love from afar.</p>
</section>
<!-- CAPÍTULO III — FILM -->
<section class="film reveal" id="film">
  <span class="chapter" data-en="Chapter III — The Film" data-es="Capítulo III — El Film">Chapter III — The Film</span>
  <h2 class="film__title" data-en="Before being a store, Travesía was a question." data-es="Antes de ser una tienda, Travesía fue una pregunta.">Before being a store, Travesía was a question.</h2>
  <div class="film__player"><button class="film__play" data-track="VideoClick" aria-label="Play film"><svg width="22" height="22" viewBox="0 0 24 24" fill="currentColor"><path d="M8 5v14l11-7z"/></svg></button></div>
  <a href="our-story.html#film" class="btn-secondary" data-track="VideoClick" data-en="Watch the Film" data-es="Ver el Film">Watch the Film</a>
</section>
<!-- EARLY ACCESS -->
<section class="ea only-ea" id="early-access">
  <div class="ea__wrap">
    <div id="eaForm">
      <span class="chapter" data-en="Raíces — Early Access" data-es="Raíces — Early Access">Raíces — Early Access</span>
      <h2 data-en="Join the priority list." data-es="Únete a la lista prioritaria.">Join the priority list.</h2>
      <p class="ea__lead" data-en="Early Access members receive updates, priority access, and direct word on the official preorder opening." data-es="Los miembros del Early Access reciben actualizaciones, acceso prioritario y comunicación directa sobre la apertura de la preventa.">Early Access members receive updates, priority access, and direct word on the official preorder opening.</p>
      <form id="eaFormEl" novalidate>
        <div><label data-en="Name" data-es="Nombre">Name</label><input type="text" name="name" required data-en-ph="Your name" data-es-ph="Tu nombre" placeholder="Your name"></div>
        <div><label data-en="Email" data-es="Correo electrónico">Email</label><input type="email" name="email" required data-en-ph="you@email.com" data-es-ph="tu@correo.com" placeholder="you@email.com"></div>
        <div class="row2">
          <div><label data-en="City" data-es="Ciudad">City</label><input type="text" name="city" data-en-ph="City" data-es-ph="Ciudad" placeholder="City"></div>
          <div><label data-en="Country" data-es="País">Country</label><input type="text" name="country" data-en-ph="Country" data-es-ph="País" placeholder="Country"></div>
        </div>
        <div>
          <label data-en="What connects you most with Travesía?" data-es="¿Qué te conecta más con Travesía?">What connects you most with Travesía?</label>
          <select name="connection">
            <option value="colombian" data-en="Colombian coffee" data-es="Café colombiano">Colombian coffee</option>
            <option value="origin" data-en="Santander origin" data-es="Origen Santander">Santander origin</option>
            <option value="diaspora" data-en="Nostalgia / diaspora" data-es="Nostalgia / diáspora">Nostalgia / diaspora</option>
            <option value="gift" data-en="A gift" data-es="Regalo">A gift</option>
            <option value="specialty" data-en="Specialty coffee" data-es="Specialty coffee">Specialty coffee</option>
            <option value="film" data-en="The story / film" data-es="Historia / Film">The story / film</option>
            <option value="design" data-en="Design / brand" data-es="Diseño / marca">Design / brand</option>
            <option value="other" data-en="Other" data-es="Otro">Other</option>
          </select>
        </div>
        <label class="consent"><input type="checkbox" name="consent" required><span data-en="I authorize Travesía to store my data to send me updates about Early Access and the Raíces preorder." data-es="Autorizo a Travesía a guardar mis datos para enviarme actualizaciones sobre el Early Access y la preventa de Raíces.">I authorize Travesía to store my data to send me updates about Early Access and the Raíces preorder.</span></label>
        <button type="submit" data-en="Join Early Access" data-es="Unirme al Early Access">Join Early Access</button>
      </form>
    </div>
    <div class="ea__thanks" id="eaThanks">
      <h2 data-en="Thank you." data-es="Gracias.">Thank you.</h2>
      <p data-en="Thank you for joining the Raíces Early Access. We'll send updates and early access when the official preorder opens." data-es="Gracias por unirte al Early Access de Raíces. Te enviaremos actualizaciones y acceso anticipado cuando abramos la preventa oficial.">Thank you for joining the Raíces Early Access. We'll send updates and early access when the official preorder opens.</p>
    </div>
  </div>
</section>
<!-- NEWSLETTER -->
<section class="newsletter" id="contact">
  <h2 data-en="Join the Journey." data-es="Únete a la Travesía.">Join the Journey.</h2>
  <p data-en="Receive stories, releases, and preorder updates." data-es="Recibe historias, lanzamientos y actualizaciones de preventa.">Receive stories, releases, and preorder updates.</p>
  <div class="newsletter__form">
    <input type="email" data-en-ph="Your email" data-es-ph="Tu correo" placeholder="Your email">
    <button data-en="Subscribe" data-es="Suscribirse">Subscribe</button>
  </div>
  <label class="consent-inline"><input type="checkbox"> <span data-en="I authorize Travesía to store my data to send me updates." data-es="Autorizo a Travesía a guardar mis datos para enviarme actualizaciones.">I authorize Travesía to store my data to send me updates.</span></label>
</section>
<!-- FOOTER -->
<footer class="footer">
  <div class="footer__grid">
    <div class="footer__brand"><div class="logo"><img src="assets/logo-horizontal-white.png" alt="Travesía — A Story in Every Cup"></div><p class="tagline">A Story in Every Cup</p><div class="footer__social">Instagram · Facebook · Twitter</div></div>
    <div class="footer__col"><h4>Travesía</h4><a href="#raices">Raíces</a><a href="our-story.html" data-en="Our Story" data-es="Nuestra Historia">Our Story</a><a href="#film">Film</a><a href="#contact" data-en="Contact" data-es="Contacto">Contact</a></div>
    <div class="footer__col"><h4 data-en="Support / Legal" data-es="Soporte / Legal">Support / Legal</h4><a href="legal.html#privacy" data-en="Privacy Policy" data-es="Política de Privacidad">Privacy Policy</a><a href="legal.html#cookies" data-en="Cookie Policy" data-es="Política de Cookies">Cookie Policy</a><a href="legal.html#terms" data-en="Terms &amp; Conditions" data-es="Términos y Condiciones">Terms &amp; Conditions</a><a href="legal.html#shipping" data-en="Shipping &amp; Returns" data-es="Envíos y Devoluciones">Shipping &amp; Returns</a><a href="#contact" data-en="Customer Service" data-es="Atención al Cliente">Customer Service</a></div>
  </div>
  <p class="footer__copy">© 2026 Travesía Colombian Corp. All rights reserved.</p>
</footer>
<script>
const SITE_PHASE = 'early-access'; /* 'early-access' | 'preorder' — mantener igual en las 3 páginas */
let LANG = 'en';
function track(event, params){params=params||{};window.dataLayer=window.dataLayer||[];window.dataLayer.push(Object.assign({event:event},params));if(window.fbq){const s={Lead:'Lead',ViewContent:'ViewContent',AddToCart:'AddToCart',Purchase:'Purchase'};if(s[event])fbq('track',s[event],params);else fbq('trackCustom',event,params);}if(window.ttq){const s={Lead:'SubmitForm',ViewContent:'ViewContent',AddToCart:'AddToCart',Purchase:'CompletePayment'};if(s[event])ttq.track(s[event],params);else ttq.track(event,params);}}
const nav=document.getElementById('nav');
window.addEventListener('scroll',()=>nav.classList.toggle('scrolled',window.scrollY>80),{passive:true});
const mm=document.getElementById('mobileMenu');
document.getElementById('burger').addEventListener('click',()=>mm.classList.add('open'));
document.getElementById('mmClose').addEventListener('click',()=>mm.classList.remove('open'));
mm.querySelectorAll('a').forEach(a=>a.addEventListener('click',()=>mm.classList.remove('open')));
function render(){
  document.documentElement.lang=LANG;
  const ea=SITE_PHASE==='early-access';
  document.querySelectorAll('.only-ea').forEach(el=>el.style.display=ea?'':'none');
  document.querySelectorAll('.only-po').forEach(el=>el.style.display=ea?'none':'');
  document.querySelectorAll('[data-en]').forEach(el=>el.innerHTML=el.getAttribute('data-'+LANG));
  document.querySelectorAll('[data-en-ph]').forEach(el=>el.setAttribute('placeholder',el.getAttribute('data-'+LANG+'-ph')));
  const p=ea?'ea':'po';
  document.querySelectorAll('.cta-main').forEach(el=>{el.innerHTML=el.getAttribute('data-'+p+'-'+LANG);el.setAttribute('href',ea?'#early-access':'raices.html');});
  document.querySelectorAll('.lang button').forEach(b=>b.classList.toggle('active',b.dataset.lang===LANG));
}
function setLang(l){const prev=LANG;LANG=l;render();if(l!==prev)track("LanguageSwitch",{from:prev,to:l,phase:SITE_PHASE,page:"home"});}
document.querySelectorAll('.lang button').forEach(b=>b.addEventListener('click',()=>setLang(b.dataset.lang)));
document.querySelectorAll('[data-track]').forEach(el=>el.addEventListener('click',()=>track(el.getAttribute('data-track'),{phase:SITE_PHASE,lang:LANG})));
const eaFormEl=document.getElementById('eaFormEl');
if(eaFormEl){eaFormEl.addEventListener('submit',(e)=>{
  e.preventDefault();
  const f=e.target;
  f.email.style.borderColor='';
  const emailRegex=/^[^\s@]+@[^\s@]+\.[^\s@]+$/;
  // Validaciones
  if(!f.name.value.trim()){alert(LANG==='es'?'Por favor, ingresa tu nombre.':'Please enter your name.');f.name.focus();return;}
  if(!emailRegex.test(f.email.value.trim())){f.email.style.borderColor='#ff4d4d';alert(LANG==='es'?'Por favor, ingresa un correo electrónico válido.':'Please enter a valid email address.');f.email.focus();return;}
  if(!f.consent.checked){alert(LANG==='es'?'Debes aceptar la política de privacidad.':'You must accept the privacy policy.');return;}
  // Klaviyo (requiere el snippet de Klaviyo con tu Public API Key cargado en el <head>)
  if(window._learnq){
    window._learnq.push(['identify',{'$email':f.email.value.trim(),'$first_name':f.name.value.trim(),'City':f.city.value.trim(),'Country':f.country.value.trim(),'Connection':f.connection.value}]);
    window._learnq.push(['track','Subscribed to Waitlist']);
  }
  // Analítica (GA4 / Meta / TikTok) — se mantiene además de Klaviyo
  track('EarlyAccessSubmit',{phase:SITE_PHASE,lang:LANG,connection:f.connection.value});
  track('Lead',{source:'early_access'});
  // Pantalla de gracias
  document.getElementById('eaForm').style.display='none';
  const t=document.getElementById('eaThanks');t.style.display='block';t.scrollIntoView({behavior:'smooth',block:'center'});
});}

/* Newsletter */
(function(){
  var nf=document.querySelector('.newsletter__form');
  if(!nf)return;
  var btn=nf.querySelector('button');
  var inp=nf.querySelector('input[type="email"]');
  var consent=document.querySelector('.consent-inline input');
  var thanks=document.createElement('p');
  thanks.style.cssText='font-family:var(--font-sans);font-size:13px;color:var(--teal-deep);margin-top:18px;';
  thanks.setAttribute("data-en","Thank you for joining. We\'ll be in touch.");
  thanks.setAttribute('data-es','Gracias por unirte. Estaremos en contacto.');
  thanks.style.display='none';
  nf.parentNode.insertBefore(thanks,nf.nextSibling);
  btn.addEventListener('click',function(){
    if(!inp.value||!/^[^\s@]+@[^\s@]+\.[^\s@]+$/.test(inp.value)){
      inp.style.borderColor='#9b3b2f';inp.focus();return;
    }
    inp.style.borderColor='';
    if(consent&&!consent.checked){alert(LANG==='es'?'Por favor acepta los términos.':'Please accept the terms.');return;}
    if(window._learnq){
      window._learnq.push(['identify',{'$email':inp.value.trim()}]);
      window._learnq.push(['track','Newsletter Signup']);
    }
    track('NewsletterSubmit',{phase:SITE_PHASE,lang:LANG});
    nf.style.display='none';
    thanks.style.display='block';
    thanks.innerHTML=thanks.getAttribute('data-'+LANG);
  });
})();

render();
track('PageView',{phase:SITE_PHASE});track('ViewContent',{content_name:'home',phase:SITE_PHASE});
/* Additional events: ParticipantsSectionView, EventGalleryView tracked on our-story.html via IntersectionObserver */
const obs=new IntersectionObserver((es)=>es.forEach(e=>{if(e.isIntersecting){e.target.classList.add('in');obs.unobserve(e.target);}}),{threshold:0.14});
document.querySelectorAll('.reveal').forEach(el=>obs.observe(el));
setTimeout(()=>document.querySelectorAll('.reveal').forEach(el=>el.classList.add('in')),1500);
</script>
</body>
</html>

<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Legal — Travesia Colombian Coffee</title>
<meta name="description" content="Privacy Policy, Cookie Policy, Terms and Conditions, and Shipping policy for Travesia Colombian Coffee.">
<link rel="icon" type="image/png" href="assets/symbol-color.png">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,500;0,600;1,300;1,400;1,500&family=DM+Sans:wght@300;400;500&display=swap" rel="stylesheet">
<style>
:root{--coffee:#473224;--coffee-deep:#3d2a1c;--teal:#018E86;--teal-deep:#09685F;--gold:#BE9F56;--gold-soft:#cdb877;--beige:#E1D6C0;--paper:#F2EADB;--cream:#FAF8F4;--ink:#2e2014;--font-hero:'Cormorant Garamond',serif;--font-display:'Cormorant Garamond',serif;--font-serif:'Cormorant Garamond',serif;--font-sans:'DM Sans',system-ui,sans-serif;}
*{margin:0;padding:0;box-sizing:border-box;}html{scroll-behavior:smooth;}
body{background:var(--paper);color:var(--ink);font-family:var(--font-serif);-webkit-font-smoothing:antialiased;overflow-x:hidden;}
img{display:block;max-width:100%;}a{color:inherit;text-decoration:none;}button{font-family:inherit;cursor:pointer;border:none;background:none;}
a:focus-visible,button:focus-visible{outline:2px solid var(--gold);outline-offset:3px;}
body::after{content:"";position:fixed;inset:0;z-index:9999;pointer-events:none;opacity:.03;mix-blend-mode:overlay;background-image:url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='120' height='120'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.85' numOctaves='2'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)'/%3E%3C/svg%3E");}
/* Nav */
.nav{position:fixed;top:0;left:0;right:0;z-index:100;height:72px;display:grid;grid-template-columns:auto 1fr auto;align-items:center;padding:0 24px;background:rgba(58,39,25,.94);backdrop-filter:blur(8px);-webkit-backdrop-filter:blur(8px);}
.nav__logo{justify-self:center;line-height:0;}.nav__logo img{height:34px;width:auto;max-width:170px;object-fit:contain;}
.nav__links{display:none;gap:36px;justify-content:center;list-style:none;}
.nav__links a{font-family:var(--font-sans);font-size:13px;text-transform:uppercase;letter-spacing:.12em;color:var(--cream);transition:color .2s;}
.nav__links a:hover{color:var(--gold);}
.nav__right{display:flex;align-items:center;gap:20px;justify-self:end;}
.lang{display:flex;align-items:center;gap:6px;font-family:var(--font-sans);font-size:13px;text-transform:uppercase;letter-spacing:.12em;}
.lang button{color:var(--cream);transition:color .2s;}.lang button.active{color:var(--gold);}.lang span{color:var(--beige);opacity:.5;}
.burger{color:var(--cream);justify-self:start;display:flex;flex-direction:column;gap:5px;padding:6px 0;}
.burger span{width:24px;height:1.5px;background:currentColor;display:block;}
.mobile-menu{position:fixed;inset:0;z-index:99;background:var(--coffee-deep);display:flex;flex-direction:column;justify-content:center;align-items:center;gap:32px;transform:translateX(-100%);transition:transform .35s;}
.mobile-menu.open{transform:translateX(0);}
.mobile-menu a{font-family:var(--font-sans);font-size:15px;text-transform:uppercase;letter-spacing:.12em;color:var(--cream);}
.mobile-menu .mm-close{position:absolute;top:24px;right:24px;color:var(--cream);font-size:28px;}
@media(min-width:980px){.nav{height:80px;padding:0 80px;}.nav__logo{justify-self:start;}.nav__logo img{height:42px;max-width:230px;}.nav__links{display:flex;}.burger{display:none;}.mobile-menu{display:none;}}
/* Legal layout */
.legal-header{background:var(--coffee-deep);padding:140px 24px 72px;text-align:center;}
.legal-header h1{font-family:var(--font-display);font-size:clamp(30px,4vw,44px);font-weight:600;letter-spacing:-0.01em;color:var(--cream);margin-bottom:12px;}
.legal-header p{font-family:var(--font-serif);font-style:italic;font-size:17px;color:rgba(225,214,192,.7);}
.legal-nav{background:var(--beige);padding:0 24px;border-bottom:1px solid rgba(71,50,36,.12);}
.legal-nav__wrap{max-width:780px;margin:0 auto;display:flex;gap:0;overflow-x:auto;}
.legal-nav a{font-family:var(--font-sans);font-size:11px;text-transform:uppercase;letter-spacing:.14em;color:var(--teal-deep);padding:18px 20px;display:block;white-space:nowrap;border-bottom:2px solid transparent;transition:border-color .2s;}
.legal-nav a:hover{border-bottom-color:var(--teal-deep);}
.legal-body{max-width:780px;margin:0 auto;padding:60px 24px 100px;}
.legal-section{margin-bottom:72px;}
.legal-section:last-child{margin-bottom:0;}
.legal-section h2{font-family:var(--font-display);font-size:clamp(22px,3vw,30px);font-weight:600;letter-spacing:-0.01em;color:var(--ink);margin-bottom:8px;padding-top:16px;}
.legal-section .updated{font-family:var(--font-sans);font-size:11px;text-transform:uppercase;letter-spacing:.14em;color:var(--teal-deep);margin-bottom:28px;display:block;}
.legal-section h3{font-family:var(--font-sans);font-size:13px;text-transform:uppercase;letter-spacing:.1em;color:var(--coffee);margin:28px 0 10px;}
.legal-section p{font-family:var(--font-serif);font-size:17px;line-height:1.65;color:var(--ink);margin-bottom:16px;}
.legal-section p:last-child{margin-bottom:0;}
.legal-section a{color:var(--teal-deep);text-decoration:underline;text-underline-offset:3px;}
hr.legal-rule{border:0;border-top:1px solid rgba(71,50,36,.14);margin:60px 0;}
/* Footer */
.footer{background:var(--coffee-deep);color:var(--beige);padding:72px 24px 56px;}
.footer__grid{display:grid;grid-template-columns:1fr;gap:40px;max-width:1100px;margin:0 auto;}
.footer__brand .logo img{height:34px;width:auto;}
.footer__brand .tagline{font-family:var(--font-hero);font-size:17px;letter-spacing:.02em;color:rgba(225,214,192,.82);margin:16px 0 16px;}
.footer__social{display:flex;gap:18px;color:var(--beige);}
.footer__col h4{font-family:var(--font-sans);font-size:13px;text-transform:uppercase;letter-spacing:.12em;color:var(--gold);margin-bottom:16px;font-weight:500;}
.footer__col a{display:block;font-family:var(--font-sans);font-size:13px;font-weight:300;color:rgba(225,214,192,.8);margin-bottom:10px;transition:color .2s;}
.footer__col a:hover{color:var(--cream);}
.footer__copy{text-align:center;margin-top:48px;font-family:var(--font-sans);font-size:11px;color:rgba(225,214,192,.5);}
@media(min-width:980px){.footer{padding:80px 80px 56px;}.footer__grid{grid-template-columns:1.4fr 1fr 1fr;gap:64px;}}
</style>
</head>
<body>
<nav class="nav">
  <button class="burger" id="burger" aria-label="Open menu"><span></span><span></span><span></span></button>
  <a href="index.html" class="nav__logo"><img src="assets/logo-horizontal-white.png" alt="Travesía — A Story in Every Cup"></a>
  <ul class="nav__links">
    <li><a href="index.html#raices">Raíces</a></li>
    <li><a href="our-story.html" data-en="Our Story" data-es="Nuestra Historia">Our Story</a></li>
    <li><a href="index.html#contact" data-en="Contact" data-es="Contacto">Contact</a></li>
  </ul>
  <div class="nav__right">
    <div class="lang"><button data-lang="en" class="active">EN</button><span>/</span><button data-lang="es">ES</button></div>
  </div>
</nav>
<div class="mobile-menu" id="mobileMenu">
  <button class="mm-close" id="mmClose" aria-label="Close menu">&times;</button>
  <a href="index.html#raices">Raíces</a>
  <a href="our-story.html" data-en="Our Story" data-es="Nuestra Historia">Our Story</a>
  <a href="index.html#contact" data-en="Contact" data-es="Contacto">Contact</a>
  <div class="lang"><button data-lang="en" class="active">EN</button><span>/</span><button data-lang="es">ES</button></div>
</div>

<div class="legal-header">
  <h1 data-en="Legal" data-es="Legal">Legal</h1>
  <p data-en="Travesia Colombian Corp. &mdash; New York" data-es="Travesia Colombian Corp. &mdash; New York">Travesia Colombian Corp. &mdash; New York</p>
</div>

<nav class="legal-nav" aria-label="Legal sections">
  <div class="legal-nav__wrap">
    <a href="#privacy" data-en="Privacy Policy" data-es="Privacidad">Privacy Policy</a>
    <a href="#cookies" data-en="Cookie Policy" data-es="Cookies">Cookie Policy</a>
    <a href="#terms" data-en="Terms &amp; Conditions" data-es="Terminos">Terms &amp; Conditions</a>
    <a href="#shipping" data-en="Shipping &amp; Returns" data-es="Envios">Shipping &amp; Returns</a>
  </div>
</nav>

<main class="legal-body">

  <!-- PRIVACY -->
  <section class="legal-section" id="privacy">
    <h2 data-en="Privacy Policy" data-es="Politica de Privacidad">Privacy Policy</h2>
    <span class="updated">Last updated: June 2026</span>

    <h3 data-en="Who we are" data-es="Quienes somos">Who we are</h3>
    <p data-en="Travesia Colombian Corp. (&ldquo;Travesia&rdquo;, &ldquo;we&rdquo;, &ldquo;our&rdquo;) operates the website travesiacolombiancoffee.com. Our contact address is info@travesiacolombiancoffee.com." data-es="Travesia Colombian Corp. (&ldquo;Travesia&rdquo;, &ldquo;nosotros&rdquo;) opera el sitio web travesiacolombiancoffee.com. Puedes contactarnos en info@travesiacolombiancoffee.com.">Travesia Colombian Corp. (&ldquo;Travesia&rdquo;, &ldquo;we&rdquo;, &ldquo;our&rdquo;) operates the website travesiacolombiancoffee.com. Our contact address is info@travesiacolombiancoffee.com.</p>

    <h3 data-en="What information we collect" data-es="Que informacion recopilamos">What information we collect</h3>
    <p data-en="When you submit the Early Access form or newsletter, we collect your name, email address, city, country, and your stated area of interest. We do not collect payment information unless you complete a purchase through Shopify Checkout." data-es="Cuando completas el formulario de Early Access o el newsletter, recopilamos tu nombre, correo electronico, ciudad, pais y tu area de interes declarada. No recopilamos informacion de pago a menos que completes una compra a traves de Shopify Checkout.">When you submit the Early Access form or newsletter, we collect your name, email address, city, country, and your stated area of interest. We do not collect payment information unless you complete a purchase through Shopify Checkout.</p>

    <h3 data-en="How we use your information" data-es="Como usamos tu informacion">How we use your information</h3>
    <p data-en="We use the information you provide to send you updates about Early Access, product releases, and the preorder when it becomes available. We do not sell your data to third parties. We may use email service providers (such as Klaviyo) to manage and send communications. Analytics data (Google Analytics 4, Meta Pixel, TikTok Pixel) helps us understand how people interact with our website." data-es="Usamos la informacion que nos proporcionas para enviarte actualizaciones sobre el Early Access, lanzamientos de productos y la preventa cuando este disponible. No vendemos tus datos a terceros. Podemos usar proveedores de servicios de correo (como Klaviyo) para gestionar y enviar comunicaciones. Los datos de analitica (Google Analytics 4, Meta Pixel, TikTok Pixel) nos ayudan a entender como las personas interactuan con nuestro sitio web.">We use the information you provide to send you updates about Early Access, product releases, and the preorder when it becomes available. We do not sell your data to third parties. We may use email service providers (such as Klaviyo) to manage and send communications. Analytics data (Google Analytics 4, Meta Pixel, TikTok Pixel) helps us understand how people interact with our website.</p>

    <h3 data-en="Your rights" data-es="Tus derechos">Your rights</h3>
    <p data-en="You may request access to, correction, or deletion of your personal data at any time by contacting us at info@travesiacolombiancoffee.com. You may unsubscribe from our communications at any time using the unsubscribe link in any email we send." data-es="Puedes solicitar acceso, correccion o eliminacion de tus datos personales en cualquier momento contactandonos en info@travesiacolombiancoffee.com. Puedes darte de baja de nuestras comunicaciones en cualquier momento usando el enlace de baja en cualquier correo que te enviemos.">You may request access to, correction, or deletion of your personal data at any time by contacting us at info@travesiacolombiancoffee.com. You may unsubscribe from our communications at any time using the unsubscribe link in any email we send.</p>

    <h3 data-en="Data retention" data-es="Retencion de datos">Data retention</h3>
    <p data-en="We retain your personal information for as long as necessary to fulfill the purposes described above, or as required by applicable law. You may request deletion at any time." data-es="Conservamos tu informacion personal durante el tiempo necesario para cumplir los propositos descritos anteriormente, o segun lo exija la ley aplicable. Puedes solicitar la eliminacion en cualquier momento.">We retain your personal information for as long as necessary to fulfill the purposes described above, or as required by applicable law. You may request deletion at any time.</p>
  </section>

  <hr class="legal-rule">

  <!-- COOKIES -->
  <section class="legal-section" id="cookies">
    <h2 data-en="Cookie Policy" data-es="Politica de Cookies">Cookie Policy</h2>
    <span class="updated">Last updated: June 2026</span>

    <h3 data-en="What are cookies" data-es="Que son las cookies">What are cookies</h3>
    <p data-en="Cookies are small text files placed on your device when you visit a website. They help us understand how you use our site and improve your experience." data-es="Las cookies son pequenos archivos de texto que se almacenan en tu dispositivo cuando visitas un sitio web. Nos ayudan a entender como usas nuestro sitio y mejorar tu experiencia.">Cookies are small text files placed on your device when you visit a website. They help us understand how you use our site and improve your experience.</p>

    <h3 data-en="Cookies we use" data-es="Cookies que usamos">Cookies we use</h3>
    <p data-en="We use analytics cookies (Google Analytics 4) to understand traffic and usage patterns. We may use advertising cookies (Meta Pixel, TikTok Pixel) to measure the performance of our campaigns. We use functional cookies necessary for the site to work correctly." data-es="Usamos cookies de analitica (Google Analytics 4) para entender el trafico y los patrones de uso. Podemos usar cookies publicitarias (Meta Pixel, TikTok Pixel) para medir el rendimiento de nuestras campanas. Usamos cookies funcionales necesarias para que el sitio funcione correctamente.">We use analytics cookies (Google Analytics 4) to understand traffic and usage patterns. We may use advertising cookies (Meta Pixel, TikTok Pixel) to measure the performance of our campaigns. We use functional cookies necessary for the site to work correctly.</p>

    <h3 data-en="Managing cookies" data-es="Gestionar cookies">Managing cookies</h3>
    <p data-en="You can control and delete cookies through your browser settings. Disabling certain cookies may affect the functionality of this website. For more information about cookies, visit allaboutcookies.org." data-es="Puedes controlar y eliminar las cookies a traves de la configuracion de tu navegador. Deshabilitar ciertas cookies puede afectar la funcionalidad de este sitio web. Para mas informacion sobre cookies, visita allaboutcookies.org.">You can control and delete cookies through your browser settings. Disabling certain cookies may affect the functionality of this website. For more information about cookies, visit allaboutcookies.org.</p>
  </section>

  <hr class="legal-rule">

  <!-- TERMS -->
  <section class="legal-section" id="terms">
    <h2 data-en="Terms &amp; Conditions" data-es="Terminos y Condiciones">Terms &amp; Conditions</h2>
    <span class="updated">Last updated: June 2026</span>

    <h3 data-en="Early Access" data-es="Early Access">Early Access</h3>
    <p data-en="Joining the Travesia Early Access list is free and does not constitute a purchase. By submitting the Early Access form, you are registering to receive priority notification when the official preorder opens. No payment is collected during the Early Access phase." data-es="Unirse a la lista de Early Access de Travesia es gratuito y no constituye una compra. Al enviar el formulario de Early Access, te registras para recibir notificacion prioritaria cuando abra la preventa oficial. No se realiza ninguna compra durante la fase de Early Access.">Joining the Travesia Early Access list is free and does not constitute a purchase. By submitting the Early Access form, you are registering to receive priority notification when the official preorder opens. No payment is collected during the Early Access phase.</p>

    <h3 data-en="Preorder" data-es="Preventa">Preorder</h3>
    <p data-en="When the preorder phase is activated, placing a preorder for Raices constitutes a purchase agreement. Orders are processed and shipped once the preorder period closes, according to the estimated schedule communicated by Travesia. Estimated shipping dates are not a guarantee and may be subject to change. Travesia will notify customers by email of any changes to the fulfillment schedule." data-es="Cuando se active la fase de preventa, realizar una reserva de Raices constituye un acuerdo de compra. Los pedidos se procesan y envian una vez que cierra el periodo de preventa, segun el cronograma estimado comunicado por Travesia. Las fechas de envio estimadas no son una garantia y pueden estar sujetas a cambios. Travesia notificara a los clientes por correo electronico sobre cualquier cambio en el cronograma de cumplimiento.">When the preorder phase is activated, placing a preorder for Raices constitutes a purchase agreement. Orders are processed and shipped once the preorder period closes, according to the estimated schedule communicated by Travesia. Estimated shipping dates are not a guarantee and may be subject to change. Travesia will notify customers by email of any changes to the fulfillment schedule.</p>

    <h3 data-en="Product" data-es="Producto">Product</h3>
    <p data-en="Raices is a specialty Colombian coffee. Product weight is 250g / 8.8 oz. As a food product, Raices is not eligible for return once the bag has been opened, except in cases of damage or defect. See Shipping &amp; Returns for details." data-es="Raices es un cafe colombiano de especialidad. El peso del producto es 250g / 8.8 oz. Como producto alimenticio, Raices no es elegible para devolucion una vez que la bolsa ha sido abierta, excepto en casos de dano o defecto. Consulta Envios y Devoluciones para mas detalles.">Raices is a specialty Colombian coffee. Product weight is 250g / 8.8 oz. As a food product, Raices is not eligible for return once the bag has been opened, except in cases of damage or defect. See Shipping &amp; Returns for details.</p>

    <h3 data-en="Pricing" data-es="Precios">Pricing</h3>
    <p data-en="Preorder price for Raices First Edition is $20.99 USD. The Editorial Edition regular price is $24.50 USD. Prices are in US dollars and do not include shipping, unless a free shipping threshold applies. Final cost is confirmed at checkout." data-es="El precio de preventa de la Primera Edicion de Raices es $20.99 USD. El precio regular de la Edicion Editorial es $24.50 USD. Los precios estan en dolares estadounidenses y no incluyen el envio, a menos que se aplique un umbral de envio gratuito. El costo final se confirma al finalizar la compra.">Preorder price for Raices First Edition is $20.99 USD. The Editorial Edition regular price is $24.50 USD. Prices are in US dollars and do not include shipping, unless a free shipping threshold applies. Final cost is confirmed at checkout.</p>

    <h3 data-en="Intellectual property" data-es="Propiedad intelectual">Intellectual property</h3>
    <p data-en="All content on this website, including text, images, design, and brand elements, is the property of Travesia Colombian Corp. and may not be reproduced or distributed without written permission." data-es="Todo el contenido de este sitio web, incluyendo texto, imagenes, diseno y elementos de marca, es propiedad de Travesia Colombian Corp. y no puede reproducirse ni distribuirse sin permiso por escrito.">All content on this website, including text, images, design, and brand elements, is the property of Travesia Colombian Corp. and may not be reproduced or distributed without written permission.</p>

    <h3 data-en="Contact" data-es="Contacto">Contact</h3>
    <p data-en="For any questions regarding these Terms, contact us at info@travesiacolombiancoffee.com." data-es="Para cualquier consulta sobre estos Terminos, contactanos en info@travesiacolombiancoffee.com.">For any questions regarding these Terms, contact us at info@travesiacolombiancoffee.com.</p>
  </section>

  <hr class="legal-rule">

  <!-- SHIPPING -->
  <section class="legal-section" id="shipping">
    <h2 data-en="Shipping &amp; Returns" data-es="Envios y Devoluciones">Shipping &amp; Returns</h2>
    <span class="updated">Last updated: June 2026</span>

    <h3 data-en="Shipping zones" data-es="Zonas de envio">Shipping zones</h3>
    <p data-en="During the first release, Travesia ships within the United States. We ship via UPS Ground from New York. Final shipping cost and estimated delivery time are confirmed at checkout." data-es="Durante el primer lanzamiento, Travesia realiza envios dentro de Estados Unidos. Enviamos por UPS Ground desde New York. El costo final de envio y el tiempo estimado de entrega se confirman al finalizar la compra.">During the first release, Travesia ships within the United States. We ship via UPS Ground from New York. Final shipping cost and estimated delivery time are confirmed at checkout.</p>

    <h3 data-en="Estimated delivery times" data-es="Tiempos estimados de entrega">Estimated delivery times</h3>
    <p data-en="Estimated transit times via UPS Ground from New York vary by ZIP Code. 1&ndash;2 business days for NY, NJ, CT. 2&ndash;3 business days for most of the East Coast. 4&ndash;5 business days for the rest of the United States. These are estimates and may vary based on carrier conditions." data-es="Los tiempos de transito estimados por UPS Ground desde New York varian segun el codigo postal. 1&ndash;2 dias habiles para NY, NJ, CT. 2&ndash;3 dias habiles para la mayor parte de la Costa Este. 4&ndash;5 dias habiles para el resto de Estados Unidos. Estas son estimaciones y pueden variar segun las condiciones del transportista.">Estimated transit times via UPS Ground from New York vary by ZIP Code. 1&ndash;2 business days for NY, NJ, CT. 2&ndash;3 business days for most of the East Coast. 4&ndash;5 business days for the rest of the United States. These are estimates and may vary based on carrier conditions.</p>

    <h3 data-en="Preorder shipping" data-es="Envio de preventa">Preorder shipping</h3>
    <p data-en="Preorder shipments are prepared and dispatched once the preorder period closes, according to the confirmed fulfillment schedule. Travesia will notify preorder customers by email with tracking information when their order ships." data-es="Los envios de preventa se preparan y despachan una vez que cierra el periodo de preventa, segun el cronograma de cumplimiento confirmado. Travesia notificara a los clientes de preventa por correo electronico con informacion de seguimiento cuando se envie su pedido.">Preorder shipments are prepared and dispatched once the preorder period closes, according to the confirmed fulfillment schedule. Travesia will notify preorder customers by email with tracking information when their order ships.</p>

    <h3 data-en="Returns and cancellations" data-es="Devoluciones y cancelaciones">Returns and cancellations</h3>
    <p data-en="As a specialty food product, Raices is not eligible for return once the bag has been opened. If your order arrives damaged or defective, please contact us within 7 days of receipt at info@travesiacolombiancoffee.com with your order number and photos of the issue. We will review each case and offer a replacement or refund where applicable." data-es="Como producto alimenticio de especialidad, Raices no es elegible para devolucion una vez que la bolsa ha sido abierta. Si tu pedido llega danado o defectuoso, contactanos dentro de los 7 dias posteriores a la recepcion en info@travesiacolombiancoffee.com con tu numero de pedido y fotos del problema. Revisaremos cada caso y ofreceremos un reemplazo o reembolso donde corresponda.">As a specialty food product, Raices is not eligible for return once the bag has been opened. If your order arrives damaged or defective, please contact us within 7 days of receipt at info@travesiacolombiancoffee.com with your order number and photos of the issue. We will review each case and offer a replacement or refund where applicable.</p>

    <p data-en="Preorder cancellations may be requested by contacting info@travesiacolombiancoffee.com before the preorder period closes. Cancellation requests after the preorder closes will be reviewed on a case-by-case basis." data-es="Las cancelaciones de preventa pueden solicitarse contactando info@travesiacolombiancoffee.com antes del cierre del periodo de preventa. Las solicitudes de cancelacion despues del cierre de la preventa se revisaran caso por caso.">Preorder cancellations may be requested by contacting info@travesiacolombiancoffee.com before the preorder period closes. Cancellation requests after the preorder closes will be reviewed on a case-by-case basis.</p>

    <h3 data-en="Contact" data-es="Contacto">Contact</h3>
    <p data-en="For shipping, returns, or any order-related questions, contact us at info@travesiacolombiancoffee.com." data-es="Para consultas de envio, devoluciones o cualquier pregunta relacionada con tu pedido, contactanos en info@travesiacolombiancoffee.com.">For shipping, returns, or any order-related questions, contact us at info@travesiacolombiancoffee.com.</p>
  </section>

</main>

<footer class="footer">
  <div class="footer__grid">
    <div class="footer__brand"><div class="logo"><img src="assets/logo-horizontal-white.png" alt="Travesía — A Story in Every Cup"></div><p class="tagline">A Story in Every Cup</p><div class="footer__social">Instagram &middot; Facebook &middot; Twitter</div></div>
    <div class="footer__col"><h4>Travesia</h4><a href="index.html#raices">Raíces</a><a href="our-story.html" data-en="Our Story" data-es="Nuestra Historia">Our Story</a><a href="index.html#film">Film</a><a href="index.html#contact" data-en="Contact" data-es="Contacto">Contact</a></div>
    <div class="footer__col"><h4 data-en="Legal" data-es="Legal">Legal</h4><a href="legal.html#privacy" data-en="Privacy Policy" data-es="Politica de Privacidad">Privacy Policy</a><a href="legal.html#cookies" data-en="Cookie Policy" data-es="Politica de Cookies">Cookie Policy</a><a href="legal.html#terms" data-en="Terms &amp; Conditions" data-es="Terminos y Condiciones">Terms &amp; Conditions</a><a href="legal.html#shipping" data-en="Shipping &amp; Returns" data-es="Envios y Devoluciones">Shipping &amp; Returns</a></div>
  </div>
  <p class="footer__copy">&copy; 2026 Travesia Colombian Corp. All rights reserved.</p>
</footer>

<script>
let LANG='en';
const mm=document.getElementById('mobileMenu');
document.getElementById('burger').addEventListener('click',()=>mm.classList.add('open'));
document.getElementById('mmClose').addEventListener('click',()=>mm.classList.remove('open'));
mm.querySelectorAll('a').forEach(a=>a.addEventListener('click',()=>mm.classList.remove('open')));
function render(){
  document.documentElement.lang=LANG;
  document.querySelectorAll('[data-en]').forEach(el=>el.innerHTML=el.getAttribute('data-'+LANG));
  document.querySelectorAll('.lang button').forEach(b=>b.classList.toggle('active',b.dataset.lang===LANG));
}
function setLang(l){LANG=l;render();}
document.querySelectorAll('.lang button').forEach(b=>b.addEventListener('click',()=>setLang(b.dataset.lang)));
render();
if(location.hash){setTimeout(()=>{var el=document.querySelector(location.hash);if(el)el.scrollIntoView({behavior:'smooth',block:'start'});},200);}
</script>
</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Our Story — Travesía</title>
<meta name="description" content="Travesía is the journey we share with those who dared to cross borders.">
<link rel="icon" type="image/png" href="assets/symbol-color.png">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,500;0,600;1,300;1,400;1,500&family=DM+Sans:wght@300;400;500&display=swap" rel="stylesheet">
<style>
/* TRAVESIA — Our Story */
:root{--coffee:#473224;--coffee-deep:#3d2a1c;--teal:#018E86;--teal-deep:#09685F;--gold:#BE9F56;--gold-soft:#cdb877;--beige:#E1D6C0;--paper:#F2EADB;--cream:#FAF8F4;--ink:#2e2014;--font-hero:'Cormorant Garamond',serif;--font-display:'Cormorant Garamond',serif;--font-serif:'Cormorant Garamond',serif;--font-sans:'DM Sans',system-ui,sans-serif;}
*{margin:0;padding:0;box-sizing:border-box;}html{scroll-behavior:smooth;}
body{background:var(--paper);color:var(--ink);font-family:var(--font-serif);-webkit-font-smoothing:antialiased;overflow-x:hidden;}
img{display:block;max-width:100%;object-fit:cover;}a{color:inherit;text-decoration:none;}button{font-family:inherit;cursor:pointer;border:none;background:none;}
a:focus-visible,button:focus-visible{outline:2px solid var(--gold);outline-offset:3px;}
body::after{content:"";position:fixed;inset:0;z-index:9999;pointer-events:none;opacity:.03;mix-blend-mode:overlay;background-image:url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='120' height='120'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.85' numOctaves='2'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)'/%3E%3C/svg%3E");}
.chapter{font-family:var(--font-sans);font-size:11px;text-transform:uppercase;letter-spacing:.34em;color:var(--teal-deep);display:inline-flex;align-items:center;gap:14px;}
.chapter::before{content:"";width:36px;height:1px;background:var(--teal-deep);}
/* Nav */
.nav{position:fixed;top:0;left:0;right:0;z-index:100;height:72px;display:grid;grid-template-columns:auto 1fr auto;align-items:center;padding:0 24px;background:rgba(58,39,25,.94);backdrop-filter:blur(8px);-webkit-backdrop-filter:blur(8px);}
.nav__logo{justify-self:center;line-height:0;}.nav__logo img{height:34px;width:auto;max-width:170px;object-fit:contain;}
.nav__links{display:none;gap:36px;justify-content:center;list-style:none;}
.nav__links a{font-family:var(--font-sans);font-size:13px;text-transform:uppercase;letter-spacing:.12em;color:var(--cream);transition:color .2s;}
.nav__links a:hover{color:var(--gold);}
.nav__right{display:flex;align-items:center;gap:20px;justify-self:end;}
.lang{display:flex;align-items:center;gap:6px;font-family:var(--font-sans);font-size:13px;text-transform:uppercase;letter-spacing:.12em;}
.lang button{color:var(--cream);transition:color .2s;}.lang button.active{color:var(--gold);}.lang span{color:var(--beige);opacity:.5;}
.cart{color:var(--cream);width:22px;height:22px;}
.burger{color:var(--cream);justify-self:start;display:flex;flex-direction:column;gap:5px;padding:6px 0;}
.burger span{width:24px;height:1.5px;background:currentColor;display:block;}
.mobile-menu{position:fixed;inset:0;z-index:99;background:var(--coffee-deep);display:flex;flex-direction:column;justify-content:center;align-items:center;gap:32px;transform:translateX(-100%);transition:transform .35s;}
.mobile-menu.open{transform:translateX(0);}
.mobile-menu a{font-family:var(--font-sans);font-size:15px;text-transform:uppercase;letter-spacing:.12em;color:var(--cream);}
.mobile-menu .mm-social{display:flex;gap:24px;margin-top:24px;color:var(--beige);}
.mobile-menu .mm-close{position:absolute;top:24px;right:24px;color:var(--cream);font-size:28px;}
@media(min-width:980px){.nav{height:80px;padding:0 80px;}.nav__logo{justify-self:start;}.nav__logo img{height:42px;max-width:230px;}.nav__links{display:flex;}.burger{display:none;}.mobile-menu{display:none;}}
.btn-primary{font-family:var(--font-sans);font-size:12px;font-weight:500;text-transform:uppercase;letter-spacing:.16em;background:var(--gold);color:var(--coffee);padding:16px 38px;border-radius:0;display:inline-block;transition:background .25s;}
.btn-primary:hover{background:var(--gold-soft);}
/* Opening */
.opening{position:relative;min-height:90vh;display:flex;flex-direction:column;align-items:center;justify-content:center;text-align:center;padding:140px 24px;overflow:hidden;background:radial-gradient(120% 80% at 50% 30%,rgba(1,142,134,0) 30%,rgba(58,39,25,.28) 100%),radial-gradient(140% 110% at 50% 8%,#15a89d 0%,var(--teal) 30%,var(--teal-deep) 62%,#0b5d54 100%);}
.opening__logo{position:relative;z-index:2;}.opening__logo img{width:170px;max-width:55%;height:auto;margin:0 auto 28px;}
.opening__tagline{position:relative;z-index:2;font-family:var(--font-hero);font-size:clamp(18px,2.4vw,24px);letter-spacing:.02em;color:var(--gold-soft);margin:2px 0 30px;}
.opening p{position:relative;z-index:2;max-width:600px;font-family:var(--font-serif);font-style:italic;font-size:clamp(19px,2.6vw,24px);line-height:1.45;color:rgba(250,248,244,.9);}
.opening .roots-link{position:relative;z-index:2;display:inline-block;margin-top:28px;font-family:var(--font-sans);font-size:12px;text-transform:uppercase;letter-spacing:.16em;color:var(--gold-soft);}
/* River */
.river{position:relative;min-height:62vh;display:flex;align-items:center;justify-content:center;text-align:center;background:linear-gradient(155deg,#1f8079,#0b5d54);overflow:hidden;}
.river::after{content:"";position:absolute;inset:0;background:radial-gradient(70% 70% at 50% 50%,rgba(0,0,0,0) 40%,rgba(11,93,84,.3) 100%);}
.river p{position:relative;z-index:2;max-width:560px;padding:0 24px;font-family:var(--font-serif);font-style:italic;font-size:clamp(20px,3vw,26px);line-height:1.45;color:var(--cream);}
/* Film */
.film{padding:clamp(90px,12vh,150px) 24px;text-align:center;background:var(--paper);}
.film .chapter{justify-content:center;margin-bottom:24px;}
.film p{max-width:560px;margin:0 auto 36px;font-family:var(--font-serif);font-size:18px;color:var(--coffee);}
.film__player{position:relative;aspect-ratio:16/9;max-width:880px;margin:0 auto;background:linear-gradient(135deg,#018E86,#0b5d54);display:flex;align-items:center;justify-content:center;border:1px solid rgba(190,159,86,.3);}
.film__play{width:74px;height:74px;border-radius:50%;border:1px solid rgba(250,248,244,.7);display:flex;align-items:center;justify-content:center;color:var(--cream);transition:background .25s;}
.film__play:hover{background:rgba(250,248,244,.12);}
/* The First Gathering */
.gathering{background:var(--coffee);color:var(--beige);padding:clamp(90px,12vh,150px) 24px;}
.gathering .chapter{justify-content:center;color:var(--gold);display:flex;margin-bottom:18px;}
.gathering .chapter::before{background:var(--gold);}
.gathering__title{font-family:var(--font-display);font-size:clamp(28px,4vw,44px);font-weight:600;letter-spacing:-0.01em;color:var(--cream);text-align:center;margin-bottom:16px;}
.gathering__sub{font-family:var(--font-serif);font-style:italic;font-size:clamp(16px,2vw,19px);color:rgba(225,214,192,.82);text-align:center;max-width:560px;margin:0 auto 52px;line-height:1.5;}
/* Gallery grid: 1 large + 5 secondary */
.gathering__grid{max-width:1120px;margin:0 auto;display:grid;gap:14px;grid-template-columns:1fr 1fr;grid-template-rows:auto;}
.gathering__grid .g-main{grid-column:1/2;grid-row:1/3;}
.gathering__grid .g-side{grid-column:2/3;}
.g-img{position:relative;overflow:hidden;background:linear-gradient(160deg,#09685F,#3d2a1c);}
.g-img.g-main{aspect-ratio:4/5;}
.g-img.g-side{aspect-ratio:4/5;}
.g-img img{width:100%;height:100%;object-fit:cover;display:block;transition:transform .6s ease;}
.g-img:hover img{transform:scale(1.03);}
.g-img__ph{width:100%;height:100%;background:linear-gradient(145deg,#09685F 0%,#3d2a1c 100%);display:flex;align-items:center;justify-content:center;}
.g-img__ph::after{content:"";display:block;width:32px;height:32px;border-radius:50%;border:1px solid rgba(190,159,86,.4);}
@media(min-width:720px){
  .gathering__grid{grid-template-columns:1.25fr 1fr 1fr;grid-template-rows:auto auto auto;}
  .gathering__grid .g-main{grid-column:1/2;grid-row:1/3;}
  .gathering__grid .g-side{grid-column:auto;grid-row:auto;}
}
@media(max-width:480px){
  .gathering__grid{grid-template-columns:1fr;grid-template-rows:auto;}
  .gathering__grid .g-main{grid-column:1/2;grid-row:auto;}
  .g-img.g-main{aspect-ratio:4/3;}
}
.gathering__note{text-align:center;margin-top:32px;font-family:var(--font-sans);font-size:11px;text-transform:uppercase;letter-spacing:.18em;color:rgba(225,214,192,.45);}
/* Participants */
.participants{background:var(--paper);padding:clamp(90px,12vh,150px) 24px;}
.participants .chapter{justify-content:center;display:flex;margin-bottom:18px;}
.participants__title{font-family:var(--font-display);font-size:clamp(30px,4.5vw,46px);font-weight:600;letter-spacing:-0.01em;color:var(--ink);text-align:center;margin-bottom:12px;}
.participants__sub{font-family:var(--font-serif);font-style:italic;font-size:17px;color:var(--coffee);text-align:center;max-width:480px;margin:0 auto 52px;line-height:1.5;}
.participants__grid{max-width:1080px;margin:0 auto;display:grid;grid-template-columns:repeat(2,1fr);gap:28px;}
@media(min-width:600px){.participants__grid{grid-template-columns:repeat(3,1fr);gap:32px;}}
@media(min-width:920px){.participants__grid{grid-template-columns:repeat(5,1fr);gap:28px;}}
.person{display:flex;flex-direction:column;}
.person__photo{position:relative;aspect-ratio:3/4;overflow:hidden;background:linear-gradient(145deg,#473224,#3d2a1c);margin-bottom:14px;border:1px solid rgba(190,159,86,.15);}
.person__photo img{width:100%;height:100%;object-fit:cover;display:block;filter:grayscale(.25);}
.person__photo .person__ph{position:absolute;inset:0;display:flex;align-items:center;justify-content:center;font-family:var(--font-display);font-size:clamp(28px,4vw,38px);color:rgba(225,214,192,.25);letter-spacing:.04em;}
.person__flag{font-size:18px;line-height:1;margin-bottom:6px;}
.person__name{font-family:var(--font-display);font-size:15px;color:var(--ink);line-height:1.2;margin-bottom:3px;overflow-wrap:break-word;word-break:break-word;}
.person__country{font-family:var(--font-sans);font-size:10px;text-transform:uppercase;letter-spacing:.18em;color:var(--teal-deep);}
.person__label{font-family:var(--font-serif);font-style:italic;font-size:13px;color:rgba(71,50,36,.65);margin-top:5px;line-height:1.3;}
/* CTA */
.cta{position:relative;text-align:center;padding:clamp(110px,16vh,190px) 24px;color:var(--cream);overflow:hidden;background:radial-gradient(120% 100% at 50% 40%,var(--teal) 0%,var(--teal-deep) 55%,#0b5d54 100%);}
.cta::before{content:"";position:absolute;inset:0;background:radial-gradient(70% 70% at 50% 50%,rgba(0,0,0,0) 45%,rgba(11,93,84,.3) 100%);}
.cta h2{position:relative;z-index:2;font-family:var(--font-display);font-size:clamp(34px,5vw,54px);font-weight:600;letter-spacing:-0.01em;color:var(--cream);margin-bottom:32px;}
.cta .btn-primary{position:relative;z-index:2;}
/* Footer */
.footer{background:var(--coffee-deep);color:var(--beige);padding:72px 24px 56px;}
.footer__grid{display:grid;grid-template-columns:1fr;gap:40px;max-width:1100px;margin:0 auto;}
.footer__brand .logo img{height:34px;width:auto;}
.footer__brand .tagline{font-family:var(--font-hero);font-size:17px;letter-spacing:.02em;color:rgba(225,214,192,.82);margin:16px 0 16px;}
.footer__social{display:flex;gap:18px;color:var(--beige);}
.footer__col h4{font-family:var(--font-sans);font-size:13px;text-transform:uppercase;letter-spacing:.12em;color:var(--gold);margin-bottom:16px;font-weight:500;}
.footer__col a{display:block;font-family:var(--font-sans);font-size:13px;font-weight:300;color:rgba(225,214,192,.8);margin-bottom:10px;transition:color .2s;}
.footer__col a:hover{color:var(--cream);}
.footer__copy{text-align:center;margin-top:48px;font-family:var(--font-sans);font-size:11px;color:rgba(225,214,192,.5);}
@media(min-width:980px){.footer{padding:80px 80px 56px;}.footer__grid{grid-template-columns:1.4fr 1fr 1fr;gap:64px;}}
@media(prefers-reduced-motion:reduce){html{scroll-behavior:auto;}}
/* Made by mom section */
.mom-section{background:var(--cream);padding:clamp(80px,10vh,130px) 24px;}
.mom__inner{max-width:1060px;margin:0 auto;display:grid;grid-template-columns:1fr;gap:48px;align-items:center;}
@media(min-width:720px){.mom__inner{grid-template-columns:1.1fr 1fr;gap:72px;}}
.mom__img-wrap{position:relative;border-radius:2px;overflow:hidden;aspect-ratio:16/9;}
.mom__img-wrap img{width:100%;height:100%;object-fit:cover;display:block;}
.mom__text .chapter{margin-bottom:20px;}
.mom__text h3{font-family:var(--font-display);font-size:clamp(28px,4vw,42px);font-weight:600;line-height:1.1;letter-spacing:-0.01em;color:var(--ink);margin-bottom:22px;}
.mom__text p{font-family:var(--font-serif);font-style:italic;font-size:clamp(16px,1.9vw,19px);line-height:1.6;color:var(--coffee);max-width:440px;}
/* Cup closing */
.cup-close{position:relative;height:clamp(300px,45vh,520px);overflow:hidden;}
.cup-close img{width:100%;height:100%;object-fit:cover;object-position:center 40%;display:block;}
.cup-close::after{content:"";position:absolute;inset:0;background:linear-gradient(to bottom,rgba(15,75,70,.1) 0%,rgba(9,104,95,.45) 100%);}
</style>
</head>
<body>
<nav class="nav">
  <button class="burger" id="burger" aria-label="Open menu"><span></span><span></span><span></span></button>
  <a href="index.html" class="nav__logo"><img src="assets/logo-horizontal-white.png" alt="Travesía — A Story in Every Cup"></a>
  <ul class="nav__links">
    <li><a href="index.html#raices">Raíces</a></li>
    <li><a href="our-story.html" data-en="Our Story" data-es="Nuestra Historia">Our Story</a></li>
    <li><a href="index.html#film">Film</a></li>
    <li><a href="index.html#contact" data-en="Contact" data-es="Contacto">Contact</a></li>
  </ul>
  <div class="nav__right">
    <div class="lang"><button data-lang="en" class="active">EN</button><span>/</span><button data-lang="es">ES</button></div>
    <a href="raices.html" aria-label="Raices"><svg class="cart" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.4"><path d="M6 6h15l-1.5 9h-12z"/><circle cx="9" cy="20" r="1"/><circle cx="18" cy="20" r="1"/><path d="M6 6 5 3H2"/></svg></a>
  </div>
</nav>
<div class="mobile-menu" id="mobileMenu">
  <button class="mm-close" id="mmClose" aria-label="Close menu">&times;</button>
  <a href="index.html#raices">Raíces</a>
  <a href="our-story.html" data-en="Our Story" data-es="Nuestra Historia">Our Story</a>
  <a href="index.html#film">Film</a>
  <a href="index.html#contact" data-en="Contact" data-es="Contacto">Contact</a>
  <div class="lang"><button data-lang="en" class="active">EN</button><span>/</span><button data-lang="es">ES</button></div>
  <div class="mm-social">Instagram &middot; Facebook &middot; Twitter</div>
</div>

<section class="opening">
  <div class="opening__logo"><img src="assets/logo-vertical-notag.png" alt="Travesía — A Story in Every Cup"></div>
  <p class="opening__tagline">A Story in Every Cup</p>
  <p data-en="Travesia is the journey we share with those who dared to cross borders &mdash; geographic, emotional, and personal." data-es="Travesia es el viaje que compartimos con quienes se atrevieron a cruzar fronteras &mdash; geograficas, emocionales y personales.">Travesia is the journey we share with those who dared to cross borders &mdash; geographic, emotional, and personal.</p>
  <a href="#gathering" class="roots-link" data-en="The First Gathering &rarr;" data-es="El Primer Encuentro &rarr;">The First Gathering &rarr;</a>
</section>

<section class="river">
  <p data-en="We were born from the desire to honor our roots and turn memory into a bridge between cultures." data-es="Nacimos del deseo de honrar nuestras raices y convertir la memoria en un puente entre culturas.">We were born from the desire to honor our roots and turn memory into a bridge between cultures.</p>
</section>

<section class="film" id="film">
  <span class="chapter" data-en="The Film" data-es="El Film">The Film</span>
  <p data-en="The film that gave Travesia its first voice &mdash; recorded between Bucaramanga and New York." data-es="El film que le dio a Travesia su primera voz &mdash; grabado entre Bucaramanga y New York.">The film that gave Travesia its first voice &mdash; recorded between Bucaramanga and New York.</p>
  <div class="film__player"><button class="film__play" data-track="VideoClick" aria-label="Play film"><svg width="22" height="22" viewBox="0 0 24 24" fill="currentColor"><path d="M8 5v14l11-7z"/></svg></button></div>
</section>

<section class="gathering" id="gathering">
  <span class="chapter" data-en="The First Gathering" data-es="El Primer Encuentro">The First Gathering</span>
  <h2 class="gathering__title" data-en="The First Gathering" data-es="El Primer Encuentro">The First Gathering</h2>
  <p class="gathering__sub" data-en="A private gathering in New York where Travesía shared its first chapter with people from different origins, memories, and journeys." data-es="Un encuentro privado en New York donde Travesía compartió su primer capítulo con personas de distintos orígenes, memorias y travesías.">A private gathering in New York where Travesía shared its first chapter with people from different origins, memories, and journeys.</p>
  <div class="gathering__grid">
    <figure class="g-img g-main">
      <img src="assets/event/event-gathering-01.jpg" alt="Guests holding Raíces bags at The First Gathering" loading="lazy">
    </figure>
    <figure class="g-img g-side">
      <img src="assets/event/event-gathering-02.jpg" alt="Travesía guest with Raíces bag" loading="lazy">
    </figure>
    <figure class="g-img g-side">
      <img src="assets/event/event-gathering-03.jpg" alt="The First Gathering event moment" loading="lazy">
    </figure>
    <figure class="g-img g-side">
      <img src="assets/event/event-gathering-04.jpg" alt="Travesía event guest interaction" loading="lazy">
    </figure>
    <figure class="g-img g-side">
      <img src="assets/event/event-gathering-05.jpg" alt="Raíces bags at the Travesía event" loading="lazy">
    </figure>
    <figure class="g-img g-side">
      <img src="assets/event/event-gathering-06.jpg" alt="Travesía first gathering in New York" loading="lazy">
    </figure>
    <figure class="g-img g-side">
      <img src="assets/event/event-gathering-07.jpg" alt="Travesía community moment" loading="lazy">
    </figure>
    <figure class="g-img g-side">
      <img src="assets/event/event-gathering-08.jpg" alt="Travesía event atmosphere" loading="lazy">
    </figure>
  </div>
  <p class="gathering__note" data-en="New York &middot; 2026" data-es="New York &middot; 2026">New York &middot; 2026</p>
</section>


<!-- BOLSA MADE BY MOM -->
<section class="mom-section">
  <div class="mom__inner">
    <div class="mom__img-wrap">
      <img src="assets/event/event-bolsa-made-by-mom.jpg" alt="Travesia bag — Made by mom, Made in Colombia" loading="lazy">
    </div>
    <div class="mom__text">
      <span class="chapter" data-en="Made by mom" data-es="Hecho por mama">Made by mom</span>
      <h3 data-en="Made by mom.<br>Made in Colombia." data-es="Hecho por mama.<br>Hecho en Colombia.">Made by mom.<br>Made in Colombia.</h3>
      <p data-en="Every bag that arrives with your Raices was sewn by hand in Bucaramanga, Colombia. Not a factory. A family. Warmth you can feel before the first sip." data-es="Cada bolsa que llega con tu Raices fue cosida a mano en Bucaramanga, Colombia. No es una fabrica. Es una familia. Calidez que se siente antes del primer sorbo.">Every bag that arrives with your Raices was sewn by hand in Bucaramanga, Colombia. Not a factory. A family. Warmth you can feel before the first sip.</p>
    </div>
  </div>
</section>

<section class="participants" id="participants">
  <span class="chapter" data-en="Many stories" data-es="Muchas historias">Many stories</span>
  <h2 class="participants__title" data-en="Many stories. One cup." data-es="Muchas historias. Una taza.">Many stories. One cup.</h2>
  <p class="participants__sub" data-en="Ten journeys. Ten origins. The first chapter of Travesia." data-es="Diez travesias. Diez origenes. El primer capitulo de Travesia.">Ten journeys. Ten origins. The first chapter of Travesia.</p>
  <div class="participants__grid">
    <article class="person">
      <div class="person__photo">
        <img src="assets/participants/pierre-zorza.jpg" alt="Pierre Zorza" loading="lazy" onerror="this.style.display='none';">
        <div class="person__ph">PZ</div>
      </div>
      <div class="person__flag">&#x1F1EB;&#x1F1F7;</div>
      <div class="person__name">Pierre Zorza</div>
      <div class="person__country" data-en="France" data-es="Francia">France</div>
      <div class="person__label" data-en="Part of Travesia's first chapter." data-es="Parte del primer capitulo de Travesia.">Part of Travesia's first chapter.</div>
    </article>
    <article class="person">
      <div class="person__photo">
        <img src="assets/participants/juliana-salcedo.jpg" alt="Juliana Salcedo" loading="lazy" onerror="this.style.display='none';">
        <div class="person__ph">JS</div>
      </div>
      <div class="person__flag">&#x1F1E8;&#x1F1F4;</div>
      <div class="person__name">Juliana Salcedo</div>
      <div class="person__country" data-en="Colombia" data-es="Colombia">Colombia</div>
      <div class="person__label" data-en="Part of Travesia's first chapter." data-es="Parte del primer capitulo de Travesia.">Part of Travesia's first chapter.</div>
    </article>
    <article class="person">
      <div class="person__photo">
        <img src="assets/participants/panagiotis-monogioudis.jpg" alt="Panagiotis Monogioudis" loading="lazy" onerror="this.style.display='none';">
        <div class="person__ph">PM</div>
      </div>
      <div class="person__flag">&#x1F1EC;&#x1F1F7;</div>
      <div class="person__name">Panagiotis Monogioudis</div>
      <div class="person__country" data-en="Greece" data-es="Grecia">Greece</div>
      <div class="person__label" data-en="Part of Travesia's first chapter." data-es="Parte del primer capitulo de Travesia.">Part of Travesia's first chapter.</div>
    </article>
    <article class="person">
      <div class="person__photo">
        <img src="assets/participants/wilson-pinilla.jpg" alt="Wilson Pinilla" loading="lazy" onerror="this.style.display='none';">
        <div class="person__ph">WP</div>
      </div>
      <div class="person__flag">&#x1F1E8;&#x1F1F4;</div>
      <div class="person__name">Wilson Pinilla</div>
      <div class="person__country" data-en="Colombia" data-es="Colombia">Colombia</div>
      <div class="person__label" data-en="Part of Travesia's first chapter." data-es="Parte del primer capitulo de Travesia.">Part of Travesia's first chapter.</div>
    </article>
    <article class="person">
      <div class="person__photo">
        <img src="assets/participants/ruoyu-ma.jpg" alt="Ruoyu Ma" loading="lazy" onerror="this.style.display='none';">
        <div class="person__ph">RM</div>
      </div>
      <div class="person__flag">&#x1F1E8;&#x1F1F3;</div>
      <div class="person__name">Ruoyu Ma</div>
      <div class="person__country" data-en="China" data-es="China">China</div>
      <div class="person__label" data-en="Part of Travesia's first chapter." data-es="Parte del primer capitulo de Travesia.">Part of Travesia's first chapter.</div>
    </article>
    <article class="person">
      <div class="person__photo">
        <img src="assets/participants/andrea-noriega.jpg" alt="Andrea Noriega" loading="lazy" onerror="this.style.display='none';">
        <div class="person__ph">AN</div>
      </div>
      <div class="person__flag">&#x1F1F2;&#x1F1FD;</div>
      <div class="person__name">Andrea Noriega</div>
      <div class="person__country" data-en="Mexico" data-es="Mexico">Mexico</div>
      <div class="person__label" data-en="Part of Travesia's first chapter." data-es="Parte del primer capitulo de Travesia.">Part of Travesia's first chapter.</div>
    </article>
    <article class="person">
      <div class="person__photo">
        <img src="assets/participants/maria-rojas.jpg" alt="Maria Rojas" loading="lazy" onerror="this.style.display='none';">
        <div class="person__ph">MR</div>
      </div>
      <div class="person__flag">&#x1F1FB;&#x1F1EA;</div>
      <div class="person__name">Maria Rojas</div>
      <div class="person__country" data-en="Venezuela" data-es="Venezuela">Venezuela</div>
      <div class="person__label" data-en="Part of Travesia's first chapter." data-es="Parte del primer capitulo de Travesia.">Part of Travesia's first chapter.</div>
    </article>
    <article class="person">
      <div class="person__photo">
        <img src="assets/participants/egor-klevtcov.jpg" alt="Egor Klevtcov" loading="lazy" onerror="this.style.display='none';">
        <div class="person__ph">EK</div>
      </div>
      <div class="person__flag">&#x1F1F7;&#x1F1FA;</div>
      <div class="person__name">Egor Klevtcov</div>
      <div class="person__country" data-en="Russia" data-es="Rusia">Russia</div>
      <div class="person__label" data-en="Part of Travesia's first chapter." data-es="Parte del primer capitulo de Travesia.">Part of Travesia's first chapter.</div>
    </article>
    <article class="person">
      <div class="person__photo">
        <img src="assets/participants/djamal-salaouatchi.jpg" alt="Djamal Salaouatchi" loading="lazy" onerror="this.style.display='none';">
        <div class="person__ph">DS</div>
      </div>
      <div class="person__flag">&#x1F1E9;&#x1F1FF;</div>
      <div class="person__name">Djamal Salaouatchi</div>
      <div class="person__country" data-en="Algeria" data-es="Argelia">Algeria</div>
      <div class="person__label" data-en="Part of Travesia's first chapter." data-es="Parte del primer capitulo de Travesia.">Part of Travesia's first chapter.</div>
    </article>
    <article class="person">
      <div class="person__photo">
        <img src="assets/participants/massama-diakite.jpg" alt="Massama Diakite" loading="lazy" onerror="this.style.display='none';">
        <div class="person__ph">MD</div>
      </div>
      <div class="person__flag">&#x1F1F2;&#x1F1F1;</div>
      <div class="person__name">Massama Diakite</div>
      <div class="person__country" data-en="Mali" data-es="Mali">Mali</div>
      <div class="person__label" data-en="Part of Travesia's first chapter." data-es="Parte del primer capitulo de Travesia.">Part of Travesia's first chapter.</div>
    </article>
  </div>
</section>

<!-- CUP CLOSING -->
<section class="cup-close">
  <img src="assets/event/event-travesia-cup-logo.jpg" alt="Travesia — A story in every cup" loading="lazy">
</section>

<section class="cta">
  <h2 data-en="Now it's your turn." data-es="Ahora es tu turno.">Now it's your turn.</h2>
  <a href="index.html#early-access" class="btn-primary cta-main" data-track="PreorderClick" data-ea-en="Join Early Access" data-ea-es="Unirme al Early Access" data-po-en="Preorder Raíces" data-po-es="Reservar Raíces">Join Early Access</a>
</section>

<footer class="footer">
  <div class="footer__grid">
    <div class="footer__brand"><div class="logo"><img src="assets/logo-horizontal-white.png" alt="Travesía — A Story in Every Cup"></div><p class="tagline">A Story in Every Cup</p><div class="footer__social">Instagram &middot; Facebook &middot; Twitter</div></div>
    <div class="footer__col"><h4>Travesia</h4><a href="index.html#raices">Raíces</a><a href="our-story.html" data-en="Our Story" data-es="Nuestra Historia">Our Story</a><a href="index.html#film">Film</a><a href="index.html#contact" data-en="Contact" data-es="Contacto">Contact</a></div>
    <div class="footer__col"><h4 data-en="Support / Legal" data-es="Soporte / Legal">Support / Legal</h4><a href="legal.html#privacy" data-en="Privacy Policy" data-es="Politica de Privacidad">Privacy Policy</a><a href="legal.html#cookies" data-en="Cookie Policy" data-es="Politica de Cookies">Cookie Policy</a><a href="legal.html#terms" data-en="Terms &amp; Conditions" data-es="Terminos y Condiciones">Terms &amp; Conditions</a><a href="legal.html#shipping" data-en="Shipping &amp; Returns" data-es="Envios y Devoluciones">Shipping &amp; Returns</a><a href="index.html#contact" data-en="Customer Service" data-es="Atencion al Cliente">Customer Service</a></div>
  </div>
  <p class="footer__copy">&copy; 2026 Travesia Colombian Corp. All rights reserved.</p>
</footer>

<script>
const SITE_PHASE='early-access'; let LANG='en';
function track(event,params){params=params||{};window.dataLayer=window.dataLayer||[];window.dataLayer.push(Object.assign({event:event},params));if(window.fbq){const s={Lead:'Lead',ViewContent:'ViewContent',AddToCart:'AddToCart',Purchase:'Purchase'};if(s[event])fbq('track',s[event],params);else fbq('trackCustom',event,params);}if(window.ttq){const s={Lead:'SubmitForm',ViewContent:'ViewContent',AddToCart:'AddToCart',Purchase:'CompletePayment'};if(s[event])ttq.track(s[event],params);else ttq.track(event,params);}}
const mm=document.getElementById('mobileMenu');
document.getElementById('burger').addEventListener('click',()=>mm.classList.add('open'));
document.getElementById('mmClose').addEventListener('click',()=>mm.classList.remove('open'));
mm.querySelectorAll('a').forEach(a=>a.addEventListener('click',()=>mm.classList.remove('open')));
function render(){
  document.documentElement.lang=LANG;
  const ea=SITE_PHASE==='early-access';
  document.querySelectorAll('[data-en]').forEach(el=>el.innerHTML=el.getAttribute('data-'+LANG));
  const p=ea?'ea':'po';
  document.querySelectorAll('.cta-main').forEach(el=>{el.innerHTML=el.getAttribute('data-'+p+'-'+LANG);el.setAttribute('href',ea?'index.html#early-access':'raices.html');});
  document.querySelectorAll('.lang button').forEach(b=>b.classList.toggle('active',b.dataset.lang===LANG));
}
function setLang(l){const prev=LANG;LANG=l;render();if(l!==prev)track('LanguageSwitch',{from:prev,to:l,phase:SITE_PHASE,page:'our_story'});}
document.querySelectorAll('.lang button').forEach(b=>b.addEventListener('click',()=>setLang(b.dataset.lang)));
document.querySelectorAll('[data-track]').forEach(el=>el.addEventListener('click',()=>track(el.getAttribute('data-track'),{phase:SITE_PHASE,lang:LANG})));
render();
track('PageView',{phase:SITE_PHASE});
track('ViewContent',{content_name:'our_story',phase:SITE_PHASE});
/* IntersectionObserver — section tracking */
var obs=new IntersectionObserver(function(entries){
  entries.forEach(function(e){
    if(!e.isIntersecting)return;
    var id=e.target.id;
    if(id==='gathering')track('EventGalleryView',{phase:SITE_PHASE,lang:LANG});
    if(id==='participants')track('ParticipantsSectionView',{phase:SITE_PHASE,lang:LANG});
    obs.unobserve(e.target);
  });
},{threshold:0.15});
['gathering','participants'].forEach(function(id){var el=document.getElementById(id);if(el)obs.observe(el);});
</script>
</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Raíces — Travesía</title>
<meta name="description" content="Raíces — specialty Colombian coffee from Santander.">
<link rel="icon" type="image/png" href="assets/symbol-color.png">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,500;0,600;1,300;1,400;1,500&family=DM+Sans:wght@300;400;500&display=swap" rel="stylesheet">
<style>
/* TRAVESÍA — Producto Raíces · paleta oficial · dos fases (SITE_PHASE en script). */
:root{--coffee:#473224;--coffee-deep:#3d2a1c;--night:#3d2a1c;--teal:#018E86;--teal-deep:#09685F;--gold:#BE9F56;--gold-soft:#cdb877;--beige:#E1D6C0;--paper:#F2EADB;--cream:#FAF8F4;--ink:#2e2014;--font-hero:'Cormorant Garamond',serif;--font-display:'Cormorant Garamond',serif;--font-serif:'Cormorant Garamond',serif;--font-sans:'DM Sans',system-ui,sans-serif;}
*{margin:0;padding:0;box-sizing:border-box;}html{scroll-behavior:smooth;}
body{background:var(--paper);color:var(--ink);font-family:var(--font-serif);-webkit-font-smoothing:antialiased;overflow-x:hidden;}
img{display:block;max-width:100%;}a{color:inherit;text-decoration:none;}button{font-family:inherit;cursor:pointer;border:none;background:none;}
a:focus-visible,button:focus-visible,input:focus-visible,select:focus-visible{outline:2px solid var(--gold);outline-offset:3px;}
.only-ea,.only-po{display:none;}
body::after{content:"";position:fixed;inset:0;z-index:9999;pointer-events:none;opacity:.03;mix-blend-mode:overlay;background-image:url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='120' height='120'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.85' numOctaves='2'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)'/%3E%3C/svg%3E");}
.chapter{font-family:var(--font-sans);font-size:11px;text-transform:uppercase;letter-spacing:.34em;color:var(--gold);display:inline-flex;align-items:center;gap:14px;}
.chapter::before{content:"";width:36px;height:1px;background:var(--gold);}
.nav{position:fixed;top:0;left:0;right:0;z-index:100;height:72px;display:grid;grid-template-columns:auto 1fr auto;align-items:center;padding:0 24px;background:rgba(58,39,25,.94);backdrop-filter:blur(8px);-webkit-backdrop-filter:blur(8px);}
.nav__logo{justify-self:center;line-height:0;}.nav__logo img{height:34px;width:auto;max-width:170px;object-fit:contain;}
.nav__links{display:none;gap:36px;justify-content:center;list-style:none;}
.nav__links a{font-family:var(--font-sans);font-size:13px;text-transform:uppercase;letter-spacing:.12em;color:var(--cream);transition:color .2s;}
.nav__links a:hover{color:var(--gold);}
.nav__right{display:flex;align-items:center;gap:20px;justify-self:end;}
.lang{display:flex;align-items:center;gap:6px;font-family:var(--font-sans);font-size:13px;text-transform:uppercase;letter-spacing:.12em;}
.lang button{color:var(--cream);transition:color .2s;}.lang button.active{color:var(--gold);}.lang span{color:var(--beige);opacity:.5;}
.cart{color:var(--cream);width:22px;height:22px;}
.burger{color:var(--cream);justify-self:start;display:flex;flex-direction:column;gap:5px;padding:6px 0;}
.burger span{width:24px;height:1.5px;background:currentColor;display:block;}
.mobile-menu{position:fixed;inset:0;z-index:99;background:var(--coffee-deep);display:flex;flex-direction:column;justify-content:center;align-items:center;gap:32px;transform:translateX(-100%);transition:transform .35s;}
.mobile-menu.open{transform:translateX(0);}
.mobile-menu a{font-family:var(--font-sans);font-size:15px;text-transform:uppercase;letter-spacing:.12em;color:var(--cream);}
.mobile-menu .mm-social{display:flex;gap:24px;margin-top:24px;color:var(--beige);}
.mobile-menu .mm-close{position:absolute;top:24px;right:24px;color:var(--cream);font-size:28px;}
@media(min-width:980px){.nav{height:80px;padding:0 80px;}.nav__logo{justify-self:start;}.nav__logo img{height:42px;max-width:230px;}.nav__links{display:flex;}.burger{display:none;}.mobile-menu{display:none;}}
.btn-primary{font-family:var(--font-sans);font-size:12px;font-weight:500;text-transform:uppercase;letter-spacing:.16em;background:var(--gold);color:var(--coffee);padding:16px 38px;border-radius:0;display:inline-block;transition:background .25s;}
.btn-primary:hover{background:var(--gold-soft);}
/* Producto */
.product{position:relative;background:var(--coffee);color:var(--beige);padding:130px 24px 90px;overflow:hidden;}
.product::before{content:"";position:absolute;inset:0;background:radial-gradient(80% 80% at 30% 25%,rgba(0,0,0,0) 40%,rgba(58,39,25,.28) 100%);pointer-events:none;}
.product__grid{position:relative;max-width:1140px;margin:0 auto;display:grid;grid-template-columns:1fr;gap:48px;}
.gallery__main{aspect-ratio:1/1;background:radial-gradient(70% 60% at 50% 38%,#5e4230,var(--coffee-deep));border:1px solid rgba(190,159,86,.3);margin-bottom:14px;display:flex;align-items:flex-end;justify-content:center;color:rgba(225,214,192,.5);font-family:var(--font-sans);font-size:11px;letter-spacing:.2em;text-transform:uppercase;padding:22px;}
.gallery__thumbs{display:grid;grid-template-columns:repeat(3,1fr);gap:12px;}
.gallery__thumbs div{aspect-ratio:1/1;background:var(--coffee-deep);border:1px solid rgba(190,159,86,.18);display:flex;align-items:center;justify-content:center;color:rgba(225,214,192,.5);font-family:var(--font-sans);font-size:10px;text-transform:uppercase;letter-spacing:.12em;}
.info .chapter{margin-bottom:18px;}
.info__title{font-family:var(--font-display);font-size:clamp(38px,6vw,60px);color:var(--cream);margin:6px 0 20px;}
.info__story{font-family:var(--font-serif);font-style:italic;font-size:17px;line-height:1.5;color:rgba(225,214,192,.85);margin-bottom:24px;max-width:46ch;}
.notes{font-family:var(--font-sans);font-size:12px;color:var(--gold-soft);letter-spacing:.06em;margin-bottom:28px;}
.ea-box{border:1px solid rgba(190,159,86,.4);padding:24px;margin-bottom:24px;}
.ea-box h3{font-family:var(--font-display);font-size:20px;color:var(--cream);margin-bottom:10px;}
.ea-box p{font-family:var(--font-serif);font-size:16px;color:rgba(225,214,192,.85);line-height:1.5;}
.price-block .now{font-family:var(--font-serif);font-size:24px;color:var(--cream);}
.price-block .later{display:block;font-family:var(--font-sans);font-size:12px;font-weight:300;color:rgba(225,214,192,.6);margin:4px 0 28px;}
.disclaimer{margin-top:24px;max-width:52ch;font-family:var(--font-serif);font-size:15px;line-height:1.5;color:rgba(225,214,192,.72);border-top:1px solid rgba(190,159,86,.25);padding-top:20px;}
@media(min-width:980px){.product__grid{grid-template-columns:1fr 1fr;gap:70px;}}
/* Ficha */
.spec{background:var(--beige);padding:90px 24px;}
.spec__wrap{max-width:720px;margin:0 auto;}
.spec h2{font-family:var(--font-display);font-size:clamp(24px,3.5vw,34px);color:var(--ink);margin-bottom:28px;text-align:center;}
.spec table{width:100%;border-collapse:collapse;}
.spec td{padding:14px 0;border-bottom:1px solid rgba(71,50,36,.18);vertical-align:top;}
.spec td.field{font-family:var(--font-sans);font-size:12px;text-transform:uppercase;letter-spacing:.12em;color:var(--teal-deep);width:42%;}
.spec td.value{font-family:var(--font-serif);font-size:17px;color:var(--ink);}
/* FAQ */
.faq{padding:90px 24px;background:var(--paper);}
.faq h2,.faq details{max-width:760px;margin-left:auto;margin-right:auto;}
.faq h2{font-family:var(--font-display);font-size:clamp(24px,3.5vw,34px);color:var(--ink);margin-bottom:32px;text-align:center;}
.faq details{border-bottom:1px solid rgba(71,50,36,.18);padding:18px 0;}
.faq summary{font-family:var(--font-sans);font-weight:500;font-size:15px;color:var(--ink);cursor:pointer;list-style:none;display:flex;justify-content:space-between;align-items:center;gap:16px;}
.faq summary::-webkit-details-marker{display:none;}
.faq summary::after{content:"+";color:var(--gold);font-size:20px;}
.faq details[open] summary::after{content:"\2013";}
.faq p{font-family:var(--font-serif);font-size:16px;line-height:1.5;color:var(--coffee);margin-top:14px;}
/* Footer */
.footer{background:var(--coffee-deep);color:var(--beige);padding:72px 24px 56px;}
.footer__grid{display:grid;grid-template-columns:1fr;gap:40px;max-width:1100px;margin:0 auto;}
.footer__brand .logo img{height:34px;width:auto;}
.footer__brand .tagline{font-family:var(--font-hero);font-size:17px;letter-spacing:.02em;color:rgba(225,214,192,.82);margin:16px 0 16px;}
.footer__social{display:flex;gap:18px;color:var(--beige);}
.footer__col h4{font-family:var(--font-sans);font-size:13px;text-transform:uppercase;letter-spacing:.12em;color:var(--gold);margin-bottom:16px;font-weight:500;}
.footer__col a{display:block;font-family:var(--font-sans);font-size:13px;font-weight:300;color:rgba(225,214,192,.8);margin-bottom:10px;transition:color .2s;}
.footer__col a:hover{color:var(--cream);}
.footer__copy{text-align:center;margin-top:48px;font-family:var(--font-sans);font-size:11px;color:rgba(225,214,192,.5);}
@media(min-width:980px){.footer{padding:80px 80px 56px;}.footer__grid{grid-template-columns:1.4fr 1fr 1fr;gap:64px;}}
.info__title,.spec h2,.faq h2{font-weight:600;letter-spacing:-0.01em;}
/* ===== Raices - Estimador de envio UPS ===== */
.shipping-estimator{background:var(--cream);border:1px solid rgba(190,159,86,.35);padding:28px 26px 22px;margin-top:32px;}
.shipping-estimator__title{font-family:var(--font-sans);font-size:10px;text-transform:uppercase;letter-spacing:.26em;color:var(--coffee);margin-bottom:18px;}
.shipping-estimator__row{display:flex;gap:10px;align-items:stretch;flex-wrap:wrap;}
.shipping-estimator input{flex:1 1 160px;font-family:var(--font-sans);font-size:14px;color:var(--coffee);background:var(--paper);border:1px solid rgba(190,159,86,.5);padding:11px 14px;outline:none;min-width:0;transition:border-color .2s;}
.shipping-estimator input::placeholder{color:rgba(71,50,36,.45);}
.shipping-estimator input:focus{border-color:var(--gold);}
.shipping-estimator button{font-family:var(--font-sans);font-size:11px;font-weight:500;text-transform:uppercase;letter-spacing:.18em;background:var(--teal-deep);color:var(--cream);padding:11px 24px;border:none;cursor:pointer;transition:background .22s;white-space:nowrap;}
.shipping-estimator button:hover{background:var(--teal);}
.shipping-estimator__output{margin-top:14px;font-family:var(--font-serif);font-size:16px;font-style:italic;color:var(--teal-deep);line-height:1.4;}
.shipping-estimator__output:empty{margin-top:0;}
.shipping-estimator__output.error{color:#8b3a2a;font-style:normal;font-size:14px;}
.shipping-estimator__note{margin-top:14px;font-family:var(--font-sans);font-size:11px;color:rgba(71,50,36,.55);line-height:1.5;letter-spacing:.02em;}
@media(max-width:440px){.shipping-estimator__row{flex-direction:column;}.shipping-estimator button{width:100%;}}
/* ===== The Travesia Experience ===== */
.experience{background:var(--teal-deep);color:var(--cream);padding:clamp(80px,10vh,130px) 24px;text-align:center;}
.experience__wrap{max-width:580px;margin:0 auto;}
.experience__chapter{display:block;font-family:var(--font-sans);font-size:10px;text-transform:uppercase;letter-spacing:.28em;color:var(--gold-soft);margin-bottom:28px;}
.experience__text{font-family:var(--font-serif);font-style:italic;font-size:clamp(18px,2.4vw,22px);line-height:1.6;color:rgba(250,248,244,.92);margin-bottom:28px;}
.experience__sign{font-family:var(--font-hero);font-size:17px;letter-spacing:.02em;color:var(--gold-soft);margin-bottom:22px;}
.experience__card{font-family:var(--font-sans);font-size:12px;color:rgba(250,248,244,.55);letter-spacing:.04em;border-top:1px solid rgba(190,159,86,.25);padding-top:18px;margin-top:8px;line-height:1.5;}
</style>
</head>
<body>
<nav class="nav">
  <button class="burger" id="burger" aria-label="Open menu"><span></span><span></span><span></span></button>
  <a href="index.html" class="nav__logo"><img src="assets/logo-horizontal-white.png" alt="Travesía — A Story in Every Cup"></a>
  <ul class="nav__links">
    <li><a href="raices.html">Raíces</a></li>
    <li><a href="our-story.html" data-en="Our Story" data-es="Nuestra Historia">Our Story</a></li>
    <li><a href="index.html#film">Film</a></li>
    <li><a href="index.html#contact" data-en="Contact" data-es="Contacto">Contact</a></li>
  </ul>
  <div class="nav__right">
    <div class="lang"><button data-lang="en" class="active">EN</button><span>/</span><button data-lang="es">ES</button></div>
    <a href="raices.html" aria-label="Raices"><svg class="cart" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.4"><path d="M6 6h15l-1.5 9h-12z"/><circle cx="9" cy="20" r="1"/><circle cx="18" cy="20" r="1"/><path d="M6 6 5 3H2"/></svg></a>
  </div>
</nav>
<div class="mobile-menu" id="mobileMenu">
  <button class="mm-close" id="mmClose" aria-label="Close menu">&times;</button>
  <a href="raices.html">Raíces</a>
  <a href="our-story.html" data-en="Our Story" data-es="Nuestra Historia">Our Story</a>
  <a href="index.html#film">Film</a>
  <a href="index.html#contact" data-en="Contact" data-es="Contacto">Contact</a>
  <div class="lang"><button data-lang="en" class="active">EN</button><span>/</span><button data-lang="es">ES</button></div>
  <div class="mm-social">Instagram &middot; Facebook &middot; Twitter</div>
</div>
<section class="product">
  <div class="product__grid">
    <div class="gallery">
      <div class="gallery__main"></div>
      <div class="gallery__thumbs"><div></div><div></div><div></div></div>
    </div>
    <div class="info">
      <span class="chapter" data-en="First edition - Santander, Colombia" data-es="Primera edicion - Santander, Colombia">First edition - Santander, Colombia</span>
      <h1 class="info__title">Raíces</h1>
      <p class="info__story" data-en="Raices is Travesia's first limited release — a specialty Colombian coffee from Santander, created as the first chapter of a journey between origin, memory, and New York." data-es="Raices es la primera edicion limitada de Travesia — un cafe colombiano de especialidad de Santander, creado como el primer capitulo de una travesia entre el origen, la memoria y New York.">Raices is Travesia's first limited release — a specialty Colombian coffee from Santander, created as the first chapter of a journey between origin, memory, and New York.</p>
      <p class="notes" data-en="Chocolate - Panela - Red fruits - Almond" data-es="Chocolate - Panela - Frutos rojos - Almendra">Chocolate - Panela - Red fruits - Almond</p>
      <div class="ea-box only-ea">
        <h3 data-en="First Edition — Early Access" data-es="Primera Edicion — Early Access">First Edition — Early Access</h3>
        <p data-en="Raices is not on sale yet. Join the priority list now to get early access to the official preorder. This is registration, not a purchase." data-es="Raices aun no esta a la venta. Unete ahora a la lista prioritaria para recibir acceso anticipado a la preventa oficial. Esto es un registro, no una compra.">Raices is not on sale yet. Join the priority list now to get early access to the official preorder. This is registration, not a purchase.</p>
      </div>
      <a href="index.html#early-access" class="btn-primary cta-main" data-track="PreorderClick" data-ea-en="Join Early Access" data-ea-es="Unirme al Early Access" data-po-en="Preorder Raíces" data-po-es="Reservar Raíces">Join Early Access</a>
      <div class="price-block only-po">
        <span class="now" data-en="Raices — First Edition · $20.99" data-es="Raices — Primera Edicion · $20.99">Raices — First Edition · $20.99</span>
        <span class="later" data-en="Editorial Edition · $24.50 after first release" data-es="Edicion Editorial · $24.50 despues del primer lanzamiento">Editorial Edition · $24.50 after first release</span>
      </div>
      <p class="disclaimer only-po" data-en="Raices is Travesia's first limited release — a specialty Colombian coffee from Santander. Orders are prepared after the preorder closes and shipped according to the confirmed schedule. Shipping is calculated at checkout." data-es="Raices es la primera edicion limitada de Travesia — un cafe colombiano de especialidad de Santander. Los pedidos se preparan tras el cierre de la preventa y se envian segun el cronograma confirmado. El envio se calcula al finalizar la compra.">Raices is Travesia's first limited release — a specialty Colombian coffee from Santander.</p>
      <div class="shipping-estimator only-po">
        <h4 class="shipping-estimator__title" data-en="Estimate delivery time" data-es="Estimar tiempo de entrega">Estimate delivery time</h4>
        <div class="shipping-estimator__row">
          <input id="zipInput" type="text" inputmode="numeric" maxlength="5"
            data-en-ph="ZIP Code" data-es-ph="Codigo ZIP" placeholder="ZIP Code">
          <button id="zipCheck" data-en="Check" data-es="Verificar">Check</button>
        </div>
        <div id="zipResult" class="shipping-estimator__output" aria-live="polite"></div>
        <p class="shipping-estimator__note"
          data-en="Estimated UPS® Ground delivery from New York. Free shipping on orders $49+. Final shipping cost and delivery time are confirmed at checkout."
          data-es="Entrega estimada por UPS® Ground desde New York. Envío gratis en pedidos de $49+. El costo final de envio y el tiempo de entrega se confirman al finalizar la compra.">Estimated UPS® Ground delivery from New York. Free shipping on orders $49+. Final shipping cost and delivery time are confirmed at checkout.</p>
      </div>
    </div>
  </div>
</section>

<!-- THE TRAVESIA EXPERIENCE -->
<section class="experience">
  <div class="experience__wrap">
    <span class="experience__chapter" data-en="The Travesia Experience" data-es="La Experiencia Travesia">The Travesia Experience</span>
    <p class="experience__text" data-en="Before the first sip, pause for a moment. Hold the bag with both hands, bring it slowly to your nose, close your eyes, and breathe deeply. Let the aroma awaken your memories, your origin, and the moments that live within you." data-es="Antes del primer sorbo, detente un momento. Sostен la bolsa con ambas manos, acercala lentamente a tu nariz, cierra los ojos y respira profundo. Deja que el aroma despierte tus recuerdos, tu origen y los momentos que viven en ti.">Before the first sip, pause for a moment. Hold the bag with both hands, bring it slowly to your nose, close your eyes, and breathe deeply. Let the aroma awaken your memories, your origin, and the moments that live within you.</p>
    <p class="experience__sign">Travesia &mdash; <em>A Story in Every Cup</em></p>
    <p class="experience__card" data-en="Each bag includes a vertical experience card with a sensory ritual on one side and preparation guidance on the other." data-es="Cada bolsa incluye una tarjeta vertical de experiencia con un ritual sensorial por un lado y una guia de preparacion por el otro.">Each bag includes a vertical experience card with a sensory ritual on one side and preparation guidance on the other.</p>
  </div>
</section>

<section class="spec">
  <div class="spec__wrap">
    <h2 data-en="Product details" data-es="Ficha tecnica">Product details</h2>
    <table>
      <tr><td class="field" data-en="Name" data-es="Nombre">Name</td><td class="value">Raices</td></tr>
      <tr><td class="field" data-en="Type" data-es="Tipo">Type</td><td class="value" data-en="Specialty Colombian Coffee" data-es="Cafe colombiano de especialidad">Specialty Colombian Coffee</td></tr>
      <tr><td class="field" data-en="Origin" data-es="Origen">Origin</td><td class="value">Santander, Colombia</td></tr>
      <tr><td class="field" data-en="Size" data-es="Tamano">Size</td><td class="value">250g / 8.8 oz</td></tr>
      <tr><td class="field" data-en="Process" data-es="Proceso">Process</td><td class="value" data-en="Washed" data-es="Lavado">Washed</td></tr>
      <tr><td class="field" data-en="Tasting notes" data-es="Notas de cata">Tasting notes</td><td class="value" data-en="Chocolate - Panela - Red fruits - Almond" data-es="Chocolate - Panela - Frutos rojos - Almendra">Chocolate - Panela - Red fruits - Almond</td></tr>
      <tr class="only-ea"><td class="field" data-en="Status" data-es="Estado">Status</td><td class="value" data-en="Early Access - preorder opening soon" data-es="Early Access - preventa proximamente">Early Access - preorder opening soon</td></tr>
      <tr class="only-po"><td class="field" data-en="Status" data-es="Estado">Status</td><td class="value" data-en="Preorder - limited to 300" data-es="Preventa - solo 300 unidades">Preorder - limited to 300</td></tr>
      <tr class="only-po"><td class="field" data-en="Preorder Price" data-es="Precio de preventa">Preorder Price</td><td class="value">$20.99</td></tr>
      <tr class="only-po"><td class="field" data-en="Regular Price" data-es="Precio regular">Regular Price</td><td class="value" data-en="$24.50 — Editorial Edition" data-es="$24.50 — Edicion Editorial">$24.50 — Editorial Edition</td></tr>
      <tr class="only-po"><td class="field" data-en="Shipping" data-es="Envio">Shipping</td><td class="value" data-en="Calculated at checkout" data-es="Calculado al finalizar la compra">Calculated at checkout</td></tr>
      <tr><td class="field" data-en="Support" data-es="Soporte">Support</td><td class="value">info@travesiacolombiancoffee.com</td></tr>
    </table>
  </div>
</section>
<section class="faq">
  <h2 data-en="Frequently asked" data-es="Preguntas frecuentes">Frequently asked</h2>
  <details class="only-ea"><summary data-en="Is Early Access a purchase?" data-es="Early Access es una compra?">Is Early Access a purchase?</summary><p data-en="No. Early Access is free registration for the priority list. You secure early access to the official preorder when it opens." data-es="No. El Early Access es un registro gratuito a la lista prioritaria. Aseguras acceso anticipado a la preventa oficial cuando abra.">No. Early Access is free registration for the priority list.</p></details>
  <details class="only-ea"><summary data-en="When will the preorder open?" data-es="Cuando abrira la preventa?">When will the preorder open?</summary><p data-en="Early Access members will be the first to know by email when the official preorder opens." data-es="Los miembros del Early Access seran los primeros en enterarse por correo cuando abra la preventa oficial.">Early Access members will be the first to know by email.</p></details>
  <details><summary data-en="Does it come ground or whole bean?" data-es="Viene molido o en grano?">Does it come ground or whole bean?</summary><p data-en="Raices is available whole bean or ground. Select your preference at checkout." data-es="Raices esta disponible en grano entero o molido. Selecciona tu preferencia al finalizar la compra.">Raices is available whole bean or ground. Select your preference at checkout.</p></details>
  <details><summary data-en="How should I store it?" data-es="Como conservarlo?">How should I store it?</summary><p data-en="Store in a cool, dry place away from direct sunlight. Consume within 30 days of opening for best flavor. The resealable bag keeps freshness between uses." data-es="Conserva en un lugar fresco y seco, alejado de la luz directa del sol. Consume dentro de los 30 dias posteriores a la apertura para un mejor sabor. La bolsa resellable mantiene la frescura entre usos.">Store in a cool, dry place away from direct sunlight. Consume within 30 days of opening for best flavor. The resealable bag keeps freshness between uses.</p></details>
  <details class="only-po"><summary data-en="What is preorder?" data-es="Que significa preventa?">What is preorder?</summary><p data-en="Preorder is early access to the first chapter of Travesia. You reserve Raices now; orders are processed according to the release schedule confirmed by Travesia." data-es="La preventa es acceso anticipado al primer capitulo de Travesia. Reservas Raices ahora; los pedidos se procesan segun el cronograma de lanzamiento confirmado por Travesia.">Preorder is early access to the first chapter of Travesia.</p></details>
  <details class="only-po"><summary data-en="When will my order ship?" data-es="Cuando se enviara mi pedido?">When will my order ship?</summary><p data-en="Orders are prepared after the preorder closes and ship according to the estimated schedule confirmed by Travesia. You will be notified by email." data-es="Los pedidos se preparan tras el cierre de la preventa y se envian segun el cronograma estimado confirmado por Travesia. Te notificaremos por correo.">Orders are prepared after the preorder closes.</p></details>
  <details class="only-po"><summary data-en="Can I cancel my preorder?" data-es="Puedo cancelar mi preventa?">Can I cancel my preorder?</summary><p data-en="Preorder cancellations may be requested before the preorder period closes by contacting info@travesiacolombiancoffee.com. Please include your order number. Requests after closure are reviewed on a case-by-case basis." data-es="Las cancelaciones de preventa pueden solicitarse antes del cierre del periodo de preventa contactando info@travesiacolombiancoffee.com. Incluye tu numero de pedido. Las solicitudes despues del cierre se revisan caso por caso.">Preorder cancellations may be requested before the preorder period closes by contacting info@travesiacolombiancoffee.com.</p></details>
  <details class="only-po"><summary data-en="What happens if the estimated date changes?" data-es="Que pasa si cambia la fecha estimada?">What happens if the estimated date changes?</summary><p data-en="If the estimated date changes, Travesia will notify you by email with the updated schedule." data-es="Si la fecha estimada cambia, Travesia te notificara por correo con el cronograma actualizado.">If the estimated date changes, Travesia will notify you by email.</p></details>
  <details><summary data-en="Where do you ship?" data-es="En que paises estara disponible el envio?">Where do you ship?</summary><p data-en="During the first release, Travesia will ship within the United States. Shipping options, final cost, and estimated delivery time are confirmed at checkout." data-es="Durante el primer lanzamiento, Travesia realizara envios dentro de Estados Unidos. Las opciones de envio, el costo final y el tiempo estimado de entrega se confirman al finalizar la compra.">During the first release, Travesia will ship within the United States.</p></details>
  <details><summary data-en="How do I contact Travesia?" data-es="Como contacto a Travesia?">How do I contact Travesia?</summary><p data-en="You can contact Travesia at info@travesiacolombiancoffee.com" data-es="Puedes contactar a Travesia en info@travesiacolombiancoffee.com">You can contact Travesia at info@travesiacolombiancoffee.com</p></details>
</section>
<footer class="footer">
  <div class="footer__grid">
    <div class="footer__brand"><div class="logo"><img src="assets/logo-horizontal-white.png" alt="Travesía — A Story in Every Cup"></div><p class="tagline">A Story in Every Cup</p><div class="footer__social">Instagram &middot; Facebook &middot; Twitter</div></div>
    <div class="footer__col"><h4>Travesia</h4><a href="raices.html">Raíces</a><a href="our-story.html" data-en="Our Story" data-es="Nuestra Historia">Our Story</a><a href="index.html#film">Film</a><a href="index.html#contact" data-en="Contact" data-es="Contacto">Contact</a></div>
    <div class="footer__col"><h4 data-en="Support / Legal" data-es="Soporte / Legal">Support / Legal</h4><a href="legal.html#privacy" data-en="Privacy Policy" data-es="Politica de Privacidad">Privacy Policy</a><a href="legal.html#cookies" data-en="Cookie Policy" data-es="Politica de Cookies">Cookie Policy</a><a href="legal.html#terms" data-en="Terms &amp; Conditions" data-es="Terminos y Condiciones">Terms &amp; Conditions</a><a href="legal.html#shipping" data-en="Shipping &amp; Returns" data-es="Envios y Devoluciones">Shipping &amp; Returns</a><a href="index.html#contact" data-en="Customer Service" data-es="Atencion al Cliente">Customer Service</a></div>
  </div>
  <p class="footer__copy">&copy; 2026 Travesia Colombian Corp. All rights reserved.</p>
</footer>
<script>
const SITE_PHASE='early-access'; let LANG='en';
const PAGE=document.body.dataset.page||'raices';
function track(event,params){params=params||{};window.dataLayer=window.dataLayer||[];window.dataLayer.push(Object.assign({event:event},params));if(window.fbq){const s={Lead:'Lead',ViewContent:'ViewContent',AddToCart:'AddToCart',Purchase:'Purchase'};if(s[event])fbq('track',s[event],params);else fbq('trackCustom',event,params);}if(window.ttq){const s={Lead:'SubmitForm',ViewContent:'ViewContent',AddToCart:'AddToCart',Purchase:'CompletePayment'};if(s[event])ttq.track(s[event],params);else ttq.track(event,params);}}
const mm=document.getElementById('mobileMenu');
document.getElementById('burger').addEventListener('click',()=>mm.classList.add('open'));
document.getElementById('mmClose').addEventListener('click',()=>mm.classList.remove('open'));
mm.querySelectorAll('a').forEach(a=>a.addEventListener('click',()=>mm.classList.remove('open')));
function render(){document.documentElement.lang=LANG;const ea=SITE_PHASE==='early-access';
  document.querySelectorAll('.only-ea').forEach(el=>el.style.display=ea?'':'none');
  document.querySelectorAll('.only-po').forEach(el=>el.style.display=ea?'none':'');
  document.querySelectorAll('[data-en]').forEach(el=>el.innerHTML=el.getAttribute('data-'+LANG));
  document.querySelectorAll('[data-en-ph]').forEach(el=>el.placeholder=el.getAttribute('data-'+LANG+'-ph'));
  const p=ea?'ea':'po';
  document.querySelectorAll('.cta-main').forEach(el=>{el.innerHTML=el.getAttribute('data-'+p+'-'+LANG);el.setAttribute('href',ea?'index.html#early-access':'#');});
  document.querySelectorAll('.lang button').forEach(b=>b.classList.toggle('active',b.dataset.lang===LANG));}
function setLang(l){const prev=LANG;LANG=l;render();if(l!==prev)track("LanguageSwitch",{from:prev,to:l,phase:SITE_PHASE,page:"raices"});}
document.querySelectorAll('.lang button').forEach(b=>b.addEventListener('click',()=>setLang(b.dataset.lang)));
document.querySelectorAll('[data-track]').forEach(el=>el.addEventListener('click',function(){
  var ev=this.getAttribute('data-track');
  track(ev,{phase:SITE_PHASE,lang:LANG,product:'raices'});
  if(ev==='PreorderClick'&&SITE_PHASE==='preorder')track('BeginCheckout',{phase:SITE_PHASE,lang:LANG,product:'raices',price:20.99,currency:'USD'});
}));
/* ===== TRAVESIA - UPS Ground delivery estimator ===== */
(function(){
  var zipInput=document.getElementById('zipInput');
  var zipCheck=document.getElementById('zipCheck');
  var zipResult=document.getElementById('zipResult');
  if(!zipInput||!zipCheck||!zipResult)return;
  var lastZip=null;
  var MSGS={
    invalid:{en:'Please enter a valid 5-digit ZIP Code.',es:'Por favor, ingresa un codigo ZIP valido de 5 digitos.'},
    d01:{en:'UPS Ground: estimated delivery in 1-2 business days.',es:'UPS Ground: entrega estimada en 1-2 dias habiles.'},
    d23:{en:'UPS Ground: estimated delivery in 2-3 business days.',es:'UPS Ground: entrega estimada en 2-3 dias habiles.'},
    d45:{en:'UPS Ground: estimated delivery in 4-5 business days.',es:'UPS Ground: entrega estimada en 4-5 dias habiles.'}
  };
  function getKey(d){if(d==='0'||d==='1')return 'd01';if(d==='2'||d==='3'||d==='4')return 'd23';return 'd45';}
  function renderZipResult(){
    if(lastZip===null)return;
    if(lastZip===''){zipResult.textContent=MSGS.invalid[LANG];zipResult.classList.add('error');return;}
    zipResult.textContent=MSGS[getKey(lastZip[0])][LANG];zipResult.classList.remove('error');
  }
  function checkZip(){
    var zip=(zipInput.value||'').replace(/\s/g,'');
    if(!/^\d{5}$/.test(zip)){lastZip='';zipResult.textContent=MSGS.invalid[LANG];zipResult.classList.add('error');return;}
    lastZip=zip;zipResult.textContent=MSGS[getKey(zip[0])][LANG];zipResult.classList.remove('error');
    track('ShippingEstimateCheck',{zip_prefix:zip[0],page:PAGE,lang:LANG,phase:SITE_PHASE});
  }
  zipCheck.addEventListener('click',checkZip);
  zipInput.addEventListener('keydown',function(e){if(e.key==='Enter')checkZip();});
  var _origSetLang=setLang;
  setLang=function(l){_origSetLang(l);renderZipResult();};
})();
render();track('PageView',{phase:SITE_PHASE});track('ViewContent',{content_name:'raices',phase:SITE_PHASE});

</script>
</body>
</html>
