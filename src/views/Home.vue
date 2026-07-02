<template>
  <div class="home">
    <section class="hero">
      <div class="hero-content">
        <h1>Hi, I'm cchichan</h1>
        <p class="subtitle">Frontend Developer & Tech Enthusiast</p>
        <p class="description">
          I'm passionate about building beautiful, interactive web experiences 
          with modern technologies. Welcome to my personal website!
        </p>
        <div class="hero-links">
          <router-link to="/projects" class="btn btn-primary">View Projects</router-link>
          <router-link to="/contact" class="btn btn-secondary">Get in Touch</router-link>
        </div>
      </div>
    </section>

    <section class="skills">
      <h2>Skills</h2>
      <div class="skills-grid">
        <div class="skill-card">
          <span class="skill-icon">💻</span>
          <h3>Frontend Development</h3>
          <p>Vue.js, React, JavaScript, TypeScript</p>
        </div>
        <div class="skill-card">
          <span class="skill-icon">🎨</span>
          <h3>UI/UX Design</h3>
          <p>CSS3, SCSS, Responsive Design, Figma</p>
        </div>
        <div class="skill-card">
          <span class="skill-icon">🚀</span>
          <h3>Tools & DevOps</h3>
          <p>Git, Vite, Webpack, Docker</p>
        </div>
      </div>
    </section>
  </div>
</template>

<style scoped>
.home {
  min-height: 100vh;
}

.hero {
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  color: white;
  padding: 100px 20px;
  text-align: center;
}

.hero-content {
  max-width: 800px;
  margin: 0 auto;
}

.hero h1 {
  font-size: 3.5rem;
  margin-bottom: 20px;
}

.subtitle {
  font-size: 1.5rem;
  opacity: 0.9;
  margin-bottom: 30px;
}

.description {
  font-size: 1.1rem;
  line-height: 1.8;
  opacity: 0.85;
  margin-bottom: 40px;
}

.hero-links {
  display: flex;
  gap: 15px;
  justify-content: center;
  flex-wrap: wrap;
}

.btn {
  padding: 14px 32px;
  border-radius: 8px;
  text-decoration: none;
  font-weight: 600;
  transition: all 0.3s ease;
  display: inline-block;
}

.btn-primary {
  background: white;
  color: #667eea;
}

.btn-primary:hover {
  transform: translateY(-2px);
  box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
}

.btn-secondary {
  border: 2px solid white;
  color: white;
  background: transparent;
}

.btn-secondary:hover {
  background: white;
  color: #667eea;
}

.skills {
  padding: 80px 20px;
  background: #f8f9fa;
}

.skills h2 {
  text-align: center;
  font-size: 2.5rem;
  margin-bottom: 50px;
  color: #333;
}

.skills-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 30px;
  max-width: 1200px;
  margin: 0 auto;
}

.skill-card {
  background: white;
  padding: 40px;
  border-radius: 12px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  text-align: center;
  transition: transform 0.3s ease;
}

.skill-card:hover {
  transform: translateY(-5px);
}

.skill-icon {
  font-size: 3rem;
  margin-bottom: 20px;
}

.skill-card h3 {
  font-size: 1.4rem;
  margin-bottom: 15px;
  color: #333;
}

.skill-card p {
  color: #666;
  line-height: 1.6;
}

@media (max-width: 768px) {
  .hero h1 {
    font-size: 2.5rem;
  }
  
  .subtitle {
    font-size: 1.2rem;
  }
  
  .skills h2 {
    font-size: 2rem;
  }
}
</style>