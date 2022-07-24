<template>
  <main>
    <Boot v-if="!bootComplete"/>
    <Interface v-if="bootComplete"/>
  </main>
</template>

<script>
import Interface from '~/components/Interface.vue';

export default {
  components: { Interface },
  name: 'IndexPage',
  data:  () => {
      return {
        bootComplete: false,
      }
  },
  created() {
    this.$nuxt.$on('booted', () => this.booted() );
  }, 
  methods: {
    booted() {
      this.bootComplete = true
    }
  }
}
</script>
