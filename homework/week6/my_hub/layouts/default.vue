<template>
  <v-app>
    <toolbar />
    <nuxt />
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
