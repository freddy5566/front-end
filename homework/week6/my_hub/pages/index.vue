<template>
  <div class="grid-box">
    <div class="profile">
      <profileColumn />
    </div>
    <card
      class="card"
      repo="cs193p-2017-fall-demo-and-solution"
    />
  </div>
</template>

<script>

import ProfileColumn from '@/components/ProfileColumn.vue'
import Card from '@/components/Card.vue'

export default {
  components: {
    ProfileColumn,
    Card
  }
}
</script>

<style scoped>
.grid-box {
  display: grid;
  grid-template-columns: 20% 80%;
}
.profile {
  margin: 100px;
}

.card {
  margin: 100px 10px 10px 10px;
}
</style>
