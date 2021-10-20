<template>
  <div>
    <Header />
    <div class="max-w-5xl">
      <section>
        <div class="mx-12">
          <h1>ToDo Management App</h1>
          <p class="text-xl">ToDo管理アプリ</p>
        </div>
        <swiper
          class="swiper my-4"
          :options="swiperOptions"
        >
          <swiper-slide><img src="/works/todo_management_app/01.png" /></swiper-slide>
          <swiper-slide><img src="/works/todo_management_app/02.png" /></swiper-slide>
          <swiper-slide><img src="/works/todo_management_app/03.png" /></swiper-slide>
        </swiper>
      </section>
      <div class="flex flex-col m-12">
        <a class="underline" href="https://github.com/KamichanR/flutter_todoapp" target="_blank" rel="noopener noreferrer">github.com/KamichanR/flutter_todoapp (Source Codes)</a>
        <p class="font-semibold my-8 text-center">
          Design, Dart, Flutter, SQLite
        </p>
        <p>
          一般的なToDo管理アプリを作成しました。タスク名、優先度、期限、メモを記入することができます。<br>
          Dart, Flutter, SQLiteを初めて学習して、その振り返りとしてこのアプリを作りました。クロスプラットフォーム開発のり弁性を体感出来たことに加えて、データベースの操作やCRUD機能を学習できました。
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
      title: 'ToDo Management App',
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
