<script>
import TableHead from './TableHead.svelte';
import TableRow from './TableRow.svelte';
import { faker } from "@faker-js/faker";

function generatePeople(count) {

    let tableData = [];

    while (count != 0) {
        const person = {
            name: faker.name.findName(),
            email: faker.internet.email(),
            phone: faker.phone.phoneNumber(),
            vehicle: faker.vehicle.vehicle(),
        };
        tableData.push(person);
        count--;
}
return tableData;
};

let tableData = generatePeople(15);
</script>

<table>
    <TableHead tableHead={tableData}/>
    <TableRow tableRow={tableData}/>
    
</table>