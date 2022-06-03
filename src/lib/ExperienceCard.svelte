<script>
  export let logo
  export let alt
  export let title
  export let verified

  import '../styles/experience-card.css'
</script>

<article class="experience-card">
  <img class="experience-logo" src={logo} alt={alt}>
  <span>{title}</span>
  <img class="verified-logo" src={verified} alt="Verified logo">
</article>
