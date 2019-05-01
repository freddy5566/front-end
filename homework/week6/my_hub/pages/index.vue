<template>
  <div class="grid-box">
    <div class="profile">
      <profileColumn />
    </div>
    <div class="personal-section">
      <div class="nav__buttons">
        <v-btn
          v-for="(button, index) in navButtons"
          :key="index"
          small
        >
          {{ button.buttonName }}
        </v-btn>
      </div>
      <div class="section-title">
        <p>Pined</p>
      </div>
      <div class="repos">
        <card
          v-for="(repo, index) in repos"
          :key="index"
          class="repos__card"
          :repo="repo.repoName"
        />
      </div>
      <div class="section-title">
        <p>10000 contributions in last year</p>
      </div>
      <div class="activities">
        <div class="activities__images">
          <v-img :src="activities.path" />
          <div class="activities__strategy">
            <div class="activities__strategy__buttons">
              <v-btn
                v-for="(repo, index) in contributedRepos"
                :key="index"
                small
              >
                {{ repo.repoName }}
              </v-btn>
            </div>
            <div class="activities__description">
              <div class="description__text">
                <strong>
                  Activities Overview
                </strong>
                <p>
                  Contributed to polydice/iCook-iOS, jamfly/Vocal-Fairy-IOS, jamfly/undergraduate-goal and 5 other repositories
                </p>
              </div>
              <div class="description__image">
                <v-img :src="activityGraph.path" />
              </div>
            </div>
          </div>
        </div>
        <div class="activities__buttons">
          <v-btn
            v-for="(button, index) in activityButtons"
            :key="index"
            small
          >
            {{ button.year }}
          </v-btn>
        </div>
      </div>
      <div class="contribution__block">
        <div class="section-title">
          <p>Contribution activity</p>
          <div class="contribution__description">
            <span>Create 49 commits in 6 repositories</span><br>
            <span>jamfly/WWDC-2019 19 commits</span><br>
            <span>jamfly/mirco-lab 9 commits</span><br>
            <span>NTUT-npc/TAT-IOS 0 commits</span><br>
            <span>jamfly/algirithm-and-data-structure-review 6 commits</span><br>
            <span>polydice/iCook-IOS 3 commits</span><br><br>
            <span>Created a pull request in NTUT-NPC/TAT-IOS that received 1 comment</span>
          </div>
          <div class="contribution__comment">
            <div class="contribution__description">
              <span>Feature/setUp login</span><br>
              <span>LoginViewController store token within touched/foced store account it still looks shitty, but it will be fixed in nearly future</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>

import ProfileColumn from '@/components/ProfileColumn.vue'
import Card from '@/components/Card.vue'

export default {
  components: {
    ProfileColumn,
    Card
  },
  data() {
    return {
      repos: [
        { repoName: 'cs193p-2017-fall-demo-and-solution' },
        { repoName: 'cs193p-2017-fall-demo-and-solution' },
        { repoName: 'cs193p-2017-fall-demo-and-solution' },
        { repoName: 'cs193p-2017-fall-demo-and-solution' }
      ],
      navButtons: [
        { buttonName: 'Overview' },
        { buttonName: 'Repositorie' },
        { buttonName: 'Projects' },
        { buttonName: 'Stars' },
        { buttonName: 'Followers' },
        { buttonName: 'Followings' }
      ],
      activities: {
        path: require('@/static/github-hi-there.jpg')
      },
      activityGraph: {
        path: require('@/static/activity-graph.jpg')
      },
      activityButtons: [
        { year: '2019' },
        { year: '2018' },
        { year: '2017' }
      ],
      contributedRepos: [
        { repoName: 'Apple' },
        { repoName: 'Google' },
        { repoName: 'NPC' },
        { repoName: 'More' }
      ]
    }
  }
}
</script>

<style scoped>
.grid-box {
  display: grid;
  grid-template-columns: 21% 79%;
}

.profile {
  margin: 100px;
}

.personal-section {
  display: flex;
  flex-direction: column;
  width: 50%;
}

.nav__buttons {
  display: flex;
  margin-top: 100px;
  border: 1px solid black;
}

.section-title p {
  font-size: 1.3rem;
  font-weight: 400;
  border: 1px solid black;
  margin: 0px;
  padding-left: 15px;
  margin-bottom: 10px;
}

.repos {
  margin: 10px 10px 10px 0px;
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
}

.repos__card {
  margin: 0px 10px 10px 10px;
}

.activities {
  display: flex;
}

.activities__images {
  display: flex;
  flex-direction: column;
  width: 750px;
}

.activities__buttons {
  display: flex;
  flex-direction: column;
  border: 1px solid black;
}

.activities__strategy {
  border: 1px solid black;
  width: 650px;
  height: 300px;
  margin-top: 10px;
}

.activities__strategy__buttons {
  display: flex;
  border: 1px solid black;
}

.activities__description {
  padding: 50px;
  display: flex;
}

.description__text {
  width: 300px;
}

.description__image {
  margin-left: 50px;
  width: 200px;
  height: 200px;
}

.contribution__block {
  width: 650px;
  height: 350px;
  border: 1px solid black;
}

.contribution__description {
  margin-left: 50px;
}

.contribution__comment {
  border: 1px solid black;
  margin-top: 20px;
}
</style>
