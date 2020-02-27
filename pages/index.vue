<template>
  <v-layout column justify-center align-center>
    <div class="video-frame">
      <video muted autoplay :src="video"></video>
      <p>
        社会人コミュニティ<br />
        社 やしろ
      </p>
    </div>
    <div class="img-frame">
      <img :src="img" />
    </div>
    <div class="carousel">
      <carousel
        :per-page="2"
        :per-page-custom="[
          [480, 1],
          [780, 2]
        ]"
        :autoplay="true"
        :autoplay-timeout="4000"
        :speed="2000"
        :loop="true"
      >
        <slide>Event info 1</slide>
        <slide>Event info 2 </slide>
        <slide>Event info 3 </slide>
        <slide>Event info 4 </slide>
        <slide>Event info 5 </slide>
        <slide>Event info 6 </slide>
      </carousel>
    </div>
    <v-flex xs12 sm8 md6>
      <div class="text-center">
        <!--   <logo />
        <vuetify-logo /> -->
      </div>
      <v-card>
        <v-card-title class="headline">
          いま願うその背中を押す場所に
        </v-card-title>
        <v-card-text>
          <p>
            あなたにとっって屋代（神社）とは、どんな場所ですか？<br />
            どうしてもかなえたいお願い事がある時に、お祈りをして神様にお願いをする場所ですか<br />
            本来、お参りは自分の宣誓の場所としてあるものです。<br />
            「今年はきっと彼氏ができますように」と願う場所ではなく、<br />
            「今年は彼氏ができるように、友達を増やし、美容を意識して、人を笑顔にできるように努力します！」と神様に迎って誓う場所であるべきです。<br />
            <br />
            私たちはそんな頑張りたい人たちがお互いを高め合える<br />
            そんな場所を目指しています。<br />
          </p>
          <p>
            For more information for this code, check out the
            <a href="https://github.com/naru20181117/yashiro" target="_blank">
              Github
            </a>
          </p>
          <p>
            If you wanna see the deployed site, please check the
            <a href="https://yashiro.netlify.com/" target="_blank" title="site">
              site. </a
            >.
          </p>
          <p>
            Wanna see a old site?
            <a href="https://zenkokucdc.wordpress.com/" target="_blank">
              全国キャリアセンター
            </a>
          </p>
          <p>
            Thank you for watching with your concern and I look forward to
            having more exciting activity with you.
          </p>
          <div class="text-xs-right">
            <em><small>&mdash; Naruhiro Tsukazaki</small></em>
          </div>
          <hr class="my-3" />
          <a href="https://www.facebook.com/eto.ryuji" target="_blank">
            Eto Ryuji
          </a>
          <br />
          <a href="https://github.com/nuxt/nuxt.js" target="_blank">
            Nuxt GitHub
          </a>
        </v-card-text>
        <v-card-actions>
          <v-spacer />
          <v-btn color="primary" nuxt to="/inspire">
            Continue
          </v-btn>
        </v-card-actions>
      </v-card>
    </v-flex>
  </v-layout>
</template>

<script>
import { Carousel, Slide } from 'vue-carousel'
import imgUrl from 'static/images/yashiro.jpg'
// import imgUrl from 'static/images/参拝.jpg'
// import imgUrl from 'static/images/神社.jpg'
import videoUrl from '~/components/movie/ink_b.mp4'
// import Logo from '~/components/Logo.vue'
// import VuetifyLogo from '~/components/VuetifyLogo.vue'

export default {
  components: {
    // Logo,
    // VuetifyLogo,
    Carousel,
    Slide
  },
  data() {
    return {
      // src: 'https://www.youtube.com/watch?v=IXAgGr5gR98&feature=emb_logo'
      video: videoUrl,
      img: imgUrl
    }
  }
}
</script>

<style>
.video-frame {
  position: relative;
}
.video-frame p {
  font-family: 'cursive';
  font-size: 4vw;
  position: absolute;
  color: white;
  top: 50%;
  left: 50%;
  -ms-transform: translate(-50%, -50%);
  -webkit-transform: translate(-50%, -50%);
  transform: translate(-50%, -50%);
  margin: 0;
  padding: 0;
  line-height: 2em;
  text-align: center;
}
.video-frame video {
  width: 100vw;
  max-width: 100%;
  height: auto;
}
.img-frame img {
  width: 100%;
  max-width: 100%;
  height: auto;
}
p {
  line-height: 35px;
}

.VueCarousel-inner {
  margin-top: 30px;
}

.VueCarousel-slide {
  height: 150px;
  color: #fff;
  background: #4db56a;
  display: flex;
  align-items: center;
  justify-content: center;
  border-right: 1px solid #fff;
  box-sizing: border-box;
  font-size: 20px;
}
</style>
