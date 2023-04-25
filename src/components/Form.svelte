<script>
  export let addValor
  export let input = 0

  const handleEnter = (e) => {
    if (e.key == 'Enter') {
      addValor(input)
      e.preventDefault()
    }
  }
</script>

<form on:submit|preventDefault>
  <p>Ingrese la cantidad de recetas del lote:</p>
  <input
    type="number"
    bind:value={input}
    on:keyup|preventDefault={handleEnter} />
</form>
