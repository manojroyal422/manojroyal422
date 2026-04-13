<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Manoj Royal | AI Engineer</title>

<link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700&family=JetBrains+Mono&display=swap" rel="stylesheet">
<link href="https://unpkg.com/aos@2.3.1/dist/aos.css" rel="stylesheet">

<style>
*{margin:0;padding:0;box-sizing:border-box}
body{
  background:#0a0a0a;
  color:#00f7ff;
  font-family:'JetBrains Mono', monospace;
  scroll-behavior:smooth;
}

/* NAVBAR */
nav{
  position:fixed;
  top:0;
  width:100%;
  background:rgba(0,0,0,0.7);
  backdrop-filter:blur(10px);
  display:flex;
  justify-content:space-between;
  padding:1rem 2rem;
  z-index:1000;
}
nav a{color:#fff;text-decoration:none;margin-left:20px}

/* HERO */
.hero{
  height:100vh;
  display:flex;
  flex-direction:column;
  justify-content:center;
  align-items:center;
  text-align:center;
}
.hero h1{
  font-size:4rem;
  font-family:Orbitron;
  background:linear-gradient(45deg,#00f7ff,#ff00cc);
  -webkit-background-clip:text;
  -webkit-text-fill-color:transparent;
}
.typing{
  font-size:1.5rem;
  margin:1rem;
}

/* BUTTON */
.btn{
  padding:10px 20px;
  border:1px solid #00f7ff;
  border-radius:30px;
  text-decoration:none;
  color:#00f7ff;
  margin-top:20px;
}

/* SECTION */
section{padding:100px 20px}

/* PROJECT */
.projects{
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(300px,1fr));
  gap:20px;
}
.card{
  padding:20px;
  border:1px solid #00f7ff;
  border-radius:20px;
  transition:0.3s;
}
.card:hover{
  transform:translateY(-10px);
  box-shadow:0 0 20px #00f7ff;
}

/* SKILLS */
.skills{
  display:flex;
  flex-wrap:wrap;
  gap:15px;
  justify-content:center;
}
.skill{
  padding:10px 15px;
  border:1px solid #00f7ff;
  border-radius:20px;
}

/* FOOTER */
footer{
  text-align:center;
  padding:20px;
  border-top:1px solid #00f7ff;
}
</style>
</head>

<body>

<!-- NAV -->
<nav>
  <div>Manoj AI</div>
  <div>
    <a href="#projects">Projects</a>
    <a href="#skills">Skills</a>
    <a href="#contact">Contact</a>
  </div>
</nav>

<!-- HERO -->
<section class="hero">
  <h1>Manoj Royal</h1>
  <div class="typing">AI | Machine Learning | Deep Learning</div>
  <a href="resume.pdf" class="btn">Download Resume</a>
</section>

<!-- PROJECTS -->
<section id="projects" data-aos="fade-up">
<h2 align="center">🚀 Projects</h2>

<div class="projects">

<div class="card">
<h3>BrainAI</h3>
<p>3D U-Net brain tumor segmentation using Flask</p>
<a href="https://github.com/manojroyal422" class="btn">View</a>
</div>

<div class="card">
<h3>Factory Guard AI</h3>
<p>AI surveillance system using YOLO</p>
<a href="https://github.com/manojroyal422" class="btn">View</a>
</div>

<div class="card">
<h3>Stock Prediction</h3>
<p>AI stock prediction system</p>
<a href="https://github.com/manojroyal422" class="btn">View</a>
</div>

</div>
</section>

<!-- SKILLS -->
<section id="skills" data-aos="fade-up">
<h2 align="center">🧠 Skills</h2>

<div class="skills">
<div class="skill">Python</div>
<div class="skill">TensorFlow</div>
<div class="skill">OpenCV</div>
<div class="skill">Flask</div>
<div class="skill">ML</div>
<div class="skill">Deep Learning</div>
</div>

</section>

<!-- CONTACT -->
<section id="contact" data-aos="fade-up">
<h2 align="center">📬 Contact</h2>
<p align="center">manojroyal200347@gmail.com</p>
<p align="center">
<a href="https://github.com/manojroyal422" class="btn">GitHub</a>
<a href="https://linkedin.com/in/YOUR-LINKEDIN" class="btn">LinkedIn</a>
</p>
</section>

<!-- FOOTER -->
<footer>
🚀 Manoj Royal | AI Engineer
</footer>

<script src="https://unpkg.com/aos@2.3.1/dist/aos.js"></script>
<script>AOS.init();</script>

</body>
</html>
