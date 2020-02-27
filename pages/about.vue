<template>
  <v-layout>
    <v-flex class="text-center">
      <div class="img-frame">
        <img :src="img" />
      </div>
      <blockquote class="blockquote">
        &#8220;First, solve the problem. Then, write the code.&#8221;
        <footer>
          <small>
            <em>&mdash;John Johnson</em>
          </small>
        </footer>
      </blockquote>
    </v-flex>
  </v-layout>
</template>

<script>
import imgUrl from 'static/images/yashiro.jpg'
// import imgUrl from 'static/images/参拝.jpg'
// import imgUrl from 'static/images/神社.jpg'

export default {
  data() {
    return {
      img: imgUrl
    }
  }
}
</script>

<style>
.img-frame img {
  width: 100%;
  max-width: 100%;
  height: auto;
}
</style>
