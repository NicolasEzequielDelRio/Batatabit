<style>
  header {
    width: 100%;
    height: 334px;
    min-width: 320px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    text-align: center;
    background: linear-gradient(208.83deg, var(--black) 16.69%, var(--orange) 100%);
    position: relative;
  }

  img {
    width: 150px;
    align-self: center;
    margin-top: 45px;
  }

  div {
    width: 90%;
    height: 218px;
    min-width: 288px;
    max-width: 900px;
    align-self: center;
    margin-top: 48px;
    text-align: center;
  }

  h1 {
    font-size: 2.4rem;
    font-weight: bold;
    line-height: 2.6rem;
    color: white;
  }

  p {
    margin-top: 25px;
    font-size: 1.4rem;
    font-weight: 500;
    line-height: 1.8rem;
    color: var(--soft-orange);
  }

  a {
    width: 150px;
    height: 48px;
    display: block;
    margin: 0 auto;
    padding: 15px;
    font-size: 1.4rem;
    font-weight: bold;
    line-height: 1;
    text-decoration: none;
    border-radius: 4px;
    box-shadow: 0px 4px 8px rgba(89, 73, 30, 0.16);
    background: var(--off-white);
    color: var(--black);
    position: absolute;
    left: 0;
    right: 0;
    bottom: -19px;
  }

  span {
    width: 13px;
    height: 8px;
    display: inline-block;
    margin-left: 10px;
    background-image: url(/assets/icons/down-arrow.svg);
  }

  @media (min-width: 568px) {
    header {
      height: 290px;
    }
  }

  @media (min-width: 768px) {
    header {
      height: 285px;
    }

    img {
      width: 250px;
    }

    p {
      font-size: 1.6rem;
    }
  }

  @media (min-width: 1024px) {
    h1 {
      font-size: 2.5rem;
    }
  }
</style>

<header>
  <img src="assets/images/logo.svg" alt="Logo de Batatabit" />
  <div>
    <h1>La próxima revolución en el intercambio de criptomodenas.</h1>
    <p>Batatabit te ayuda a navegar entre los diferentes precios y tendencias.</p>
    <a href="#details">Conoce más <span /></a>
  </div>
</header>
