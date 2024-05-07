<script setup>
import 'primevue/resources/themes/aura-light-green/theme.css'
import '~/assets/css/reset.css'

import { useToast } from 'primevue/usetoast'

const toast = useToast()

function show() {
  toast.add({ severity: 'info', summary: 'Info', detail: 'This works!!', life: 3000 })
}
</script>

<template>
  <div bg="slate-600" h="100vh 100svh">
    <Toast />
    <Button label="Show Toast" @click="show()" />
  </div>
</template>
