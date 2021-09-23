<script>
  import ContactCard from "./ContactCard.svelte";

  let name = "Satheesh";
  let age = 34;

  $: dogYears = age / 7;
  $: upperCaseName = name.toUpperCase();

  function incrementAge() {
    age += 1;
  }

  function decrementAge() {
    age -= 1;
  }

  function nameInput(event) {
    const enteredValue = event.target.value;
    name = enteredValue;
  }
</script>

<h1>
  Hello {upperCaseName}, your age is {age} ! You are {dogYears} dog years old
</h1>
<button on:click={incrementAge}>Increment age</button>
<button on:click={decrementAge}>Decrement age</button>
<input type="text" value={name} on:input={nameInput} />
<input type="text" bind:value={name} />
<ContactCard />

<style>
  h1 {
    color: purple;
  }
</style>
