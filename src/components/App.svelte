<script>
  import Contadores from './Contadores.svelte'
  import Detalles from './Detalles.svelte'
  import Form from './Form.svelte'

  let valores = []
  let suma = 0
  let input = ''

  const addValor = (valor) => {
    if (!valor || isNaN(valor)) return alert('Ingrese un número válido.')

    valores = [...valores, valor]
    suma += parseInt(valor)
    input = ''
  }
</script>

<h1>Contador de recetas</h1>
<Form bind:input {addValor} />
<Contadores {valores} {suma} />
<Detalles {valores} />
