<!DOCTYPE html>
<html>
<head>
  <title>Manoj Royal - AI/ML Engineer</title>
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700;900&family=JetBrains+Mono:wght@300;400;500&display=swap');
    
    * { margin: 0; padding: 0; box-sizing: border-box; }
    body {
      background: linear-gradient(135deg, #0c0c0c 0%, #1a0033 50%, #000428 100%);
      color: #00f7ff;
      font-family: 'JetBrains Mono', monospace;
      overflow-x: hidden;
      min-height: 100vh;
    }
    .container { max-width: 1400px; margin: 0 auto; padding: 0 2rem; }
    
    /* Particle Background */
    .particles {
      position: fixed; top: 0; left: 0; width: 100%; height: 100%; z-index: -1;
      background: radial-gradient(circle at 20% 80%, rgba(120,119,198,0.3) 0%, transparent 50%),
                  radial-gradient(circle at 80% 20%, rgba(255,119,198,0.3) 0%, transparent 50%),
                  radial-gradient(circle at 40% 40%, rgba(120,219,255,0.3) 0%, transparent 50%);
      animation: float 20s ease-in-out infinite;
    }
    @keyframes float { 0%, 100% { transform: translateY(0) rotate(0deg); } 50% { transform: translateY(-20px) rotate(180deg); } }
    
    /* Header */
    .hero {
      text-align: center; padding: 4rem 0; position: relative;
      background: linear-gradient(45deg, rgba(0,247,255,0.1), rgba(255,0,150,0.1));
      border: 1px solid rgba(0,247,255,0.3);
      border-radius: 20px; margin: 2rem 0;
    }
    .hero h1 {
      font-family: 'Orbitron', monospace; font-size: clamp(3rem, 8vw, 6rem);
      background: linear-gradient(45deg, #00f7ff, #ff00cc, #00ff88); 
      -webkit-background-clip: text; -webkit-text-fill-color: transparent;
      text-shadow: 0 0 30px rgba(0,247,255,0.5); animation: glow 2s ease-in-out infinite alternate;
      margin-bottom: 1rem;
    }
    @keyframes glow { from { filter: drop-shadow(0 0 20px #00f7ff); } to { filter: drop-shadow(0 0 40px #ff00cc); } }
    
    .typing { font-size: clamp(1.2rem, 3vw, 1.8rem); font-weight: 500; margin: 2rem 0; }
    
    /* Stats */
    .stats { display: flex; justify-content: center; gap: 2rem; flex-wrap: wrap; margin: 3rem 0; }
    .stat { text-align: center; padding: 1.5rem; background: rgba(0,247,255,0.1); border: 1px solid rgba(0,247,255,0.3); border-radius: 15px; min-width: 120px; }
    .stat-number { font-size: 2.5rem; font-weight: 900; background: linear-gradient(45deg, #00f7ff, #ff00cc); -webkit-background-clip: text; -webkit-text-fill-color: transparent; }
    
    /* Skills */
    .skills-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(80px, 1fr)); gap: 1.5rem; margin: 4rem 0; }
    .skill { text-align: center; padding: 1.5rem; background: rgba(255,255,255,0.05); border-radius: 20px; border: 1px solid rgba(0,247,255,0.2); transition: all 0.3s ease; cursor: pointer; }
    .skill:hover { transform: translateY(-10px) scale(1.05); box-shadow: 0 20px 40px rgba(0,247,255,0.3); border-color: #00f7ff; }
    .skill img { width: 50px; height: 50px; margin-bottom: 0.5rem; filter: drop-shadow(0 0 10px rgba(0,247,255,0.5)); }
    
    /* Projects */
    .projects { margin: 4rem 0; }
    .project-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(350px, 1fr)); gap: 2rem; }
    .project-card {
      background: linear-gradient(145deg, rgba(0,247,255,0.1), rgba(255,0,204,0.1));
      border: 1px solid rgba(0,247,255,0.3); border-radius: 25px; padding: 2rem; 
      transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275); position: relative; overflow: hidden;
    }
    .project-card::before {
      content: ''; position: absolute; top: 0; left: -100%; width: 100%; height: 100%; 
      background: linear-gradient(90deg, transparent, rgba(0,247,255,0.2), transparent);
      transition: left 0.5s; 
    }
    .project-card:hover::before { left: 100%; }
    .project-card:hover { transform: translateY(-15px) rotateX(5deg); box-shadow: 0 30px 60px rgba(0,247,255,0.4); }
    .project-title { font-family: 'Orbitron', monospace; font-size: 1.8rem; margin-bottom: 1rem; color: #00f7ff; }
    .project-tech { display: flex; gap: 0.5rem; margin: 1rem 0; flex-wrap: wrap; }
    .tech-tag { background: rgba(0,247,255,0.2); color: #00f7ff; padding: 0.3rem 0.8rem; border-radius: 20px; font-size: 0.85rem; border: 1px solid rgba(0,247,255,0.3); }
    
    /* Stats Cards */
    .stats-section { display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 2rem; margin: 4rem 0; }
    .stat-card { background: rgba(0,20,40,0.8); border: 1px solid rgba(0,247,255,0.5); border-radius: 20px; padding: 2rem; text-align: center; backdrop-filter: blur(20px); }
    
    /* Connect */
    .connect { text-align: center; margin: 4rem 0; }
    .social-grid { display: flex; justify-content: center; gap: 2rem; flex-wrap: wrap; margin-top: 2rem; }
    .social-btn { display: flex; align-items: center; gap: 1rem; padding: 1rem 2rem; background: linear-gradient(45deg, rgba(0,247,255,0.2), rgba(255,0,204,0.2)); color: #00f7ff; text-decoration: none; border: 2px solid rgba(0,247,255,0.4); border-radius: 50px; font-weight: 500; transition: all 0.3s ease; position: relative; overflow: hidden; }
    .social-btn::before { content: ''; position: absolute; top: 0; left: -100%; width: 100%; height: 100%; background: linear-gradient(90deg, transparent, rgba(255,255,255,0.3), transparent); transition: left 0.5s; }
    .social-btn:hover::before { left: 100%; }
    .social-btn:hover { transform: translateY(-3px); box-shadow: 0 15px 30px rgba(0,247,255,0.4); border-color: #00f7ff; }
    
    /* Responsive */
    @media (max-width: 768px) { .container { padding: 0 1rem; } .stats { gap: 1rem; } }
  </style>
</head>
<body>
  <div class="particles"></div>
  
  <div class="container">
    <!-- Hero -->
    <section class="hero">
      <h1>Manoj Royal</h1>
      <div class="typing">
        AI/ML Engineer | Deep Learning Architect | Computer Vision Specialist
      </div>
      [image:187]
      
      <div class="stats">
        <div class="stat">
          <div class="stat-number">10K+</div>
          <div>Code Lines</div>
        </div>
        <div class="stat">
          <div class="stat-number">50+</div>
          <div>Projects</div>
        </div>
        <div class="stat">
          <div class="stat-number">96%</div>
          <div>Accuracy</div>
        </div>
        <div class="stat">
          <div class="stat-number">3+</div>
          <div>Years Exp</div>
        </div>
      </div>
    </section>

    <!-- Skills -->
    <section class="skills-section">
      <h2 style="text-align: center; font-family: 'Orbitron'; font-size: 2.5rem; margin: 3rem 0 2rem;">🛠️ Tech Arsenal</h2>
      <div class="skills-grid">
        <div class="skill">
          <img src="https://skillicons.dev/icons?i=python" alt="Python">
          <div>Python</div>
        </div>
        <div class="skill">
          <img src="https://skillicons.dev/icons?i=tensorflow" alt="TensorFlow">
          <div>TensorFlow</div>
        </div>
        <div class="skill">
          <img src="https://skillicons.dev/icons?i=pytorch" alt="PyTorch">
          <div>PyTorch</div>
        </div>
        <div class="skill">
          <img src="https://skillicons.dev/icons?i=opencv" alt="OpenCV">
          <div>OpenCV</div>
        </div>
        <div class="skill">
          <img src="https://skillicons.dev/icons?i=flask" alt="Flask">
          <div>Flask</div>
        </div>
        <div class="skill">
          <img src="https://skillicons.dev/icons?i=git" alt="Git">
          <div>Git</div>
        </div>
        <div class="skill">
          <img src="https://skillicons.dev/icons?i=aws" alt="AWS">
          <div>AWS</div>
        </div>
        <div class="skill">
          <img src="https://skillicons.dev/icons?i=docker" alt="Docker">
          <div>Docker</div>
        </div>
      </div>
      [image:188]
    </section>

    <!-- Projects -->
    <section class="projects">
      <h2 style="text-align: center; font-family: 'Orbitron'; font-size: 2.5rem; margin: 4rem 0 2rem;">🌟 Elite Projects</h2>
      <div class="project-grid">
        <div class="project-card">
          <h3 class="project-title">🧠 BrainAI - 3D Tumor Segmentation</h3>
          <p>Production-grade 3D U-Net for MRI brain tumor detection with Flask dashboard and real-time inference.</p>
          <div class="project-tech">
            <span class="tech-tag">3D U-Net</span>
            <span class="tech-tag">PyTorch</span>
            <span class="tech-tag">Flask</span>
            <span class="tech-tag">OpenCV</span>
            <span class="tech-tag">96.8% mIoU</span>
          </div>
          <a href="#" class="social-btn" style="display: inline-block; margin-top: 1rem;">Live Demo →</a>
        </div>
        
        <div class="project-card">
          <h3 class="project-title">😷 FactoryGuard AI</h3>
          <p>Real-time industrial surveillance with YOLOv8 + anomaly detection for safety compliance.</p>
          <div class="project-tech">
            <span class="tech-tag">YOLOv8</span>
            <span class="tech-tag">RTSP</span>
            <span class="tech-tag">SocketIO</span>
            <span class="tech-tag">Docker</span>
            <span class="tech-tag">99.2% Recall</span>
          </div>
          <a href="#" class="social-btn" style="display: inline-block; margin-top: 1rem;">View Repo →</a>
        </div>
        
        <div class="project-card">
          <h3 class="project-title">🔮 StockPro Ultimate</h3>
          <p>AI-powered Indian stock analysis platform with ML predictions, screener, and real-time data.</p>
          <div class="project-tech">
            <span class="tech-tag">LSTM + XGBoost</span>
            <span class="tech-tag">Flask API</span>
            <span class="tech-tag">Redis</span>
            <span class="tech-tag">NSE Data</span>
            <span class="tech-tag">87% Accuracy</span>
          </div>
          <a href="#" class="social-btn" style="display: inline-block; margin-top: 1rem;">API Docs →</a>
        </div>
      </div>
    </section>

    <!-- Stats -->
    <section class="stats-section">
      <div class="stat-card">
        <h3 style="font-family: 'Orbitron'; color: #00f7ff;">📈 GitHub Stats</h3>
        <img src="https://github-readme-stats.vercel.app/api?username=manojroyal422&show_icons=true&theme=radical&hide_border=true&bg_color=0a0a0a&title_color=00f7ff&text_color=ffffff&icon_color=ff00cc" alt="Stats" style="width: 100%; border-radius: 15px;">
      </div>
      <div class="stat-card">
        <h3 style="font-family: 'Orbitron'; color: #00f7ff;">🔥 Streak</h3>
        <img src="https://github-readme-streak-stats.herokuapp.com/?user=manojroyal422&theme=radical&hide_border=true&background=0a0a0a&stroke=00f7ff&ring=ff00cc&currStreakLabel=00f7ff" alt="Streak" style="width: 100%; border-radius: 15px;">
      </div>
    </section>

    <!-- Connect -->
    <section class="connect">
      <h2 style="font-family: 'Orbitron'; font-size: 2.5rem; margin-bottom: 2rem;">🚀 Let's Build Something Amazing</h2>
      <p style="font-size: 1.2rem; margin-bottom: 2rem; opacity: 0.9;">Open to collaborations on production AI/ML systems</p>
      
      <div class="social-grid">
        <a href="https://linkedin.com/in/manojroyal422" class="social-btn">
          <img src="https://skillicons.dev/icons?i=linkedin" width="24"> LinkedIn
        </a>
        <a href="mailto:manojroyal200347@gmail.com" class="social-btn">
          <img src="https://skillicons.dev/icons?i=gmail" width="24"> Email
        </a>
        <a href="https://github.com/manojroyal422" class="social-btn">
          <img src="https://skillicons.dev/icons?i=github" width="24"> GitHub
        </a>
        <a href="#" class="social-btn">
          <img src="https://skillicons.dev/icons?i=portfolio" width="24"> Portfolio
        </a>
      </div>
    </section>

    <!-- Footer -->
    <footer style="text-align: center; padding: 3rem 0; border-top: 1px solid rgba(0,247,255,0.3); margin-top: 4rem;">
      <h3 style="font-family: 'Orbitron'; color: #00f7ff;">⚡ Manoj Royal 2026</h3>
      <p style="opacity: 0.7; margin-top: 0.5rem;">Turning Data into Intelligence | Building AI That Works</p>
    </footer>
  </div>

  <script>
    // Particle animation
    const particles = document.querySelector('.particles');
    for(let i = 0; i < 50; i++) {
      const particle = document.createElement('div');
      particle.style.position = 'absolute';
      particle.style.width = '2px'; particle.style.height = '2px';
      particle.style.background = `hsl(${Math.random()*360}, 70%, 60%)`;
      particle.style.left = Math.random()*100 + '%';
      particle.style.top = Math.random()*100 + '%';
      particle.style.animation = `float ${Math.random()*10 + 10}s linear infinite`;
      particles.appendChild(particle);
    }
  </script>
</body>
</html>
