<script>
  let strength = 0
  let validations = []

  export function validatePassword(e) {
    const password = e.target.value
    validations = [
      (password.length > 5),
      (password.search(/[A-Z]/) > -1),
      (password.search(/[0-9]/) > -1),
      (password.search(/[$#@!,:;?%&*=+]/) > -1)
    ]

    strength = validations.reduce((acc, cur) => acc + cur)
  }

</script>

<style>
  .strength {
    display: flex;
    height: 20px;
    width: 100%;
  }

  .bar {
    margin-right: 5px;
    height: 100%;
    width: 25%;
    transition: box-shadow 500ms;
    box-shadow: inset 0 20px #1f1f1f;
  }

  .bar-show {
    box-shadow: none;
  }

  .bar:nth-child(1) {
    background: linear-gradient(to right, red, orangered);
  }
  .bar:nth-child(2) {
    background: linear-gradient(to right, orangered, yellow);
  }
  .bar:nth-child(3) {
    background: linear-gradient(to right, yellow, yellowgreen)
  }
  .bar:nth-child(4) {
    background: linear-gradient(to right, yellowgreen, green)
  }

</style>

<div class="strength">
  <span class="bar" />
  <span class="bar" />
  <span class="bar" />
  <span class="bar" />
</div>
