<script>
    export let tableRow;
</script>

<tbody>
    {#each Object.values(tableRow) as row}
        <tr>
        {#each Object.values(row) as cell}
            <td>{cell}</td>
        {/each}
        </tr>
    {/each}
</tbody>

<style>
    td {
        border: 1px solid black;
    }
</style>