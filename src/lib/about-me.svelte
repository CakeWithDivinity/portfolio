<script lang="ts">
  interface InfoItem {
    title: string;
    value: string;
  }

  const infoItems: InfoItem[] = [
    { title: 'Age', value: `${getAge()} years` },
    { title: 'Location', value: 'Wuppertal' },
    { title: 'Occupation', value: 'Webdeveloper at Webfabric GmbH' },
    { title: 'Education', value: 'University entrance diploma (832 out of 900 possible points)' },
    { title: 'University', value: 'Aiming for Bachelor of Science in Computer Science' },
    { title: 'Outside of coding', value: 'Fitness, Skating, Solving rubix cubes, Gaming' }
  ];

  function getAge(): number {
    const today = new Date();
    const birthDate = new Date(2003, 7, 13);
    let age = today.getFullYear() - birthDate.getFullYear();
    const m = today.getMonth() - birthDate.getMonth();
    if (m < 0 || (m === 0 && today.getDate() < birthDate.getDate())) {
      age--;
    }
    return age;
  }

  const technologies: string[] = [
    'html5',
    'css3',
    'scss',
    'js',
    'ts',
    'angular',
    'rxjs',
    'ngrx',
    'karma',
    'git'
  ];
</script>

<h2 class="section-title">About Me</h2>
<div class="card">
  <div class="content">
    {#each infoItems as item}
      <span class="info-title">{item.title}:</span>
      <span class="info-value">{item.value}</span>
    {/each}
    <span class="info-title">Technolgies:</span>
    <div class="technologies">
      {#each technologies as technology}
        <img src={`/portfolio/images/logos/${technology}.png`} alt={technology} />
      {/each}
    </div>
  </div>
  <div class="portrait">
    <img src="/portfolio/images/portrait.jpg" alt="Portrait of myself" />
  </div>
</div>

<style lang="scss">
  .card {
    height: 80%;
    width: 100%;
    display: grid;
    grid-template-columns: 1fr auto;
    grid-template-rows: 100%;
    background-color: $primary;
    border-radius: 2rem;
    box-shadow: 4px 4px 4px rgba(0, 0, 0, 0.25);
  }

  .content {
    display: grid;
    grid-template-columns: auto 1fr;
    column-gap: 3rem;
    padding: 5rem;

    .info-title {
      font-size: 2.25rem;
      line-height: 2.25rem;
      color: $white;
    }

    .info-value {
      font-size: 2rem;
      line-height: 2.125rem;
      color: $white;
    }
  }

  .technologies {
    display: flex;
    gap: 1rem;
    flex-wrap: wrap;

    > img {
      height: 3rem;
      filter: drop-shadow(4px 4px 4px rgba(0, 0, 0, 0.25));
      transition: transform 0.25s ease;

      &:hover {
        transform: scale(1.15);
      }
    }
  }

  .portrait {
    height: 100%;

    > img {
      height: 100%;
      border-radius: 0rem 2rem 2rem 0rem;
      object-fit: cover;
    }
  }
</style>
