<template>
  <div>
    <Header />
    <div class="max-w-5xl">
      <section>
        <div class="mx-12">
          <h1>Hokudai Café Project</h1>
          <p class="text-xl">北大カフェプロジェクト</p>
        </div>
        <swiper
          class="swiper my-4"
          :options="swiperOptions"
        >
          <swiper-slide><img src="/portfolio/works/hokudai_cafe_project/01.png" /></swiper-slide>
          <swiper-slide><img src="/portfolio/works/hokudai_cafe_project/02.png" /></swiper-slide>
          <swiper-slide><img src="/portfolio/works/hokudai_cafe_project/03.png" /></swiper-slide>
        </swiper>
      </section>
      <div class="flex flex-col m-12">
        <a class="underline" href="https://hokcafe.com" target="_blank" rel="noopener noreferrer">hokcafe.com</a>
        <p class="font-semibold my-8 text-center">
          Design, Planning, HTML/CSS, JavaScript, Vue.js, Nuxt.js, Netlify, Photoshop, Illustrator
        </p>
        <p>
          美味しい飲み物と人と人との交流を通して心温まるカフェスペース提供する北大カフェプロジェクト様のホームページを作成しました。全体のレイアウト、ロゴ作成、写真選定、コーディングを担当しました。<br>
          ホームページの更新が途絶えており、デザインも数年前のものを利用していたので、ホームページの一新を目的に制作しました。操作性や更新性を向上させることが出来ました。ナビゲーションとスライドを中心としたデザインなので、ユーザーは迷わず閲覧することができます。<br>
          写真素材は長年北大カフェプロジェクト様が撮り続けていたものを提供していただきました。本文にマッチした最適な画像を使用して北大カフェプロジェクト様の魅力をアピールすることができました。
        </p>
      </div>
    </div>
    <Footer />
  </div>
</template>

<script>
import SwiperCore, { EffectCoverflow, Pagination } from 'swiper';
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
      title: 'Hokudai Café Project',
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
