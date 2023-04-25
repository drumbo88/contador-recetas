<script>
	export let valores = []
	export let verDetalle = false

	const toogleDetalle = (valor) => {
		verDetalle = Boolean(valor)
		return false
	}
</script>

<style>
	table th,
	table td {
		text-align: center;
		width: 100px;
	}
</style>

{#if verDetalle}
	<button
		on:click={(e) => {
			toogleDetalle(false)
			e.preventDefault()
		}}>
		Ocultar detalle
	</button>
	<table>
		<tr>
			<th>Lote</th>
			<th>Recetas</th>
		</tr>
		{#each valores as valor, index}
			<tr>
				<td>{index + 1}</td>
				<td>{valor}</td>
			</tr>
		{/each}
	</table>
{:else}
	<button
		on:click={(e) => {
			toogleDetalle(true)
			e.preventDefault()
		}}>
		Mostrar detalle
	</button>
{/if}
