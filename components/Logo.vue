<!--
  Logo image that disappears when no path is set or the file is missing,
  so the template works before you add logo files to public/.
-->
<script setup lang="ts">
import { ref, watch } from 'vue'

const props = defineProps<{ src?: string }>()
const missing = ref(false)
watch(() => props.src, () => { missing.value = false })
</script>

<template>
  <img v-if="src && !missing" :src="src" alt="" @error="missing = true" />
</template>
