<template>
  <Server :endpoint="endpoint" />
</template>

<script>

import Server from '@/components/Server.vue'

export default {
  name: "Express",
  components: {
    Server
  },
  computed: {
    endpoint: () => 'https://cors.express.com'
  }
}
</script>

<style scoped>

</style>
