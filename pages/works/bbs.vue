<template>
  <div>
    <Header />
    <div class="max-w-5xl">
      <section>
        <div class="mx-12">
          <h1>BBS</h1>
          <p class="text-xl">掲示板</p>
        </div>
        <swiper
          class="swiper my-4"
          :options="swiperOptions"
        >
          <swiper-slide><img src="/portfolio/works/bbs/01.png" /></swiper-slide>
          <swiper-slide><img src="/portfolio/works/bbs/01.png" /></swiper-slide>
          <swiper-slide><img src="/portfolio/works/bbs/01.png" /></swiper-slide>
        </swiper>
      </section>
      <div class="flex flex-col m-12">
        <a class="underline" href="https://github.com/KamichanR/laravel_bbs" target="_blank" rel="noopener noreferrer">github.com/KamichanR/laravel_bbs (Source Codes)</a>
        <p class="font-semibold my-8 text-center">
          Design, HTML/CSS, PHP, Laravel, MySQL, GitHub
        </p>
        <p>
          一般的な電子掲示板を作成しました。投稿のCRUD機能を実装しています。<br>
          PHP, Laravel, MySQLを初めて勉強して、その振り返りとしてこのサービスを作りました。CRUD機能や非同期処理の仕組みや実装方法を勉強できて、CSRF機能というセキュリティ面の学習もできました。
        </p>
      </div>
    </div>
    <Footer />
  </div>
</template>

<script>
import SwiperCore, { EffectCoverflow, Pagination } from 'swiper'
import Header from '@/components/Header.vue'
import Footer from '@/components/Footer.vue'
SwiperCore.use([EffectCoverflow, Pagination]);
export default {
  components: {
    Header,
    Footer,
  },
  data() {
    return {
      swiperOptions: {
        effect: "coverflow",
        loop: true,
        grabCursor: true,
        centeredSlides: true,
        slidesPerView: "auto",
        coverflowEffect: {
          rotate: 60,
          stretch: 0,
          depth: 50,
          modifier: 1,
          slideShadows: true,
        },
        pagination: true,
      }
    }
  },
  head() {
    return {
      title: 'BBS',
    }
  },
}
</script>

<style scoped>
.swiper-slide {
  background-position: center;
  background-size: cover;
  height: 720px;
}

@media (min-width: 768px) {
  .swiper-slide {
    width: 720px;
  }
}

@media (max-width: 767px) {
  .swiper-slide {
    width: 70%;
  }
}

.swiper-slide img {
  display: block;
  height: 100%;
  width: 100%;
}
</style>
