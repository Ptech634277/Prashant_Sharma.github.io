<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Prashant Sharma • Data Analyst Portfolio</title>
  <meta name="description" content="Prashant Sharma — Data Analyst portfolio with projects, skills, experience, and contact." />
  <style>
    :root{
      --bg: #0b1020;        /* background */
      --panel:#0f1530;      /* surfaces */
      --soft:#12193a;       /* soft surfaces */
      --text:#e6ecff;       /* primary text */
      --muted:#9fb0d6;      /* secondary text */
      --brand:#6aa6ff;      /* accent */
      --brand-2:#98f5e1;    /* accent 2 */
      --ok:#4ade80;
      --warn:#fbbf24;
      --err:#f87171;
      --shadow: 0 10px 30px rgba(0,0,0,.35), 0 2px 10px rgba(0,0,0,.25);
      --radius: 18px;
    }
    *{box-sizing:border-box}
    html,body{height:100%}
    body{
      margin:0; font-family: ui-sans-serif, system-ui, -apple-system, Segoe UI, Roboto, "Helvetica Neue", Arial, "Noto Sans", "Apple Color Emoji", "Segoe UI Emoji";
      color:var(--text); background: radial-gradient(1200px 800px at 80% -10%, #1b2452 0%, transparent 60%),
                        radial-gradient(1000px 700px at -10% 10%, #12204d 0%, transparent 55%),
                        linear-gradient(180deg, #0a0f1f 0%, #070a15 100%);
      line-height:1.6;
      -webkit-font-smoothing:antialiased; text-rendering:optimizeLegibility;
    }
    a{color:var(--brand); text-decoration:none}
    a:hover{text-decoration:underline}
    .container{max-width:1100px; margin:0 auto; padding:0 20px}
    header{
      position:sticky; top:0; z-index:50; backdrop-filter: blur(12px);
      background: rgba(7,10,21,.45); border-bottom:1px solid rgba(255,255,255,.06);
      box-shadow: 0 2px 12px rgba(0,0,0,0.08); transition: box-shadow 0.2s;
    }
    .nav{display:flex; align-items:center; justify-content:space-between; gap:12px; padding:14px 0}
    .brand{display:flex; align-items:center; gap:12px}
    .logo{width:42px; height:42px; border-radius:50%; background:linear-gradient(135deg,var(--brand),var(--brand-2)); display:grid; place-items:center; box-shadow:var(--shadow)}
    .logo span{font-weight:800; color:#0b1020}
    .title{font-size:18px; font-weight:700}
    .navlinks{display:flex; gap:16px; flex-wrap:wrap}
    .chip{padding:8px 12px; border:1px solid rgba(255,255,255,.08); border-radius:999px; color:var(--muted)}
    .chip.active, .chip:hover{border-color:rgba(255,255,255,.25); color:var(--text)}

    /* Hero */
    .hero{padding:56px 0 26px}
    .hero-grid{display:grid; grid-template-columns: 1.1fr .9fr; gap:28px}
    .card{background:linear-gradient(180deg, rgba(255,255,255,.06), rgba(255,255,255,.03)); border:1px solid rgba(255,255,255,.08); border-radius:var(--radius); box-shadow:var(--shadow)}
    .card.pad{padding:26px}
    .badge{display:inline-flex; align-items:center; gap:8px; padding:6px 10px; border-radius:999px; background:rgba(106,166,255,.16); border:1px solid rgba(106,166,255,.35); color:#cfe1ff; font-size:12px; font-weight:600}
    h1{font-size:40px; line-height:1.15; margin:14px 0 8px}
    .sub{color:var(--muted); font-size:17px}
    .kpis{display:grid; grid-template-columns:repeat(3,1fr); gap:12px; margin-top:18px}
    .kpi{background:var(--soft); border:1px solid rgba(255,255,255,.08); border-radius:14px; padding:14px}
    .kpi .n{font-size:22px; font-weight:800}
    .kpi .l{font-size:12px; color:var(--muted)}

    .hero-aside{display:grid; gap:16px}
    .avatar{height:100%; min-height:260px; border-radius:var(--radius); overflow:hidden; background:
      radial-gradient(400px 260px at 10% 0%, rgba(152,245,225,.12), transparent 50%),
      radial-gradient(400px 260px at 95% 0%, rgba(106,166,255,.12), transparent 50%),
      linear-gradient(180deg, #0f1530, #0b1020);
      border:1px solid rgba(255,255,255,.08); display:grid; place-items:center}
    .avatar .placeholder{opacity:.75; color:var(--muted)}

    /* Sections */
    section{padding:34px 0}
    section h2{font-size:28px; margin:0 0 14px}
    .grid{display:grid; gap:14px}
    .grid.cols-2{grid-template-columns:1fr 1fr}
    .grid.cols-3{grid-template-columns:repeat(3,1fr)}

    .pill{display:inline-flex; align-items:center; gap:8px; padding:8px 12px; border:1px solid rgba(255,255,255,.08); border-radius:999px; color:#dbe6ff; background:rgba(255,255,255,.03)}

    .list{display:grid; gap:12px}
    .item{padding:16px; border:1px solid rgba(255,255,255,.08); background:linear-gradient(180deg, rgba(255,255,255,.05), rgba(255,255,255,.02)); border-radius:14px}
    .item h3{margin:0 0 8px; font-size:18px}
    .item .meta{color:var(--muted); font-size:13px}
    .item ul{margin:10px 0 0 20px}

    footer{border-top:1px solid rgba(255,255,255,.08); padding:26px 0 46px; color:var(--muted)}

    /* Utilities */
    .row{display:flex; align-items:center; gap:10px; flex-wrap:wrap}
    .between{justify-content:space-between}
    .mt-2{margin-top:8px}
    .mt-3{margin-top:14px}
    .mt-4{margin-top:22px}
    .btn{display:inline-flex; align-items:center; gap:10px; padding:10px 14px; border-radius:12px; border:1px solid rgba(255,255,255,.1); background:linear-gradient(180deg, rgba(255,255,255,.08), rgba(255,255,255,.02)); color:var(--text); font-weight:600}
    .btn:hover{transform:translateY(-1px)}

    /* Responsive */
    @media (max-width: 900px){
      .hero-grid{grid-template-columns:1fr}
      .grid.cols-2{grid-template-columns:1fr}
      .grid.cols-3{grid-template-columns:1fr}
    }
  </style>
</head>
<body>
  <header>
    <div class="container nav">
      <div class="brand">
        <div class="logo"><span>PS</span></div>
        <div class="title">Prashant Sharma • Data Analyst</div>
      </div>
      <nav class="navlinks">
        <a class="chip" href="#about">About</a>
        <a class="chip" href="#skills">Skills</a>
        <a class="chip" href="#experience">Experience</a>
        <a class="chip" href="#projects">Projects</a>
        <a class="chip" href="#education">Education</a>
        <a class="chip" href="#certs">Certifications</a>
        <a class="chip" href="#contact">Contact</a>
      </nav>
    </div>
  </header>

  <main class="container">
    <!-- Hero -->
    <section class="hero">
      <div class="hero-grid">
        <div class="card pad">
          <span class="badge">Available for opportunities</span>
          <h1>Hi, I'm Prashant — a Data Analyst specializing in dashboards, reporting automation, and KPI tracking.</h1>
          <p class="sub">Gurugram, Haryana • Excel (Advanced) • Power BI • POS/ICMS • Reporting Automation • Client Communication</p>

          <div class="kpis">
            <div class="kpi"><div class="n">25%+</div><div class="l">Reporting efficiency improvement</div></div>
            <div class="kpi"><div class="n">3+ yrs</div><div class="l">Combined analytics & training</div></div>
            <div class="kpi"><div class="n">100%</div><div class="l">ICMS accuracy maintained</div></div>
          </div>

          <div class="row mt-4">
            <!-- Update the href below to your live resume link when hosted -->
            <a class="btn" href="#" id="resumeLink">Download Résumé</a>
            <a class="btn" href="https://www.linkedin.com/in/prashant-sharma-5683b2213/" target="_blank" rel="noopener">LinkedIn</a>
            <a class="btn" href="https://github.com/Ptech634277" target="_blank" rel="noopener">GitHub</a>
          </div>
        </div>
        <aside class="avatar card">
          <!-- Replace this placeholder with <img src="your-photo.jpg" alt="Prashant Sharma"/>  -->
          <img src="prashant.jpg.jpg" alt="Prashant Sharma" style="width:100%;max-width:320px;border-radius:18px;box-shadow:0 2px 16px #0002;">
        </aside>
      </div>
    </section>

    <!-- About -->
    <section id="about">
      <div class="grid cols-2">
        <div class="card pad">
          <h2>About Me</h2>
          <p>
            Data Analyst with 3+ years of combined experience in data analysis, visualization, and IT training. I build
            interactive dashboards (Power BI) and automate reporting to help teams make faster, data‑driven decisions.
            Recent wins include deploying a retail sales dashboard that integrated POS, inventory, and profit data and
            improved reporting efficiency by 25%.
          </p>
        </div>
        <div class="card pad">
          <h2>Core Strengths</h2>
          <div class="row mt-2">
            <span class="pill">KPI Design</span>
            <span class="pill">Power Query & DAX</span>
            <span class="pill">Data Cleaning</span>
            <span class="pill">ICMS & POS</span>
            <span class="pill">Client Communication</span>
            <span class="pill">Presentation Design</span>
          </div>
        </div>
      </div>
    </section>

    <!-- Skills -->
    <section id="skills">
      <div class="card pad">
        <h2>Skills</h2>
        <div class="grid cols-3 mt-2">
          <div class="item">
            <h3>Data Analysis & Viz</h3>
            <p class="meta">Excel (Advanced), Power BI, Tableau (learning)</p>
          </div>
          <div class="item">
            <h3>Data Management</h3>
            <p class="meta">ICMS, POS Reporting, Data Cleaning, KPI Tracking</p>
          </div>
          <div class="item">
            <h3>Business Tools</h3>
            <p class="meta">Microsoft Office, Reporting Automation</p>
          </div>
          <div class="item">
            <h3>Soft Skills</h3>
            <p class="meta">Client Communication, Problem Solving, Attention to Detail</p>
          </div>
          <div class="item">
            <h3>Other</h3>
            <p class="meta">ChatGPT for productivity, Data Entry</p>
          </div>
        </div>
      </div>
    </section>

    <!-- Experience -->
    <section id="experience">
      <div class="card pad">
        <h2>Experience</h2>
        <div class="list mt-2">
          <div class="item">
            <h3>Data Analyst — Vervebot <span class="meta">(Mar 2024 – Present • Gurugram, Haryana)</span></h3>
            <ul>
              <li>Designed and deployed an interactive Power BI Sales Dashboard integrating POS, inventory, and profit data.</li>
              <li>Managed invoices and inventory in ICMS with 100% accuracy and timely updates.</li>
              <li>Automated reporting processes, improving data delivery efficiency by 25%.</li>
              <li>Generated KPI‑based reports, sales trends, and top product analyses for leadership.</li>
              <li>Maintained client communication to capture requirements and deliver insights.</li>
            </ul>
          </div>
          <div class="item">
            <h3>Computer Teacher — Analyzer Institute <span class="meta">(Sep 2021 – Mar 2024 • Pilibhit, UP)</span></h3>
            <ul>
              <li>Taught computer fundamentals, programming, and software applications across levels.</li>
              <li>Developed curriculum‑aligned lesson plans and training materials.</li>
              <li>Led group and 1‑to‑1 sessions to improve technical proficiency.</li>
            </ul>
          </div>
        </div>
      </div>
    </section>

    <!-- Projects -->
    <section id="projects">
      <div class="card pad">
        <h2>Projects</h2>
        <div class="list mt-2">
          <div class="item">
            <h3>Sales Dashboard — Power BI (Vervebot Internal)</h3>
            <ul>
              <li>Built interactive visuals to analyze retail sales, profit margins, and top‑performing products.</li>
              <li>Integrated multiple data sources including POS and ICMS.</li>
              <li>Delivered KPI‑driven insights with dynamic filters for department, products, and timeframes.</li>
            </ul>
            <!-- Optional: add links to report or screenshots -->
            <!-- <div class="row mt-3"><a class="btn" href="#">View Live</a><a class="btn" href="#">Case Study</a></div> -->
          </div>
        </div>
      </div>
    </section>

    <!-- Education -->
    <section id="education">
      <div class="card pad">
        <h2>Education</h2>
        <div class="grid cols-2 mt-2">
          <div class="item">
            <h3>MBA (In Progress)</h3>
            <p class="meta">Uttaranchal University, Dehradun</p>
          </div>
          <div class="item">
            <h3>BSc in Agriculture (2023)</h3>
            <p class="meta">MJPRU, Bareilly</p>
          </div>
          <div class="item">
            <h3>Intermediate (Agriculture) — 2018</h3>
            <p class="meta">U.P. Board</p>
          </div>
          <div class="item">
            <h3>Intermediate (PCM) — 2016</h3>
            <p class="meta">U.P. Board</p>
          </div>
          <div class="item">
            <h3>High School — 2014</h3>
            <p class="meta">U.P. Board</p>
          </div>
        </div>
      </div>
    </section>

    <!-- Certifications -->
    <section id="certs">
      <div class="card pad">
        <h2>Certifications</h2>
        <div class="grid cols-2 mt-2">
          <div class="item">
            <h3>Domestic Data Entry Operator</h3>
            <p class="meta">Unifiers Social Ventures Pvt. Ltd.</p>
            <p>Skills: Data Entry, Microsoft Excel, Data Management</p>
          </div>
          <div class="item">
            <h3>CCC (Course on Computer Concepts)</h3>
            <p class="meta">NIELIT</p>
            <p>Skills: Computer Fundamentals, MS Office, Basic Programming</p>
          </div>
          <div class="item">
            <h3>'O'-Level</h3>
            <p class="meta">NIELIT</p>
            <p>Skills: Programming, Database Management, Web Design</p>
          </div>
        </div>
      </div>
    </section>

    <!-- Contact -->
    <section id="contact">
      <div class="card pad">
        <h2>Contact</h2>
        <div class="grid cols-2 mt-2">
          <div class="item">
            <h3>Let's connect</h3>
            <p class="meta">I'm open to data analyst roles, dashboard projects, and freelance reporting automation.</p>
            <div class="row mt-3">
              <a class="btn" href="mailto:prashantpbt98@outlook.com">Email</a>
              <a class="btn" href="tel:+918439491083">Call</a>
              <a class="btn" href="https://www.linkedin.com/in/prashant-sharma-5683b2213/" target="_blank" rel="noopener">LinkedIn</a>
            </div>
          </div>
          <div class="item">
            <h3>Details</h3>
            <p class="meta">Gurugram, Haryana • English • Hindi</p>
            <p class="meta">Email: prashantpbt98@outlook.com • Phone: 8439491083</p>
          </div>
        </div>
      </div>
    </section>

  </main>

  <footer>
    <div class="container row between">
      <div>© <span id="year"></span> Prashant Sharma — Data Analyst</div>
      <div class="row">
        <a class="chip" href="#about">Back to top ↑</a>
      </div>
    </div>
  </footer>

  <script>
    // Smooth scroll for nav links
    document.querySelectorAll('a[href^="#"]').forEach(a=>{
      a.addEventListener('click', e=>{
        const href = a.getAttribute('href');
        if(href.length>1){
          e.preventDefault();
          document.querySelector(href).scrollIntoView({behavior:'smooth'});
        }
      })
    })

    // Active nav on scroll
    const chips = document.querySelectorAll('.navlinks .chip');
    const sections = [...document.querySelectorAll('main section')];
    const setActive = () => {
      const y = window.scrollY + 120; // header offset
      let current = sections[0].id;
      for(const s of sections){ if(s.offsetTop <= y) current = s.id; }
      chips.forEach(c=>{
        const match = c.getAttribute('href') === `#${current}`;
        c.classList.toggle('active', match);
      })
    };
    window.addEventListener('scroll', setActive); setActive();

    // Footer year
    document.getElementById('year').textContent = new Date().getFullYear();

    // Update resume link if you place resume in same folder as index.html
    // Rename your PDF to resume.pdf for an instant working link.
    const resumeHrefCandidate = 'resume.pdf';
    fetch(resumeHrefCandidate, {method:'HEAD'}).then(r=>{
      if(r.ok) document.getElementById('resumeLink').setAttribute('href', resumeHrefCandidate);
    }).catch(()=>{});
  </script>
</body>
</html>
