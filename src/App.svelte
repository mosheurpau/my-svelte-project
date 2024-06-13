<script>
  import svelteLogo from "./assets/svelte.svg";
  import viteLogo from "/vite.svg";
  import Counter from "./lib/Counter.svelte";
  let count = 0;
</script>

<h1>Practice State</h1>
<main>
  <div>
    <p>Counter value is: {count}</p>

    <button on:click={() => count++}>Incriment</button>
    <button on:click={() => count--}>Decriment</button>
  </div>
</main>
