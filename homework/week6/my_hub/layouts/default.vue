<template>
  <v-app>
    <toolbar />
    <nuxt class="defalut-style" />
    <v-footer
      fixed
      app
      dark
    >
      <span>&copy; 2019</span>
    </v-footer>
  </v-app>
</template>

<script>
import Toolbar from '@/components/Toolbar'

export default {
  components: {
    Toolbar
  },
  data() {
    return {
    }
  }
}
</script>

<style scoped>
.defalut-style {
  background-color: white;
}
</style>
