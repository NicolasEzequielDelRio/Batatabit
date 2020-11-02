<script>
  import Header from './components/Header.svelte';
  import Exchange from './components/Exchange.svelte';
  import Details from './components/Details.svelte';
  import Footer from './components/Footer.svelte';
</script>

<style>
  main {
    background-color: var(--off-white);
  }

  section {
    height: 50vh;
    min-width: 320px;
    padding-top: 60px;
    background-image: url(/assets/images/bitcoinbaby2x.jpg);
    background-repeat: no-repeat;
    background-size: cover;
    background-position: center;
  }

  section h2 {
    font-size: 2.4rem;
    text-align: center;
    color: white;
  }

  @media (min-width: 568px) {
    section {
      max-height: 450px;
      display: flex;
      align-items: center;
      justify-content: center;
      padding: 0;
    }
  }

  @media (min-width: 640px) {
    section h2 {
      font-size: 3.2rem;
    }
  }
</style>

<Header />
<main>
  <Exchange />
  <Details />
  <section>
    <h2>Conócelo hoy.</h2>
  </section>
</main>
<Footer />
