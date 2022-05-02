<script>
  export let variant;
</script>

<button class={variant}>
  <slot>Add</slot>
</button>

<style>
  button {
    color: #ffffff;
    width: 150px;
    height: 40px;
    justify-self: end;
  }
</style>
