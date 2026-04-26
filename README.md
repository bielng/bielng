<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>TaJ - Data Scientist Portfolio</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      background: linear-gradient(135deg, #0a0f1e 0%, #0c1222 100%);
      font-family: 'Segoe UI', 'Inter', -apple-system, BlinkMacSystemFont, 'Roboto', sans-serif;
      padding: 2rem;
      display: flex;
      justify-content: center;
    }

    .readme-container {
      max-width: 1200px;
      width: 100%;
      background: rgba(12, 20, 30, 0.65);
      backdrop-filter: blur(10px);
      border-radius: 2rem;
      border: 1px solid rgba(79, 195, 247, 0.25);
      padding: 2rem;
      box-shadow: 0 20px 40px rgba(0, 0, 0, 0.4);
    }

    /* Header Section */
    .header {
      text-align: center;
      margin-bottom: 2rem;
    }

    h1 {
      font-size: 3rem;
      background: linear-gradient(120deg, #fff, #4FC3F7, #81d4fa);
      background-clip: text;
      -webkit-background-clip: text;
      color: transparent;
      margin-bottom: 0.5rem;
    }

    .tagline {
      color: #b8d8fc;
      font-size: 1.1rem;
      letter-spacing: 1px;
      display: flex;
      justify-content: center;
      gap: 1.5rem;
      flex-wrap: wrap;
      margin: 1rem 0;
    }

    .badge-container {
      display: flex;
      justify-content: center;
      gap: 0.8rem;
      flex-wrap: wrap;
      margin: 1.2rem 0;
    }

    .badge {
      background: rgba(79, 195, 247, 0.12);
      padding: 0.4rem 1rem;
      border-radius: 30px;
      font-size: 0.8rem;
      border: 1px solid rgba(79, 195, 247, 0.4);
      color: #cae3ff;
    }

    /* Animated Skills Grid - MOST DESIGNED PART */
    .skills-section {
      margin: 2.5rem 0;
    }

    .section-title {
      font-size: 1.8rem;
      font-weight: 700;
      margin-bottom: 1.5rem;
      background: linear-gradient(135deg, #e0f0ff, #7bc5f9);
      background-clip: text;
      -webkit-background-clip: text;
      color: transparent;
      border-left: 4px solid #4FC3F7;
      padding-left: 1rem;
    }

    .skills-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(130px, 1fr));
      gap: 1.2rem;
    }

    .skill-card {
      background: linear-gradient(145deg, rgba(25, 35, 55, 0.7), rgba(18, 25, 45, 0.8));
      backdrop-filter: blur(6px);
      padding: 1rem 0.5rem;
      border-radius: 1.5rem;
      text-align: center;
      transition: all 0.35s cubic-bezier(0.2, 0.9, 0.6, 1.1);
      border: 1px solid rgba(79, 195, 247, 0.2);
      cursor: default;
      animation: fadeInUp 0.5s ease backwards;
      animation-delay: calc(var(--order) * 0.03s);
    }

    .skill-card:hover {
      transform: translateY(-8px) scale(1.02);
      border-color: #4FC3F7;
      box-shadow: 0 15px 25px -12px rgba(79, 195, 247, 0.5);
      background: rgba(30, 45, 70, 0.9);
    }

    .skill-icon {
      height: 55px;
      display: flex;
      align-items: center;
      justify-content: center;
      margin-bottom: 0.6rem;
      font-size: 2.8rem;
    }

    .skill-icon img {
      max-width: 48px;
      max-height: 48px;
      filter: drop-shadow(0 2px 4px rgba(0,0,0,0.3));
      transition: transform 0.2s;
    }

    .skill-card:hover .skill-icon img {
      transform: scale(1.08);
      filter: drop-shadow(0 0 6px #4FC3F7);
    }

    .skill-name {
      font-weight: 600;
      font-size: 0.85rem;
      color: #e2efff;
      margin-bottom: 0.2rem;
    }

    .skill-cat {
      font-size: 0.7rem;
      color: #8bb4e6;
    }

    /* Stats Row */
    .stats-row {
      display: flex;
      flex-wrap: wrap;
      gap: 1.5rem;
      margin: 2rem 0;
      background: rgba(0, 0, 0, 0.25);
      border-radius: 1.5rem;
      padding: 1rem;
    }

    .stat-block {
      flex: 1;
      text-align: center;
      background: rgba(10, 18, 28, 0.5);
      border-radius: 1.2rem;
      padding: 0.8rem;
    }

    .stat-block h4 {
      color: #4FC3F7;
      font-size: 0.9rem;
    }

    .stat-number {
      font-size: 1.6rem;
      font-weight: bold;
      color: white;
    }

    /* Connect & Footer */
    .connect-links {
      display: flex;
      justify-content: center;
      gap: 2rem;
      margin: 1.5rem 0;
    }

    .connect-links a {
      color: #cce4ff;
      font-size: 1.6rem;
      transition: all 0.2s;
    }

    .connect-links a:hover {
      color: #4FC3F7;
      transform: translateY(-3px);
    }

    .fun-fact {
      text-align: center;
      color: #9ac2e6;
      font-size: 0.85rem;
      margin-top: 1rem;
      padding-top: 1rem;
      border-top: 1px solid rgba(79, 195, 247, 0.2);
    }

    @keyframes fadeInUp {
      from {
        opacity: 0;
        transform: translateY(20px);
      }
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }

    @media (max-width: 700px) {
      body { padding: 1rem; }
      .skills-grid { grid-template-columns: repeat(auto-fill, minmax(100px, 1fr)); }
      h1 { font-size: 2.2rem; }
    }
  </style>
</head>
<body>
<div class="readme-container">
  
  <!-- HEADER with name and intro -->
  <div class="header">
    <h1>Hey there, I'm <span style="color:#4FC3F7;">TaJ</span></h1>
    <div class="tagline">
      <span>📊 Data Scientist</span> • <span>🤖 Data Enthusiast</span> • <span>🌍 Refugee Tech Advocate</span>
    </div>
    <div class="badge-container">
      <span class="badge">🧠 AI & Data Engineering @ITESO</span>
      <span class="badge">🐍 Python • AWS • Power BI</span>
      <span class="badge">🚀 Empowering marginalized communities</span>
    </div>
  </div>

  <!-- MOST DESIGNED SECTION: ANIMATED LANGUAGES & TOOLS (beautiful glass cards) -->
  <div class="skills-section">
    <div class="section-title">
      ⚡ Languages & Tools · animated showcase
    </div>
    <div class="skills-grid" id="skillsGrid"></div>
  </div>

  <!-- GITHUB STATS & STREAK (visual placeholder) -->
  <div class="stats-row">
    <div class="stat-block">
      <h4><i class="fas fa-code"></i> Top Languages</h4>
      <div class="stat-number">Python · SQL · JS</div>
    </div>
    <div class="stat-block">
      <h4><i class="fas fa-fire"></i> Current Focus</h4>
      <div class="stat-number">Generative AI & AWS</div>
    </div>
    <div class="stat-block">
      <h4><i class="fas fa-chart-line"></i> Open Source</h4>
      <div class="stat-number">Data for Humanity</div>
    </div>
  </div>

  <!-- CONNECT & LINKS -->
  <div class="connect-links">
    <a href="mailto:ngunartaban@gmail.com" target="_blank" title="Email"><i class="fas fa-envelope"></i></a>
    <a href="https://www.linkedin.com/in/taban-ngunar-x217/" target="_blank" title="LinkedIn"><i class="fab fa-linkedin"></i></a>
    <a href="https://github.com/bielng" target="_blank" title="GitHub"><i class="fab fa-github"></i></a>
    <a href="#" title="Skills Without Borders"><i class="fas fa-hands-helping"></i></a>
  </div>

  <div class="fun-fact">
    💡 Fun fact: I believe tech can change the world — and I love coding while watching sci-fi shows 🚀🛸
  </div>
</div>

<!-- Font Awesome & script for dynamic animated skills -->
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
<script>
  // Beautiful curated data for skills with icons (both fontawesome and custom images)
  const skillsSet = [
    { name: "Python", category: "Language", iconType: "fab", icon: "python", color: "#3776AB" },
    { name: "JavaScript", category: "Language", iconType: "fab", icon: "js", color: "#F7DF1E" },
    { name: "HTML5", category: "Web", iconType: "fab", icon: "html5", color: "#E34F26" },
    { name: "CSS3", category: "Web", iconType: "fab", icon: "css3-alt", color: "#1572B6" },
    { name: "Tailwind", category: "CSS", iconType: "fab", icon: "tailwind", color: "#38B2AC" },
    { name: "NumPy", category: "Data Science", iconType: "custom", icon: "https://raw.githubusercontent.com/devicons/devicon/master/icons/numpy/numpy-original.svg" },
    { name: "Pandas", category: "Data Science", iconType: "custom", icon: "https://raw.githubusercontent.com/devicons/devicon/master/icons/pandas/pandas-original.svg" },
    { name: "Seaborn", category: "Viz", iconType: "custom", icon: "https://seaborn.pydata.org/_images/logo-mark-lightbg.svg" },
    { name: "Matplotlib", category: "Plotting", iconType: "custom", icon: "https://upload.wikimedia.org/wikipedia/commons/8/84/Matplotlib_icon.svg" },
    { name: "Scikit-learn", category: "ML", iconType: "custom", icon: "https://upload.wikimedia.org/wikipedia/commons/0/05/Scikit_learn_logo_small.svg" },
    { name: "Power BI", category: "BI", iconType: "custom", icon: "https://www.vectorlogo.zone/logos/microsoft_powerbi/microsoft_powerbi-icon.svg" },
    { name: "MySQL", category: "Database", iconType: "custom", icon: "https://raw.githubusercontent.com/devicons/devicon/master/icons/mysql/mysql-original-wordmark.svg" },
    { name: "Excel", category: "Analytics", iconType: "custom", icon: "https://cdn.worldvectorlogo.com/logos/microsoft-excel-2013.svg" },
    { name: "AWS", category: "Cloud", iconType: "custom", icon: "https://raw.githubusercontent.com/devicons/devicon/master/icons/amazonwebservices/amazonwebservices-original-wordmark.svg" },
    { name: "Jupyter", category: "Notebook", iconType: "custom", icon: "https://raw.githubusercontent.com/devicons/devicon/master/icons/jupyter/jupyter-original-wordmark.svg" },
    { name: "Git", category: "Version Ctrl", iconType: "custom", icon: "https://www.vectorlogo.zone/logos/git-scm/git-scm-icon.svg" },
    { name: "GCP", category: "Cloud", iconType: "custom", icon: "https://www.vectorlogo.zone/logos/google_cloud/google_cloud-icon.svg" },
    { name: "PyCharm", category: "IDE", iconType: "custom", icon: "https://resources.jetbrains.com/storage/products/pycharm/img/meta/pycharm_logo_300x300.png" },
    { name: "VS Code", category: "Editor", iconType: "custom", icon: "https://raw.githubusercontent.com/devicons/devicon/master/icons/vscode/vscode-original.svg" }
  ];

  const grid = document.getElementById('skillsGrid');
  
  function buildCards() {
    grid.innerHTML = '';
    skillsSet.forEach((skill, idx) => {
      const card = document.createElement('div');
      card.className = 'skill-card';
      card.style.setProperty('--order', idx);
      
      const iconDiv = document.createElement('div');
      iconDiv.className = 'skill-icon';
      
      if (skill.iconType === 'fab') {
        const i = document.createElement('i');
        i.className = `fab fa-${skill.icon}`;
        i.style.fontSize = '2.8rem';
        i.style.color = skill.color || '#4FC3F7';
        iconDiv.appendChild(i);
      } else {
        // custom image
        const img = document.createElement('img');
        img.src = skill.icon;
        img.alt = skill.name;
        img.loading = 'lazy';
        img.onerror = () => {
          // fallback icon if image fails
          const fallback = document.createElement('i');
          fallback.className = 'fas fa-code';
          fallback.style.fontSize = '2.5rem';
          fallback.style.color = '#aaa';
          iconDiv.innerHTML = '';
          iconDiv.appendChild(fallback);
        };
        iconDiv.appendChild(img);
      }
      
      const nameSpan = document.createElement('div');
      nameSpan.className = 'skill-name';
      nameSpan.innerText = skill.name;
      
      const catSpan = document.createElement('div');
      catSpan.className = 'skill-cat';
      catSpan.innerText = skill.category;
      
      card.appendChild(iconDiv);
      card.appendChild(nameSpan);
      card.appendChild(catSpan);
      grid.appendChild(card);
    });
  }
  
  buildCards();
</script>
</body>
</html>
