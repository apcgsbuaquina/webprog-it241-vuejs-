<template>
  <div class="main-layout">
    <header>
      <div class="logo">
        <a href="index.html">Gian Ace Buaquiña <span class="subtitle">Student</span></a>
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
          <img src="/images/profile-picture.jpg" alt="Gian Ace Buaquiña">
        </div> 
        <div class="hero-text">
          <h1>Hello!</h1>
          <div class="text-container">
            <p>Welcome to my personal space on the web. I'm a passionate individual with diverse interests ranging from technology to creative pursuits. I believe in continuous learning and making meaningful connections. Explore my profile to learn more about what drives me and what I enjoy doing.</p>
          </div>
          <a href="#about" class="cta-button">Learn More</a>
        </div>
      </div>
    </div>

    <div class="page-content">
      <section id="about">
        <h2>About Me</h2>
        <p class="about-text">
          I'm an Information Technology student who enjoys building things with code and figuring out how to 
          solve real-world problems. I like learning new tech, improving my skills, and seeing how ideas turn into something that 
          actually works. When I'm not on my laptop, I'm usually out exploring new places, trying different food spots, or just 
          looking for my next favorite meal. I'm easy to work with, adaptable, and I always put effort into what I do.
        </p>
        <a href="javascript:void(0)" class="cta-button" style="margin-top: 2rem;">See More</a>
      </section>

      <section id="hobbies">
        <h2>My Hobbies</h2>
        <div class="hobbies-grid">
          <div v-for="hobby in hobbies" :key="hobby.title" class="hobby-item">
            <h3>{{ hobby.title }}</h3>
            <p>{{ hobby.description }}</p>
            <a class="see-more cta-button cta-small" href="javascript:void(0)">See more</a>
          </div>
        </div>
      </section>

      <section id="contact">
        <h2>Get In Touch</h2>
        <div class="contact-info">
          <div class="contact-item">
            <div class="contact-icon">
              <img src="/images/email.png" alt="Email">
            </div>
            <div>
              <strong>Email</strong><br>
              gianacebuaquina27@gmail.com
            </div>
          </div>
          <div class="contact-item">
            <div class="contact-icon">
              <img src="/images/linkedin.jpg" alt="LinkedIn">
            </div>
            <div>
              <strong>LinkedIn</strong><br>
              https://www.linkedin.com/in/gian-ace-buaqui%C3%B1a-67b9a0321/
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
import './css/styles.css';

const hobbies = [
  { title: 'Photography', description: 'Exploring and capturing each moment.' },
  { title: 'Music', description: 'Discovering new artists and genres.' },
  { title: 'Movies', description: 'I luv films that make me cry.' },
  { title: 'Video Games', description: 'Sometimes.' },
  { title: 'Doomscrolling', description: 'Or maybe watching dumb stuff on Youtube.' }
];
</script>

<style>
</style>