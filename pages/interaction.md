# Interaction

The count is: {{ count }}

<button class="primary" @click="count++">count++</button>

<script setup>

import { ref } from 'vue'

const count = ref(0)

</script>