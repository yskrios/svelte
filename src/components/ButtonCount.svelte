<script>
  import { count } from "../store/store.js";
  function handleClick() {
    count.update((n) => n + 1);
  }
</script>

<button on:click={handleClick}>
  CLick {$count === 0 ? "" : $count}
</button>

<style>
  button {
    background-color: #f7f7;
    color: #fff;
    border: none;
    border-radius: 4px;
    padding: 0.5rem;
  }
</style>
