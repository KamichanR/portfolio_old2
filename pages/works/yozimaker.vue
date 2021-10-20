<template>
  <div>
    <Header />
    <div class="max-w-5xl">
      <section>
        <div class="mx-12">
          <h1>YoziMaker</h1>
          <p class="text-xl">よじメーカー</p>
        </div>
        <swiper
          class="swiper my-4"
          :options="swiperOptions"
        >
          <swiper-slide><img src="/works/yozimaker/01.png" /></swiper-slide>
          <swiper-slide><img src="/works/yozimaker/02.png" /></swiper-slide>
          <swiper-slide><img src="/works/yozimaker/03.png" /></swiper-slide>
        </swiper>
      </section>
      <div class="flex flex-col m-12">
        <a class="underline" href="https://yozimaker.xyz/" target="_blank" rel="noopener noreferrer">yozimaker.xyz</a>
        <p class="font-semibold my-8 text-center">
          Design, Planning, HTML/CSS, JavaScript, Vue.js, GitHub
        </p>
        <p>
          好きな言葉（一文字～六文字、四文字が最適）を入力して、はんこ風のアイコンを作成できるサービスです。文字、文字の色や太さ、枠の色や太さ、はんこ名を設定できるので、好みのオリジナルはんこ風アイコンを作成することができます。<br>
          Vue.jsを初めて学習して、その振り返りとしてこのサービスを作りました。双方向バインディングやルーティングの勉強が出来たことに加えて、Tailwind CSSを使うことができました。
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
      title: 'YoziMaker',
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
