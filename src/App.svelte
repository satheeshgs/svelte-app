<script>
  let name = "Satheesh";
  let age = 34;

  $: dogYears = age / 7;

  function incrementAge() {
    age += 1;
  }

  function decrementAge() {
    age -= 1;
  }
</script>

<h1>Hello {name}, your age is {age} ! You are {dogYears} dog years old</h1>
<button on:click={incrementAge}>Increment age</button>
<button on:click={decrementAge}>Decrement age</button>

<style>
  h1 {
    color: purple;
  }
</style>
