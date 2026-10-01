<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Mr X - Software Engineer & AI/ML Architect</title>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
      background: linear-gradient(135deg, #0f0c29 0%, #302b63 50%, #24243e 100%);
      color: #e0e0e0;
      line-height: 1.6;
      overflow-x: hidden;
    }

    .container {
      max-width: 1000px;
      margin: 0 auto;
      padding: 60px 40px;
    }

    /* HERO SECTION */
    .hero {
      text-align: center;
      margin-bottom: 80px;
      animation: fadeInUp 1s ease-out;
    }

    .hero-title {
      font-size: 72px;
      font-weight: 700;
      background: linear-gradient(120deg, #a78bfa 0%, #60a5fa 50%, #34d399 100%);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
      margin-bottom: 12px;
      letter-spacing: -1px;
      animation: slideDown 0.8s ease-out;
    }

    .hero-subtitle {
      font-size: 24px;
      font-weight: 500;
      color: #b0b0b0;
      margin-bottom: 8px;
      animation: slideDown 0.9s ease-out 0.1s both;
    }

    .hero-description {
      font-size: 16px;
      color: #888;
      max-width: 600px;
      margin: 24px auto;
      animation: slideDown 1s ease-out 0.2s both;
    }

    .stats-row {
      display: flex;
      justify-content: center;
      gap: 40px;
      margin-top: 40px;
      animation: slideDown 1.1s ease-out 0.3s both;
    }

    .stat {
      text-align: center;
    }

    .stat-number {
      font-size: 28px;
      font-weight: 700;
      background: linear-gradient(120deg, #a78bfa, #60a5fa);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
    }

    .stat-label {
      font-size: 13px;
      color: #888;
      margin-top: 4px;
      text-transform: uppercase;
      letter-spacing: 0.5px;
    }

    /* CARDS & SECTIONS */
    .section {
      margin-bottom: 60px;
    }

    .section-title {
      font-size: 32px;
      font-weight: 700;
      margin-bottom: 40px;
      color: #ffffff;
      position: relative;
      padding-bottom: 12px;
    }

    .section-title::after {
      content: '';
      position: absolute;
      bottom: 0;
      left: 0;
      width: 60px;
      height: 3px;
      background: linear-gradient(90deg, #a78bfa, #60a5fa);
      border-radius: 2px;
    }

    .grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
      gap: 24px;
    }

    .card {
      background: rgba(255, 255, 255, 0.05);
      border: 1px solid rgba(167, 139, 250, 0.2);
      border-radius: 12px;
      padding: 28px;
      backdrop-filter: blur(10px);
      transition: all 0.3s ease;
      cursor: pointer;
      animation: fadeInUp 0.8s ease-out backwards;
    }

    .card:hover {
      background: rgba(255, 255, 255, 0.08);
      border-color: rgba(167, 139, 250, 0.4);
      transform: translateY(-4px);
      box-shadow: 0 20px 40px rgba(0, 0, 0, 0.3);
    }

    .card h3 {
      font-size: 18px;
      font-weight: 600;
      margin-bottom: 12px;
      color: #ffffff;
    }

    .card p {
      font-size: 14px;
      color: #aaa;
      margin-bottom: 16px;
      line-height: 1.6;
    }

    .tag-group {
      display: flex;
      flex-wrap: wrap;
      gap: 8px;
    }

    .tag {
      display: inline-block;
      background: rgba(167, 139, 250, 0.15);
      color: #a78bfa;
      padding: 4px 12px;
      border-radius: 20px;
      font-size: 12px;
      font-weight: 500;
      border: 1px solid rgba(167, 139, 250, 0.3);
    }

    /* TECH STACK */
    .tech-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(140px, 1fr));
      gap: 20px;
    }

    .tech-item {
      background: rgba(255, 255, 255, 0.03);
      border: 1px solid rgba(167, 139, 250, 0.15);
      border-radius: 10px;
      padding: 16px;
      text-align: center;
      transition: all 0.3s ease;
    }

    .tech-item:hover {
      background: rgba(167, 139, 250, 0.1);
      border-color: rgba(167, 139, 250, 0.4);
    }

    .tech-icon {
      font-size: 32px;
      margin-bottom: 8px;
    }

    .tech-name {
      font-size: 13px;
      font-weight: 600;
      color: #fff;
    }

    /* FEATURES LIST */
    .feature-list {
      list-style: none;
    }

    .feature-list li {
      padding: 16px 0;
      border-bottom: 1px solid rgba(167, 139, 250, 0.1);
      display: flex;
      align-items: flex-start;
      gap: 16px;
    }

    .feature-list li:last-child {
      border-bottom: none;
    }

    .feature-icon {
      color: #a78bfa;
      font-weight: 700;
      flex-shrink: 0;
      width: 24px;
    }

    .feature-text {
      flex: 1;
    }

    .feature-title {
      font-weight: 600;
      color: #fff;
      margin-bottom: 4px;
    }

    .feature-desc {
      font-size: 14px;
      color: #999;
    }

    /* FOOTER */
    .footer {
      border-top: 1px solid rgba(167, 139, 250, 0.15);
      padding-top: 40px;
      text-align: center;
      margin-top: 80px;
      animation: fadeInUp 1.2s ease-out 0.5s both;
    }

    .social-links {
      display: flex;
      justify-content: center;
      gap: 20px;
      margin-bottom: 24px;
    }

    .social-link {
      width: 44px;
      height: 44px;
      display: flex;
      align-items: center;
      justify-content: center;
      background: rgba(167, 139, 250, 0.1);
      border: 1px solid rgba(167, 139, 250, 0.2);
      border-radius: 8px;
      color: #a78bfa;
      text-decoration: none;
      font-weight: 600;
      transition: all 0.3s ease;
    }

    .social-link:hover {
      background: rgba(167, 139, 250, 0.2);
      border-color: rgba(167, 139, 250, 0.4);
      transform: translateY(-2px);
    }

    .footer-text {
      font-size: 13px;
      color: #888;
      margin-top: 24px;
    }

    /* ANIMATIONS */
    @keyframes fadeInUp {
      from {
        opacity: 0;
        transform: translateY(30px);
      }
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }

    @keyframes slideDown {
      from {
        opacity: 0;
        transform: translateY(-20px);
      }
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }

    .card:nth-child(2) {
      animation-delay: 0.1s;
    }

    .card:nth-child(3) {
      animation-delay: 0.2s;
    }

    .card:nth-child(4) {
      animation-delay: 0.3s;
    }

    /* RESPONSIVE */
    @media (max-width: 640px) {
      .container {
        padding: 40px 20px;
      }

      .hero-title {
        font-size: 48px;
      }

      .hero-subtitle {
        font-size: 18px;
      }

      .stats-row {
        gap: 20px;
      }

      .section-title {
        font-size: 24px;
      }

      .grid {
        grid-template-columns: 1fr;
      }
    }
  </style>
</head>
<body>
  <div class="container">
    <!-- HERO SECTION -->
    <div class="hero">
      <h1 class="hero-title">Mr X</h1>
      <p class="hero-subtitle">Software Engineer & AI/ML Architect</p>
      <p class="hero-description">Building intelligent systems with React, Node.js, Python & LLMs. Final year at Riphah. Crafting beautiful code & elegant AI solutions.</p>
      
      <div class="stats-row">
        <div class="stat">
          <div class="stat-number">6+</div>
          <div class="stat-label">Projects</div>
        </div>
        <div class="stat">
          <div class="stat-number">15+</div>
          <div class="stat-label">Pull Requests</div>
        </div>
        <div class="stat">
          <div class="stat-number">2</div>
          <div class="stat-label">Internships</div>
        </div>
      </div>
    </div>

    <!-- AI/ML PROJECTS -->
    <div class="section">
      <h2 class="section-title">🤖 AI/ML Systems</h2>
      <div class="grid">
        <div class="card">
          <h3>ExamGPT</h3>
          <p>RAG-powered chatbot for examination departments. Handles PDF ingestion, context-aware Q&A, and intelligent document analysis.</p>
          <div class="tag-group">
            <span class="tag">LangChain</span>
            <span class="tag">OpenAI</span>
            <span class="tag">RAG</span>
          </div>
        </div>

        <div class="card">
          <h3>Haqdar</h3>
          <p>Urdu-language legal awareness system for Pakistan. Final year project combining LLMs with domain-specific knowledge bases.</p>
          <div class="tag-group">
            <span class="tag">LLMs</span>
            <span class="tag">Django</span>
            <span class="tag">NLP</span>
          </div>
        </div>

        <div class="card">
          <h3>Prompt Engineering</h3>
          <p>Advanced techniques including few-shot learning, chain-of-thought reasoning, and multi-domain applications with GPT-4 & Claude.</p>
          <div class="tag-group">
            <span class="tag">Prompting</span>
            <span class="tag">Optimization</span>
            <span class="tag">LLMs</span>
          </div>
        </div>

        <div class="card">
          <h3>TensorFlow Models</h3>
          <p>Production-ready ML implementations on Kaggle & Colab. CNNs, RNNs, and Transformer-based architectures.</p>
          <div class="tag-group">
            <span class="tag">TensorFlow</span>
            <span class="tag">Deep Learning</span>
            <span class="tag">Hugging Face</span>
          </div>
        </div>
      </div>
    </div>

    <!-- FULL-STACK PROJECTS -->
    <div class="section">
      <h2 class="section-title">🚀 Full-Stack Development</h2>
      <div class="grid">
        <div class="card">
          <h3>RetroReels.exe</h3>
          <p>AI-powered aesthetic content creation brand. Modern UI, real-time image generation, deployed on Vercel.</p>
          <div class="tag-group">
            <span class="tag">React</span>
            <span class="tag">Next.js</span>
            <span class="tag">AI</span>
          </div>
        </div>

        <div class="card">
          <h3>Dev Portfolio</h3>
          <p>High-performance personal portfolio. Glassmorphism design, Framer Motion animations, Lighthouse 95+ scores.</p>
          <div class="tag-group">
            <span class="tag">Next.js</span>
            <span class="tag">TailwindCSS</span>
            <span class="tag">Design</span>
          </div>
        </div>

        <div class="card">
          <h3>MERN Apps</h3>
          <p>Full-stack applications with MongoDB, Express, React, Node.js. State management, real-time updates, authentication.</p>
          <div class="tag-group">
            <span class="tag">MERN</span>
            <span class="tag">MongoDB</span>
            <span class="tag">API</span>
          </div>
        </div>

        <div class="card">
          <h3>Azure PDC</h3>
          <p>Cloud infrastructure implementation on Microsoft Azure. Resource management, CI/CD pipelines, cost optimization.</p>
          <div class="tag-group">
            <span class="tag">Azure</span>
            <span class="tag">DevOps</span>
            <span class="tag">Cloud</span>
          </div>
        </div>
      </div>
    </div>

    <!-- TECH STACK -->
    <div class="section">
      <h2 class="section-title">💻 Technology Stack</h2>
      
      <h3 style="color: #a78bfa; font-size: 16px; font-weight: 600; margin-bottom: 20px;">Frontend</h3>
      <div class="tech-grid">
        <div class="tech-item">
          <div class="tech-icon">⚛️</div>
          <div class="tech-name">React</div>
        </div>
        <div class="tech-item">
          <div class="tech-icon">▲</div>
          <div class="tech-name">Next.js</div>
        </div>
        <div class="tech-item">
          <div class="tech-icon">🔷</div>
          <div class="tech-name">TypeScript</div>
        </div>
        <div class="tech-item">
          <div class="tech-icon">🎨</div>
          <div class="tech-name">TailwindCSS</div>
        </div>
        <div class="tech-item">
          <div class="tech-icon">✨</div>
          <div class="tech-name">Framer Motion</div>
        </div>
      </div>

      <h3 style="color: #a78bfa; font-size: 16px; font-weight: 600; margin-top: 32px; margin-bottom: 20px;">Backend & Data</h3>
      <div class="tech-grid">
        <div class="tech-item">
          <div class="tech-icon">🟢</div>
          <div class="tech-name">Node.js</div>
        </div>
        <div class="tech-item">
          <div class="tech-icon">🟠</div>
          <div class="tech-name">Django</div>
        </div>
        <div class="tech-item">
          <div class="tech-icon">🍃</div>
          <div class="tech-name">MongoDB</div>
        </div>
        <div class="tech-item">
          <div class="tech-icon">🐘</div>
          <div class="tech-name">PostgreSQL</div>
        </div>
        <div class="tech-item">
          <div class="tech-icon">⚙️</div>
          <div class="tech-name">Prisma</div>
        </div>
      </div>

      <h3 style="color: #a78bfa; font-size: 16px; font-weight: 600; margin-top: 32px; margin-bottom: 20px;">AI/ML & LLMs</h3>
      <div class="tech-grid">
        <div class="tech-item">
          <div class="tech-icon">🐍</div>
          <div class="tech-name">Python</div>
        </div>
        <div class="tech-item">
          <div class="tech-icon">🧠</div>
          <div class="tech-name">LangChain</div>
        </div>
        <div class="tech-item">
          <div class="tech-icon">🤖</div>
          <div class="tech-name">Hugging Face</div>
        </div>
        <div class="tech-item">
          <div class="tech-icon">🔥</div>
          <div class="tech-name">TensorFlow</div>
        </div>
        <div class="tech-item">
          <div class="tech-icon">☁️</div>
          <div class="tech-name">OpenAI</div>
        </div>
      </div>

      <h3 style="color: #a78bfa; font-size: 16px; font-weight: 600; margin-top: 32px; margin-bottom: 20px;">Cloud & DevOps</h3>
      <div class="tech-grid">
        <div class="tech-item">
          <div class="tech-icon">☁️</div>
          <div class="tech-name">Azure</div>
        </div>
        <div class="tech-item">
          <div class="tech-icon">▲</div>
          <div class="tech-name">Vercel</div>
        </div>
        <div class="tech-item">
          <div class="tech-icon">🐙</div>
          <div class="tech-name">GitHub</div>
        </div>
        <div class="tech-item">
          <div class="tech-icon">📦</div>
          <div class="tech-name">Docker</div>
        </div>
        <div class="tech-item">
          <div class="tech-icon">⚡</div>
          <div class="tech-name">Git</div>
        </div>
      </div>
    </div>

    <!-- EXPERTISE -->
    <div class="section">
      <h2 class="section-title">✨ Core Expertise</h2>
      <ul class="feature-list">
        <li>
          <div class="feature-icon">🎯</div>
          <div class="feature-text">
            <div class="feature-title">LLMs & RAG Systems</div>
            <div class="feature-desc">Building production RAG pipelines, prompt engineering, and AI-driven applications with LangChain</div>
          </div>
        </li>
        <li>
          <div class="feature-icon">🚀</div>
          <div class="feature-text">
            <div class="feature-title">Full-Stack MERN</div>
            <div class="feature-desc">End-to-end web development with React, Node.js, MongoDB. Scalable architectures and clean code</div>
          </div>
        </li>
        <li>
          <div class="feature-icon">☁️</div>
          <div class="feature-text">
            <div class="feature-title">Microsoft Azure</div>
            <div class="feature-desc">Cloud infrastructure, CI/CD pipelines, resource management, and deployment optimization</div>
          </div>
        </li>
        <li>
          <div class="feature-icon">🎨</div>
          <div class="feature-text">
            <div class="feature-title">UI/UX & Design</div>
            <div class="feature-desc">Modern design systems, glassmorphism, responsive layouts, and aesthetic-driven interfaces</div>
          </div>
        </li>
        <li>
          <div class="feature-icon">📊</div>
          <div class="feature-text">
            <div class="feature-title">Machine Learning</div>
            <div class="feature-desc">TensorFlow, deep learning models, NLP, computer vision on Kaggle and Colab</div>
          </div>
        </li>
        <li>
          <div class="feature-icon">🔀</div>
          <div class="feature-text">
            <div class="feature-title">Version Control & Collaboration</div>
            <div class="feature-desc">Git workflow, 15+ PRs merged, collaborative development, GitHub best practices</div>
          </div>
        </li>
      </ul>
    </div>

    <!-- FOOTER -->
    <div class="footer">
      <div class="social-links">
        <a href="https://linkedin.com/in/mahmoodkhan9517" class="social-link" title="LinkedIn">in</a>
        <a href="https://github.com/codingwithmahmo" class="social-link" title="GitHub">⚡</a>
        <a href="https://dev-mahmood.vercel.app" class="social-link" title="Portfolio">→</a>
        <a href="mailto:mahmood.mkhan03@gmail.com" class="social-link" title="Email">✉</a>
      </div>
      <p class="footer-text">Built with code, coffee ☕, and a passion for elegant solutions</p>
      <p class="footer-text" style="margin-top: 12px; font-size: 12px; color: #666;">© 2026 Mr X • Always learning, always building</p>
    </div>
  </div>
</body>
</html>

---

## 🌌 Developer Profile

```javascript
const mrX = {
  name: "Mr X",
  role: "Software Engineer & AI/ML Architect",
  university: "Riphah International University 🎓",
  location: "Islamabad, Pakistan 🇵🇰",
  semester: "7th",
  
  expertise: {
    frontend: ["React", "Next.js", "TypeScript", "TailwindCSS"],
    backend: ["Node.js", "Django", "Express"],
    databases: ["MongoDB", "PostgreSQL", "Prisma"],
    aiml: ["LLMs", "RAG Systems", "TensorFlow", "Hugging Face", "LangChain"],
    cloud: ["Microsoft Azure", "Vercel", "Netlify"],
    devops: ["Git", "GitHub Actions", "Docker"]
  },
  
  currentlyBuilding: [
    "🤖 ExamGPT - RAG Chatbot",
    "📜 Haqdar - Urdu Legal RAG System (FYP)",
    "🎬 RetroReels - AI Content Creation"
  ]
};
```

---

## 🚀 AI & ML Projects

| Project | Tech Stack | Description |
|---------|-----------|-------------|
| **Exam.AI** 📚 | LangChain, OpenAI, RAG | Intelligent exam department chatbot with PDF ingestion |
| **Prompt Engineering Hub** 🧠 | GPT-4, Claude, Chain-of-Thought | Advanced LLM optimization techniques |
| **TensorFlow Projects** 🔬 | CNN, RNN, Transformers | Production ML models on Kaggle & Colab |

---

## 🎨 Full-Stack Projects

| Project | Stack | Status |
|---------|-------|--------|
| **Dev Portfolio** 💼 | Next.js, TailwindCSS, Framer Motion | Live - Glassmorphism Design |

---

## ☁️ Cloud & DevOps

### Microsoft Azure
- Azure PDC Implementation (Group 7)
- Resource Groups, VMs, App Services
- CI/CD Pipelines & Cost Optimization

### GitHub & Version Control
- **15+ Pull Requests** reviewed & merged
- Feature branches → Code review → Production
- GitHub Actions automation
- Vercel/Netlify deployments

---

## 🛠 Tech Stack

### 💻 Frontend
![React](https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=000&labelColor=1e1b4b)
![Next.js](https://img.shields.io/badge/Next.js-000?style=for-the-badge&logo=nextdotjs&logoColor=fff&labelColor=1e1b4b)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=fff&labelColor=1e1b4b)
![TailwindCSS](https://img.shields.io/badge/Tailwind-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=fff&labelColor=1e1b4b)

### ⚙️ Backend
![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=fff&labelColor=1e1b4b)
![Django](https://img.shields.io/badge/Django-092E20?style=for-the-badge&logo=django&logoColor=fff&labelColor=1e1b4b)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=fff&labelColor=1e1b4b)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-336791?style=for-the-badge&logo=postgresql&logoColor=fff&labelColor=1e1b4b)

### 🤖 AI/ML & LLMs
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=fff&labelColor=1e1b4b)
![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=for-the-badge&logo=chainlink&logoColor=fff&labelColor=1e1b4b)
![OpenAI](https://img.shields.io/badge/OpenAI-412991?style=for-the-badge&logo=openai&logoColor=fff&labelColor=1e1b4b)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=fff&labelColor=1e1b4b)
![Hugging Face](https://img.shields.io/badge/Hugging%20Face-FFD21E?style=for-the-badge&logo=huggingface&logoColor=000&labelColor=1e1b4b)

### ☁️ Cloud
![Azure](https://img.shields.io/badge/Microsoft%20Azure-0078D4?style=for-the-badge&logo=microsoftazure&logoColor=fff&labelColor=1e1b4b)
![Vercel](https://img.shields.io/badge/Vercel-000?style=for-the-badge&logo=vercel&logoColor=fff&labelColor=1e1b4b)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=fff&labelColor=1e1b4b)

---

## 📊 GitHub Stats

<div align="center">

![GitHub Stats](https://github-readme-stats.vercel.app/api?username=codingwithmahmo&show_icons=true&theme=midnight-purple&title_color=a78bfa&text_color=e9d5ff&icon_color=c4b5fd&bg_color=1e1b4b&border_color=6366f1)

![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=codingwithmahmo&layout=compact&theme=midnight-purple&title_color=a78bfa&text_color=e9d5ff&bg_color=1e1b4b&border_color=6366f1)

</div>

---

## 🌐 Connect

<div align="center">

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/mahmoodkhan9517/)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/codingwithmahmo/)
[![Portfolio](https://img.shields.io/badge/Portfolio-a78bfa?style=for-the-badge&logo=vercel&logoColor=white)](https://dev-mahmood.vercel.app/)
[![Email](https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:mahmood.mkhan03@gmail.com)

<br/>

**✨ Code is art. Intelligence is the medium. The future is the canvas. ✨**

</div>
