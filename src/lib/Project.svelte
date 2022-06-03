<script>
  export let firstImage
  export let secondImage
  export let title
  export let description
  export let technologies

  import '../styles/project.css'
</script>

<article class="project">
  <div class="project-images">
    <img src={firstImage} alt="First project showcase">
    <img src={secondImage} alt="Second project showcase">
  </div>
  <div class="project-description">
    <h1>{title}</h1>
    <p>{description}</p>
    <p>Technologies used:</p>
    <div class="technologies">
      {#each technologies as technology}
        <img src={technology} alt="Technology used">
      {/each}
    </div>
  </div>
</article>
