<script>
  let name = "Satheesh";
  let age = 34;

  function incrementAge() {
    age += 1;
  }

  function decrementAge() {
    age -= 1;
  }
</script>

<h1>Hello {name}, my age is {age} !</h1>
<button on:click={incrementAge}>Increment age</button>
<button on:click={decrementAge}>Decrement age</button>

<style>
  h1 {
    color: purple;
  }
</style>
