<div class="hero">
  <h1>Hendrik Loewe</h1>
  <p>A young frontend developer based in</p>
  <p>Wuppertal, Germany</p>
</div>

<style lang="scss">
  .hero {
    position: absolute;
    top: 50%;
    left: 7.5%;
    transform: translateY(-50%);

    @media screen and (max-width: $bp-width-small) {
      left: 50%;
      transform: translate(-50%, -50%);
      text-align: center;
    }
  }

  h1 {
    font-size: 6rem;
    color: $white;

    @media screen and (max-width: $bp-width-small) {
      margin-bottom: 2.5rem;
      line-height: 6rem;
    }
  }

  p {
    font-size: 2rem;
    color: $white;
  }
</style>
