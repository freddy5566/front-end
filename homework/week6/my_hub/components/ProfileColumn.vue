<template>
  <div id="profileColumn">
    <div class="profile__avatar">
      <v-img :src="avatar.path" />
    </div>
    <div class="profile__description">
      <h3>
        媽宗痛
      </h3>
      <p>
        媽宗痛
      </p>

      <br>
      <p>
        窩4媽宗痛
      </p>
      <p>
        最喜歡鹿茸
      </p>
      <br>
      <br>
      <p>
        降龍十八掌算什麼
      </p>
      <p>
        我會油電雙漲
      </p>
      <br>
      <p>哇尬藝</p>
      <p>DNF</p>
      <p>ㄏ勝</p>
      <br>
      <p><strong>@KMT</strong>前任主席</p>
      <br>
    </div>
    <v-btn>
      Edit
    </v-btn>
    <div class="profile__organizations">
      <v-img
        v-for="(organization, index) in organizations"
        :key="index"
        :src="organization.path"
        width="36px"
        height="36px"
        class="profile__organization"
      />
    </div>
  </div>
</template>

<script>
export default {
  name: 'ProfileColumn',
  data() {
    return {
      avatar: { path: require('@/static/媽宗痛.png') },
      organizations: [
        { path: require('@/static/川普.jpeg') },
        { path: require('@/static/蔡英文.jpeg') },
        { path: require('@/static/安倍.jpeg') }
      ]
    }
  }
}
</script>

<style scoped>
h3 {
  font-size: 2rem;
}

p {
  font-size: 1.3rem;
  /* border: 1px solid black; */
  margin: 0px;
}

#profileColumn {
  display: flex;
  flex-direction: column;
  /* border: 1px solid black; */
  width: 250px;
  margin: 0px;
  padding: 0px;
}

.profile__avatar {
  justify-content: center;
}

.profile__description {
  justify-content: center;
}

.profile__organizations {
  display: flex;
}

.profile__organization {
  margin: 10px;
}
</style>
