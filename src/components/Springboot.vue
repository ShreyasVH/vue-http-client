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
    endpoint: () => 'https://cors.springboot.com'
  }
}
</script>

<style scoped>

</style>
