# Interaction

The count is: {{ count }}

<button @click="count++">count++</button>

<script setup>

import { ref } from 'vue'

const count = ref(0)

</script>