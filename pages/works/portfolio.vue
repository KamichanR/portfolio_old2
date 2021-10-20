<template>
  <div>
    <Header />
    <div class="max-w-5xl">
      <section>
        <div class="mx-12">
          <h1>Portfolio</h1>
          <p class="text-xl">ポートフォリオ</p>
        </div>
        <swiper
          class="swiper my-4"
          :options="swiperOptions"
        >
          <swiper-slide><img src="/works/portfolio/01.png" /></swiper-slide>
          <swiper-slide><img src="/works/portfolio/02.png" /></swiper-slide>
          <swiper-slide><img src="/works/portfolio/03.png" /></swiper-slide>
        </swiper>
      </section>
      <div class="flex flex-col m-12">
        <a class="underline" href="/" target="_blank" rel="noopener noreferrer">kamichanr.github.io/portfolio/</a>
        <p class="font-semibold my-8 text-center">
          Design, Planning, HTML/CSS, JavaScript, Vue.js, Nuxt.js, GitHub, Photoshop, Illustrator
        </p>
        <p>
          このポートフォリオサイトを作成しました。今まで制作したWebサイト・アプリケーションの紹介をしています。シンプルなデザインにして、ユーザーがスムーズに閲覧できるようにしました。
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
      title: 'Portfolio',
    }
  },
}
</script>

<style scoped>
.swiper-slide {
  background-position: center;
  background-size: cover;
  height: 100%;
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
