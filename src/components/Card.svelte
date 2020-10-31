<script>
  export let img;
  export let title;
  export let description;
</script>

<style>
  article {
    width: 90%;
    min-width: 288px;
    max-width: 400px;
    margin: 15px auto;
    padding: 15px 15px 25px;
    border-radius: 4px;
    background-color: var(--black);
    box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.16);
  }

  span {
    width: 20px;
    height: 20px;
    display: inline-block;
    margin-bottom: 10px;
    background-size: cover;
  }

  h3 {
    margin-bottom: 15px;
    font-size: 1.8rem;
    color: white;
  }

  p {
    font-size: 1.4rem;
    font-weight: 500;
    line-height: 1.8rem;
    color: #808080;
  }
</style>

<article>
  <span style="background-image: url({img})" />
  <h3>{title}</h3>
  <p>{description}</p>
</article>
