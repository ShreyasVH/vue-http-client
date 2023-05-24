<template>
  <div>
    <Play />
    <br />
    <hr />
    <br />
    <Springboot />
    <br />
    <hr />
    <br />
    <Phalcon />
    <br />
    <hr />
    <br />
    <Express />
    <br />
    <hr />
    <br />
    <DotnetCore />
  </div>
</template>

<script>
  import Play from '@/components/Play.vue';
  import Springboot from '@/components/Springboot.vue';
  import Phalcon from '@/components/Phalcon.vue';
  import Express from '@/components/Express.vue';
  import DotnetCore from '@/components/DotnetCore.vue';
  export default {
    name: 'App',
    components: {
      Play,
      Springboot,
      Phalcon,
      Express,
      DotnetCore
    }
  }
</script>

