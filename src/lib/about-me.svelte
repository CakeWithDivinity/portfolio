<h2 class="section-title">About Me</h2>
<div class="card">
  <div class="content" />
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

  .portrait {
    height: 100%;

    > img {
      height: 100%;
      border-radius: 0rem 2rem 2rem 0rem;
      object-fit: cover;
    }
  }
</style>
