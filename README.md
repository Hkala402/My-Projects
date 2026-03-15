<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Himanshu Kala — AI Quality Engineer</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@300;400;500;600;700&family=Lora:wght@400;600&display=swap" rel="stylesheet">
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  :root {
    --blue:       #1a56db;
    --blue-light: #e8f0fe;
    --blue-mid:   #3b82f6;
    --navy:       #0f1f3d;
    --white:      #ffffff;
    --offwhite:   #f5f7fa;
    --text:       #1e293b;
    --muted:      #64748b;
    --border:     #dde3ef;
    --tag-bg:     #e8f0fe;
    --tag-color:  #1a56db;
  }

  html { scroll-behavior: smooth; }

  body {
    background: var(--white);
    color: var(--text);
    font-family: 'Plus Jakarta Sans', sans-serif;
    font-weight: 400;
    line-height: 1.7;
    font-size: 16px;
  }

  nav {
    position: fixed; top: 0; left: 0; right: 0; z-index: 100;
    display: flex; align-items: center; justify-content: space-between;
    padding: 1rem 5rem;
    background: rgba(255,255,255,0.96);
    backdrop-filter: blur(10px);
    border-bottom: 1px solid var(--border);
  }
  .nav-logo {
    font-family: 'Lora', serif;
    font-size: 1.15rem; font-weight: 600;
    color: var(--navy); text-decoration: none;
  }
  .nav-logo span { color: var(--blue); }
  .nav-links { display: flex; gap: 2.5rem; list-style: none; }
  .nav-links a {
    color: var(--muted); text-decoration: none;
    font-size: 0.875rem; font-weight: 500;
    transition: color 0.2s;
  }
  .nav-links a:hover { color: var(--blue); }
  .nav-btns { display: flex; gap: 0.6rem; align-items: center; }
  .nav-btn-resume {
    background: var(--navy); color: white;
    padding: 0.4rem 1rem; border-radius: 6px;
    font-size: 0.8rem; font-weight: 600;
    text-decoration: none; transition: background 0.2s;
  }
  .nav-btn-resume:hover { background: #1a3260; }
  .nav-btn-linkedin {
    background: #0077b5; color: white;
    padding: 0.4rem 1rem; border-radius: 6px;
    font-size: 0.8rem; font-weight: 600;
    text-decoration: none; transition: background 0.2s;
  }
  .nav-btn-linkedin:hover { background: #005e93; }
  .nav-btn-contact {
    background: white; color: var(--navy);
    padding: 0.4rem 1rem; border-radius: 6px;
    font-size: 0.8rem; font-weight: 500;
    text-decoration: none; border: 1.5px solid var(--border);
    transition: border-color 0.2s, color 0.2s;
  }
  .nav-btn-contact:hover { border-color: var(--blue); color: var(--blue); }

  #hero {
    min-height: 100vh;
    display: flex; flex-direction: column; justify-content: center;
    padding: 8rem 5rem 4rem;
    background: linear-gradient(135deg, #f0f4ff 0%, #ffffff 60%, #f8faff 100%);
    position: relative; overflow: hidden;
  }
  .hero-blob {
    position: absolute; top: -80px; right: -80px;
    width: 500px; height: 500px;
    background: radial-gradient(circle, #dbeafe 0%, transparent 70%);
    border-radius: 50%; pointer-events: none;
  }
  .hero-blob2 {
    position: absolute; bottom: -100px; left: -60px;
    width: 350px; height: 350px;
    background: radial-gradient(circle, #ede9fe 0%, transparent 70%);
    border-radius: 50%; pointer-events: none;
  }
  .hero-inner { position: relative; max-width: 780px; }
  .hero-badge {
    display: inline-flex; align-items: center; gap: 0.5rem;
    background: var(--tag-bg); color: var(--blue);
    font-size: 0.78rem; font-weight: 600;
    letter-spacing: 0.1em; text-transform: uppercase;
    padding: 0.4rem 1rem; border-radius: 100px;
    margin-bottom: 1.8rem;
    animation: fadeUp 0.5s ease both;
  }
  .badge-dot { width: 6px; height: 6px; background: var(--blue); border-radius: 50%; }
  .hero-name {
    font-family: 'Lora', serif;
    font-size: clamp(2.8rem, 6vw, 5rem);
    font-weight: 600; color: var(--navy);
    line-height: 1.1; letter-spacing: -0.02em;
    animation: fadeUp 0.6s 0.1s ease both;
  }
  .hero-name span { color: var(--blue); }
  .hero-subtitle {
    margin-top: 1rem; font-size: 1.1rem; font-weight: 500;
    color: var(--muted);
    animation: fadeUp 0.6s 0.2s ease both;
  }
  .hero-desc {
    margin-top: 1.2rem; max-width: 560px;
    font-size: 1rem; color: #4b5563;
    animation: fadeUp 0.6s 0.3s ease both;
  }
  .hero-cta {
    margin-top: 2.2rem; display: flex; gap: 1rem; flex-wrap: wrap;
    animation: fadeUp 0.6s 0.4s ease both;
  }
  .btn-primary {
    background: var(--blue); color: #fff;
    padding: 0.75rem 2rem; border-radius: 8px;
    font-size: 0.9rem; font-weight: 600;
    text-decoration: none; transition: background 0.2s, transform 0.15s;
  }
  .btn-primary:hover { background: #1446c0; transform: translateY(-1px); }
  .btn-outline {
    background: white; color: var(--navy);
    padding: 0.75rem 2rem; border-radius: 8px;
    font-size: 0.9rem; font-weight: 500;
    text-decoration: none; border: 1.5px solid var(--border);
    transition: border-color 0.2s, color 0.2s;
  }
  .btn-outline:hover { border-color: var(--blue); color: var(--blue); }
  .btn-resume {
    background: #0f1f3d; color: #fff;
    padding: 0.75rem 1.6rem; border-radius: 8px;
    font-size: 0.9rem; font-weight: 600;
    text-decoration: none; display: inline-flex; align-items: center; gap: 0.45rem;
    transition: background 0.2s, transform 0.15s;
  }
  .btn-resume:hover { background: #1a3260; transform: translateY(-1px); }
  .btn-linkedin {
    background: #0077b5; color: #fff;
    padding: 0.75rem 1.6rem; border-radius: 8px;
    font-size: 0.9rem; font-weight: 600;
    text-decoration: none; display: inline-flex; align-items: center; gap: 0.45rem;
    transition: background 0.2s, transform 0.15s;
  }
  .btn-linkedin:hover { background: #005e93; transform: translateY(-1px); }
  .btn-contact {
    background: white; color: var(--navy);
    padding: 0.75rem 1.6rem; border-radius: 8px;
    font-size: 0.9rem; font-weight: 500;
    text-decoration: none; display: inline-flex; align-items: center; gap: 0.45rem;
    border: 1.5px solid var(--border);
    transition: border-color 0.2s, color 0.2s;
  }
  .btn-contact:hover { border-color: var(--blue); color: var(--blue); }
  .btn-icon { font-size: 0.95rem; }
  .hero-stats {
    display: flex; gap: 3rem; margin-top: 4rem;
    padding-top: 2.5rem; border-top: 1px solid var(--border);
    animation: fadeUp 0.6s 0.5s ease both;
  }
  .stat-num { font-family: 'Lora', serif; font-size: 2rem; font-weight: 600; color: var(--blue); }
  .stat-label { font-size: 0.78rem; font-weight: 500; color: var(--muted); letter-spacing: 0.05em; text-transform: uppercase; margin-top: 0.15rem; }

  section { padding: 5.5rem 5rem; }
  .section-inner { max-width: 1000px; margin: 0 auto; }
  .section-label { font-size: 0.75rem; font-weight: 700; letter-spacing: 0.15em; text-transform: uppercase; color: var(--blue); margin-bottom: 0.4rem; }
  .section-title { font-family: 'Lora', serif; font-size: 2rem; font-weight: 600; color: var(--navy); }
  .title-underline { width: 48px; height: 3px; background: var(--blue); border-radius: 2px; margin-top: 0.5rem; margin-bottom: 3rem; }

  #about { background: var(--white); }
  .about-grid { display: grid; grid-template-columns: 1.1fr 0.9fr; gap: 4rem; align-items: start; }
  .about-text p { color: #4b5563; margin-bottom: 1.1rem; font-size: 1rem; }
  .contact-list { margin-top: 1.5rem; display: flex; flex-direction: column; gap: 0.7rem; }
  .contact-row {
    display: flex; align-items: center; gap: 1rem;
    padding: 0.6rem 1rem;
    background: var(--offwhite); border-radius: 8px;
  }
  .contact-icon { font-size: 1rem; width: 20px; text-align: center; }
  .contact-label { font-size: 0.78rem; font-weight: 600; color: var(--muted); text-transform: uppercase; letter-spacing: 0.06em; min-width: 55px; }
  .contact-val { font-size: 0.9rem; color: var(--text); }
  .highlight-cards { display: flex; flex-direction: column; gap: 1rem; }
  .h-card {
    background: var(--white); border: 1px solid var(--border);
    border-radius: 12px; padding: 1.2rem 1.4rem;
    display: flex; gap: 1rem; align-items: flex-start;
    transition: border-color 0.2s, box-shadow 0.2s;
  }
  .h-card:hover { border-color: var(--blue-mid); box-shadow: 0 2px 16px rgba(26,86,219,0.07); }
  .h-card-icon {
    width: 36px; height: 36px; flex-shrink: 0;
    background: var(--tag-bg); border-radius: 8px;
    display: flex; align-items: center; justify-content: center; font-size: 1rem;
  }
  .h-card h4 { font-size: 0.92rem; font-weight: 600; color: var(--navy); margin-bottom: 0.2rem; }
  .h-card p { font-size: 0.83rem; color: var(--muted); }

  #skills { background: var(--offwhite); }
  .skills-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 1.5rem; }
  .skill-box { background: var(--white); border: 1px solid var(--border); border-radius: 12px; padding: 1.5rem; }
  .skill-box-title { font-size: 0.78rem; font-weight: 700; letter-spacing: 0.1em; text-transform: uppercase; color: var(--blue); margin-bottom: 1rem; padding-bottom: 0.7rem; border-bottom: 1px solid var(--border); }
  .skill-tags { display: flex; flex-wrap: wrap; gap: 0.5rem; }
  .skill-tag { background: var(--tag-bg); color: var(--tag-color); font-size: 0.78rem; font-weight: 500; padding: 0.3rem 0.85rem; border-radius: 100px; transition: background 0.2s; }
  .skill-tag:hover { background: #c7d9fd; }

  #experience { background: var(--white); }
  .exp-item {
    display: grid; grid-template-columns: 220px 1fr; gap: 2rem;
    padding: 2rem 0; border-bottom: 1px solid var(--border);
  }
  .exp-item:last-child { border-bottom: none; }
  .exp-period { display: inline-block; background: var(--tag-bg); color: var(--blue); font-size: 0.75rem; font-weight: 600; padding: 0.3rem 0.8rem; border-radius: 100px; margin-bottom: 0.6rem; }
  .exp-company-name { font-size: 0.9rem; font-weight: 600; color: var(--navy); }
  .exp-company-type { font-size: 0.8rem; color: var(--muted); margin-top: 0.1rem; }
  .exp-role { font-size: 1.1rem; font-weight: 600; color: var(--navy); margin-bottom: 0.8rem; }
  .exp-list { display: flex; flex-direction: column; gap: 0.45rem; list-style: none; }
  .exp-list li { display: flex; gap: 0.7rem; font-size: 0.9rem; color: #4b5563; }
  .exp-list li::before { content: ''; width: 6px; height: 6px; flex-shrink: 0; background: var(--blue); border-radius: 50%; margin-top: 0.55rem; }

  #projects { background: var(--offwhite); }
  .projects-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 1.5rem; margin-bottom: 2.5rem; }
  .project-card {
    background: var(--white); border: 1px solid var(--border);
    border-radius: 12px; padding: 1.8rem;
    transition: border-color 0.2s, box-shadow 0.2s;
  }
  .project-card:hover { border-color: var(--blue-mid); box-shadow: 0 4px 20px rgba(26,86,219,0.08); }
  .project-chip { display: inline-block; background: var(--tag-bg); color: var(--blue); font-size: 0.72rem; font-weight: 700; letter-spacing: 0.1em; text-transform: uppercase; padding: 0.25rem 0.75rem; border-radius: 100px; margin-bottom: 0.8rem; }
  .project-title { font-size: 1rem; font-weight: 700; color: var(--navy); margin-bottom: 0.5rem; }
  .project-desc { font-size: 0.86rem; color: var(--muted); margin-bottom: 1rem; }
  .project-list { list-style: none; display: flex; flex-direction: column; gap: 0.35rem; }
  .project-list li { display: flex; gap: 0.6rem; font-size: 0.84rem; color: #4b5563; }
  .project-list li::before { content: '→'; color: var(--blue); flex-shrink: 0; }

  .ach-grid { display: grid; grid-template-columns: repeat(2, 1fr); gap: 1rem; }
  .ach-card { background: var(--white); border: 1px solid var(--border); border-radius: 12px; padding: 1.2rem 1.4rem; display: flex; gap: 1rem; align-items: flex-start; }
  .ach-num { width: 32px; height: 32px; flex-shrink: 0; background: var(--blue); color: white; border-radius: 8px; display: flex; align-items: center; justify-content: center; font-size: 0.78rem; font-weight: 700; }
  .ach-text { font-size: 0.88rem; color: #4b5563; }

  footer {
    background: var(--navy); padding: 2.5rem 5rem;
    display: flex; align-items: center; justify-content: space-between;
  }
  .footer-logo { font-family: 'Lora', serif; font-size: 1.1rem; color: white; font-weight: 600; }
  .footer-logo span { color: #60a5fa; }
  .footer-right { font-size: 0.82rem; color: #94a3b8; }

  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(18px); }
    to   { opacity: 1; transform: translateY(0); }
  }

  @media (max-width: 900px) {
    nav, #hero, section, footer { padding-left: 1.5rem; padding-right: 1.5rem; }
    .nav-links { display: none; }
    .about-grid, .skills-grid, .projects-grid, .ach-grid { grid-template-columns: 1fr; }
    .exp-item { grid-template-columns: 1fr; gap: 0.5rem; }
    .hero-stats { gap: 1.5rem; flex-wrap: wrap; }
    footer { flex-direction: column; gap: 0.5rem; text-align: center; }
  }
</style>
</head>
<body>

<nav>
  <a href="#hero" class="nav-logo">Himanshu <span>Kala</span></a>
  <ul class="nav-links">
    <li><a href="#about">About</a></li>
    <li><a href="#skills">Skills</a></li>
    <li><a href="#experience">Experience</a></li>
    <li><a href="#projects">Projects</a></li>
  </ul>
  <div class="nav-btns">
    <a href="Himanshu_Kala_Resume.pdf" download class="nav-btn-resume">📄 Resume</a>
    <a href="https://www.linkedin.com/in/" target="_blank" class="nav-btn-linkedin">💼 LinkedIn</a>
    <a href="mailto:hkala402@gmail.com" class="nav-btn-contact">✉️ Contact</a>
  </div>
</nav>

<section id="hero">
  <div class="hero-blob"></div>
  <div class="hero-blob2"></div>
  <div class="hero-inner">
    <div class="hero-badge"><span class="badge-dot"></span> Open to Opportunities</div>
    <h1 class="hero-name">Himanshu<br><span>Kala</span></h1>
    <p class="hero-subtitle">AI Quality Assurance Engineer · LLM Evaluation · AI Safety</p>
    <p class="hero-desc">Specializing in GPT-style LLM evaluation, hallucination detection, and AI safety validation. Ensuring reliable, safe, and high-performance AI products through rigorous testing.</p>
    <div class="hero-cta">
      <a href="Himanshu_Kala_Resume.pdf" download class="btn-resume"><span class="btn-icon">📄</span> Resume</a>
      <a href="https://www.linkedin.com/in/" target="_blank" class="btn-linkedin"><span class="btn-icon">💼</span> LinkedIn</a>
      <a href="mailto:hkala402@gmail.com" class="btn-contact"><span class="btn-icon">✉️</span> Contact</a>
    </div>
    <div class="hero-stats">
      <div><div class="stat-num">2+</div><div class="stat-label">Years Experience</div></div>
      <div><div class="stat-num">300+</div><div class="stat-label">Responses / Week</div></div>
      <div><div class="stat-num">AI</div><div class="stat-label">Safety Focused</div></div>
    </div>
  </div>
</section>

<section id="about">
  <div class="section-inner">
    <p class="section-label">Who I Am</p>
    <h2 class="section-title">About Me</h2>
    <div class="title-underline"></div>
    <div class="about-grid">
      <div class="about-text">
        <p>I'm an AI-focused Quality Assurance Engineer with over 2 years of experience in manual and automation testing, with deep specialization in GPT-style LLM evaluation and AI safety validation.</p>
        <p>My work sits at the intersection of AI quality and safety — I help ensure that conversational AI systems behave accurately, ethically, and reliably before they reach real users.</p>
        <p>From hallucination detection to adversarial prompt design, I test the edges of AI systems so they're ready for the real world. I thrive in Agile environments and collaborate closely with cross-functional teams.</p>
        <div class="contact-list">
          <div class="contact-row"><span class="contact-icon">📞</span><span class="contact-label">Phone</span><span class="contact-val">+91 7417517798</span></div>
          <div class="contact-row"><span class="contact-icon">✉️</span><span class="contact-label">Email</span><span class="contact-val"><a href="mailto:hkala402@gmail.com" style="color:var(--blue);text-decoration:none;">hkala402@gmail.com</a></span></div>
          <div class="contact-row"><span class="contact-icon">📍</span><span class="contact-label">Location</span><span class="contact-val">Meerut, India</span></div>
        </div>
      </div>
      <div class="highlight-cards">
        <div class="h-card"><div class="h-card-icon">🤖</div><div><h4>LLM Evaluation Specialist</h4><p>Validating 300+ model responses weekly for accuracy, relevance & logical consistency.</p></div></div>
        <div class="h-card"><div class="h-card-icon">🛡️</div><div><h4>AI Safety Engineer</h4><p>Systematic detection of harmful, biased, and policy-violating AI outputs.</p></div></div>
        <div class="h-card"><div class="h-card-icon">⚡</div><div><h4>Adversarial Prompt Designer</h4><p>Structured edge-case prompting to stress-test conversational AI robustness.</p></div></div>
        <div class="h-card"><div class="h-card-icon">🔗</div><div><h4>API & Automation Tester</h4><p>REST API validation using Postman across authentication, payloads, and error handling.</p></div></div>
      </div>
    </div>
  </div>
</section>

<section id="skills">
  <div class="section-inner">
    <p class="section-label">What I Know</p>
    <h2 class="section-title">Skills & Expertise</h2>
    <div class="title-underline"></div>
    <div class="skills-grid">
      <div class="skill-box">
        <div class="skill-box-title">AI & LLM Testing</div>
        <div class="skill-tags">
          <span class="skill-tag">GPT-style LLM Evaluation</span>
          <span class="skill-tag">Hallucination Detection</span>
          <span class="skill-tag">AI Safety Evaluation</span>
          <span class="skill-tag">Harmful Content Detection</span>
          <span class="skill-tag">LLM Validation</span>
          <span class="skill-tag">Conversational AI Testing</span>
          <span class="skill-tag">Prompt Testing</span>
          <span class="skill-tag">Manual Response Validation</span>
        </div>
      </div>
      <div class="skill-box">
        <div class="skill-box-title">Testing Methodologies</div>
        <div class="skill-tags">
          <span class="skill-tag">Manual Testing</span>
          <span class="skill-tag">End-to-End Testing</span>
          <span class="skill-tag">Smoke & Sanity Testing</span>
          <span class="skill-tag">Regression Testing</span>
          <span class="skill-tag">Test Case Design</span>
          <span class="skill-tag">Defect Lifecycle</span>
          <span class="skill-tag">Agile / Scrum</span>
        </div>
      </div>
      <div class="skill-box">
        <div class="skill-box-title">Tools & Platforms</div>
        <div class="skill-tags">
          <span class="skill-tag">Postman</span>
          <span class="skill-tag">JIRA</span>
          <span class="skill-tag">LogRocket</span>
          <span class="skill-tag">Relay</span>
          <span class="skill-tag">Retool</span>
          <span class="skill-tag">Slack</span>
          <span class="skill-tag">SQL</span>
        </div>
      </div>
    </div>
  </div>
</section>

<section id="experience">
  <div class="section-inner">
    <p class="section-label">Where I've Worked</p>
    <h2 class="section-title">Work Experience</h2>
    <div class="title-underline"></div>
    <div class="exp-item">
      <div>
        <div class="exp-period">Oct 2023 – Present</div>
        <div class="exp-company-name">Simublade Technology</div>
        <div class="exp-company-type">AI Products Company</div>
      </div>
      <div>
        <div class="exp-role">Associate QA Engineer</div>
        <ul class="exp-list">
          <li>Conduct GPT-style LLM evaluation — validating 300+ model responses weekly for contextual relevance, factual accuracy, and logical consistency.</li>
          <li>Perform hallucination detection to identify fabricated and misleading AI outputs, reducing model response defects during regression cycles.</li>
          <li>Execute AI safety testing to detect unsafe, harmful, biased, or policy-violating responses.</li>
          <li>Design structured, adversarial, and edge-case prompts to test robustness of conversational AI systems.</li>
          <li>Conduct regression testing after model updates to ensure stability and performance consistency.</li>
          <li>Perform REST API testing using Postman — validating payloads, authentication, status codes, and error handling.</li>
          <li>Validate AI-powered video transformation pipelines ensuring lip-sync, facial alignment, and voice accuracy.</li>
          <li>Collaborate with cross-functional teams in Agile/Scrum environment to deliver AI-driven features.</li>
        </ul>
      </div>
    </div>
  </div>
</section>

<section id="projects">
  <div class="section-inner">
    <p class="section-label">What I've Built & Achieved</p>
    <h2 class="section-title">Projects & Achievements</h2>
    <div class="title-underline"></div>
    <div class="projects-grid">
      <div class="project-card">
        <div class="project-chip">Featured Project</div>
        <div class="project-title">AI Video Automation — Tavus AI Integration</div>
        <p class="project-desc">End-to-end QA for AI-powered video personalization workflows using the Tavus platform and Phoenix AI model.</p>
        <ul class="project-list">
          <li>Tested AI-based video personalization converting raw inputs into personalized videos.</li>
          <li>Validated Phoenix AI model outputs for facial expression realism and speech synchronization.</li>
          <li>Regression testing for conversational AI modules and digital avatar systems.</li>
          <li>Ensured performance stability across AI deployment updates.</li>
        </ul>
      </div>
      <div class="project-card">
        <div class="project-chip">Conversational AI</div>
        <div class="project-title">Digital Human Interaction Testing</div>
        <p class="project-desc">Comprehensive validation of digital human and conversational AI interaction systems for production reliability.</p>
        <ul class="project-list">
          <li>Performed end-to-end testing of conversational AI workflows.</li>
          <li>Validated digital avatar lip-sync and voice accuracy pipelines.</li>
          <li>Ensured high response accuracy standards before production deployment.</li>
        </ul>
      </div>
    </div>
    <div class="ach-grid">
      <div class="ach-card"><div class="ach-num">01</div><div class="ach-text">Improved AI response validation efficiency by implementing a structured prompt testing strategy across teams.</div></div>
      <div class="ach-card"><div class="ach-num">02</div><div class="ach-text">Strengthened AI safety compliance through systematic harmful-content detection workflows.</div></div>
      <div class="ach-card"><div class="ach-num">03</div><div class="ach-text">Recognized for analytical debugging skills and proactive communication during AI product releases.</div></div>
      <div class="ach-card"><div class="ach-num">04</div><div class="ach-text">Consistently ensured high model response accuracy and safety before every production deployment.</div></div>
    </div>
  </div>
</section>

<footer>
  <div class="footer-logo">Himanshu <
