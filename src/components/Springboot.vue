<template>
  <Server :endpoint="endpoint" />
</template>

<script>

import Server from '@/components/Server.vue'

export default {
  name: "Springboot",
  components: {
    Server
  },
  computed: {
    endpoint: () => 'http://localhost:9013'
  }
}
</script>

<style scoped>

</style>