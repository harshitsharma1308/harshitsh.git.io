# harshitsh.git.io
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Harshit Sharma — Computer Science, Lovely Professional University</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Fraunces:opsz,wght@9..144,400;9..144,500;9..144,600&family=Inter:wght@400;500;600&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet">
<style>
  :root{
    --bg: #0E1A14;
    --bg-soft: #142720;
    --surface: #16261E;
    --border: #24382D;
    --text: #EAF2EC;
    --text-muted: #93AA9C;
    --text-dim: #5E7568;
    --green: #7FD99A;
    --green-soft: #CFE8B8;
    --green-deep: #3E8F5C;
  }

  *{ box-sizing: border-box; margin:0; padding:0; }

  html{ scroll-behavior: smooth; }

  body{
    background: var(--bg);
    color: var(--text);
    font-family: 'Inter', sans-serif;
    line-height: 1.6;
    -webkit-font-smoothing: antialiased;
  }

  a{ color: inherit; text-decoration:none; }

  .wrap{
    max-width: 1120px;
    margin: 0 auto;
    padding: 0 32px;
  }

  ::selection{ background: var(--green-deep); color: #071009; }

  /* subtle backdrop texture */
  body::before{
    content:"";
    position: fixed;
    inset: 0;
    background:
      radial-gradient(60% 40% at 82% 8%, rgba(127,217,154,0.10), transparent 60%),
      radial-gradient(40% 30% at 10% 60%, rgba(127,217,154,0.05), transparent 60%);
    pointer-events: none;
    z-index: 0;
  }

  /* ---------- NAV ---------- */
  header{
    position: sticky;
    top: 0;
    z-index: 50;
    background: rgba(14,26,20,0.85);
    backdrop-filter: blur(10px);
    border-bottom: 1px solid var(--border);
  }

  nav{
    display:flex;
    align-items:center;
    justify-content: space-between;
    padding: 20px 0;
  }

  .logo{
    font-family: 'JetBrains Mono', monospace;
    font-size: 15px;
    font-weight: 500;
    color: var(--text);
    letter-spacing: -0.02em;
  }
  .logo span{ color: var(--green); }

  .nav-links{
    display:flex;
    gap: 36px;
    list-style:none;
    font-size: 14.5px;
    color: var(--text-muted);
  }
  .nav-links a{ transition: color .15s ease; }
  .nav-links a:hover{ color: var(--text); }

  .nav-cta{
    font-family:'Inter', sans-serif;
    font-size: 14px;
    font-weight: 600;
    padding: 9px 18px;
    border: 1px solid var(--green-deep);
    border-radius: 8px;
    color: var(--green-soft);
    transition: background .15s ease, color .15s ease;
  }
  .nav-cta:hover{ background: var(--green-deep); color: #071009; }

  .nav-toggle{ display:none; background:none; border:none; color:var(--text); font-size:22px; cursor:pointer; }

  /* ---------- HERO ---------- */
  .hero{
    position: relative;
    z-index: 1;
    padding: 96px 0 72px;
    display: grid;
    grid-template-columns: 1.15fr 0.85fr;
    gap: 56px;
    align-items: center;
  }

  .kicker{
    font-family:'JetBrains Mono', monospace;
    font-size: 13px;
    color: var(--green);
    margin-bottom: 20px;
    display:flex;
    align-items:center;
    gap: 8px;
  }
  .kicker::before{
    content:"";
    width: 7px; height: 7px;
    border-radius: 50%;
    background: var(--green);
    box-shadow: 0 0 0 4px rgba(127,217,154,0.15);
  }

  h1{
    font-family:'Fraunces', serif;
    font-weight: 500;
    font-size: clamp(2.4rem, 4.2vw, 3.6rem);
    line-height: 1.08;
    letter-spacing: -0.01em;
    color: var(--text);
    max-width: 15ch;
  }
  h1 em{
    font-style: italic;
    color: var(--green-soft);
  }

  .hero-desc{
    margin-top: 24px;
    max-width: 46ch;
    color: var(--text-muted);
    font-size: 16px;
  }

  .hero-actions{
    margin-top: 34px;
    display:flex;
    gap: 14px;
    flex-wrap: wrap;
  }

  .btn-primary, .btn-secondary{
    font-size: 14.5px;
    font-weight: 600;
    padding: 13px 22px;
    border-radius: 8px;
    display:inline-flex;
    align-items:center;
    gap: 8px;
    transition: transform .15s ease, background .15s ease, border-color .15s ease;
  }
  .btn-primary{
    background: var(--green);
    color: #071009;
  }
  .btn-primary:hover{ transform: translateY(-1px); background: var(--green-soft); }

  .btn-secondary{
    border: 1px solid var(--border);
    color: var(--text);
  }
  .btn-secondary:hover{ border-color: var(--green-deep); transform: translateY(-1px); }

  /* hero panel: terminal-style card instead of a photo */
  .hero-panel{
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 14px;
    overflow: hidden;
  }
  .panel-bar{
    display:flex;
    align-items:center;
    gap: 6px;
    padding: 12px 16px;
    border-bottom: 1px solid var(--border);
  }
  .panel-bar span{
    width: 9px; height:9px; border-radius:50%;
    background: var(--border);
  }
  .panel-bar .file{
    margin-left: 10px;
    font-family:'JetBrains Mono', monospace;
    font-size: 12px;
    color: var(--text-dim);
  }
  .panel-body{
    padding: 22px 20px 24px;
    font-family:'JetBrains Mono', monospace;
    font-size: 13px;
    color: var(--text-muted);
  }
  .panel-body .ln{ display:flex; gap: 14px; margin-bottom: 9px; }
  .panel-body .no{ color: var(--text-dim); width: 14px; text-align:right; flex-shrink:0; }
  .panel-body .kw{ color: var(--green); }
  .panel-body .st{ color: var(--green-soft); }
  .panel-body .cm{ color: var(--text-dim); font-style: italic; }

  .panel-stats{
    display:grid;
    grid-template-columns: repeat(3, 1fr);
    border-top: 1px solid var(--border);
  }
  .panel-stats div{
    padding: 16px;
    border-right: 1px solid var(--border);
  }
  .panel-stats div:last-child{ border-right:none; }
  .panel-stats strong{
    display:block;
    font-family:'Fraunces', serif;
    font-size: 22px;
    color: var(--green-soft);
    font-weight: 500;
  }
  .panel-stats span{
    font-size: 11.5px;
    color: var(--text-dim);
    font-family:'JetBrains Mono', monospace;
  }

  /* ---------- SECTION SHELL ---------- */
  section{ position: relative; z-index:1; padding: 84px 0; border-top: 1px solid var(--border); }
  .sec-head{ margin-bottom: 44px; }
  .sec-num{
    font-family:'JetBrains Mono', monospace;
    font-size: 12.5px;
    color: var(--text-dim);
    margin-bottom: 10px;
  }
  .sec-title{
    font-family:'Fraunces', serif;
    font-weight: 500;
    font-size: clamp(1.6rem, 2.6vw, 2.1rem);
    color: var(--text);
  }
  .sec-sub{
    margin-top: 12px;
    color: var(--text-muted);
    max-width: 60ch;
    font-size: 15px;
  }

  /* ---------- ABOUT ---------- */
  .about-grid{
    display:grid;
    grid-template-columns: 1fr 1fr;
    gap: 48px;
  }
  .about-grid p{ color: var(--text-muted); margin-bottom: 16px; font-size: 15.5px; }
  .about-grid p strong{ color: var(--text); font-weight: 600; }

  .fact-list{ border-top: 1px solid var(--border); }
  .fact{
    display:flex;
    justify-content: space-between;
    padding: 14px 0;
    border-bottom: 1px solid var(--border);
    font-size: 14.5px;
  }
  .fact .k{ color: var(--text-dim); font-family:'JetBrains Mono', monospace; font-size: 13px; }
  .fact .v{ color: var(--text); text-align:right; }

  /* ---------- SKILLS ---------- */
  .skills-grid{
    display:grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 1px;
    background: var(--border);
    border: 1px solid var(--border);
    border-radius: 12px;
    overflow: hidden;
  }
  .skill-card{
    background: var(--bg-soft);
    padding: 26px 24px;
  }
  .skill-card h3{
    font-family:'JetBrains Mono', monospace;
    font-size: 12.5px;
    text-transform: none;
    color: var(--green);
    margin-bottom: 14px;
  }
  .skill-card ul{ list-style:none; display:flex; flex-wrap:wrap; gap: 8px; }
  .skill-card li{
    font-size: 13.5px;
    color: var(--text-muted);
    border: 1px solid var(--border);
    padding: 5px 11px;
    border-radius: 6px;
  }

  /* ---------- PROJECTS ---------- */
  .projects{ display:flex; flex-direction:column; gap: 1px; background: var(--border); border:1px solid var(--border); border-radius: 12px; overflow:hidden; }
  .project{
    background: var(--bg-soft);
    padding: 30px 28px;
    display:grid;
    grid-template-columns: 1fr 2fr;
    gap: 28px;
  }
  .project-meta{ display:flex; flex-direction:column; gap: 6px; }
  .project-meta .date{ font-family:'JetBrains Mono', monospace; font-size: 12px; color: var(--text-dim); }
  .project-meta h3{ font-family:'Fraunces', serif; font-size: 19px; font-weight: 500; color: var(--text); }
  .project-body ul{ list-style:none; }
  .project-body li{
    position: relative;
    padding-left: 18px;
    color: var(--text-muted);
    font-size: 14.5px;
    margin-bottom: 8px;
  }
  .project-body li::before{
    content:"›";
    position:absolute; left:0; color: var(--green);
  }
  .tech-row{ margin-top: 12px; display:flex; flex-wrap:wrap; gap: 8px; }
  .tech-row span{
    font-family:'JetBrains Mono', monospace;
    font-size: 11.5px;
    color: var(--green-soft);
    border: 1px solid var(--green-deep);
    padding: 3px 9px;
    border-radius: 20px;
  }

  /* ---------- CERTIFICATIONS ---------- */
  .cert-row{ display:grid; grid-template-columns: 1fr 1fr; gap: 1px; background: var(--border); border:1px solid var(--border); border-radius: 12px; overflow:hidden; }
  .cert{ background: var(--bg-soft); padding: 26px 26px; display:flex; justify-content:space-between; align-items:flex-start; }
  .cert h3{ font-family:'Fraunces', serif; font-weight:500; font-size: 17px; color: var(--text); margin-bottom: 6px; }
  .cert .org{ color: var(--text-muted); font-size: 13.5px; }
  .cert .date{ font-family:'JetBrains Mono', monospace; font-size: 12px; color: var(--text-dim); white-space:nowrap; }

  /* ---------- EDUCATION ---------- */
  .timeline{ border-left: 1px solid var(--border); padding-left: 32px; display:flex; flex-direction:column; gap: 36px; }
  .tl-item{ position: relative; }
  .tl-item::before{
    content:"";
    position:absolute; left:-37.5px; top: 4px;
    width: 9px; height:9px; border-radius:50%;
    background: var(--green);
    box-shadow: 0 0 0 4px var(--bg), 0 0 0 5px var(--border);
  }
  .tl-item .date{ font-family:'JetBrains Mono', monospace; font-size: 12px; color: var(--text-dim); margin-bottom: 6px; }
  .tl-item h3{ font-family:'Fraunces', serif; font-weight: 500; font-size: 18.5px; color: var(--text); }
  .tl-item p{ color: var(--text-muted); font-size: 14.5px; margin-top: 4px; }

  /* ---------- CONTACT ---------- */
  .contact-box{
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 16px;
    padding: 56px 48px;
    text-align:center;
  }
  .contact-box h2{
    font-family:'Fraunces', serif;
    font-weight: 500;
    font-size: clamp(1.7rem, 3vw, 2.4rem);
    max-width: 20ch;
    margin: 0 auto 16px;
  }
  .contact-box p{ color: var(--text-muted); max-width: 42ch; margin: 0 auto 30px; }
  .contact-actions{ display:flex; justify-content:center; gap: 14px; flex-wrap:wrap; }

  footer{
    border-top: 1px solid var(--border);
    padding: 28px 0;
    text-align:center;
    font-size: 13px;
    color: var(--text-dim);
    font-family:'JetBrains Mono', monospace;
  }

  /* ---------- RESPONSIVE ---------- */
  @media (max-width: 860px){
    .nav-links, .nav-cta{ display:none; }
    .nav-toggle{ display:block; }
    .hero{ grid-template-columns: 1fr; padding-top: 56px; }
    .about-grid{ grid-template-columns: 1fr; }
    .skills-grid{ grid-template-columns: 1fr; }
    .project{ grid-template-columns: 1fr; }
    .cert-row{ grid-template-columns: 1fr; }
    .contact-box{ padding: 40px 24px; }
  }

  @media (prefers-reduced-motion: reduce){
    html{ scroll-behavior:auto; }
    *{ transition:none !important; }
  }
</style>
</head>
<body>

<header>
  <div class="wrap">
    <nav>
      <a class="logo" href="#top">harshit<span>.dev</span></a>
      <ul class="nav-links">
        <li><a href="#about">About</a></li>
        <li><a href="#skills">Skills</a></li>
        <li><a href="#projects">Projects</a></li>
        <li><a href="#certifications">Certifications</a></li>
        <li><a href="#education">Education</a></li>
      </ul>
      <a class="nav-cta" href="#contact">Get in touch</a>
      <button class="nav-toggle" aria-label="Menu">☰</button>
    </nav>
  </div>
</header>

<main id="top">

  <!-- HERO -->
  <section style="border-top:none;">
    <div class="wrap hero">
      <div>
        <div class="kicker">B.Tech Computer Science, Lovely Professional University</div>
        <h1>Harshit Sharma writes the query, wires the circuit, and <em>ships the result.</em></h1>
        <p class="hero-desc">Second-year CSE undergraduate who works comfortably across two very different layers of a system — relational data on one side, embedded electronics on the other — with Python, SQL and a growing set of dev tools in between.</p>
        <div class="hero-actions">
          <a class="btn-primary" href="#projects">View projects →</a>
          <a class="btn-secondary" href="mailto:harshitsharma1308.8@gmail.com">Download resume</a>
        </div>
      </div>

      <div class="hero-panel">
        <div class="panel-bar">
          <span></span><span></span><span></span>
          <div class="file">profile.sql</div>
        </div>
        <div class="panel-body">
          <div class="ln"><span class="no">1</span><span><span class="kw">SELECT</span> name, cgpa, focus</span></div>
          <div class="ln"><span class="no">2</span><span><span class="kw">FROM</span> students</span></div>
          <div class="ln"><span class="no">3</span><span><span class="kw">WHERE</span> name = <span class="st">'Harshit Sharma'</span>;</span></div>
          <div class="ln"><span class="no">4</span><span class="cm">-- CGPA: 8.5 · CSE, LPU · Aug 2025–Present</span></div>
        </div>
        <div class="panel-stats">
          <div><strong>8.5</strong><span>CGPA SO FAR</span></div>
          <div><strong>2</strong><span>PROJECTS BUILT</span></div>
          <div><strong>2</strong><span>CERTIFICATIONS</span></div>
        </div>
      </div>
    </div>
  </section>

  <!-- ABOUT -->
  <section id="about">
    <div class="wrap">
      <div class="sec-head">
        <div class="sec-num">01 — About</div>
        <h2 class="sec-title">Still early, already building.</h2>
      </div>
      <div class="about-grid">
        <div>
          <p>Harshit is currently pursuing a <strong>B.Tech in Computer Science and Engineering</strong> at Lovely Professional University, Punjab, holding a CGPA of <strong>8.5</strong> so far. His coursework spans DSA, OOP, computer networks and cryptography, alongside self-directed work in data querying and embedded systems.</p>
          <p>Outside the classroom, he's been sharpening two practical skill sets in parallel: writing SQL to make sense of relational data, and building small hardware systems with Arduino — most recently a real-time electricity monitoring setup that tracks generation and usage across appliances.</p>
        </div>
        <div class="fact-list">
          <div class="fact"><span class="k">LOCATION</span><span class="v">Punjab, India</span></div>
          <div class="fact"><span class="k">EMAIL</span><span class="v">harshitsharma1308.8@gmail.com</span></div>
          <div class="fact"><span class="k">PHONE</span><span class="v">+91 98119 41112</span></div>
          <div class="fact"><span class="k">PROFILES</span><span class="v">LinkedIn · GitHub</span></div>
          <div class="fact"><span class="k">CORE SUBJECTS</span><span class="v">DSA, OOP, Networks, Cryptography</span></div>
        </div>
      </div>
    </div>
  </section>

  <!-- SKILLS -->
  <section id="skills">
    <div class="wrap">
      <div class="sec-head">
        <div class="sec-num">02 — Skills</div>
        <h2 class="sec-title">The stack, layer by layer.</h2>
      </div>
      <div class="skills-grid">
        <div class="skill-card">
          <h3>Languages</h3>
          <ul><li>Python</li><li>SQL</li><li>C</li><li>Java (basics)</li></ul>
        </div>
        <div class="skill-card">
          <h3>Web Technologies</h3>
          <ul><li>HTML</li><li>CSS</li><li>JavaScript</li></ul>
        </div>
        <div class="skill-card">
          <h3>Developer Tools</h3>
          <ul><li>Jupyter Notebook</li><li>Excel</li><li>Power BI</li><li>Arduino IDE</li></ul>
        </div>
        <div class="skill-card">
          <h3>Core Subjects</h3>
          <ul><li>DSA</li><li>OOP</li><li>Computer Networks</li><li>Cryptography</li></ul>
        </div>
        <div class="skill-card">
          <h3>Soft Skills</h3>
          <ul><li>Analytical Thinking</li><li>Problem Solving</li><li>Communication</li><li>Tactical Thinking</li></ul>
        </div>
      </div>
    </div>
  </section>

  <!-- PROJECTS -->
  <section id="projects">
    <div class="wrap">
      <div class="sec-head">
        <div class="sec-num">03 — Projects</div>
        <h2 class="sec-title">Two systems, two different worlds.</h2>
      </div>
      <div class="projects">
        <div class="project">
          <div class="project-meta">
            <span class="date">Aug 2026 — Present</span>
            <h3>SQL Practice Queries</h3>
          </div>
          <div class="project-body">
            <ul>
              <li>Practiced relational data querying by solving beginner-to-intermediate SQL problems centered on real datasets.</li>
              <li>Built queries using SELECT, JOIN and GROUP BY to combine and summarize data across multiple relational tables.</li>
              <li>Strengthened relational database fluency as a foundation for more advanced querying and data-analysis work.</li>
            </ul>
            <div class="tech-row"><span>SQL</span></div>
          </div>
        </div>

        <div class="project">
          <div class="project-meta">
            <span class="date">Nov 2025</span>
            <h3>Smart Electricity Management System</h3>
          </div>
          <div class="project-body">
            <ul>
              <li>Addressed undetected energy loss across different electrical appliances by building a real-time monitoring setup.</li>
              <li>Integrated Arduino Uno/Nano with piezo and current sensors, a relay module, and an OLED display for live readings.</li>
              <li>Delivered an automatic count of electricity generated versus consumed, helping route power to appliances that need less of it.</li>
            </ul>
            <div class="tech-row"><span>Arduino Uno</span><span>Arduino Nano</span><span>Sensors</span><span>Arduino IDE</span></div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- CERTIFICATIONS -->
  <section id="certifications">
    <div class="wrap">
      <div class="sec-head">
        <div class="sec-num">04 — Certifications</div>
        <h2 class="sec-title">Formalizing the fundamentals.</h2>
      </div>
      <div class="cert-row">
        <div class="cert">
          <div>
            <h3>Python Certification</h3>
            <div class="org">Infosys Springboard</div>
          </div>
          <div class="date">Jul 2026</div>
        </div>
        <div class="cert">
          <div>
            <h3>Introduction to Cybersecurity</h3>
            <div class="org">Infosys Springboard</div>
          </div>
          <div class="date">Mar 2026</div>
        </div>
      </div>
    </div>
  </section>

  <!-- EDUCATION -->
  <section id="education">
    <div class="wrap">
      <div class="sec-head">
        <div class="sec-num">05 — Education</div>
        <h2 class="sec-title">Where it's been building up.</h2>
      </div>
      <div class="timeline">
        <div class="tl-item">
          <div class="date">Aug 2025 — Present</div>
          <h3>Lovely Professional University, Punjab</h3>
          <p>B.Tech in Computer Science and Engineering — CGPA: 8.5</p>
        </div>
        <div class="tl-item">
          <div class="date">Apr 2024 — Mar 2025</div>
          <h3>PM SHREE Kendriya Vidyalaya No. 2, AFS Hindon</h3>
          <p>Class 12, Senior Secondary</p>
        </div>
        <div class="tl-item">
          <div class="date">Apr 2022 — Mar 2023</div>
          <h3>PM SHREE Kendriya Vidyalaya No. 2, AFS Hindon</h3>
          <p>Class 10, Secondary</p>
        </div>
      </div>
    </div>
  </section>

  <!-- CONTACT -->
  <section id="contact">
    <div class="wrap">
      <div class="contact-box">
        <h2>Open to internships and collaborative projects.</h2>
        <p>Whether it's a data problem, a hardware build, or something in between — reach out and let's talk.</p>
        <div class="contact-actions">
          <a class="btn-primary" href="mailto:harshitsharma1308.8@gmail.com">Email Harshit</a>
          <a class="btn-secondary" href="tel:+919811941112">Call +91 98119 41112</a>
        </div>
      </div>
    </div>
  </section>

</main>

<footer>
  <div class="wrap">© 2026 Harshit Sharma — built with HTML, CSS &amp; a bit of SQL.</div>
</footer>

<script>
  const toggle = document.querySelector('.nav-toggle');
  const links = document.querySelector('.nav-links');
  const cta = document.querySelector('.nav-cta');
  if (toggle) {
    toggle.addEventListener('click', () => {
      const open = links.style.display === 'flex';
      links.style.display = open ? 'none' : 'flex';
      cta.style.display = open ? 'none' : 'inline-flex';
      links.style.flexDirection = 'column';
      links.style.position = 'absolute';
      links.style.top = '64px';
      links.style.left = '0';
      links.style.right = '0';
      links.style.background = 'var(--bg-soft)';
      links.style.padding = '20px 32px';
      links.style.borderBottom = '1px solid var(--border)';
      cta.style.margin = '0 32px 20px';
    });
  }
</script>

</body>
</html>
