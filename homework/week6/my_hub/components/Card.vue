<template>
  <div class="card">
    <v-card />
    <a href="">{{ repo }}</a>
    <div class="language">
      <span class="language__dot" />
      <p class="language__text">
        swift
      </p>
      <i class="fas fa-star star" />
      <p class="language__text">
        10000
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Card',
  props: {
    repo: {
      type: String,
      require: true,
      default: 'hahaha'
    }
  }
}
</script>

<style scoped>
.card {
  background-color: white;
  width: 300px;
  height: 100px;
  border: 1px solid black;
  padding: 10px;
}

.language {
  display: flex;
  margin-top: 40px;
}

.language__text {
  display: flex;
  border: 1px solid black;
  height: 20px;
  padding: 0;
  margin-left: 2px;
  margin-right: 5px;
}

.language__dot {
  height: 10px;
  width: 10px;
  background-color: orange;
  border-radius: 50%;
  border: 1px solid black;
  margin-top: 5px;
}

.star {
  border: 1px solid black;
  padding: 0px;
  height: 20px;
  margin-left: 2px;
}
</style>
