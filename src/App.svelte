<script>
  import svelteLogo from "./assets/svelte.svg";
  import viteLogo from "/vite.svg";
  import Counter from "./lib/Counter.svelte";
  import ChildComponent from "./component/ChildComponent.svelte";
  let count = 0;
  $: doubled = count * 2;
  let hobby = "";
  let time = 1;
</script>

<h1>Basics of Svelte</h1>
<main>
  <div>
    <p>---Practice State---</p>
    <p>Counter value is: {count}</p>

    <button on:click={() => count++}>Incriment</button>
    <button on:click={() => count--}>Decriment</button>
  </div>
  <br />
  <div>
    <p>Doubled is {doubled}</p>

    <p>---Reactive Declarations and Updates---</p>
    <button on:click={() => (count += 1)}>Doubled Increment</button>
  </div>
  <br />
  <div>
    <p>---Props and State Management---</p>
    <ChildComponent name="Svelte" country="Bangladesh" />
  </div>
  <br />

  <div>
    <h5>Simple Data Binding</h5>
    <p>
      We can use bind: to create two-way bindings between an input and a
      variable.
    </p>
    <h5>My hobbies are: {hobby}</h5>
    <input bind:value={hobby} placeholder="Enter your hobby" />
  </div>
  <br />
  <div>
    <p>Event Handling: Use on:event to handle events</p>
    <button on:click={() => (time += 1)}>
      Clicked {time}
      {time <= 1 ? "hour" : "hours"}
    </button>
  </div>
</main>
