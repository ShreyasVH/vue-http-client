<template>
  <Server :endpoint="endpoint" />
</template>

<script>

import Server from '@/components/Server.vue'

export default {
  name: "DotnetCore",
  components: {
    Server
  },
  computed: {
    endpoint: () => 'https://cors.dotnetcore.com'
  }
}
</script>

<style scoped>

</style>
