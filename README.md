<!doctype html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width,initial-scale=1">
<title>Uswa Arooj — Cyber Security Engineer</title>
<style>
:root{
  --black:#07080a;
  --ink:#0c0e12;
  --card:#111419;
  --card2:#15191f;
  --gold:#c8a96b;
  --gold2:#ead49b;
  --violet:#9b7bb7;
  --white:#f5f2eb;
  --muted:#969ba5;
  --line:#272b31;
}
*{box-sizing:border-box}
html{scroll-behavior:smooth}
body{
 margin:0;background:var(--black);color:var(--white);
 font-family:Inter,Arial,sans-serif;line-height:1.65;
}
a{text-decoration:none;color:inherit}
.wrap{width:min(1180px,calc(100% - 44px));margin:auto}

/* HERO */
.hero{
 min-height:100vh;position:relative;overflow:hidden;
 display:flex;align-items:center;
 border-bottom:1px solid var(--line);
 background:
   radial-gradient(ellipse at 80% 25%,rgba(155,123,183,.12),transparent 32%),
   radial-gradient(ellipse at 15% 80%,rgba(200,169,107,.07),transparent 30%),
   #07080a;
}
.hero-grid{
 position:absolute;inset:0;opacity:.28;
 background-image:
  linear-gradient(rgba(200,169,107,.035) 1px,transparent 1px),
  linear-gradient(90deg,rgba(200,169,107,.035) 1px,transparent 1px);
 background-size:72px 72px;
 mask-image:linear-gradient(to right,transparent,#000 35%,#000 70%,transparent);
}
.orbit{
 position:absolute;width:620px;height:620px;right:-170px;top:50%;
 transform:translateY(-50%);border:1px solid rgba(200,169,107,.12);
 border-radius:50%;box-shadow:0 0 100px rgba(155,123,183,.08);
}
.orbit:before,.orbit:after{
 content:"";position:absolute;border:1px solid rgba(155,123,183,.10);
 border-radius:50%;inset:70px;transform:rotate(35deg) scaleX(1.5);
}
.orbit:after{inset:160px;transform:rotate(-25deg) scaleX(1.6)}
.hero-content{position:relative;z-index:2;max-width:820px;padding:80px 0}
.kicker{
 color:var(--gold2);font:600 11px/1.2 ui-monospace,Consolas,monospace;
 letter-spacing:.22em;text-transform:uppercase;margin-bottom:28px;
}
h1{
 margin:0;font-family:Georgia,"Times New Roman",serif;
 font-weight:400;font-size:clamp(64px,9vw,126px);
 letter-spacing:-.065em;line-height:.82;
}
.name-line{display:block}
.name-line:last-child{color:var(--gold)}
.role{
 margin:34px 0 0;padding-left:18px;border-left:2px solid var(--gold);
 font-size:15px;letter-spacing:.12em;text-transform:uppercase;color:#d5d1ca;
}
.hero-copy{max-width:680px;color:var(--muted);font-size:17px;margin-top:24px}
.actions{display:flex;gap:12px;flex-wrap:wrap;margin-top:34px}
.btn{
 border:1px solid var(--gold);padding:11px 19px;
 font:600 11px ui-monospace,monospace;letter-spacing:.14em;
 color:var(--gold2);background:transparent;
}
.btn.primary{background:var(--gold);color:#111}
.btn:hover{box-shadow:0 0 25px rgba(200,169,107,.18)}
.meta{display:flex;gap:28px;margin-top:48px;flex-wrap:wrap}
.meta-item{border-left:1px solid var(--line);padding-left:14px}
.meta b{display:block;color:var(--gold2);font:700 10px ui-monospace,monospace;letter-spacing:.12em}
.meta span{color:var(--muted);font-size:12px}

/* SECTIONS */
section{padding:105px 0;border-bottom:1px solid var(--line)}
.section-head{display:flex;justify-content:space-between;gap:30px;align-items:flex-end;margin-bottom:42px}
.index{color:var(--gold);font:700 11px ui-monospace,monospace;letter-spacing:.18em}
h2{
 margin:8px 0 0;font:400 clamp(34px,5vw,58px)/1 Georgia,"Times New Roman",serif;
 letter-spacing:-.04em;
}
.intro{max-width:640px;color:var(--muted);font-size:15px}

/* ABOUT */
.about{display:grid;grid-template-columns:1.15fr .85fr;gap:70px}
.quote{
 border-top:1px solid var(--gold);border-bottom:1px solid var(--line);
 padding:28px 0;font:400 25px/1.35 Georgia,serif;color:#ded8ce;
}
.signature{margin-top:22px;color:var(--gold);font:10px ui-monospace,monospace;letter-spacing:.16em}

/* CARDS */
.cards{display:grid;grid-template-columns:repeat(3,1fr);gap:16px}
.card{
 background:linear-gradient(145deg,var(--card2),var(--card));
 border:1px solid var(--line);padding:27px;min-height:205px;
 position:relative;overflow:hidden;
}
.card:after{
 content:"";position:absolute;width:90px;height:1px;left:27px;top:0;
 background:linear-gradient(90deg,var(--gold),transparent);
}
.card-no{position:absolute;right:20px;top:18px;color:#41454d;font:10px ui-monospace,monospace}
.card h3{font:600 13px/1.4 Inter,Arial,sans-serif;letter-spacing:.1em;color:var(--gold2);margin:15px 0}
.card p{font-size:13px;color:var(--muted);margin:0}
.tags{display:flex;flex-wrap:wrap;gap:6px;margin-top:18px}
.tag{border:1px solid #30343b;color:#aaa6a0;padding:4px 7px;font:9px ui-monospace,monospace}

/* PROJECT FEATURE */
.project-list{display:grid;grid-template-columns:1fr 1fr;gap:1px;background:var(--line);border:1px solid var(--line)}
.project{
 background:var(--card);padding:30px;min-height:190px;
}
.project h3{font:500 20px Georgia,serif;color:var(--white);margin:8px 0 10px}
.project .alias{font:9px ui-monospace,monospace;color:var(--gold);letter-spacing:.15em}
.project p{font-size:13px;color:var(--muted);max-width:480px}
.project:hover{background:#14171c}

/* SKILLS */
.skill-layout{display:grid;grid-template-columns:1fr 1fr;gap:18px}
.skill-box{background:var(--card);border:1px solid var(--line);padding:28px}
.skill-box h3{font:11px ui-monospace,monospace;letter-spacing:.16em;color:var(--gold);margin:0 0 20px}
.pills{display:flex;flex-wrap:wrap;gap:8px}
.pill{background:#0b0d10;border:1px solid #2a2e35;padding:8px 10px;color:#c7c5c0;font:11px ui-monospace,monospace}

/* EXPERIENCE */
.timeline{max-width:900px;border-left:1px solid #333;margin-top:20px}
.job{padding:0 0 48px 35px;position:relative}
.job:before{content:"";position:absolute;left:-4px;top:6px;width:7px;height:7px;border-radius:50%;background:var(--gold)}
.job .date{color:var(--gold);font:9px ui-monospace,monospace;letter-spacing:.15em}
.job h3{margin:8px 0 4px;font:500 21px Georgia,serif}
.job p{margin:0;color:var(--muted);font-size:13px}

/* DIRECTION */
.direction{
 background:linear-gradient(110deg,#0e0f12,#151119 55%,#0d0e11);
}
.flow{display:grid;grid-template-columns:repeat(6,1fr);border:1px solid var(--line);margin-top:35px}
.flow div{padding:24px 8px;text-align:center;border-right:1px solid var(--line);font:9px ui-monospace,monospace;color:#c8c0b5}
.flow div:last-child{border:0}
.flow strong{display:block;color:var(--gold);font-size:15px;margin-bottom:9px}

/* FOOTER */
footer{padding:85px 0;text-align:center}
footer h2{color:var(--gold)}
footer p{color:var(--muted)}
.footline{margin-top:35px;color:#565a62;font:9px ui-monospace,monospace;letter-spacing:.16em}

@media(max-width:850px){
 .about,.skill-layout{grid-template-columns:1fr}
 .cards{grid-template-columns:1fr}
 .project-list{grid-template-columns:1fr}
 .flow{grid-template-columns:repeat(3,1fr)}
 .flow div:nth-child(3){border-right:0}
}
@media(max-width:600px){
 .wrap{width:min(100% - 28px,1180px)}
 .hero-content{padding:65px 0}
 .orbit{opacity:.45;right:-350px}
 section{padding:75px 0}
 .section-head{display:block}
 .flow{grid-template-columns:1fr 1fr}
 .flow div{border-bottom:1px solid var(--line)}
 .flow div:nth-child(2n){border-right:0}
 .meta{gap:16px}
}
</style>
</head>
<body>

<header class="hero">
<div class="hero-grid"></div><div class="orbit"></div>
<div class="wrap">
<div class="hero-content">
<div class="kicker">Cyber Security / AI Automation / Security Research</div>
<h1><span class="name-line">USWA</span><span class="name-line">AROOJ</span></h1>
<div class="role">Cyber Security Engineer &nbsp;|&nbsp; AI Automation Engineer</div>
<p class="hero-copy">I design and build practical security, intelligence and automation systems — combining cybersecurity, AI, OSINT and modern engineering.</p>
<div class="actions">
<a class="btn primary" href="https://github.com/Uswarooj">VIEW GITHUB</a>
<a class="btn" href="https://www.linkedin.com/in/ruthlesseagle">LINKEDIN</a>
</div>
<div class="meta">
<div class="meta-item"><b>FOCUS</b><span>Security + AI</span></div>
<div class="meta-item"><b>BUILD</b><span>Automation Systems</span></div>
<div class="meta-item"><b>RESEARCH</b><span>OSINT / Security</span></div>
<div class="meta-item"><b>STACK</b><span>Python / TypeScript</span></div>
</div>
</div>
</div>
</header>

<section>
<div class="wrap">
<div class="section-head"><div><div class="index">01 — PROFILE</div><h2>Engineering with<br>security in mind.</h2></div></div>
<div class="about">
<div>
<p class="intro">I am a Cyber Security Engineer and AI Automation Engineer focused on practical systems across cybersecurity, artificial intelligence, automation, OSINT and modern software engineering.</p>
<p class="intro">My work includes security research, security automation, Python tooling, OSINT systems, web scraping, AI-assisted workflows, intelligent search systems, business automation, web applications, APIs and SaaS systems.</p>
<p class="intro">I turn complex and repetitive processes into workflows that are automated, intelligent, reliable and security-conscious.</p>
</div>
<div>
<div class="quote">“The goal is not to automate everything. The goal is to build systems that know what should be automated.”</div>
<div class="signature">USWA AROOJ / ENGINEERING APPROACH</div>
</div>
</div>
</div>
</section>

<section>
<div class="wrap">
<div class="section-head"><div><div class="index">02 — EXPERTISE</div><h2>Three disciplines.<br>One direction.</h2></div></div>
<div class="cards">
<div class="card"><span class="card-no">01</span><h3>SECURITY ENGINEERING</h3><p>Security research, web application security, vulnerability assessment, network security, security testing, secure SDLC and security automation.</p><div class="tags"><span class="tag">WEB SECURITY</span><span class="tag">VULNERABILITY</span><span class="tag">RESEARCH</span></div></div>
<div class="card"><span class="card-no">02</span><h3>AI & AUTOMATION</h3><p>AI agents, intelligent workflows, research automation, LLM workflows, business automation and API-driven systems.</p><div class="tags"><span class="tag">AI AGENTS</span><span class="tag">LLM</span><span class="tag">WORKFLOWS</span></div></div>
<div class="card"><span class="card-no">03</span><h3>INTELLIGENCE</h3><p>OSINT, threat intelligence, web research, information gathering, search automation and public-data processing.</p><div class="tags"><span class="tag">OSINT</span><span class="tag">THREAT INTEL</span><span class="tag">DATA</span></div></div>
</div>
</div>
</section>

<section>
<div class="wrap">
<div class="section-head"><div><div class="index">03 — SELECTED WORK</div><h2>Systems I have<br>worked on.</h2></div><p class="intro">Professional/company-owned projects are represented with portfolio aliases. Proprietary code and internal information remain private.</p></div>
<div class="project-list">
<div class="project"><div class="alias">AI / AUTOMATION</div><h3>Agency Intelligence Copilot</h3><p>AI-assisted system for agency operations, customer workflows and repetitive business processes.</p><div class="tags"><span class="tag">TYPESCRIPT</span><span class="tag">AI</span><span class="tag">AUTOMATION</span></div></div>
<div class="project"><div class="alias">SEARCH / DATA</div><h3>Intelligent Search Platform</h3><p>Search-oriented system for information discovery, automated processing and intelligent workflows.</p><div class="tags"><span class="tag">TYPESCRIPT</span><span class="tag">SEARCH</span><span class="tag">DATA</span></div></div>
<div class="project"><div class="alias">SEARCH / AUTOMATION</div><h3>Search & Discovery Engine</h3><p>Information-processing workflow designed around automated search and operational data processing.</p><div class="tags"><span class="tag">TYPESCRIPT</span><span class="tag">SEARCH</span></div></div>
<div class="project"><div class="alias">OSINT / PYTHON</div><h3>Speaker Intelligence Pipeline</h3><p>Python automation for researching publicly available speaker, event and professional information.</p><div class="tags"><span class="tag">PYTHON</span><span class="tag">OSINT</span></div></div>
<div class="project"><div class="alias">OSINT / RESEARCH</div><h3>Professional Intelligence Mapper</h3><p>Automation workflow for discovering and organizing publicly available professional information.</p><div class="tags"><span class="tag">PYTHON</span><span class="tag">OSINT</span></div></div>
<div class="project"><div class="alias">SOCIAL / INTELLIGENCE</div><h3>Social Intelligence Pipeline</h3><p>Public-data workflow for discovering relevant social content and processing engagement information.</p><div class="tags"><span class="tag">SCRAPING</span><span class="tag">OSINT</span></div></div>
<div class="project"><div class="alias">WEB / APPLICATION</div><h3>Healthcare Operations Platform</h3><p>Modern web application developed within a healthcare and business-oriented environment.</p><div class="tags"><span class="tag">JAVASCRIPT</span><span class="tag">WEB APP</span><span class="tag">API</span></div></div>
</div>
</div>
</section>

<section>
<div class="wrap">
<div class="section-head"><div><div class="index">04 — CYBERSECURITY</div><h2>Security toolkit.</h2></div></div>
<div class="skill-layout">
<div class="skill-box"><h3>SECURITY DOMAINS</h3><div class="pills"><span class="pill">Web Application Security</span><span class="pill">Vulnerability Assessment</span><span class="pill">Security Research</span><span class="pill">Security Automation</span><span class="pill">Network Security</span><span class="pill">Threat Intelligence</span><span class="pill">OSINT</span><span class="pill">Incident Response</span><span class="pill">Digital Forensics</span><span class="pill">AI Security</span><span class="pill">DevSecOps</span></div></div>
<div class="skill-box"><h3>TOOLS</h3><div class="pills"><span class="pill">Kali Linux</span><span class="pill">Nmap</span><span class="pill">Burp Suite</span><span class="pill">Wireshark</span><span class="pill">Metasploit</span><span class="pill">OWASP ZAP</span><span class="pill">OpenVAS</span><span class="pill">Snort</span><span class="pill">Aircrack-ng</span><span class="pill">Sysinternals</span></div></div>
</div>
</div>
</section>

<section>
<div class="wrap">
<div class="section-head"><div><div class="index">05 — AI / AUTOMATION</div><h2>Intelligence that<br>moves workflows.</h2></div></div>
<div class="skill-layout">
<div class="skill-box"><h3>AI SYSTEMS</h3><div class="pills"><span class="pill">AI Agents</span><span class="pill">AI Automation</span><span class="pill">AI-assisted Workflows</span><span class="pill">Prompt Engineering</span><span class="pill">LLM Workflows</span><span class="pill">Multi-Agent Research</span></div></div>
<div class="skill-box"><h3>AUTOMATION</h3><div class="pills"><span class="pill">Research Automation</span><span class="pill">Business Automation</span><span class="pill">API Automation</span><span class="pill">Data Processing</span><span class="pill">Intelligent Search</span><span class="pill">Workflow Orchestration</span></div></div>
</div>
</div>
</section>

<section>
<div class="wrap">
<div class="section-head"><div><div class="index">06 — TECHNOLOGY</div><h2>Technical stack.</h2></div></div>
<div class="skill-box">
<div class="pills">
<span class="pill">Python</span><span class="pill">TypeScript</span><span class="pill">JavaScript</span><span class="pill">SQL</span><span class="pill">React</span><span class="pill">Node.js</span><span class="pill">Express.js</span><span class="pill">MongoDB</span><span class="pill">REST APIs</span><span class="pill">Vercel</span><span class="pill">Git</span><span class="pill">GitHub</span><span class="pill">VS Code</span><span class="pill">Postman</span><span class="pill">Linux</span><span class="pill">Windows</span>
</div>
</div>
</div>
</section>

<section>
<div class="wrap">
<div class="section-head"><div><div class="index">07 — EXPERIENCE</div><h2>Professional<br>trajectory.</h2></div></div>
<div class="timeline">
<div class="job"><div class="date">CURRENT</div><h3>Cyber Security Engineer | AI Automation Engineer</h3><p>Security research, security automation, AI-powered workflows, Python scripting, OSINT, web scraping, testing, architecture and technical documentation.</p></div>
<div class="job"><div class="date">LEADERSHIP</div><h3>Technical Team Lead</h3><p>Technical coordination across development workflows, testing, automation and project delivery.</p></div>
<div class="job"><div class="date">EDUCATION</div><h3>Coding & AI Instructor</h3><p>Teaching programming and AI concepts through practical, project-based learning.</p></div>
<div class="job"><div class="date">DESIGN</div><h3>Junior Pitch Deck Designer</h3><p>Pitch deck and presentation design combining visual communication, business storytelling and technical presentation.</p></div>
</div>
</div>
</section>

<section class="direction">
<div class="wrap">
<div class="section-head"><div><div class="index">08 — DIRECTION</div><h2>The intersection<br>I'm building toward.</h2></div></div>
<div class="flow">
<div><strong>01</strong>CYBERSECURITY</div>
<div><strong>02</strong>SECURITY AUTOMATION</div>
<div><strong>03</strong>AI SECURITY</div>
<div><strong>04</strong>DETECTION ENGINEERING</div>
<div><strong>05</strong>CLOUD SECURITY</div>
<div><strong>06</strong>AI AGENTS</div>
</div>
</div>
</section>

<footer>
<div class="wrap">
<div class="index">09 — CONNECT</div>
<h2>CYBERSECURITY × AI × AUTOMATION</h2>
<p>Building. Automating. Securing.</p>
<div class="actions" style="justify-content:center">
<a class="btn primary" href="https://github.com/Uswarooj">GITHUB</a>
<a class="btn" href="https://www.linkedin.com/in/ruthlesseagle">LINKEDIN</a>
</div>
<div class="footline">USWA AROOJ / CYBER SECURITY ENGINEER / AI AUTOMATION ENGINEER</div>
</div>
</footer>
</body>
</html>
