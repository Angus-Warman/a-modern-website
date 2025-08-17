# Interaction

The count is: {{ count }}

<button class="primary" @click="count++">count++</button>

<input type="text"></input>
<br>
<input type="number"></input>
<br>
<input type="range"></input>
<br>
<input type="file"></input>
<br>
<textarea></textarea>

<script setup>

import { ref } from 'vue'

const count = ref(0)

</script>