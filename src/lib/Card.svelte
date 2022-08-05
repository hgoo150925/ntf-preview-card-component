<script>
  import { data } from '../data';
</script>

<main>
  <div class="container">
    {#each data as { title, paragraph, eth, eth_text, equilibrium, icon_ethereum, icon_clock }}
      <img class="equilibrium--img" src={equilibrium} alt="Equilibrium" />
      <div class="container__text">
        <h1>{title}</h1>
        <p>{paragraph}</p>
      </div>
      <div class="container__price">
        <ul>
          <li><img src={icon_ethereum} alt="icon-ethereum" /> {eth}</li>
          <li><img src={icon_clock} alt="icon-clock" /> {eth_text}</li>
        </ul>
      </div>
    {/each}
  </div>
</main>

<style>
  .equilibrium--img {
    border-radius: 3.5rem;
    padding: 2.5rem;
    width: 35rem;
  }
  .container {
    background-color: hsl(216, 50%, 16%);
    border-radius: 1rem;
    margin: 15rem auto;
    max-width: 35.5rem;
    height: 59.6rem;
  }
  .container__text h1 {
    color: #fff;
    font-size: 2.2rem;
    font-weight: 600;
  }
  .container__text p {
    color: hsl(215, 51%, 70%);
    font-size: 1.8rem;
    font-weight: 300;
    margin: 2rem 0 0 0;
  }
  .container__text {
    font-family: 'Outfit', sans-serif;
    margin: 0.5rem 0 0 2.5rem;
  }

  .container__price {
    font-family: 'Outfit', sans-serif;
    margin: 1rem 0 0 0;
  }
  ul {
    list-style: none;
    display: flex;
    gap: 1rem;
  }
  ul li {
    justify-content: space-around;
  }
  ul li:nth-child(1)::before {
    content: '';
    background-image: url('../../src/assets/images/icon-ethereum.svg');
    background-repeat: no-repeat;
    background-size: cover;
    background-position: center;
    left: 0;
    top: 50%;
    transform: translateY(-50%);
  }
  ul li:nth-child(1) {
    color: hsl(178, 100%, 50%);
    font-size: 1.5rem;
    font-weight: 900;
  }
  ul li:nth-child(2) {
    color: hsl(215, 51%, 70%);
  }
</style>
