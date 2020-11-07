<template>
<div v-if="enabled('view:experimental')">
  <slot />
</div>
</template>

<script>
import {
  hasPermissions
} from '@bcwdev/auth0provider-client'
export const enabled = hasPermissions
</script>

<style scoped>
</style>
