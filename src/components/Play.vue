<template>
  <Server :endpoint="endpoint" />
</template>

<script>

import Server from '@/components/Server.vue'

export default {
  name: "Play",
  components: {
    Server
  },
  computed: {
    endpoint: () => 'http://localhost:9012'
  }
}
</script>

<style scoped>

</style>