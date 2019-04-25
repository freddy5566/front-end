<template>
  <v-toolbar
    dark
    color="black"
    fixed="true"
  >
    <v-btn icon>
      <v-icon>fab fa-github</v-icon>
    </v-btn>
    <div class="toolbar__text-field">
      <v-text-field
        v-model="first"
        solo
        label="Search"
      />
    </div>
    <div>
      <v-btn
        v-for="(button, index) in buttons"
        :key="index"
        color="black"
        class="toolbar__action-button"
      >
        {{ button.name }}
      </v-btn>
    </div>
    <v-spacer />
    <v-btn icon>
      <v-icon>fas fa-bell</v-icon>
    </v-btn>
    <v-btn icon>
      <v-icon>fas fa-plus</v-icon>
    </v-btn>
    <v-avatar size="36px">
      <v-img :src="avatar.path" />
    </v-avatar>
  </v-toolbar>
</template>

<script>
export default {
  name: 'Toolbar',
  data() {
    return {
      isFixed: true,
      buttons: [
        { name: 'Pull requests' },
        { name: 'Issues' },
        { name: 'Marketplace' },
        { name: 'Explore' }
      ],
      avatar: { path: require('@/static/媽宗痛.png') }
    }
  }
}
</script>

<style scoped>
.toolbar__text-field {
  display: flex;
  align-self: center;
  margin: 0 0 0 10px;
  width: 300px;
  height: 50px;
}

.toolbar__action-button {
  margin: 0px;
  padding: 10px;
}
</style>
