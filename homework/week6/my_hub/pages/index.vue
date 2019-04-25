<template>
  <div class="profile">
    <profileColumn />
  </div>
</template>

<script>

import ProfileColumn from '@/components/ProfileColumn.vue'

export default {
  components: {
    ProfileColumn
  }
}
</script>

<style scoped>
.profile {
  margin: 100px;
}
</style>
