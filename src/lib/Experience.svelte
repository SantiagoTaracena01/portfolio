<script>
  import '../styles/experience.css'
  import ExperienceCard from './ExperienceCard.svelte'

  import Figma from '../assets/icons/figma.png'
  import Photoshop from '../assets/icons/photoshop.png'
  import Illustrator from '../assets/icons/illustrator.png'
  import React from '../assets/icons/react.png'
  import Svelte from '../assets/icons/svelte.png'
  import Solid from '../assets/icons/solid.png'

  import Verified from '../assets/icons/verified.png'

  const designExperience = [
    {
      logo: Figma,
      alt: 'Figma logo',
      title: 'Figma',
      verified: Verified,
    }, {
      logo: Photoshop,
      alt: 'Photoshop logo',
      title: 'Photoshop',
      verified: Verified,
    }, {
      logo: Illustrator,
      alt: 'Illustrator logo',
      title: 'Illustrator',
      verified: Verified,
    },
  ]

  const developmentExperience = [
    {
      logo: React,
      alt: 'React logo',
      title: 'React',
      verified: Verified,
    }, {
      logo: Svelte,
      alt: 'Svelte logo',
      title: 'Svelte',
      verified: Verified,
    }, {
      logo: Solid,
      alt: 'Solid logo',
      title: 'Solid',
      verified: Verified,
    },
  ]
</script>

<main class="experience">
  <div class="experience-container">
    {#each designExperience as item}
      <ExperienceCard
        logo={item.logo}
        alt={item.alt}
        title={item.title}
        verified={item.verified}
      />
    {/each}
  </div>
  <div class="experience-container">
    {#each developmentExperience as item}
      <ExperienceCard
        logo={item.logo}
        alt={item.alt}
        title={item.title}
        verified={item.verified}
      />
    {/each}
  </div>
</main>
