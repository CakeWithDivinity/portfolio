<script context="module" lang="ts">
  export const prerender = true;
</script>

<script lang="ts">
  import AboutMe from '$lib/about-me.svelte';
  import Hero from '$lib/hero.svelte';
  import Projects from '$lib/projects/projects.svelte';
  import Contact from '$lib/contact.svelte';
</script>

<section class="hero-section">
  <Hero />
</section>

<section class="about-me-section">
  <AboutMe />
</section>

<section class="projects-section">
  <Projects />
</section>

<section class="contact-section">
  <Contact />
</section>

<style lang="scss">
  section {
    width: 100%;
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;

    @media screen and (max-width: $bp-width-small) {
      margin-bottom: 5rem;
    }
  }

  .hero-section {
    position: relative;
  }

  .about-me-section {
    padding-inline: 10rem;

    @media screen and (max-width: $bp-width-small) {
      padding-inline: 1rem;
    }
  }
</style>
