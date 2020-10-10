<script context="module">
  import Form from './Form.svelte'
</script>

<style>
  main {
    height: 100vh;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }

  h1 {
    font-family: 'Roboto';
    font-weight: 700;
    text-align: center;
  }
</style>

<!-- HTML-->
<main>
  <h1>Sign Up</h1>

  <Form />
</main>
