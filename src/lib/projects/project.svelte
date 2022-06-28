<script lang="ts">
  import type { ProjectItem } from 'src/types/project';

  export let project: ProjectItem | undefined = undefined;
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
    box-shadow: 6px 6px 10px 4px rgba(0, 0, 0, 0.25);
    transition: transform 150ms ease-out;

    &:hover {
      transform: scale(1.125);
    }

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
      color: $white;
    }

    > p {
      text-align: justify;
      color: $white;
    }
  }
</style>
