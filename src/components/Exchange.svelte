<script>
  import tables from '../tables.js';

  let coins = true;

  function slide() {
    if (coins) {
      document.getElementById('coins').style.display = 'none';
      document.getElementById('commissions').style.display = 'block';
    } else {
      document.getElementById('commissions').style.display = 'none';
      document.getElementById('coins').style.display = 'block';
    }

    coins = !coins;
  }
</script>

<style>
  .exchange {
    padding: 75px 0 30px;
    text-align: center;
  }

  .description {
    width: 90%;
    min-width: 288px;
    max-width: 900px;
    margin: 0 auto;
  }

  .description h2 {
    margin: 40px 0 20px;
    font-size: 2.4rem;
    line-height: 2.6rem;
    color: var(--black);
  }

  .description p {
    margin-bottom: 30px;
    font-size: 1.4rem;
    font-weight: 500;
    line-height: 1.6rem;
    color: #757575;
  }

  .tables {
    max-width: 1024px;
    display: flex;
    justify-content: center;
    align-items: center;
    margin: 35px auto 0;
  }

  .tables div {
    width: 70%;
    height: 360px;
    min-width: 235px;
    max-width: 500px;
    margin: 0 12px;
    font-family: 'Inter', sans-serif;
  }

  .tables div h3 {
    margin-bottom: 15px;
    font-size: 1.8rem;
    line-height: 2.3rem;
  }

  .tables div > span {
    width: 190px;
    height: 30px;
    padding: 8px;
    font-size: 1.2rem;
    border-radius: 8px;
    color: #757575;
  }

  .tables > span {
    width: 12px;
    height: 18px;
    display: inline-block;
    margin-bottom: 34px;
    background: url(/assets/icons/right-arrow.svg) no-repeat;
    background-size: cover;
  }

  .tables .left {
    transform: rotate(180deg);
  }

  #coins h3 {
    color: var(--orange);
  }

  #coins > span {
    background-color: var(--soft-orange);
  }

  #commissions {
    display: none;
  }

  #commissions h3 {
    color: var(--blue);
  }

  #commissions > span {
    background-color: var(--soft-blue);
  }

  table {
    width: 90%;
    height: 250px;
    min-width: 230px;
    max-width: 300px;
    margin: 0 auto 25px;
  }

  table tr:first-of-type td:first-of-type {
    border-top-left-radius: 15px;
  }

  table tr:first-of-type td:last-of-type {
    border-top-right-radius: 15px;
  }

  table tr:last-of-type td:first-of-type {
    border-bottom-left-radius: 15px;
  }

  table tr:last-of-type td:last-of-type {
    border-bottom-right-radius: 15px;
  }

  table tr td {
    width: 50%;
    font-size: 1.6rem;
    font-weight: 500;
    background-color: white;
    color: var(--grey);
  }

  table tr td:last-of-type {
    font-size: 1.4rem;
    font-weight: 400;
    color: #757575;
  }

  table span {
    width: 15px;
    height: 15px;
    display: inline-block;
    margin-left: 10px;
    background-repeat: no-repeat;
    background-size: cover;
  }

  @media (min-width: 568px) {
    .tables div {
      margin: 0;
    }
  }

  @media (min-width: 768px) {
    .tables > span {
      display: none;
    }

    #commissions {
      display: block;
    }
  }
</style>

<section class="exchange">
  <div class="description">
    <figure><img src="assets/images/Bitcoin.svg" alt="Bitcoin" /></figure>
    <h2>Visibilizamos todas las tasas de cambio.</h2>
    <p>
      Traemos información en tiempo real de las casas de cambio y las monedas más importantes del
      mundo.
    </p>
  </div>
  <section class="tables">
    {#if !coins}<span class="left" on:click={slide} />{/if}
    {#each tables as { id, title, latestUpdate, items }}
      <div {id}>
        <h3>{title}</h3>
        <table>
          {#each items as { name, value, icon }}
            <tr>
              <td>{name}</td>
              <td>
                {value}
                {#if icon}<span style="background-image: url({icon})" />{/if}
              </td>
            </tr>
          {/each}
        </table>
        <span><b>Actualizado:</b> {latestUpdate}</span>
      </div>
    {/each}
    {#if coins}<span on:click={slide} />{/if}
  </section>
</section>
