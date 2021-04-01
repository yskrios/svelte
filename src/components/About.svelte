<script>
  import Button from "./Button.svelte";

  let someText = "Frontend Developer at Globant";
  let count = 0;
  let styles = { darkMode: false };
  function handleClick() {
    count += 1;
  }

  function toggle() {
    styles.darkMode = !styles.darkMode;
    window.document.body.classList.toggle("dark-mode");
  }
</script>

<div class="About">
  <p>
    {someText}
  </p>
  {#if !styles.darkMode}
    <p>{someText}</p>
  {:else}
    <p>Hello dark-mode</p>
  {/if}

  <Button text="Click" {count} on:click={handleClick} />
  <Button text="DarkMode" on:click={toggle} />
</div>

<style>
  p {
    color: (--theme-color);
  }
</style>
