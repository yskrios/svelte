<script>
  import About from "./components/About.svelte";
  import Person from "./components/Person.svelte";
  import Skills from "./components/Skills.svelte";
  import Text from "./components/Text.svelte";
  import Input from "./components/Input.svelte";
  import Photos from "./components/Photos.svelte";
  export let name;
  export let lastname;
  let svelteLogo = " https://arepa.s3.amazonaws.com/svelte-logo.png";

  const data = {
    name: "Yessica",
    lastname: "Rios",
    age: "27",
  };
</script>

<main>
  <h1>Hello {name} {lastname}!</h1>
  <About />
  <Text anotherText="Hola!" />
  <Text />
  <Person name={data.name} lastname={data.lastname} age={data.age} />
  <Skills />
  <Input />
  <Photos />
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

  :global(body.dark-mode) {
    background-color: #1d3040;
    color: #bfc2c7;
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
