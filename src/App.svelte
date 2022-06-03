<script>
  import Typewriter from 'svelte-typewriter'
  import Header from './lib/Header.svelte'
  import About from './lib/About.svelte'
  import Experience from './lib/Experience.svelte'
  import Projects from './lib/Projects.svelte'
  import Contact from './lib/Contact.svelte'
  import './styles/app.css'

  let animationHasFinished = false
</script>

<div class="typewriter-animation-container">
  <Typewriter cascade interval={[30, 60, 90]} on:done={() => {
    animationHasFinished = true
  }}>
    <h1 class="initial-header">Hi! My name is Santiago,</h1>
    <p class="initial-text">and I love to keep things simple!</p>
  </Typewriter>
</div>
{#if (animationHasFinished)}
  <div class="container">
    <div id="home" class="home rendering-element">
      <Header />
    </div>
    <div id="about" class="about rendering-element">
      <About />
    </div>
    <div id="experience" class="experience rendering-element">
      <Experience />
    </div>
    <div id="projects" class="projects rendering-element">
      <Projects />
    </div>
    <div id="contact" class="contact rendering-element">
      <Contact />
    </div>
  </div>
{/if}
