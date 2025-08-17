# Interaction

The count is: {{ count }}

<button class="primary" @click="count++">count++</button>

<label>Text: </label>
<input type="text"></input>
<br>
<input type="number"></input>
<br>
<label>Checkbox: </label>
<input type="checkbox"></input>
<br>
<input type="range"></input>
<br>
<input type="file"></input>
<br>
<input type="datetime-local"></input>
<br>
<textarea></textarea>

<DataTable class="display" :columns="columns" :data="data">
</DataTable>

<script setup>
	
import { ref } from 'vue'

const count = ref(0)

import DataTable from 'datatables.net-vue3';
import DataTablesCore from 'datatables.net-dt';
 
DataTable.use(DataTablesCore);

const columns = [
  { title: 'Name' },
  { title: 'Position' },
  { title: 'Office' },
  { title: 'Extension' },
  { title: 'Start date' },
  { title: 'Salary' },
];

const data = [
	["Joe Guy", "Head Boss", "The", 1, "1/2/3", "Money"]
]

</script>