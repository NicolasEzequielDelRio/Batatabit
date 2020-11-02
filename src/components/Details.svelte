<script>
  import details from '../productDetails.js';
  import Card from './Card.svelte';
</script>

<style>
  #details {
    min-width: 320px;
    padding: 25px 10px;
    background-color: var(--warm-black);
    position: relative;
  }

  span {
    width: 40px;
    height: 25px;
    margin: 0 auto;
    background-image: url(/assets/icons/batata.svg);
    position: absolute;
    top: -10px;
    left: 0;
    right: 0;
  }

  div {
    width: 90%;
    min-width: 288px;
    margin: 40px auto 0;
    text-align: center;
  }

  div h2 {
    margin-bottom: 20px;
    font-size: 2.4rem;
    line-height: 2.6rem;
    color: white;
  }

  div p {
    margin-bottom: 30px;
    font-size: 1.4rem;
    font-weight: 500;
    line-height: 1.8rem;
    color: #808080;
  }

  @media (min-width: 768px) {
    #details section {
      max-width: 1024px;
      display: grid;
      grid-template-columns: 1fr 1fr;
      margin: 0 auto;
    }
  }
</style>

<section id="details">
  <span />
  <div>
    <h2>Creamos un producto sin comparación.</h2>
    <p>Confiable y diseñado para su uso diario.</p>
  </div>
  <section>
    {#each details as { img, title, description }}
      <Card {img} {title} {description} />
    {/each}
  </section>
</section>
