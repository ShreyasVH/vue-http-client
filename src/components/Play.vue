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
    endpoint: () => 'https://cors.playframework.com'
  }
}
</script>

<style scoped>

</style>
