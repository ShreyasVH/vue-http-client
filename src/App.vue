<template>
  <div>
    <Play />
    <Springboot />
  </div>
</template>

<script>
  import Play from '@/components/Play.vue';
  import Springboot from '@/components/Springboot.vue';
  export default {
    name: 'App',
    components: {
      Play,
      Springboot
    }
  }
</script>

