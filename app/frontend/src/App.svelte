<script>
  import { Greet } from "../wailsjs/go/main/App.js";
  import Header from "./components/Header.svelte";

  let resultText = "Please enter your name below 👇";
  let name;

  function greet() {
    Greet(name).then((result) => (resultText = result));
  }
</script>

<Header />
<main>
  <section class="stripe-app-container">
    <div class="heading">
      <h2>{resultText}</h2>
    </div>
       <div class="input-area">
      <input bind:value={name} placeholder="Your name..." />
      <button on:click={greet}>Greet Me</button>
    </div>
    <div class="card-container">
      <div class="card-xs">
        <div class="img"></div>
        <h5 class="name">app name</h5>
      </div>
      <div class="card-xs">
        <div class="img"></div>
        <h5 class="name">app name</h5>
      </div>
    </div>
  </section>
</main>

<style>
  section {
    margin-top: var(--space-md);
    width: var(--app-max-width);

    & .heading {
      margin-bottom: var(--space-sm);
      margin-top: var(--space-sm);
      margin-inline: var(--space-xs);
      font-size: var(--lg-font-size);
    }

    & .card-container {
      display: flex;
    }
  }

  .card-xs {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    width: 120px;
    height: auto;
    margin-inline: var(--space-xs);

    & .img {
      background: black;
      width: 100px;
      height: 100px;
      border-radius: 12px;
    }

    &.name {
      font-size: var(--md-font-size);
    }
  }
</style>
