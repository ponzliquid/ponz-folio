<template>
  <div>

    <img src="../assets/ponz_by_40kino.png" v-on:mouseover="mouseOver" width="100" height="100">

    <h1>{{ Ponz }}</h1>

    <h3>{{ profile }}</h3>
    <div id="container">
      <span>
        <Tweet :id="'1031516795952230400'"></Tweet>
      </span>
    </div>

    <div class="spacer">
    </div>
    <!-- <h4>{{ skill_major }}</h4> -->
    <!-- <h4>{{ skill_program }}</h4> -->
    <!-- <h4>{{ skill_tool }}</h4> -->
    <div class="spacer">
    </div>

    <h2>
      <!-- See 👉 -->
      See my
      <!-- See ➡ -->
      <!-- <br> -->
      <router-link to="/discography">
      Discography
      </router-link>
      <!-- 👈 -->
      <br>
    </h2>

    <div class="spacer">
    </div>

    <h2>{{ title_contact }}</h2>
    <ul>
        <li>
        <a
          href="https://twitter.com/ponzliquid"
          target="_blank"
          class="icon"
        >
        <i class="fab fa-twitter fa-2x" />
        </a>
      </li>
      <li>
        <a
          target="_blank"
          class="icon"
        >
        <div>
          <i class="fab fa-discord fa-2x" @click="openAlertModal(discord_msg)" />
        </div>
        </a>
      </li>
      <li>
        <a
          href="https://github.com/ponzliquid"
          target="_blank"
          class="icon"
        >
        <i class="fab fa-github fa-2x" />
        </a>
      </li>
      <li>
        <a
          target="_blank"
          class="icon"
        >
        <i class="fas fa-envelope fa-2x" @click="openAlertModal(email_msg)" />
        </a>
      </li>
    </ul>

  </div>
</template>

<script>
import modal from './Modal/modal'
import { Tweet, Moment, Timeline } from 'vue-tweet-embed'
export default {
  name: 'Ponzliquid',
  data () {
    return {
      Ponz: 'Ponz',
      title_contact: '👇Contact👇',
      profile: 'Vocaloid Producer, Composer',
      skill_program: 'ASNI-C, Unity-C#, Verilog-HDL, Python3, Vue.js',
      // skill_music: 'Piano, Perfect pitch, Voice imitation',
      skill_major: 'Reconfigurable Computing, Heterogeneous Computing, High-level Synthesis',
      skill_tool: 'Ableton Live 10, Garageband, Studio One 3, Piapro Studio, Vocaloid Editor 5',
      showModal: false,
      discord_msg: 'UserID: <br><br> ponzliquid#2732<br>',
      email_msg: 'ponzliquid <br> at <br> gmail.com'
    }
  },
  components: {
    modal,
    'Timeline': Timeline,
    'Tweet': Tweet,
    'Moment': Moment
  },
  methods: {
    mouseOver: function () {
    },
    openAlertModal (message) {
      modal.alert(message)
    }
  }
}
</script>

<style scoped>

h1{
  display: center;
  font-weight: normal;
  font-size: xx-large;
}
h2{
  font-weight: normal;
  font-size: large;
  margin-bottom: 20px;
}
h3{
  font-weight: normal;
  font-size: medium;
  margin-bottom: 48px;
  color: #696773;
}
h4{
  font-weight: lighter;
  font-size: small;
  color: #696773;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  padding: 24px;
  margin-bottom: 12px;
}
a {
  color: #FED766;
}
a.icon {
  color: #EFF1F3;
}
a:hover {
  color: #FED766;
}
.frame-wrapper__video {
  position: relative;
  width: 100%;
  height: 0;
  padding-bottom: 56.25%;
  overflow: hidden;
}
.frame-wrapper__video iframe {
  width: 100%;
  height: 100%;
  position: absolute;
  top: 0;
  left: 0;
}
.yt {
  position: relative;
  width: 100%;
  height: 0;
  padding-bottom: 56.25%;
  overflow: hidden;
}
.yt iframe {
  width: 100%;
  height: 100%;
  position: absolute;
  top: 0;
  left: 0;
}
#container {
  max-width: 400px;
  margin: 0 auto;
}
.spacer{
  margin-top: 40px;
  opacity: 0.8;
}

</style>
