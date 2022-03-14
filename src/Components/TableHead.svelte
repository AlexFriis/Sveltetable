<script>
    //export tableHead to be used in PeopleTable.svelte
    export let tableHead;
</script>

<thead>
    <tr>
        <!--Returns an array of a given objects' own enumerable property names(keys)-->
        {#each Object.keys(tableHead[0]) as columnName}
            <th>
                {columnName}
            </th>
        {/each}
    </tr>
</thead>

<style>
    th {
        border: 1px solid black;
    }
</style>