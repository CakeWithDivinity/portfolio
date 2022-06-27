<script lang="ts">
  import type { ProjectContent } from 'src/types/project';

  export let project: ProjectContent | undefined = undefined;
</script>

{#if project}
  <div class="project">
    <img src={project.imageSrc} alt={project.imageAlt} />
    <h3>{project.title}</h3>
    <p>{project.text}</p>
  </div>
{/if}

<style lang="scss">
  .project {
    display: flex;
    flex-direction: column;
    align-items: center;
    width: 20rem;
    color: $white;
    background-color: $primary;
    border-radius: 2rem;

    > *:not(img) {
      padding-inline: 2rem;
    }

    img {
      width: 100%;
      border-radius: 2rem 2rem 0rem 0rem;
    }

    > h3 {
      font-size: 2rem;
      margin-top: 0.5rem;
    }

    > p {
      text-align: justify;
    }
  }
</style>
