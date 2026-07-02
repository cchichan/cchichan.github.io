<template>
  <div class="projects">
    <section class="projects-header">
      <h1>My Projects</h1>
      <p>A collection of my recent work and personal projects</p>
    </section>

    <section class="projects-grid">
      <div class="project-card" v-for="project in projects" :key="project.id">
        <div class="project-image">
          <img :src="project.image" :alt="project.title" />
        </div>
        <div class="project-content">
          <div class="project-tags">
            <span v-for="tag in project.tags" :key="tag" class="tag">{{ tag }}</span>
          </div>
          <h3>{{ project.title }}</h3>
          <p>{{ project.description }}</p>
          <div class="project-links">
            <a :href="project.github" target="_blank" class="link-btn">GitHub</a>
            <a :href="project.demo" target="_blank" class="link-btn primary">Demo</a>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script setup>
const projects = [
  {
    id: 1,
    title: 'Vue3 Dashboard',
    description: 'A modern admin dashboard built with Vue3 and Tailwind CSS. Features include real-time data visualization, responsive layout, and dark mode support.',
    image: 'https://trae-api-cn.mchost.guru/api/ide/v1/text_to_image?prompt=modern%20admin%20dashboard%20interface%20with%20charts%20and%20data%20visualization&image_size=landscape_16_9',
    tags: ['Vue3', 'Tailwind CSS', 'Chart.js'],
    github: 'https://github.com',
    demo: '#'
  },
  {
    id: 2,
    title: 'E-commerce Store',
    description: 'A full-featured e-commerce application with product catalog, shopping cart, and checkout system.',
    image: 'https://trae-api-cn.mchost.guru/api/ide/v1/text_to_image?prompt=ecommerce%20online%20store%20interface%20with%20products&image_size=landscape_16_9',
    tags: ['React', 'Redux', 'Node.js'],
    github: 'https://github.com',
    demo: '#'
  },
  {
    id: 3,
    title: 'Task Management App',
    description: 'A productivity tool for managing tasks and projects. Supports drag-and-drop, due dates, and team collaboration.',
    image: 'https://trae-api-cn.mchost.guru/api/ide/v1/text_to_image?prompt=task%20management%20app%20interface%20with%20todo%20lists&image_size=landscape_16_9',
    tags: ['Vue3', 'TypeScript', 'Firebase'],
    github: 'https://github.com',
    demo: '#'
  },
  {
    id: 4,
    title: 'Weather App',
    description: 'A weather application that fetches real-time weather data and displays forecasts for any location.',
    image: 'https://trae-api-cn.mchost.guru/api/ide/v1/text_to_image?prompt=weather%20app%20interface%20with%20sun%20and%20clouds&image_size=landscape_16_9',
    tags: ['Vue3', 'OpenWeather API'],
    github: 'https://github.com',
    demo: '#'
  }
]
</script>

<style scoped>
.projects {
  min-height: 100vh;
  padding: 80px 20px;
  background: #f8f9fa;
}

.projects-header {
  text-align: center;
  margin-bottom: 60px;
}

.projects-header h1 {
  font-size: 3rem;
  color: #333;
  margin-bottom: 20px;
}

.projects-header p {
  font-size: 1.2rem;
  color: #666;
}

.projects-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
  gap: 40px;
  max-width: 1400px;
  margin: 0 auto;
}

.project-card {
  background: white;
  border-radius: 16px;
  overflow: hidden;
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.project-card:hover {
  transform: translateY(-10px);
  box-shadow: 0 20px 40px rgba(0, 0, 0, 0.15);
}

.project-image {
  height: 250px;
  overflow: hidden;
}

.project-image img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  transition: transform 0.5s ease;
}

.project-card:hover .project-image img {
  transform: scale(1.05);
}

.project-content {
  padding: 30px;
}

.project-tags {
  display: flex;
  flex-wrap: wrap;
  gap: 8px;
  margin-bottom: 20px;
}

.tag {
  padding: 6px 14px;
  background: #667eea;
  color: white;
  border-radius: 20px;
  font-size: 0.85rem;
}

.project-content h3 {
  font-size: 1.5rem;
  margin-bottom: 15px;
  color: #333;
}

.project-content p {
  color: #666;
  line-height: 1.7;
  margin-bottom: 25px;
}

.project-links {
  display: flex;
  gap: 12px;
}

.link-btn {
  padding: 10px 20px;
  border: 2px solid #ddd;
  border-radius: 8px;
  text-decoration: none;
  color: #666;
  font-weight: 500;
  transition: all 0.3s ease;
}

.link-btn:hover {
  border-color: #667eea;
  color: #667eea;
}

.link-btn.primary {
  background: #667eea;
  border-color: #667eea;
  color: white;
}

.link-btn.primary:hover {
  background: #5a6fd6;
  border-color: #5a6fd6;
}

@media (max-width: 768px) {
  .projects-header h1 {
    font-size: 2.2rem;
  }
  
  .projects-grid {
    grid-template-columns: 1fr;
  }
}
</style>