<script lang="ts">
  import Project from './project.svelte';
  import type { ProjectContent } from 'src/types/project';

  const comingSoonProject: ProjectContent = {
    imageSrc: 'https://picsum.photos/300/200',
    imageAlt: 'Placeholder image for an unfinished project',
    text: `Lorem ipsum dolor sit amet, consectetur adipiscing
             elit. Proin cursus ligula non aliquet maximus. 
             Cras non pellentesque leo, sit amet rhoncus mi. Nullam 
             lacinia accumsan metus eu aliquet. Etiam viverra mi at
             lacinia pulvinar. Sed et nulla sed nibh dapibus viverra
            sit amet eu enim.`,
    title: 'Coming soon...'
  };

  const projects: ProjectContent[] = [comingSoonProject, comingSoonProject, comingSoonProject];
</script>

<h2 class="section-title">Projects</h2>
<div class="project-container">
  {#each projects as project}
    <Project bind:project />
  {/each}
</div>

<style lang="scss">
  .project-container {
    display: flex;
    justify-content: space-between;
    gap: 5rem;
    height: 60%;
    padding-inline: 5rem;
  }
</style>
