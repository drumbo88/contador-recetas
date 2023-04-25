<script>
  export let valores = []
  export let suma = 0
</script>

<style>
  table th,
  table td {
    text-align: center;
    width: 100px;
    font-size: 30px;
  }
</style>


<table>
  <tr>
    <th>Lotes</th>
    <th>Recetas</th>
    <th>Prom.</th>
  </tr>
  <tr>
    <td>{valores.length}</td>
    <td>{suma}</td>
    <td>{valores.length ? (suma / valores.length).toFixed(2) : '-'}</td>
  </tr>
</table>
