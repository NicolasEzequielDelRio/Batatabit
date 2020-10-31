<script>
  import Header from './components/Header.svelte';
  import Exchange from './components/Exchange.svelte';
  import Details from './components/Details.svelte';
</script>

<style>
  main {
    background-color: var(--off-white);
  }
</style>

<Header />
<main>
  <Exchange />
  <Details />
</main>
