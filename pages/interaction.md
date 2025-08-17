# Interaction

The count is: {{ count }}

<button class="primary" @click="count++">count++</button>

<label>Text: </label>
<input type="text"></input>
<br>
<input type="numeric"></input>
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

<script setup>

import { ref } from 'vue'

const count = ref(0)

</script>