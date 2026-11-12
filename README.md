# axmedali-jpg.github.io
# Ahmed Ali and Personal IT Portfolio Website
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Ahmed Ali | IT Student at Eastern Michigan University</title>
<meta name="description" content="Ahmed Ali – EMU Information Technology sophomore passionate about applying tech skills to real-world issues. IT Support, Data Analytics, System Administration.">
<style>
  :root{
    --navy:#0b1f3a;
    --navy-2:#102a4c;
    --navy-3:#17375f;
    --gold:#d4a017;
    --gold-soft:#f1c94b;
    --ink:#142033;
    --muted:#5a6b82;
    --bg:#f6f7fa;
    --card:#ffffff;
    --line:#e3e7ee;
    --radius:16px;
    --shadow:0 10px 30px rgba(11,31,58,.08);
    --max:1100px;
  }
  *{box-sizing:border-box;margin:0;padding:0}
  html{scroll-behavior:smooth;scroll-padding-top:76px}
  body{
    font-family:system-ui,-apple-system,"Segoe UI",Roboto,Helvetica,Arial,sans-serif;
    color:var(--ink);background:var(--bg);line-height:1.65;-webkit-font-smoothing:antialiased;
  }
  a{color:inherit;text-decoration:none}
  img,svg{max-width:100%}
  .container{width:100%;max-width:var(--max);margin:0 auto;padding:0 24px}
  section{padding:96px 0}
  .eyebrow{
    display:inline-block;font-size:.78rem;font-weight:700;letter-spacing:.16em;text-transform:uppercase;
    color:var(--gold);margin-bottom:12px
  }
  h2{font-size:clamp(1.8rem,4vw,2.5rem);line-height:1.15;color:var(--navy);letter-spacing:-.02em}
  .section-head{margin-bottom:48px;max-width:640px}
  .section-head p{color:var(--muted);margin-top:12px}
  .btn{
    display:inline-flex;align-items:center;gap:10px;padding:14px 26px;border-radius:999px;font-weight:600;
    font-size:.98rem;border:2px solid transparent;cursor:pointer;transition:transform .2s,box-shadow .2s,background .2s,color .2s;
    font-family:inherit
  }
  .btn:hover{transform:translateY(-2px)}
  .btn-gold{background:var(--gold);color:var(--navy);box-shadow:0 8px 22px rgba(212,160,23,.35)}
  .btn-gold:hover{background:var(--gold-soft)}
  .btn-ghost{border-color:rgba(255,255,255,.35);color:#fff}
  .btn-ghost:hover{border-color:var(--gold);color:var(--gold)}
  .btn-navy{background:var(--navy);color:#fff}
  .btn-navy:hover{background:var(--navy-3)}
  :focus-visible{outline:3px solid var(--gold);outline-offset:3px;border-radius:6px}

  /* NAV */
  header.nav{
    position:fixed;inset:0 0 auto 0;z-index:100;transition:background .3s,box-shadow .3s,padding .3s;
    padding:18px 0
  }
  header.nav.scrolled{background:rgba(11,31,58,.96);backdrop-filter:blur(8px);box-shadow:0 4px 20px rgba(0,0,0,.2);padding:12px 0}
  .nav-inner{display:flex;align-items:center;justify-content:space-between}
  .logo{display:flex;align-items:center;gap:10px;color:#fff;font-weight:700;letter-spacing:.02em}
  .logo-mark{
    width:38px;height:38px;border-radius:10px;background:var(--gold);color:var(--navy);
    display:grid;place-items:center;font-weight:800;font-size:.95rem
  }
  nav ul{display:flex;gap:30px;list-style:none;align-items:center}
  nav a.link{color:rgba(255,255,255,.82);font-size:.94rem;font-weight:500;position:relative;padding:4px 0;transition:color .2s}
  nav a.link::after{content:"";position:absolute;left:0;bottom:-2px;height:2px;width:0;background:var(--gold);transition:width .25s}
  nav a.link:hover,nav a.link.active{color:#fff}
  nav a.link:hover::after,nav a.link.active::after{width:100%}
  .menu-btn{display:none;background:none;border:0;color:#fff;cursor:pointer;padding:6px}
  .menu-btn svg{width:28px;height:28px}

  /* HERO */
  .hero{
    min-height:100vh;display:flex;align-items:center;color:#fff;position:relative;overflow:hidden;padding:140px 0 90px;
    background:
      radial-gradient(900px 500px at 85% 10%,rgba(212,160,23,.18),transparent 60%),
      radial-gradient(700px 500px at 0% 100%,rgba(23,55,95,.9),transparent 60%),
      linear-gradient(160deg,var(--navy) 0%,var(--navy-2) 100%);
  }
  .hero::before{
    content:"";position:absolute;inset:0;opacity:.07;
    background-image:linear-gradient(#fff 1px,transparent 1px),linear-gradient(90deg,#fff 1px,transparent 1px);
    background-size:48px 48px;mask-image:radial-gradient(circle at 70% 30%,#000,transparent 70%);
    -webkit-mask-image:radial-gradient(circle at 70% 30%,#000,transparent 70%)
  }
  .hero-grid{display:grid;grid-template-columns:1.3fr .9fr;gap:56px;align-items:center;position:relative}
  .pill{
    display:inline-flex;align-items:center;gap:8px;padding:8px 16px;border:1px solid rgba(255,255,255,.2);
    border-radius:999px;font-size:.84rem;color:rgba(255,255,255,.9);background:rgba(255,255,255,.06);margin-bottom:24px
  }
  .dot{width:8px;height:8px;background:var(--gold);border-radius:50%;box-shadow:0 0 0 4px rgba(212,160,23,.25)}
  .hero h1{font-size:clamp(2.6rem,7vw,4.6rem);line-height:1.05;letter-spacing:-.03em;margin-bottom:20px}
  .hero h1 span{color:var(--gold)}
  .hero p.lead{font-size:clamp(1.05rem,2vw,1.3rem);color:rgba(255,255,255,.82);max-width:560px;margin-bottom:34px}
  .hero-cta{display:flex;flex-wrap:wrap;gap:14px}
  .hero-card{
    background:rgba(255,255,255,.06);border:1px solid rgba(255,255,255,.14);border-radius:24px;padding:30px;
    backdrop-filter:blur(6px)
  }
  .avatar{
    width:108px;height:108px;border-radius:50%;margin-bottom:20px;display:grid;place-items:center;
    background:linear-gradient(135deg,var(--gold),var(--gold-soft));color:var(--navy);font-size:2.3rem;font-weight:800;
    box-shadow:0 0 0 6px rgba(212,160,23,.2)
  }
  .hero-card h3{font-size:1.3rem;margin-bottom:4px}
  .hero-card .sub{color:rgba(255,255,255,.7);font-size:.92rem;margin-bottom:20px}
  .facts{list-style:none;display:grid;gap:12px;font-size:.93rem}
  .facts li{display:flex;gap:12px;align-items:flex-start;color:rgba(255,255,255,.88)}
  .facts svg{flex:none;width:18px;height:18px;margin-top:4px;color:var(--gold)}
  .scroll-hint{position:absolute;bottom:26px;left:50%;transform:translateX(-50%);color:rgba(255,255,255,.5);font-size:.75rem;letter-spacing:.2em;text-transform:uppercase}

  /* ABOUT */
  .about-grid{display:grid;grid-template-columns:1.2fr 1fr;gap:56px;align-items:start}
  .about-text p{margin-bottom:18px;color:#33445e}
  .stats{display:grid;grid-template-columns:repeat(2,1fr);gap:16px}
  .stat{
    background:var(--card);border:1px solid var(--line);border-radius:var(--radius);padding:24px;box-shadow:var(--shadow)
  }
  .stat b{display:block;font-size:1.5rem;color:var(--navy);letter-spacing:-.01em}
  .stat span{font-size:.86rem;color:var(--muted)}
  .stat.gold{border-top:4px solid var(--gold)}
  .interest-tags{display:flex;flex-wrap:wrap;gap:10px;margin-top:8px}
  .tag{
    padding:8px 16px;border-radius:999px;background:rgba(11,31,58,.07);color:var(--navy);font-weight:600;font-size:.88rem
  }

  /* EXPERIENCE */
  #experience{background:#fff}
  .timeline{position:relative;padding-left:34px;display:grid;gap:28px}
  .timeline::before{content:"";position:absolute;left:9px;top:8px;bottom:8px;width:2px;background:linear-gradient(var(--gold),var(--line))}
  .t-item{position:relative;background:var(--bg);border:1px solid var(--line);border-radius:var(--radius);padding:26px 28px;transition:transform .25s,box-shadow .25s}
  .t-item:hover{transform:translateY(-4px);box-shadow:var(--shadow)}
  .t-item::before{
    content:"";position:absolute;left:-34px;top:30px;width:20px;height:20px;border-radius:50%;background:var(--gold);
    border:4px solid #fff;box-shadow:0 0 0 2px var(--gold)
  }
  .t-top{display:flex;flex-wrap:wrap;justify-content:space-between;gap:8px 16px;margin-bottom:6px}
  .t-item h3{font-size:1.15rem;color:var(--navy)}
  .date{font-size:.84rem;font-weight:700;color:#8a6a0c;background:rgba(212,160,23,.15);padding:4px 12px;border-radius:999px;white-space:nowrap}
  .org{color:var(--muted);font-size:.93rem;margin-bottom:12px}
  .t-item ul{padding-left:18px;color:#33445e;font-size:.95rem}
  .t-item li{margin-bottom:4px}

  /* SKILLS */
  .skill-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(240px,1fr));gap:22px}
  .skill-card{
    background:var(--card);border:1px solid var(--line);border-radius:var(--radius);padding:28px;box-shadow:var(--shadow);
    transition:transform .25s,border-color .25s
  }
  .skill-card:hover{transform:translateY(-5px);border-color:var(--gold)}
  .icon{
    width:52px;height:52px;border-radius:14px;background:var(--navy);color:var(--gold);display:grid;place-items:center;margin-bottom:18px
  }
  .icon svg{width:26px;height:26px}
  .skill-card h3{font-size:1.1rem;color:var(--navy);margin-bottom:6px}
  .skill-card p{font-size:.93rem;color:var(--muted)}
  .subhead{margin:56px 0 18px;font-size:1.1rem;color:var(--navy)}
  .chips{display:flex;flex-wrap:wrap;gap:10px}
  .chip{padding:9px 18px;border-radius:10px;background:#fff;border:1px solid var(--line);font-size:.9rem;font-weight:600;color:var(--navy)}
  .chip.gold{border-color:var(--gold);background:rgba(212,160,23,.1)}

  /* PORTFOLIO */
  #portfolio{background:#fff}
  .proj-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(290px,1fr));gap:24px}
  .proj{
    border-radius:var(--radius);overflow:hidden;border:1px solid var(--line);background:var(--bg);display:flex;flex-direction:column;
    transition:transform .25s,box-shadow .25s
  }
  .proj:hover{transform:translateY(-6px);box-shadow:var(--shadow)}
  .proj-thumb{
    height:170px;display:grid;place-items:center;color:var(--gold);
    background:linear-gradient(135deg,var(--navy),var(--navy-3));position:relative
  }
  .proj-thumb svg{width:56px;height:56px}
  .proj-thumb .badge{
    position:absolute;top:14px;right:14px;font-size:.72rem;font-weight:700;letter-spacing:.08em;text-transform:uppercase;
    background:var(--gold);color:var(--navy);padding:4px 10px;border-radius:999px
  }
  .proj-body{padding:24px;flex:1;display:flex;flex-direction:column}
  .proj-body h3{color:var(--navy);margin-bottom:8px;font-size:1.1rem}
  .proj-body p{font-size:.93rem;color:var(--muted);flex:1}
  .proj-body .chips{margin-top:16px}
  .proj-body .chip{font-size:.78rem;padding:5px 12px}
  .note{margin-top:30px;font-size:.88rem;color:var(--muted);text-align:center}

  /* CONTACT */
  #contact{
    background:linear-gradient(160deg,var(--navy),var(--navy-2));color:#fff;position:relative;overflow:hidden
  }
  #contact h2{color:#fff}
  #contact .section-head p{color:rgba(255,255,255,.75)}
  .contact-grid{display:grid;grid-template-columns:1fr 1.1fr;gap:48px;align-items:start}
  .contact-list{display:grid;gap:16px;list-style:none}
  .contact-list a{
    display:flex;align-items:center;gap:16px;padding:18px 20px;border-radius:14px;border:1px solid rgba(255,255,255,.14);
    background:rgba(255,255,255,.05);transition:background .2s,border-color .2s,transform .2s
  }
  .contact-list a:hover{background:rgba(255,255,255,.1);border-color:var(--gold);transform:translateX(4px)}
  .c-icon{width:44px;height:44px;border-radius:12px;background:var(--gold);color:var(--navy);display:grid;place-items:center;flex:none}
  .c-icon svg{width:22px;height:22px}
  .contact-list small{display:block;color:rgba(255,255,255,.6);font-size:.78rem;text-transform:uppercase;letter-spacing:.08em}
  .contact-list span{font-weight:600;word-break:break-word}
  form{background:#fff;color:var(--ink);padding:30px;border-radius:20px;display:grid;gap:16px}
  label{font-size:.85rem;font-weight:600;color:var(--navy);display:block;margin-bottom:6px}
  input,textarea{
    width:100%;padding:13px 15px;border-radius:10px;border:1px solid var(--line);font:inherit;background:var(--bg);color:var(--ink)
  }
  input:focus,textarea:focus{outline:none;border-color:var(--gold);box-shadow:0 0 0 3px rgba(212,160,23,.25)}
  textarea{min-height:120px;resize:vertical}
  .form-note{font-size:.8rem;color:var(--muted)}

  footer{background:#071529;color:rgba(255,255,255,.6);text-align:center;padding:28px 24px;font-size:.86rem}
  footer b{color:var(--gold)}

  /* ANIMATIONS */
  .reveal{opacity:0;transform:translateY(28px);transition:opacity .7s ease,transform .7s ease;transition-delay:var(--d,0s)}
  .reveal.in{opacity:1;transform:none}
  @media (prefers-reduced-motion:reduce){
    html{scroll-behavior:auto}
    .reveal{opacity:1;transform:none;transition:none}
    *{transition-duration:.01ms!important}
  }

  /* RESPONSIVE */
  @media (max-width:900px){
    section{padding:72px 0}
    .hero-grid,.about-grid,.contact-grid{grid-template-columns:1fr}
    .hero{padding-top:120px}
    .scroll-hint{display:none}
    .menu-btn{display:block}
    nav ul{
      position:absolute;top:100%;left:0;right:0;flex-direction:column;gap:0;background:var(--navy);padding:8px 24px 20px;
      max-height:0;overflow:hidden;opacity:0;transition:max-height .3s,opacity .3s;align-items:stretch
    }
    nav ul.open{max-height:420px;opacity:1}
    nav ul li{padding:12px 0;border-bottom:1px solid rgba(255,255,255,.08)}
    header.nav:not(.scrolled){background:rgba(11,31,58,.92)}
  }
  @media (max-width:520px){
    .container{padding:0 18px}
    .stats{grid-template-columns:1fr 1fr}
    .hero-cta .btn{width:100%;justify-content:center}
    .t-item{padding:22px 20px}
  }
</style>
</head>
<body>

<header class="nav" id="nav">
  <div class="container nav-inner">
    <a href="#home" class="logo" aria-label="Ahmed Ali home"><span class="logo-mark">AA</span><span>Ahmed Ali</span></a>
    <button class="menu-btn" id="menuBtn" aria-label="Toggle menu" aria-expanded="false">
      <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round"><path d="M4 7h16M4 12h16M4 17h16"/></svg>
    </button>
    <nav aria-label="Main">
      <ul id="menu">
        <li><a class="link" href="#about">About</a></li>
        <li><a class="link" href="#experience">Experience</a></li>
        <li><a class="link" href="#skills">Skills</a></li>
        <li><a class="link" href="#portfolio">Portfolio</a></li>
        <li><a class="link" href="#contact">Contact</a></li>
      </ul>
    </nav>
  </div>
</header>

<main>
<!-- HERO -->
<section class="hero" id="home">
  <div class="container hero-grid">
    <div class="reveal">
      <div class="pill"><span class="dot"></span> Eastern Michigan University &middot; Class of 2029</div>
      <h1>Hi, I'm <span>Ahmed Ali.</span></h1>
      <p class="lead">EMU Information Technology (IT) sophomore passionate about applying tech skills to real-world issues.</p>
      <div class="hero-cta">
        <a class="btn btn-gold" href="resume.pdf" download>
          <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round"><path d="M12 3v12m0 0l-4-4m4 4l4-4M4 21h16"/></svg>
          Download Resume
        </a>
        <a class="btn btn-ghost" href="#contact">Get in Touch</a>
      </div>
    </div>
    <aside class="hero-card reveal" style="--d:.15s">
      <div class="avatar" aria-hidden="true">AA</div>
      <h3>Ahmed Ali</h3>
      <p class="sub">B.S. Information Technology</p>
      <ul class="facts">
        <li><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M22 10L12 5 2 10l10 5 10-5z"/><path d="M6 12v5c3 2 9 2 12 0v-5"/></svg>Game Above College of Engineering and Technology</li>
        <li><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><rect x="3" y="4" width="18" height="18" rx="2"/><path d="M16 2v4M8 2v4M3 10h18"/></svg>Sophomore &middot; Graduating May 2029</li>
        <li><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M12 21s-7-6.2-7-11a7 7 0 0114 0c0 4.8-7 11-7 11z"/><circle cx="12" cy="10" r="2.5"/></svg>Ypsilanti, Michigan</li>
      </ul>
    </aside>
  </div>
  <div class="scroll-hint">Scroll</div>
</section>

<!-- ABOUT -->
<section id="about">
  <div class="container">
    <div class="section-head reveal">
      <span class="eyebrow">About Me</span>
      <h2>Technology with a purpose</h2>
    </div>
    <div class="about-grid">
      <div class="about-text reveal">
        <p>I'm a sophomore at Eastern Michigan University studying Information Technology in the Game Above College of Engineering and Technology. I'm passionate about applying tech skills to real-world issues, whether that means helping someone solve a hardware problem, making sense of data, or keeping systems running smoothly.</p>
        <p>Outside the classroom, I work customer-facing at Meijer, take part in the National Society of Black Engineers (NSBE) at EMU, and build creative and marketing skills in design, social media, and presentations. That mix lets me bridge technical work and clear communication.</p>
        <p><strong>Career interests</strong></p>
        <div class="interest-tags">
          <span class="tag">IT Support</span>
          <span class="tag">Data Analytics</span>
          <span class="tag">System Administration</span>
        </div>
      </div>
      <div class="stats reveal" style="--d:.15s">
        <div class="stat gold"><b>B.S. IT</b><span>Eastern Michigan University</span></div>
        <div class="stat gold"><b>May 2029</b><span>Expected graduation</span></div>
        <div class="stat"><b>NSBE</b><span>EMU chapter member</span></div>
        <div class="stat"><b>3</b><span>Career interest areas</span></div>
      </div>
    </div>
  </div>
</section>

<!-- EXPERIENCE -->
<section id="experience">
  <div class="container">
    <div class="section-head reveal">
      <span class="eyebrow">Experience</span>
      <h2>Where I've been building skills</h2>
    </div>
    <div class="timeline">
      <article class="t-item reveal">
        <div class="t-top"><h3>Cashier</h3><span class="date">Mar 2026 &ndash; Present</span></div>
        <p class="org">Meijer &middot; 3825 Carpenter Rd, Ypsilanti, MI 48197</p>
        <ul>
          <li>Serve customers in a fast-paced retail environment, handling transactions accurately.</li>
          <li>Build communication, reliability, and problem-solving skills that carry directly into IT support.</li>
        </ul>
      </article>
      <article class="t-item reveal" style="--d:.08s">
        <div class="t-top"><h3>Member</h3><span class="date">Sep 2026 &ndash; Present</span></div>
        <p class="org">National Society of Black Engineers (NSBE) &middot; Eastern Michigan University</p>
        <ul>
          <li>Active member of a professional community supporting students in engineering and technology.</li>
          <li>Networking, professional development, and peer support.</li>
        </ul>
      </article>
      <article class="t-item reveal" style="--d:.16s">
        <div class="t-top"><h3>Digital Hardware Support Lab</h3><span class="date">Sep 2026</span></div>
        <p class="org">CEET 215: Computer Hardware &amp; Software &middot; Eastern Michigan University</p>
        <ul>
          <li>Hands-on lab work with computer hardware and software fundamentals.</li>
          <li>Foundation for troubleshooting and technical support skills.</li>
        </ul>
      </article>
    </div>
  </div>
</section>

<!-- SKILLS -->
<section id="skills">
  <div class="container">
    <div class="section-head reveal">
      <span class="eyebrow">Skills</span>
      <h2>Marketing and creative toolkit</h2>
      <p>Tools I use to design, communicate, and present ideas clearly.</p>
    </div>
    <div class="skill-grid">
      <div class="skill-card reveal">
        <div class="icon"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M12 19l7-7 3 3-7 7-3-3z"/><path d="M18 13l-1.5-7.5L2 2l3.5 14.5L13 18l5-5z"/><path d="M2 2l7.6 7.6"/></svg></div>
        <h3>Canva / Adobe</h3>
        <p>Graphics, flyers, and branded visuals that look polished and on message.</p>
      </div>
      <div class="skill-card reveal" style="--d:.08s">
        <div class="icon"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M21 15a2 2 0 01-2 2H7l-4 4V5a2 2 0 012-2h14a2 2 0 012 2z"/></svg></div>
        <h3>Social Media Management</h3>
        <p>Planning and publishing content to reach and engage an audience.</p>
      </div>
      <div class="skill-card reveal" style="--d:.16s">
        <div class="icon"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><rect x="3" y="3" width="18" height="18" rx="2"/><path d="M3 9h18M9 21V9"/></svg></div>
        <h3>Excel / PowerPoint</h3>
        <p>Organizing data and turning it into clear spreadsheets and presentations.</p>
      </div>
    </div>

    <h3 class="subhead reveal">Technical focus areas</h3>
    <div class="chips reveal">
      <span class="chip gold">IT Support</span>
      <span class="chip gold">Data Analytics</span>
      <span class="chip gold">System Administration</span>
      <span class="chip">Computer Hardware &amp; Software</span>
      <span class="chip">Customer Service</span>
      <span class="chip">Communication</span>
    </div>
  </div>
</section>

<!-- PORTFOLIO -->
<section id="portfolio">
  <div class="container">
    <div class="section-head reveal">
      <span class="eyebrow">Portfolio</span>
      <h2>Projects and work samples</h2>
      <p>A growing collection of coursework and creative work.</p>
    </div>
    <div class="proj-grid">
      <article class="proj reveal">
        <div class="proj-thumb"><span class="badge">Coursework</span>
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round"><rect x="4" y="4" width="16" height="16" rx="2"/><rect x="9" y="9" width="6" height="6"/><path d="M9 1v3M15 1v3M9 20v3M15 20v3M20 9h3M20 14h3M1 9h3M1 14h3"/></svg>
        </div>
        <div class="proj-body">
          <h3>Digital Hardware Support Lab</h3>
          <p>Hands-on lab from CEET 215 covering computer hardware and software fundamentals at EMU.</p>
          <div class="chips"><span class="chip">Hardware</span><span class="chip">Troubleshooting</span></div>
        </div>
      </article>
      <article class="proj reveal" style="--d:.08s">
        <div class="proj-thumb"><span class="badge">Python</span>
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round"><path d="M16 18l6-6-6-6"/><path d="M8 6l-6 6 6 6"/><path d="M14 4l-4 16"/></svg>
        </div>
        <div class="proj-body">
          <h3>Python Project</h3>
          <p>A Python project showing my programming and problem-solving skills. Replace this text with what it does and the problem it solves.</p>
          <div class="chips"><span class="chip">Python</span></div>
          <a href="https://github.com/axmedali-jpg" target="_blank" rel="noopener noreferrer" style="margin-top:16px;font-weight:600;color:var(--navy);border-bottom:2px solid var(--gold);align-self:flex-start">View on GitHub &rarr;</a>
        </div>
      </article>
    </div>
    <p class="note">More projects will be added as I complete them.</p>
  </div>
</section>

<!-- CONTACT -->
<section id="contact">
  <div class="container">
    <div class="section-head reveal">
      <span class="eyebrow">Contact</span>
      <h2>Let's connect</h2>
      <p>Looking for internships, opportunities, or just want to say hello? I'd love to hear from you.</p>
    </div>
    <div class="contact-grid">
      <ul class="contact-list reveal">
        <li><a href="mailto:aali57@emich.edu">
          <span class="c-icon"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><rect x="2" y="4" width="20" height="16" rx="2"/><path d="M22 7l-10 6L2 7"/></svg></span>
          <div><small>Email</small><span>aali57@emich.edu</span></div></a></li>
        <li><a href="https://www.linkedin.com/in/ahmed-m-ali-tech" target="_blank" rel="noopener noreferrer">
          <span class="c-icon"><svg viewBox="0 0 24 24" fill="currentColor"><path d="M4.98 3.5a2.5 2.5 0 11-.01 5 2.5 2.5 0 01.01-5zM3 9.75h4V21H3zM9.5 9.75h3.8v1.6h.06c.53-1 1.84-2.05 3.79-2.05 4.05 0 4.8 2.67 4.8 6.14V21h-4v-4.7c0-1.12-.02-2.56-1.56-2.56-1.56 0-1.8 1.22-1.8 2.48V21h-4z"/></svg></span>
          <div><small>LinkedIn</small><span>linkedin.com/in/ahmed-m-ali-tech</span></div></a></li>
        <li><a href="https://github.com/axmedali-jpg" target="_blank" rel="noopener noreferrer">
          <span class="c-icon"><svg viewBox="0 0 24 24" fill="currentColor"><path d="M12 .5a11.5 11.5 0 00-3.64 22.41c.58.1.79-.25.79-.56v-2c-3.2.7-3.88-1.37-3.88-1.37-.52-1.33-1.28-1.69-1.28-1.69-1.04-.71.08-.7.08-.7 1.15.08 1.76 1.19 1.76 1.19 1.03 1.76 2.69 1.25 3.35.96.1-.74.4-1.25.73-1.54-2.55-.29-5.24-1.28-5.24-5.69 0-1.26.45-2.28 1.19-3.09-.12-.29-.52-1.46.11-3.05 0 0 .97-.31 3.17 1.18a10.9 10.9 0 015.78 0c2.2-1.49 3.17-1.18 3.17-1.18.63 1.59.23 2.76.11 3.05.74.81 1.19 1.83 1.19 3.09 0 4.42-2.69 5.39-5.25 5.68.41.35.78 1.05.78 2.12v3.14c0 .31.21.67.8.56A11.5 11.5 0 0012 .5z"/></svg></span>
          <div><small>GitHub</small><span>github.com/axmedali-jpg</span></div></a></li>
        <li><a href="resume.pdf" download>
          <span class="c-icon"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M12 3v12m0 0l-4-4m4 4l4-4M4 21h16"/></svg></span>
          <div><small>Resume</small><span>Download Resume</span></div></a></li>
      </ul>

      <form id="contactForm" class="reveal" style="--d:.15s">
        <div><label for="name">Your name</label><input id="name" required autocomplete="name"></div>
        <div><label for="email">Your email</label><input id="email" type="email" required autocomplete="email"></div>
        <div><label for="msg">Message</label><textarea id="msg" required></textarea></div>
        <button class="btn btn-navy" type="submit">Send Message</button>
        <p class="form-note">This opens your email app with the message pre-filled.</p>
      </form>
    </div>
  </div>
</section>
</main>

<footer>
  <p>&copy; <span id="yr">2026</span> <b>Ahmed Ali</b> &middot; Eastern Michigan University &middot; B.S. Information Technology</p>
</footer>

<script>
(function(){
  var nav=document.getElementById('nav');
  var menu=document.getElementById('menu');
  var btn=document.getElementById('menuBtn');
  document.getElementById('yr').textContent=new Date().getFullYear();

  function onScroll(){nav.classList.toggle('scrolled',window.scrollY>30)}
  window.addEventListener('scroll',onScroll,{passive:true});onScroll();

  btn.addEventListener('click',function(){
    var open=menu.classList.toggle('open');
    btn.setAttribute('aria-expanded',open);
  });
  menu.addEventListener('click',function(e){
    if(e.target.tagName==='A'){menu.classList.remove('open');btn.setAttribute('aria-expanded','false')}
  });

  // Scroll reveal
  var items=document.querySelectorAll('.reveal');
  if('IntersectionObserver' in window){
    var io=new IntersectionObserver(function(entries){
      entries.forEach(function(en){
        if(en.isIntersecting){en.target.classList.add('in');io.unobserve(en.target)}
      });
    },{threshold:.12,rootMargin:'0px 0px -40px 0px'});
    items.forEach(function(el){io.observe(el)});
  }else{items.forEach(function(el){el.classList.add('in')})}

  // Active nav link
  var links=document.querySelectorAll('nav a.link');
  var secs=[].slice.call(links).map(function(a){return document.querySelector(a.getAttribute('href'))});
  if('IntersectionObserver' in window){
    var so=new IntersectionObserver(function(entries){
      entries.forEach(function(en){
        if(en.isIntersecting){
          links.forEach(function(a){a.classList.toggle('active',a.getAttribute('href')==='#'+en.target.id)});
        }
      });
    },{rootMargin:'-45% 0px -50% 0px'});
    secs.forEach(function(s){if(s)so.observe(s)});
  }

  // Contact form -> mailto
  document.getElementById('contactForm').addEventListener('submit',function(e){
    e.preventDefault();
    var n=document.getElementById('name').value.trim();
    var em=document.getElementById('email').value.trim();
    var m=document.getElementById('msg').value.trim();
    var body='Name: '+n+'\nEmail: '+em+'\n\n'+m;
    window.location.href='mailto:aali57@emich.edu?subject='+encodeURIComponent('Website message from '+n)+'&body='+encodeURIComponent(body);
  });
})();
</script>
</body>
</html>
