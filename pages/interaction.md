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

<button class="primary" @click="addRow()">Add row</button>
<button class="primary" @click="addColumn()">Add column</button>

<DataTable class="display" :columns="columns" :data="data"></DataTable>

<script setup>

import { ref, reactive } from 'vue'

const count = ref(0)
const columns = reactive([{ title: 'Column' }])
const data = reactive([])

import DataTable from 'datatables.net-vue3';
import DataTablesCore from 'datatables.net-dt';
 
DataTable.use(DataTablesCore);

function addRow() {
	let row = []

	let numColumns = columns.length

	for (var i = 0; i < numColumns; i++) {
		row.push(i)
	}

	data.push(row)
}

function addColumn() {
	let column = { title: "Column" }
	columns.push(column)
}

</script>