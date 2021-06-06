<template>
  <div style="text-align: center">
    <v-app-bar app color="blue" dark>
      <div class="text-center">
        <v-dialog v-model="dialog" width="256">
          <template v-slot:activator="{ on, attrs }">
            <v-btn color="blue lighten-1" dark v-bind="attrs" v-on="on">
              Join Us
            </v-btn>
          </template>
          <v-card>
            <v-card-title class="text-center text-h5 blue lighten-1">
              YY: 1459156949
            </v-card-title>

            <v-img src="../assets/2dcode.png" width="256" height="256"></v-img>
          </v-card>
        </v-dialog>
      </div>
      <v-spacer> </v-spacer>
      <v-btn @click="scrollDown('#about')">
          <span>关于</span>
      </v-btn>
    </v-app-bar>
    <v-parallax dark src="../assets/bgimg.jpg" height="880">
      <h1 class="text-h2 mb-4 font-weight-thin">Legend</h1>
      <h4 class="subheading">欢迎访问 Legend 公会官方网站</h4>
    </v-parallax>
    <div class="scrollDown" @click="scrollDown('#about')">
      <span></span>
    </div>
    <div id="about">
      <h1 class="mt-16" style="color: black">关于我们</h1>
      <v-divider
        color="#2196F3"
        class="my-4 mx-auto py-1"
        width="200"
        style="text-align: center"
      ></v-divider>
      <div>
        <div class="aboutText">
          <p>Legend 公会</p>
          <p>十二年老公会</p>
          <p>一直坚持最公平的金团模式</p>
          <p>拥有70版本全通经验</p>
          <p>专业代工全部免费</p>
          <p>外域练级副本每天开组</p>
          <p>加入我们，让你的TBC之路更精彩！</p>
          <div style="margin: 1000px"></div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
// import $ from 'jquery'
export default {
  methods: {
    scrollDown: function (id) {
      // console.log("qwq")
      $("html,body").animate({ scrollTop: $(id).offset().top - 100 }, 200);
    },
  },
};
</script>

<style>
.aboutText {
  color: #708090;
}
.scrollDown {
  position: absolute;
  left: 50%;
  margin-left: -10px;
  /* top: 100%; */
  margin-top: -100px;
  width: 20px;
  height: 20px;
  border-right: 3px solid #ffffff;
  border-top: 3px solid #ffffff;
  transform: rotate(135deg);
  transition: 0.25s;
}

/* .scrollDown span{
    position: absolute;
    left: 50%;
    margin-left: -10px;
    margin-top: 50px;
    border-right: 3px solid rgba(255,255,255,0.5);
    border-top: 3px solid rgba(255,255,255,0.5);
    height: 20px;
    width: 20px;
    -webkit-transform: rotate(
        135deg
    );
    transform: rotate(135deg);
    cursor: pointer;
    transition: .25s;
} */

.scrollDown span:hover {
  border-right: 3px solid white;
  border-top: 3px solid white;
}
.scrollDown span:active {
  border-right: 3px solid rgba(255, 255, 255, 0.35);
  border-top: 3px solid rgba(255, 255, 255, 0.35);
}
</style>            



