<script>
    //export tableHead to be used in PeopleTable.svelte
    export let tableHead;
</script>

<thead>
    <tr>
        <!--Returns an array of a given objects' own enumerable property names-->
        {#each Object.keys(tableHead[0]) as head}
            <th>
                {head}
            </th>
        {/each}
    </tr>
</thead>