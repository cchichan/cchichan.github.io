<template>
  <div class="contact">
    <section class="contact-header">
      <h1>Get in Touch</h1>
      <p>I'd love to hear from you! Feel free to reach out.</p>
    </section>

    <div class="contact-container">
      <section class="contact-info">
        <h2>Contact Information</h2>
        
        <div class="info-item">
          <span class="info-icon">📧</span>
          <div class="info-content">
            <h3>Email</h3>
            <p>contact@cchichan.dev</p>
          </div>
        </div>

        <div class="info-item">
          <span class="info-icon">🐙</span>
          <div class="info-content">
            <h3>GitHub</h3>
            <p><a href="https://github.com/cchichan" target="_blank">github.com/cchichan</a></p>
          </div>
        </div>

        <div class="info-item">
          <span class="info-icon">💼</span>
          <div class="info-content">
            <h3>LinkedIn</h3>
            <p><a href="#" target="_blank">linkedin.com/in/cchichan</a></p>
          </div>
        </div>

        <div class="info-item">
          <span class="info-icon">🐦</span>
          <div class="info-content">
            <h3>Twitter</h3>
            <p><a href="#" target="_blank">@cchichan</a></p>
          </div>
        </div>
      </section>

      <section class="contact-form">
        <h2>Send Me a Message</h2>
        <form @submit.prevent="handleSubmit">
          <div class="form-group">
            <label for="name">Name</label>
            <input 
              type="text" 
              id="name" 
              v-model="form.name" 
              placeholder="Your name"
              required
            />
          </div>
          <div class="form-group">
            <label for="email">Email</label>
            <input 
              type="email" 
              id="email" 
              v-model="form.email" 
              placeholder="your@email.com"
              required
            />
          </div>
          <div class="form-group">
            <label for="subject">Subject</label>
            <input 
              type="text" 
              id="subject" 
              v-model="form.subject" 
              placeholder="Message subject"
              required
            />
          </div>
          <div class="form-group">
            <label for="message">Message</label>
            <textarea 
              id="message" 
              v-model="form.message" 
              rows="5"
              placeholder="Write your message..."
              required
            ></textarea>
          </div>
          <button type="submit" class="submit-btn">Send Message</button>
        </form>
      </section>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const form = ref({
  name: '',
  email: '',
  subject: '',
  message: ''
})

const handleSubmit = () => {
  alert('Thank you for your message! I will get back to you soon.')
  form.value = { name: '', email: '', subject: '', message: '' }
}
</script>

<style scoped>
.contact {
  min-height: 100vh;
  padding: 80px 20px;
  background: #f8f9fa;
}

.contact-header {
  text-align: center;
  margin-bottom: 60px;
}

.contact-header h1 {
  font-size: 3rem;
  color: #333;
  margin-bottom: 20px;
}

.contact-header p {
  font-size: 1.2rem;
  color: #666;
}

.contact-container {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 60px;
  max-width: 1000px;
  margin: 0 auto;
}

.contact-info {
  background: white;
  padding: 40px;
  border-radius: 16px;
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
}

.contact-info h2 {
  font-size: 1.8rem;
  margin-bottom: 30px;
  color: #333;
}

.info-item {
  display: flex;
  align-items: flex-start;
  gap: 15px;
  margin-bottom: 25px;
}

.info-icon {
  font-size: 1.8rem;
  flex-shrink: 0;
}

.info-content h3 {
  font-size: 1.1rem;
  margin-bottom: 5px;
  color: #333;
}

.info-content p {
  color: #666;
}

.info-content a {
  color: #667eea;
  text-decoration: none;
}

.info-content a:hover {
  text-decoration: underline;
}

.contact-form {
  background: white;
  padding: 40px;
  border-radius: 16px;
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
}

.contact-form h2 {
  font-size: 1.8rem;
  margin-bottom: 30px;
  color: #333;
}

.form-group {
  margin-bottom: 20px;
}

.form-group label {
  display: block;
  margin-bottom: 8px;
  font-weight: 600;
  color: #333;
}

.form-group input,
.form-group textarea {
  width: 100%;
  padding: 12px 16px;
  border: 2px solid #e0e0e0;
  border-radius: 8px;
  font-size: 1rem;
  transition: border-color 0.3s ease;
  box-sizing: border-box;
}

.form-group input:focus,
.form-group textarea:focus {
  outline: none;
  border-color: #667eea;
}

.form-group textarea {
  resize: vertical;
}

.submit-btn {
  width: 100%;
  padding: 14px;
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  color: white;
  border: none;
  border-radius: 8px;
  font-size: 1.1rem;
  font-weight: 600;
  cursor: pointer;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.submit-btn:hover {
  transform: translateY(-2px);
  box-shadow: 0 8px 20px rgba(102, 126, 234, 0.4);
}

@media (max-width: 768px) {
  .contact-header h1 {
    font-size: 2.2rem;
  }
  
  .contact-container {
    grid-template-columns: 1fr;
    gap: 30px;
  }
}
</style>