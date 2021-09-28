<template>
  <div>
    <div class="spacer"></div>
    <img src="../assets/ponz_by_40kino.png" v-on:mouseover="mouseOver" width="100" height="100">

    <h1>{{ Ponz }}</h1>

    <h3>{{ profile }}</h3>

    <!-- <div class="spacer"></div>
    <h3>{{ title_contact }}</h3> -->
    <ul>
       <li>
        <a
          target="_blank"
          class="icon"
        >
        <i class="fas fa-envelope fa-2x" @click="openAlertModal(email_msg)" />
        </a>
      </li>

        <li>
        <a
          href="https://twitter.com/ponzliquid"
          target="_blank"
          class="icon"
        >
        <i class="fab fa-twitter fa-2x" />
        </a>
      </li>

        <!-- <li>
        <a
          href="https://www.instagram.com/ponzliquid/"
          target="_blank"
          class="icon"
        >
        <i class="fab fa-instagram fa-2x" />
        </a>
      </li> -->
    </ul>

    <div id="car">
        <carousel
        :per-page="1"
        :navigation-enabled="false"
        :speed="1000"
        :autoplay="true"
        :autoplayTimeout="5000"
        :autoplayHoverPause="true"
        :loop="true"
        paginationPosition="top"
        paginationActiveColor="#efefef"
        paginationColor="#000000"
        >
        <slide>
             <div id="car">
            <span><Tweet :id="'1031516795952230400'"></Tweet></span>
            </div>
        </slide>
        <slide>
             <div id="car">
                <span><Tweet :id="'1128272749447843840'"></Tweet></span>
            </div>
        </slide>
        <slide>
             <div id="car">
                <!-- <span><Tweet :id="'1144217469311078402'"></Tweet></span> -->
                <span><Tweet :id="'1222631286520479744'"></Tweet></span>
            </div>
        </slide>
        <slide>
             <div id="car">
                <span><Tweet :id="'1063414026372141058'"></Tweet></span>
            </div>
        </slide>
        <slide>
             <div id="car">
                <span><Tweet :id="'1051821456865153024'"></Tweet></span>
            </div>
        </slide>
        <slide>
             <div id="car">
                <span><Tweet :id="'1234005569331032064'"></Tweet></span>
                <!-- <span><Tweet :id="'1165467116222345216'"></Tweet></span> -->
            </div>
        </slide>
        </carousel>
    </div>

    <!-- <div id="container">
        <span><Tweet :id="'1031516795952230400'"></Tweet></span>
    </div> -->

    <div class="spacer"></div>

    <div id="container">
      <h2>{{ message_kyomukasetsu }}</h2>
      <div class="td">
        <iframe src="https://ponzliquid.fanlink.to/kyomu-kasetsu?embed=true" style="border-radius:3px" frameborder="0" ></iframe>
      </div>

      <div class="spacer"></div>

      <h2>{{ message_sfcd004 }}</h2>
      <div class="td">
        <iframe src="https://ponzliquid.fanlink.to/3ndless1ove?embed=true" style="border-radius:3px" frameborder="0" ></iframe>
      </div>

      <div class="spacer"></div>

      <h2>{{ message_sfcd003 }}</h2>
      <div class="td">
        <iframe src="https://ponzliquid.fanlink.to/prismlife?embed=true" style="border-radius:3px" frameborder="0" ></iframe>
      </div>

      <div class="spacer"></div>

      <!-- <h2>{{ message_sfcd002 }}</h2>
      <div class="td">
        <iframe src="https://ponzliquid.fanlink.to/empty-world?embed=true" style="border-radius:3px" frameborder="0" ></iframe>
      </div>

      <div class="spacer"></div> -->

      <!-- <h2>{{ message_sfcd001 }}</h2>
      <div class="td">
        <iframe src="https://ponzliquid.fanlink.to/ascension?embed=true" frameborder="0"></iframe>
      </div>

      <div class="spacer"></div> -->

      <h2>{{ message_sc }}</h2>
      <div class="sc">
        <iframe width="800" height="450" scrolling="yes" frameborder="no" allow="autoplay" src="https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/users/77993825&color=%23ff5500&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true"></iframe>
      </div>

      <div class="spacer">
      </div>

      <h2>{{ message_yt }}</h2>
      <div class="yt">
        <iframe width="560" height="315" src="https://www.youtube.com/embed/videoseries?list=PLd2KvZnOeVuh8tPWaPIlKaigHdADGn541" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>
      </div>

      <div class="spacer">
      </div>

      <h2>{{ message_nc }}</h2>
      <div class="yt">
        <!-- <iframe src="https://nico.ms/sm33603676" scrolling="yes" style="border:solid 1px #CCC;" frameborder="0"></iframe> -->
        <iframe width="312" height="176" src="https://ext.nicovideo.jp/thumb/sm33603676" scrolling="no" style="border:solid 1px #ccc;" frameborder="0"><a href="https://www.nicovideo.jp/watch/sm33603676">虚無仮説 feat.初音ミク</a></iframe>
      </div>

      <div class="spacer">
      </div>
    </div>

    <div class="spacer">
    </div>

  </div>
</template>

<script>
import modal from './Modal/modal'
import { Tweet, Moment, Timeline } from 'vue-tweet-embed'
import { Carousel, Slide } from 'vue-carousel'
export default {
  name: 'PonzSingle',
  data () {
    return {
      Ponz: 'Ponz / Shiso-P',
      title_contact: '▼ Contact ▼',
      profile: 'Vocaloid Producer, Composer, Remixer',
      skill_program: 'ASNI-C, Unity-C#, Verilog-HDL, Python3, Vue.js',
      skill_major: 'Reconfigurable Computing, Heterogeneous Computing, High-level Synthesis',
      skill_tool: 'Ableton Live 10, Garageband, Studio One 3, Piapro Studio, Vocaloid Editor 5',
      showModal: true,
      discord_msg: 'UserID: <br><br> ponzliquid#2732<br>',
      email_msg: 'ponzliquid <br> at <br> gmail.com',
      message_sfcd001: '▼ Trance Album ▼',
      message_sfcd002: '▼ Vocaloid EP ▼',
      message_sfcd003: '▼ MikuTrance EP ▼',
      message_sfcd004: '▼ MikuTrance EP ▼',
      message_kyomukasetsu: '▼ Vocaloid Single ▼',
      message_sc: '▼ SoundCloud ▼',
      message_yt: '▼ YouTube ▼',
      message_nc: '▼ NicoNico ▼'
    }
  },
  components: {
    modal,
    Carousel,
    Slide,
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
  margin-bottom: 30px;
}
h2{
  font-weight: normal;
  font-size: large;
  margin-bottom: 20px;
}
h3{
  font-weight: normal;
  font-size: medium;
  margin-bottom: 10px;
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

.td {
  position:relative;
  width:100%;
  padding-top:120%;
  padding-bottom:10%;
  overflow-y: auto;
  -webkit-overflow-scrolling: touch;
}
.td iframe{
  position:absolute;
  top:0;
  left:0;
  width:100%;
  height:100%;
}

.sc {
  position:relative;
  width:100%;
  height:0;
  padding-top:80%;
  overflow-y: auto;
  -webkit-overflow-scrolling: touch;
}
.sc iframe{
  position:absolute;
  top:0;
  left:0;
  width:100%;
  height:100%;
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

#car {
  background-color: #333333;
  max-width: 300px;
  margin: 0 auto;
}

.carousel{
  max-width: 400px;
  margin: 0 auto;
  top: 0;
}
.spacer{
  margin-top: 40px;
  opacity: 0.8;
}

</style>
