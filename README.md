<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width,initial-scale=1"/>
<title>Pavan Venkat Kumar — GitHub Profile</title>
<link href="https://fonts.googleapis.com/css2?family=Space+Mono:wght@400;700&family=Syne:wght@400;700;800&display=swap" rel="stylesheet"/>
<style>
  :root {
    --bg: #0d1117;
    --surface: #161b22;
    --border: #30363d;
    --accent: #00d4ff;
    --accent2: #6e40c9;
    --accent3: #ff4b4b;
    --text: #e6edf3;
    --muted: #8b949e;
    --glow: 0 0 30px rgba(0,212,255,0.3);
  }

  * { margin:0; padding:0; box-sizing:border-box; }

  body {
    background: var(--bg);
    color: var(--text);
    font-family: 'Space Mono', monospace;
    min-height: 100vh;
    overflow-x: hidden;
  }

  /* HERO */
  .hero {
    background: linear-gradient(135deg, #0f0c29, #302b63, #24243e);
    padding: 60px 40px 50px;
    text-align: center;
    position: relative;
    overflow: hidden;
  }
  .hero::before {
    content: '';
    position: absolute;
    inset: 0;
    background: radial-gradient(ellipse at 30% 50%, rgba(110,64,201,0.25) 0%, transparent 60%),
                radial-gradient(ellipse at 70% 50%, rgba(0,212,255,0.15) 0%, transparent 60%);
    animation: pulse 4s ease-in-out infinite alternate;
  }
  @keyframes pulse { from { opacity:0.5; } to { opacity:1; } }

  .hero-name {
    font-family: 'Syne', sans-serif;
    font-size: clamp(2rem,5vw,3.5rem);
    font-weight: 800;
    background: linear-gradient(90deg, #00d4ff, #6e40c9, #ff4b4b);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    position: relative;
    letter-spacing: -1px;
    animation: shimmer 3s linear infinite;
    background-size: 200% auto;
  }
  @keyframes shimmer {
    0% { background-position: 0% center; }
    100% { background-position: 200% center; }
  }

  .hero-sub {
    color: var(--muted);
    margin-top: 10px;
    font-size: 14px;
    letter-spacing: 3px;
    text-transform: uppercase;
    position: relative;
  }

  .typing-text {
    color: var(--accent);
    font-size: 16px;
    margin-top: 20px;
    height: 28px;
    position: relative;
  }

  .badges {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
    justify-content: center;
    margin-top: 24px;
    position: relative;
  }

  .badge {
    padding: 6px 14px;
    border-radius: 6px;
    font-size: 12px;
    font-family: 'Space Mono', monospace;
    font-weight: 700;
    cursor: pointer;
    transition: transform 0.2s, box-shadow 0.2s;
  }
  .badge:hover { transform: translateY(-2px); box-shadow: var(--glow); }
  .b-linkedin { background:#0077B5; }
  .b-github { background:#161b22; border:1px solid #30363d; }
  .b-leet { background:#FFA116; color:#000; }
  .b-gfg { background:#298D46; }
  .b-gmail { background:#D14836; }

  /* SECTIONS */
  .container { max-width: 900px; margin: 0 auto; padding: 0 24px 60px; }

  .section { margin-top: 50px; }
  .section-title {
    font-family: 'Syne', sans-serif;
    font-size: 22px;
    font-weight: 700;
    display: flex;
    align-items: center;
    gap: 10px;
    margin-bottom: 24px;
    padding-bottom: 12px;
    border-bottom: 1px solid var(--border);
  }
  .section-title span { color: var(--accent); }

  /* CODE BLOCK */
  .code-block {
    background: #0d1117;
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 28px;
    font-size: 13px;
    line-height: 1.8;
    position: relative;
    overflow: hidden;
  }
  .code-block::before {
    content: '';
    position: absolute;
    top: 0; left: 0; right: 0;
    height: 3px;
    background: linear-gradient(90deg, var(--accent), var(--accent2), var(--accent3));
  }
  .code-dots {
    display: flex; gap:6px; margin-bottom:16px;
  }
  .dot { width:12px; height:12px; border-radius:50%; }
  .dot-r { background:#ff5f57; }
  .dot-y { background:#ffbd2e; }
  .dot-g { background:#28c840; }

  .kw { color: #ff7b72; }
  .fn { color: #d2a8ff; }
  .st { color: #a5d6ff; }
  .cm { color: #8b949e; font-style: italic; }
  .val { color: #79c0ff; }
  .em { color: #ffa657; }

  /* TECH GRID */
  .tech-section { margin-bottom: 20px; }
  .tech-label {
    font-size: 11px;
    text-transform: uppercase;
    letter-spacing: 2px;
    color: var(--muted);
    margin-bottom: 10px;
  }
  .tech-pills { display: flex; flex-wrap: wrap; gap: 8px; }
  .pill {
    padding: 5px 12px;
    border-radius: 20px;
    font-size: 11px;
    font-weight: 700;
    letter-spacing: 0.5px;
    border: 1px solid transparent;
    transition: transform 0.15s, box-shadow 0.15s;
  }
  .pill:hover { transform: translateY(-2px); box-shadow: 0 4px 20px rgba(0,212,255,0.2); }
  .p-ai { background: rgba(110,64,201,0.15); border-color: rgba(110,64,201,0.4); color: #c9b8ff; }
  .p-data { background: rgba(0,212,255,0.08); border-color: rgba(0,212,255,0.3); color: #7dd3fc; }
  .p-backend { background: rgba(52,211,153,0.08); border-color: rgba(52,211,153,0.3); color: #6ee7b7; }
  .p-devops { background: rgba(251,146,60,0.08); border-color: rgba(251,146,60,0.3); color: #fdba74; }
  .p-lang { background: rgba(249,115,22,0.08); border-color: rgba(249,115,22,0.3); color: #fb923c; }

  /* STATS */
  .stats-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 16px;
  }
  .stat-card {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 12px;
    overflow: hidden;
    transition: border-color 0.2s, transform 0.2s;
  }
  .stat-card:hover { border-color: var(--accent); transform: translateY(-3px); }
  .stat-card img { width: 100%; display: block; }

  /* SKILL BARS */
  .skill-row { margin-bottom: 12px; }
  .skill-header { display: flex; justify-content: space-between; font-size: 12px; margin-bottom: 6px; }
  .skill-label { color: var(--text); }
  .skill-pct { color: var(--accent); font-weight: 700; }
  .bar-bg { background: var(--border); border-radius: 4px; height: 8px; overflow: hidden; }
  .bar-fill {
    height: 100%;
    border-radius: 4px;
    background: linear-gradient(90deg, var(--accent2), var(--accent));
    transform-origin: left;
    animation: barGrow 1.2s cubic-bezier(0.34,1.56,0.64,1) both;
  }
  @keyframes barGrow { from { transform: scaleX(0); } to { transform: scaleX(1); } }

  /* FOCUS TABLE */
  .focus-table { width: 100%; border-collapse: collapse; border-radius: 12px; overflow: hidden; }
  .focus-table th {
    background: linear-gradient(90deg, rgba(110,64,201,0.3), rgba(0,212,255,0.15));
    padding: 12px 16px;
    font-size: 12px;
    text-transform: uppercase;
    letter-spacing: 1px;
    color: var(--accent);
    text-align: center;
  }
  .focus-table td {
    padding: 12px 16px;
    text-align: center;
    font-size: 13px;
    border-bottom: 1px solid var(--border);
    background: var(--surface);
  }
  .focus-table tr:hover td { background: rgba(110,64,201,0.05); }

  /* CTA */
  .cta {
    text-align: center;
    padding: 50px 40px;
    background: linear-gradient(135deg, rgba(110,64,201,0.1), rgba(0,212,255,0.05));
    border: 1px solid var(--border);
    border-radius: 16px;
    position: relative;
    overflow: hidden;
  }
  .cta::before {
    content: '';
    position: absolute;
    top:-50%; left:-50%;
    width:200%; height:200%;
    background: conic-gradient(from 0deg, transparent, rgba(110,64,201,0.06), transparent);
    animation: spin 8s linear infinite;
  }
  @keyframes spin { to { transform: rotate(360deg); } }
  .cta-quote {
    font-style: italic;
    color: var(--muted);
    font-size: 15px;
    margin-bottom: 20px;
    position: relative;
  }
  .cta-links { display: flex; justify-content: center; gap: 20px; flex-wrap: wrap; position: relative; }
  .cta-link {
    color: var(--accent);
    text-decoration: none;
    font-weight: 700;
    font-size: 13px;
    padding: 8px 20px;
    border: 1px solid var(--accent);
    border-radius: 6px;
    transition: all 0.2s;
  }
  .cta-link:hover { background: var(--accent); color: #000; }
  .cta-link.solid { background: var(--accent); color: #000; }
  .cta-link.solid:hover { background: transparent; color: var(--accent); }

  .footer {
    background: linear-gradient(135deg, #24243e, #302b63, #0f0c29);
    height: 80px;
    margin-top: 60px;
  }
</style>
</head>
<body>

<!-- HERO -->
<div class="hero">
  <div class="hero-name">D PAVAN VENKAT KUMAR</div>
  <div class="hero-sub">AI / ML Engineer · Deep Learning · Intelligent Systems</div>
  <div class="typing-text" id="typing"></div>
  <div class="badges">
    <span class="badge b-linkedin">💼 LinkedIn</span>
    <span class="badge b-github">🐙 GitHub</span>
    <span class="badge b-leet">🔸 LeetCode</span>
    <span class="badge b-gfg">🟩 GeeksforGeeks</span>
    <span class="badge b-gmail">📧 Gmail</span>
  </div>
</div>

<div class="container">

  <!-- ABOUT CODE -->
  <div class="section">
    <div class="section-title"><span>🧠</span> About Me</div>
    <div class="code-block">
      <div class="code-dots"><div class="dot dot-r"></div><div class="dot dot-y"></div><div class="dot dot-g"></div></div>
      <div>
        <span class="kw">class</span> <span class="fn">PavanVenkatKumar</span>:<br/>
        &nbsp;&nbsp;<span class="kw">def</span> <span class="fn">__init__</span>(self):<br/>
        &nbsp;&nbsp;&nbsp;&nbsp;self.<span class="val">name</span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;= <span class="st">"D Pavan Venkat Kumar"</span><br/>
        &nbsp;&nbsp;&nbsp;&nbsp;self.<span class="val">role</span>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;= <span class="st">"AI / ML Engineer"</span><br/>
        &nbsp;&nbsp;&nbsp;&nbsp;self.<span class="val">interests</span>&nbsp;&nbsp;&nbsp;= [<span class="st">"Computer Vision"</span>, <span class="st">"AI Agents"</span>, <span class="st">"Deep Learning"</span>]<br/>
        &nbsp;&nbsp;&nbsp;&nbsp;self.<span class="val">currently</span>&nbsp;&nbsp;= [<span class="st">"Infosys Springboard ✅"</span>, <span class="st">"Spring Boot + DSA 📚"</span>]<br/>
        &nbsp;&nbsp;&nbsp;&nbsp;self.<span class="val">open_to</span>&nbsp;&nbsp;&nbsp;&nbsp;= [<span class="st">"Medical Imaging Collabs 🏥"</span>, <span class="st">"Full Stack Help 🤝"</span>]<br/>
        <br/>
        &nbsp;&nbsp;<span class="kw">def</span> <span class="fn">life_motto</span>(self) -> <span class="st">str</span>:<br/>
        &nbsp;&nbsp;&nbsp;&nbsp;<span class="kw">return</span> <span class="st">"⚡ I code to create impact — one model at a time."</span><br/>
        <br/>
        me = <span class="fn">PavanVenkatKumar</span>()<br/>
        <span class="fn">print</span>(me.<span class="fn">life_motto</span>())<br/>
        <span class="cm"># ⚡ I code to create impact — one model at a time.</span>
      </div>
    </div>
  </div>

  <!-- TECH STACK -->
  <div class="section">
    <div class="section-title"><span>🚀</span> Tech Arsenal</div>

    <div class="tech-section">
      <div class="tech-label">🤖 AI / ML / Deep Learning</div>
      <div class="tech-pills">
        <span class="pill p-ai">Python</span>
        <span class="pill p-ai">TensorFlow</span>
        <span class="pill p-ai">PyTorch</span>
        <span class="pill p-ai">Scikit-Learn</span>
        <span class="pill p-ai">Hugging Face</span>
        <span class="pill p-ai">LangChain</span>
        <span class="pill p-ai">OpenCV</span>
      </div>
    </div>

    <br/>
    <div class="tech-section">
      <div class="tech-label">📊 Data Science</div>
      <div class="tech-pills">
        <span class="pill p-data">NumPy</span>
        <span class="pill p-data">Pandas</span>
        <span class="pill p-data">Matplotlib</span>
        <span class="pill p-data">Seaborn</span>
        <span class="pill p-data">Jupyter</span>
        <span class="pill p-data">Anaconda</span>
      </div>
    </div>

    <br/>
    <div class="tech-section">
      <div class="tech-label">🌐 Backend & APIs</div>
      <div class="tech-pills">
        <span class="pill p-backend">FastAPI</span>
        <span class="pill p-backend">Streamlit</span>
        <span class="pill p-backend">Gradio</span>
        <span class="pill p-backend">Spring Boot</span>
        <span class="pill p-backend">MySQL</span>
      </div>
    </div>

    <br/>
    <div class="tech-section">
      <div class="tech-label">⚙️ DevOps & Cloud</div>
      <div class="tech-pills">
        <span class="pill p-devops">Docker</span>
        <span class="pill p-devops">AWS</span>
        <span class="pill p-devops">Git</span>
        <span class="pill p-devops">Arduino</span>
      </div>
    </div>

    <br/>
    <div class="tech-section">
      <div class="tech-label">💻 Languages</div>
      <div class="tech-pills">
        <span class="pill p-lang">C</span>
        <span class="pill p-lang">C++</span>
        <span class="pill p-lang">Java</span>
      </div>
    </div>
  </div>

  <!-- SKILL BARS -->
  <div class="section">
    <div class="section-title"><span>💡</span> What I Do Best</div>
    <div class="code-block">
      <div id="skills"></div>
    </div>
  </div>

  <!-- GITHUB STATS -->
  <div class="section">
    <div class="section-title"><span>📊</span> GitHub Statistics</div>
    <div class="stats-grid">
      <div class="stat-card">
        <img src="https://github-readme-stats.vercel.app/api?username=pavandoddavarapu&show_icons=true&theme=radical&hide_border=true&count_private=true&bg_color=161b22" alt="Stats"/>
      </div>
      <div class="stat-card">
        <img src="https://github-readme-streak-stats.herokuapp.com?user=pavandoddavarapu&theme=radical&hide_border=true&background=161b22" alt="Streak"/>
      </div>
    </div>
    <br/>
    <div style="text-align:center;">
      <img style="max-width:400px;width:100%;border-radius:12px;" src="https://github-readme-stats.vercel.app/api/top-langs/?username=pavandoddavarapu&theme=radical&hide_border=true&layout=compact&bg_color=161b22" alt="Languages"/>
    </div>
  </div>

  <!-- FOCUS TABLE -->
  <div class="section">
    <div class="section-title"><span>🎯</span> Current Focus</div>
    <table class="focus-table">
      <tr>
        <th>🔭 Working On</th>
        <th>🌱 Learning</th>
        <th>👯 Collaborating</th>
        <th>🤝 Seeking</th>
      </tr>
      <tr>
        <td>Post-Infosys Projects</td>
        <td>Spring Boot</td>
        <td>Medical Imaging AI</td>
        <td>Full Stack Dev</td>
      </tr>
      <tr>
        <td>AI Agent Systems</td>
        <td>DSA Mastery</td>
        <td>CNN Open Source</td>
        <td>React / Node.js</td>
      </tr>
    </table>
  </div>

  <!-- CTA -->
  <div class="section">
    <div class="cta">
      <div class="cta-quote">"The best models aren't just trained — they're engineered with purpose."</div>
      <div style="color:var(--muted);font-size:13px;margin-bottom:24px;position:relative;">
        📧 pavandoddavarapu7@gmail.com
      </div>
      <div class="cta-links">
        <a class="cta-link solid" href="https://drive.google.com/file/d/1WjTnETJvZvnPRNhiOI7LKTrLKdf1kOCV/view?usp=drive_link">📄 Resume</a>
        <a class="cta-link" href="https://linkedin.com/in/pavandoddavarapu">💼 LinkedIn</a>
        <a class="cta-link" href="https://github.com/pavandoddavarapu">🐙 GitHub</a>
      </div>
    </div>
  </div>

</div>

<div class="footer"></div>

<script>
  // Typing animation
  const phrases = [
    "AI / ML Engineer 🤖",
    "Deep Learning Practitioner 🧬",
    "Building Intelligent Agents 🧠",
    "Open Source Contributor 🌟",
    "Code → Impact → Change 🚀"
  ];
  let pi = 0, ci = 0, del = false;
  const el = document.getElementById('typing');
  function type() {
    const cur = phrases[pi];
    if (!del) {
      el.textContent = cur.slice(0, ++ci);
      if (ci === cur.length) { del = true; setTimeout(type, 2000); return; }
    } else {
      el.textContent = cur.slice(0, --ci);
      if (ci === 0) { del = false; pi = (pi+1) % phrases.length; }
    }
    setTimeout(type, del ? 40 : 75);
  }
  type();

  // Skill bars
  const skills = [
    { name: "🧬 Computer Vision", pct: 90 },
    { name: "🤖 AI Agents & LLMs", pct: 82 },
    { name: "📊 Data Science & EDA", pct: 88 },
    { name: "🚀 ML Model Deployment", pct: 75 },
    { name: "🌐 Backend (FastAPI/Spring)", pct: 62 },
    { name: "🔧 DevOps (Docker/AWS)", pct: 55 },
  ];
  const sc = document.getElementById('skills');
  skills.forEach((s, i) => {
    const d = document.createElement('div');
    d.className = 'skill-row';
    d.innerHTML = `
      <div class="skill-header">
        <span class="skill-label">${s.name}</span>
        <span class="skill-pct">${s.pct}%</span>
      </div>
      <div class="bar-bg">
        <div class="bar-fill" style="width:${s.pct}%;animation-delay:${i*0.15}s"></div>
      </div>
    `;
    sc.appendChild(d);
  });
</script>
</body>
</html>
