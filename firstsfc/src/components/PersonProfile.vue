<template>
  <div id="app">
    <header>
      <div class="logo">
        <router-link to="/">
          Gian Ace Buaquiña <span class="subtitle">Student</span>
        </router-link>
      </div>
      <nav>
        <ul>
          <li><a href="#about">About Me</a></li>
          <li><a href="#hobbies">Hobbies</a></li>
          <li><a href="#contact">Contact</a></li>
        </ul>
      </nav>
    </header>

    <div class="hero">
      <div class="hero-content">
        <div class="hero-image">
          <img src="@/assets/images/profile-picture.jpg" alt="Gian Ace Buaquiña">
        </div> 
        <div class="hero-text">
          <h1>Hello!</h1>
          <div class="text-container">
            <p>Welcome to my personal space on the web. I'm a passionate individual with diverse interests ranging from technology to creative pursuits.</p>
          </div>
          <a href="#about" class="cta-button">Learn More</a>
        </div>
      </div>
    </div>

    <div class="page-content">
      <section id="about">
        <h2>About Me</h2>
        <p class="about-text">{{ aboutText }}</p>
        <router-link to="/about" class="cta-button" style="margin-top: 2rem;">See More</router-link>
      </section>

      <section id="hobbies">
        <h2>My Hobbies</h2>
        <div class="hobbies-grid">
          <div v-for="hobby in hobbies" :key="hobby.title" class="hobby-item">
            <h3>{{ hobby.title }}</h3>
            <p>{{ hobby.description }}</p>
            <router-link :to="hobby.link" class="see-more cta-button cta-small">See more</router-link>
          </div>
        </div>
      </section>

      <section id="contact">
        <h2>Get In Touch</h2>
        <div class="contact-info">
          <div v-for="contact in contactInfo" :key="contact.type" class="contact-item">
            <div class="contact-icon">
              <img :src="contact.icon" :alt="contact.type">
            </div>
            <div>
              <strong>{{ contact.type }}</strong><br>
              {{ contact.value }}
            </div>
          </div>
        </div>
      </section>
    </div>

    <footer>
      <p>&copy; 2026 Gian. All rights reserved.</p>
    </footer>
  </div>
</template>

<script setup>
import { ref } from 'vue';

// Using reactive data to make the component cleaner
const aboutText = ref("I'm an Information Technology student who enjoys building things with code and figuring out how to solve real-world problems...");

const hobbies = ref([
  { title: 'Photography', description: 'Exploring and capturing each moment.', link: '/hobbies/photography' },
  { title: 'Music', description: 'Discovering new artists and genres.', link: '/hobbies/music' },
  { title: 'Movies', description: 'I luv films that make me cry.', link: '/hobbies/movies' },
  { title: 'Video Games', description: 'Sometimes.', link: '/hobbies/videogames' },
  { title: 'Doomscrolling', description: 'Or maybe watching dumb stuff on Youtube.', link: '/hobbies/doomscrolling' }
]);

const contactInfo = ref([
  { type: 'Email', value: 'gianacebuaquina27@gmail.com', icon: require('@/assets/images/socials/email.png') },
  { type: 'LinkedIn', value: 'https://www.linkedin.com/in/...', icon: require('@/assets/images/socials/linkedin.jpg') }
]);
</script>

<style scoped>
/* Paste the contents of your css/styles.css here */
/* "scoped" ensures these styles only apply to this component */

header {
  display: flex;
  justify-content: space-between;
  padding: 1rem 5%;
  /* ... rest of your styles ... */
}
</style>