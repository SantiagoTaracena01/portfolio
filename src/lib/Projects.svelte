<script>
  import Carousel from 'svelte-carousel'
  import Project from './Project.svelte'
  import '../styles/projects.css'

  import ViewOne from '../assets/projects/view-01.jpg'
  import ViewTwo from '../assets/projects/view-02.jpg'
  import GeniusOne from '../assets/projects/genius-01.jpg'
  import GeniusTwo from '../assets/projects/genius-02.jpg'
  import KodonoteOne from '../assets/projects/kodonote-01.jpg'
  import KodonoteTwo from '../assets/projects/kodonote-02.jpg'
  import JavaOne from '../assets/projects/java-01.jpg'
  import JavaTwo from '../assets/projects/java-02.jpg'
  import PortfolioOne from '../assets/projects/portfolio-01.jpg'
  import PortfolioTwo from '../assets/projects/portfolio-02.jpg'

  import React from '../assets/icons/react.png'
  import Flask from '../assets/icons/flask.png'
  import Postgres from '../assets/icons/postgresql.png'
  import Sass from '../assets/icons/sass.png'
  import Webpack from '../assets/icons/webpack.png'
  import Firebase from '../assets/icons/firebase.png'
  import Figma from '../assets/icons/figma.png'
  import Photoshop from '../assets/icons/photoshop.png'
  import Illustrator from '../assets/icons/illustrator.png'
  import Svelte from '../assets/icons/svelte.png'
  import Css from '../assets/icons/css.png'
  import Vite from '../assets/icons/vite.jpg'

  const projects = [
    {
      firstImage: ViewOne,
      secondImage: ViewTwo,
      title: 'View',
      description: 'A nice web streaming service to watch movies. Primarly focused on getting analytics and data administration.',
      technologies: [React, Flask, Postgres,],
    }, {
      firstImage: GeniusOne,
      secondImage: GeniusTwo,
      title: 'Genius Clone',
      description: 'Genius (website to check music news and lyrics) clone. Pixel-perfectly made minimalistic user interface.',
      technologies: [React, Sass, Webpack,],
    }, {
      firstImage: KodonoteOne,
      secondImage: KodonoteTwo,
      title: 'Kodonote',
      description: 'Online notebook designed for coders and CS students. Focused on personalization and details in general.',
      technologies: [React, Webpack, Firebase,],
    }, {
      firstImage: JavaOne,
      secondImage: JavaTwo,
      title: 'Modern Web Java',
      description: 'Java official website UX/UI redesign. Designed to be a modern version of Java\'s official website.',
      technologies: [Figma, Photoshop, Illustrator,],
    }, {
      firstImage: PortfolioOne,
      secondImage: PortfolioTwo,
      title: 'My Portfolio',
      description: 'My own portfolio, made from zero with technologies I learned on the road, like Vite and Svelte.',
      technologies: [Svelte, Css, Vite,],
    }
  ]
</script>

<main class="projects-container">
  <div class="carousel-container">
    <Carousel
      autoplay
      autoplayDuration={10000}
      autoplayProgressVisible
      pauseOnFocus
    >
      {#each projects as project}
        <Project
          firstImage={project.firstImage}
          secondImage={project.secondImage}
          title={project.title}
          description={project.description}
          technologies={project.technologies}
        />
      {/each}
    </Carousel>
  </div>
</main>
