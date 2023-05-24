<template>
  <Server :endpoint="endpoint" />
</template>

<script>

import Server from '@/components/Server.vue'

export default {
  name: "Phalcon",
  components: {
    Server
  },
  computed: {
    endpoint: () => 'https://cors.phalcon.com'
  }
}
</script>

<style scoped>

</style>
