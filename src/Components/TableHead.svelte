<script>
    export let tableHead;
</script>


<thead>
    <tr>
        {#each Object.keys(tableHead[0]) as head}
            <th>
                {head}
            </th>
        {/each}
    </tr>
</thead>