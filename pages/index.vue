<template>
  <v-layout column justify-center align-center>
    <video src=":src" autoplay></video>
    <img src="imgUrl" />
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
        <slide>Slide 1 Content</slide>
        <slide>Slide 2 Content</slide>
        <slide>Slide 3 Content</slide>
        <slide>Slide 4 Content</slide>
        <slide>Slide 5 Content</slide>
        <slide>Slide 6 Content</slide>
      </carousel>
    </div>
    <v-flex xs12 sm8 md6>
      <div class="text-center">
        <logo />
        <vuetify-logo />
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
            For more information on Vuetify, check out the
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
            Find a bug? Report it on the github
            <a
              href="https://github.com/vuetifyjs/vuetify/issues"
              target="_blank"
              title="contribute"
            >
              issue board </a
            >.
          </p>
          <p>
            Thank you for developing with Vuetify and I look forward to bringing
            more exciting features in the future.
          </p>
          <div class="text-xs-right">
            <em><small>&mdash; John Leider</small></em>
          </div>
          <hr class="my-3" />
          <a href="https://nuxtjs.org/" target="_blank">
            Nuxt Documentation
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
// import prayImage from 'static/images/yashiro.jpg'
import Logo from '~/components/Logo.vue'
import VuetifyLogo from '~/components/VuetifyLogo.vue'

export default {
  components: {
    Logo,
    VuetifyLogo,
    Carousel,
    Slide
  },
  data() {
    return {
      // src: 'https://www.youtube.com/watch?v=IXAgGr5gR98&feature=emb_logo'
      src: '~/components/movie/ink_b.mp4',
      imgUrl: '~/static/images/yashiro.jpg'
    }
  }
}
</script>

<style>
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
