<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Aditya Visuals — Aditya Kumar | Portfolio</title>
  <meta name="description" content="Aditya Visuals — premium graphics & brand design by Aditya Kumar. Logos, posters, social creatives, thumbnails and brand systems." />
  <meta name="theme-color" content="#0f1724" />

  <!-- Apply stored theme very early to avoid flash-of-unstyled -->
  <script>
    (function(){
      try {
        const stored = localStorage.getItem('aditya-theme');
        if (stored === 'light') {
          document.documentElement.classList.add('light');
        }
      } catch(e) { /* ignore */ }
    })();
  </script>

  <style>
    /* ========= VARIABLES ========= */
    :root{
      --bg: #0f1724;
      --card: #0b1220;
      --muted: #98a0b3;
      --text: #e6eef8;
      --accent: #ffd166;
      --accent2: #7c5cff;
      --glass: rgba(255,255,255,0.04);
      --radius: 18px;

      /* header border depends on theme */
      --header-border: rgba(255,255,255,0.12);
    }

    .light{
      --bg: #f7fafc;
      --card: #ffffff;
      --muted: #536170;
      --text: #071428;
      --accent: #ff8a00;
      --accent2: #6b46ff;
      --glass: rgba(0,0,0,0.04);

      --header-border: rgba(0,0,0,0.12);
    }

    *{box-sizing:border-box;margin:0;padding:0}
    html{scroll-behavior:smooth}
    body{
      font-family: Inter, ui-sans-serif, system-ui, -apple-system, "Segoe UI", Roboto, Helvetica, Arial;
      color: var(--text);
      background:
        radial-gradient(600px 400px at 10% 10%, rgba(124,92,255,.06), transparent),
        radial-gradient(500px 350px at 90% 90%, rgba(255,193,66,.04), transparent),
        var(--bg);
      line-height:1.6;
    }

    /* ========= CONTAINER ========= */
    .container{max-width:1180px;margin:0 auto;padding:0 20px}

    /* ========= NAVBAR ========= */
    nav.nav{position:sticky;top:12px;z-index:60}
    .nav-inner{
      display:flex;
      align-items:center;
      justify-content:space-between;
      gap:12px;
      background:linear-gradient(180deg, rgba(255,255,255,.02), rgba(255,255,255,.01));
      border-radius:14px;
      padding:10px 14px;
      backdrop-filter:blur(8px);
      border:1px solid var(--header-border); /* uses variable */
    }
    .brand{display:flex;align-items:center;gap:12px}
    .brand .logo-wrap{
      width:52px;height:52px;border-radius:999px;overflow:hidden;
      display:inline-grid;place-items:center;
      background:linear-gradient(135deg,var(--accent),var(--accent2));
      box-shadow:0 8px 30px rgba(0,0,0,.35);
      border:3px solid rgba(255,255,255,.06);
    }
    .brand .logo-wrap img{width:100%;height:100%;object-fit:cover;display:block}
    .brand .title{font-weight:700;font-size:1.05rem}

    .nav-links{display:flex;gap:18px;align-items:center}
    .nav-links a{color:var(--text);text-decoration:none;font-weight:600;opacity:.95}
    .nav-cta{display:flex;gap:10px;align-items:center}
    .btn{padding:8px 12px;border-radius:12px;border:1px solid rgba(255,255,255,.06);background:transparent;color:var(--text);cursor:pointer}
    .btn.primary{background:linear-gradient(90deg,var(--accent),var(--accent2));color:#071428;border:none;font-weight:800}

    .menu-btn{display:none;background:transparent;border:none;color:var(--text);font-size:20px}

    @media(max-width:860px){
      .nav-links{display:none}
      .menu-btn{display:block}
      /* when JS toggles .show, display vertical menu */
      .nav-links.show{display:flex;flex-direction:column;gap:12px;background:transparent;padding:8px 0;}
    }

    /* ========= HERO ========= */
    .hero{padding:64px 0 28px}
    .hero-grid{display:grid;grid-template-columns:1fr 420px;align-items:center;gap:28px}
    .kicker{display:inline-block;padding:6px 10px;border-radius:999px;background:var(--glass);border:1px solid rgba(255,255,255,.03);font-size:.78rem;color:var(--muted);font-weight:700}
    h1{font-size:clamp(28px,4.8vw,48px);line-height:1.02;margin:14px 0}
    .lead{color:var(--muted);max-width:58ch}
    .actions{display:flex;gap:12px;margin-top:18px}

    .hero-card{background:linear-gradient(180deg, rgba(255,255,255,.02), rgba(255,255,255,.01));padding:18px;border-radius:20px;border:1px solid rgba(255,255,255,.04);box-shadow:0 20px 50px rgba(0,0,0,.35)}
    .portrait{width:100%;aspect-ratio:1/1;border-radius:14px;overflow:hidden;display:block;border:6px solid rgba(255,255,255,.03)}
    .portrait img{width:100%;height:100%;object-fit:cover;display:block;transform:scale(1.02);animation:float 6s ease-in-out infinite}
    @keyframes float{0%{transform:translateY(0) scale(1.02)}50%{transform:translateY(-10px) scale(1.02)}100%{transform:translateY(0) scale(1.02)}}

    /* ========= ABOUT & SERVICES ========= */
    .about{display:grid;grid-template-columns:1fr 1fr;gap:22px;margin-top:32px}
    .card{background:var(--card);padding:20px;border-radius:14px;border:1px solid rgba(255,255,255,.03)}
    .chips{display:flex;gap:10px;flex-wrap:wrap;margin-top:12px}
    .chip{padding:8px 10px;border-radius:999px;background:rgba(255,255,255,.03);font-weight:700;color:var(--muted);font-size:.9rem}

    /* ========= WORKS GRID ========= */
    .works{margin-top:34px}
    .works-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:18px}
    .work{border-radius:12px;overflow:hidden;position:relative;border:1px solid rgba(255,255,255,.04);cursor:pointer}
    .work img{width:100%;height:320px;object-fit:cover;display:block}
    .work .meta{position:absolute;left:12px;bottom:12px;color:#fff;font-weight:700;background:linear-gradient(90deg, rgba(0,0,0,.45), transparent);padding:8px 12px;border-radius:10px}
    .work:hover{transform:translateY(-6px);box-shadow:0 20px 60px rgba(0,0,0,.35)}

    @media(max-width:1024px){.works-grid{grid-template-columns:repeat(2,1fr)}.hero-grid{grid-template-columns:1fr}}
    @media(max-width:640px){.works-grid{grid-template-columns:1fr}.about{grid-template-columns:1fr}.nav-inner{flex-direction:column;gap:10px}.hero-grid{grid-template-columns:1fr}.menu-btn{display:block}}

    /* ========= PORTFOLIO MODAL ========= */
    .modal{position:fixed;inset:0;display:none;place-items:center;background:rgba(0,0,0,.6);z-index:120}
    .modal.open{display:grid}
    .modal-card{background:var(--card);max-width:920px;width:94%;border-radius:14px;padding:18px;border:1px solid rgba(255,255,255,.04)}
    .modal-card img{width:100%;height:520px;object-fit:cover;border-radius:8px}
    .modal-close{position:absolute;top:18px;right:20px;background:transparent;border:none;color:var(--text);font-size:22px}

    /* ========= CONTACT ========= */
    .contact{margin-top:36px;display:grid;grid-template-columns:1fr 360px;gap:18px}
    form{display:grid;gap:12px}
    input,textarea{background:transparent;border:1px solid rgba(255,255,255,.06);padding:12px;border-radius:10px;color:var(--text)}
    textarea{min-height:140px}

    /* ========= FOOTER ========= */
    footer{margin-top:40px;padding:30px;border-top:1px solid rgba(255,255,255,.03);display:flex;align-items:center;justify-content:space-between;gap:12px}

    /* ========= REVEAL ANIM ========= */
    .reveal{opacity:0;transform:translateY(18px);transition:all .7s cubic-bezier(.2,.85,.25,1)}
    .reveal.show{opacity:1;transform:none}

    /* small tweaks */
    .muted{color:var(--muted)}
  </style>
</head>
<body>
  <div class="container" style="padding-top:18px">
    <!-- NAV -->
    <nav class="nav">
      <div class="nav-inner">
        <div class="brand">
          <div class="logo-wrap">
            <!-- logo placeholder -->
            <img src="C:\Users\Hp\Pictures\Screenshots\Screenshot 2025-08-25 161439.png" id="brandLogo" />
          </div>
          <div style="display:flex;flex-direction:column">
            <div class="title">Aditya Visuals</div>
            <div style="font-size:.78rem;color:var(--muted)">Creative Graphics & Brand Design</div>
          </div>
        </div>

        <div style="display:flex;align-items:center;gap:10px">
          <div class="nav-links" id="navLinks">
            <a href="#home">Home</a>
            <a href="#works">Work</a>
            <a href="#about">About</a>
            <a href="#contact">Contact</a>
          </div>
          <button class="btn" id="themeToggle" title="Toggle theme">🌙</button>
          <button class="menu-btn" id="menuBtn">☰</button>
        </div>
      </div>
    </nav>

    <!-- HERO -->
    <header class="hero" id="home">
      <div class="hero-grid">
        <div>
          <div class="kicker">Logo · Poster · Social · Thumbnails</div>
          <h1 class="reveal">I craft bold visuals that make brands <span style="background:linear-gradient(90deg,var(--accent),var(--accent2));-webkit-background-clip:text;background-clip:text;color:transparent">unforgettable</span></h1>
          <p class="lead reveal muted">I’m Aditya — a graphics designer building high-impact visual identities for startups, creators and local businesses. Clean concepts, fast delivery, premium look.</p>
          <div class="actions reveal">
            <a class="btn primary" href="#works">View Work</a>
            <a class="btn" href="#contact">Start Project</a>
          </div>
          <div style="margin-top:14px" class="reveal">
            <div class="chips">
              <div class="chip">Photoshop</div>
              <div class="chip">Illustrator</div>
              <div class="chip">Canva</div>
              <div class="chip">Figma</div>
            </div>
          </div>
        </div>

        <div class="hero-card reveal">
          <div class="portrait">
            <img src="C:\Users\Hp\Pictures\IMG_20250707_214627.jpg" alt="Aditya portrait" id="portraitImg" />
          </div>
        </div>
      </div>
    </header>

    <!-- WORKS -->
    <section id="works" class="works reveal">
      <div style="display:flex;justify-content:space-between;align-items:end;gap:12px;margin-bottom:18px">
        <h2>Selected Work</h2>
        <div class="muted">Click to open project</div>
      </div>
      <div class="works-grid">
        <div class="work" data-src="work1.jpg">
          <img src="C:\Users\Hp\Pictures\A Visuals\Untitled design.png" alt="Work 1"/>
          <div class="meta">Brand Identity • Logo</div>
        </div>
        <div class="work" data-src="work2.jpg">
          <img src="C:\Users\Hp\Pictures\A Visuals\Screenshot 2025-08-25 155959.png" alt="Work 2"/>
          <div class="meta">Event Poster • Print</div>
        </div>
        <div class="work" data-src="work3.jpg">
          <img src="C:\Users\Hp\Pictures\A Visuals\Screenshot 2025-08-25 155220.png" alt="Work 3"/>
          <div class="meta">Social Campaign</div>
        </div>
        <div class="work" data-src="work4.jpg">
          <img src="work4.jpg" alt="Work 4"/>
          <div class="meta">YouTube Thumbnails</div>
        </div>
        <div class="work" data-src="work5.jpg">
          <img src="work5.jpg" alt="Work 5"/>
          <div class="meta">Business Collaterals</div>
        </div>
        <div class="work" data-src="work6.jpg">
          <img src="work6.jpg" alt="Work 6"/>
          <div class="meta">Landing Concept</div>
        </div>
      </div>
    </section>

    <!-- ABOUT -->
    <section id="about" class="reveal">
      <h2>About Me</h2>
      <div class="about">
        <div class="card">
          <p class="muted">I’m a diploma CSE student and a passionate graphics designer. I focus on visual clarity, brand consistency and results — designs that convert and create recall. I offer: logo systems, social packs, event posters, thumbnail packages and brand kits.</p>
          <div style="margin-top:14px">
            <strong>Availability:</strong> 1 hour/day (fast turnaround for small projects)
          </div>
        </div>
        <div class="card">
          <h3>Services</h3>
          <div style="margin-top:8px" class="chips">
            <div class="chip">Logo Design</div>
            <div class="chip">Social Creatives</div>
            <div class="chip">Poster & Print</div>
            <div class="chip">YouTube Thumbnails</div>
            <div class="chip">Brand Kits</div>
          </div>
        </div>
      </div>
    </section>

    <!-- CONTACT -->
    <section id="contact" class="reveal">
      <h2>Let's Talk</h2>
      <div class="contact">
        <form action="https://formspree.io/f/your-form-id" method="POST" class="card">
          <input type="text" name="name" placeholder="Your name" required />
          <input type="email" name="email" placeholder="Email" required />
          <input type="text" name="subject" placeholder="Project type (Logo / Poster)" />
          <textarea name="message" placeholder="Brief & timeline" required></textarea>
          <div style="display:flex;gap:10px;margin-top:8px">
            <button class="btn primary" type="submit">Send Message</button>
            <a class="btn" href="mailto:adityakumarchaudhari66@gmail.com">Email Direct</a>
          </div>
        </form>
        <div class="card" style="height:100%">
          <h3>Contact</h3>
          <p class="muted">Email: <a href="mailto:adityakumarchaudhari66@gmail.com">adityakumarchaudhari66@gmail.com</a></p>
          <p class="muted">Instagram / Fiverr / Behance links here</p>
          <div style="margin-top:12px">Price starts at <strong>₹500</strong> for simple logo concepts — message for exact quote.</div>
        </div>
      </div>
    </section>

    <!-- FOOTER -->
    <footer class="reveal">
      <div style="display:flex;justify-content:space-between;align-items:center;gap:12px">
        <div class="muted">© 2025 Aditya Visuals · Aditya Kumar</div>
        <div style="display:flex;gap:10px">
          <a class="btn" href="#">Instagram</a>
          <a class="btn" href="#">Behance</a>
          <a class="btn" href="#">Fiverr</a>
        </div>
      </div>
    </footer>
  </div>

  <!-- PORTFOLIO MODAL -->
  <div id="modal" class="modal" aria-hidden="true">
    <div class="modal-card">
      <button class="modal-close" id="modalClose">✕</button>
      <img id="modalImg" src="" alt="Project" />
    </div>
  </div>

  <script>
    // Mobile menu toggle
    const menuBtn = document.getElementById('menuBtn');
    const navLinks = document.getElementById('navLinks');
    menuBtn?.addEventListener('click', ()=> navLinks.classList.toggle('show'));

    // Theme toggle + persist (uses documentElement to match early script)
    const themeBtn = document.getElementById('themeToggle');
    const storedTheme = localStorage.getItem('aditya-theme');
    // set icon according to stored (or existing class)
    if (document.documentElement.classList.contains('light') || storedTheme === 'light') {
      themeBtn.textContent = '☀️';
    } else {
      themeBtn.textContent = '🌙';
    }
    themeBtn.addEventListener('click', ()=>{
      document.documentElement.classList.toggle('light');
      const isLight = document.documentElement.classList.contains('light');
      localStorage.setItem('aditya-theme', isLight ? 'light' : 'dark');
      themeBtn.textContent = isLight ? '☀️' : '🌙';
    });

    // Reveal animations
    const reveal = new IntersectionObserver((entries)=>{
      entries.forEach(ent=>{
        if(ent.isIntersecting){
          ent.target.classList.add('show');
          reveal.unobserve(ent.target);
        }
      });
    },{threshold:0.12});
    document.querySelectorAll('.reveal').forEach(el=> reveal.observe(el));

    // Portfolio modal
    const modal = document.getElementById('modal');
    const modalImg = document.getElementById('modalImg');
    const modalClose = document.getElementById('modalClose');
    document.querySelectorAll('.work').forEach(w=>{
      w.addEventListener('click', ()=>{
        const src = w.getAttribute('data-src') || w.querySelector('img')?.src;
        modalImg.src = src;
        modal.classList.add('open');
        modal.setAttribute('aria-hidden','false');
      });
    });
    modalClose?.addEventListener('click', ()=>{ modal.classList.remove('open'); modal.setAttribute('aria-hidden','true'); modalImg.src = ''; });
    modal.addEventListener('click', (e)=>{ if(e.target === modal) { modal.classList.remove('open'); modal.setAttribute('aria-hidden','true'); modalImg.src = ''; }});

    // keyboard esc close
    document.addEventListener('keydown', e=>{ if(e.key==='Escape') { modal.classList.remove('open'); modalImg.src = ''; } });
  </script>
</body>
</html>

