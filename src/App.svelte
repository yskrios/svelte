<script>
  import About from "./components/About.svelte";
  export let name;
  export let lastname;
  let svelteLogo = " https://arepa.s3.amazonaws.com/svelte-logo.png";
</script>

<main>
  <h1>Hello {name} {lastname}!</h1>
  <About />
  <img src={svelteLogo} alt="Logo de svelte" />
</main>

<style>
  :global(body) {
    background-color: #f2f2f2;
    color: #333;
  }

  :global(:root) {
    --theme-color: purple;
  }

  main {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
  }

  h1 {
    color: #ff3e00;
    text-transform: uppercase;
    font-size: 4em;
    font-weight: 100;
  }

  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>
