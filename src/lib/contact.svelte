<script lang="ts">
  import type { ContactItem } from 'src/types/contact-item';

  const contactItems: ContactItem[] = [
    {
      imagePath: '/portfolio/images/logos/discord.png',
      imageAlt: 'Discord Logo',
      title: 'CakeWithDivinity#3141'
    },
    {
      imagePath: '/portfolio/images/logos/email.png',
      imageAlt: 'Email',
      title: 'hendrikloewe3@gmail.com',
      url: 'mailto:hendrikloewe3@gmail.com'
    },
    {
      imagePath: '/portfolio/images/logos/github.png',
      imageAlt: 'GitHub Profile',
      title: 'CakeWithDivinity',
      url: 'https://github.com/CakeWithDivinity'
    },
    {
      imagePath: '/portfolio/images/logos/linkedin.png',
      imageAlt: 'LinkedIn Profile',
      title: 'Hendrik Loewe',
      url: 'https://www.linkedin.com/in/hendrik-loewe-04ba2b202/'
    }
  ];
</script>

<h2 class="section-title">Get In Contact</h2>
<div class="contact-list">
  {#each contactItems as item}
    <div class="contact-item">
      <img src={item.imagePath} alt={item.imageAlt} />
      {#if item.url}
        <a href={item.url}>{item.title}</a>
      {:else}
        <p>{item.title}</p>
      {/if}
    </div>
  {/each}
</div>

<style lang="scss">
  .contact-list {
    height: 80%;
    width: 100%;
    display: flex;
    flex-direction: column;
    gap: 1.5rem;
    padding-inline: 30%;

    @media screen and (max-width: $bp-width-small) {
      padding-inline: 1rem;
    }
  }

  .contact-item {
    width: 100%;
    height: 5rem;
    display: flex;
    justify-content: center;
    align-items: center;
    position: relative;
    padding: 1.5rem;
    background-color: $primary;
    border-radius: 1rem;
    box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);

    > img {
      position: absolute;
      left: 1.5rem;
      top: 50%;
      transform: translateY(-50%);
      height: 4rem;

      @media screen and (max-width: $bp-width-small) {
        position: unset;
        transform: unset;
      }
    }

    > p,
    > a {
      color: $white;
      font-size: 2rem;
      text-decoration: none;

      @media screen and (max-width: $bp-width-small) {
        font-size: 1.5rem;
        text-align: center;
        flex-grow: 1;
      }
    }

    @media screen and (max-width: $bp-width-small) {
      justify-content: space-between;
    }
  }
</style>
