<template>
  <div>
    <Header />
    <section class="introduction mb-16">
      <div class="max-w-5xl mx-auto my-16 px-4 py-40 text-xl">
        <p>
          北海道出身の大学生です。<br>
          Webやプログラミングの技術を使って問題を解決し、<br>
          新しい価値や感動を提供したいと考えています。
        </p>
        <br>
        <p>
          I am a university student. I am from Hokkaido.<br>
          I would like to solve problems and issues by using web and programming skills,<br>
          and provide new values and excitement.
        </p>
      </div>
    </section>
    <section id="skills" class="flex flex-col max-w-5xl pb-16">
      <h2 class="pb-4 text-center">Skills</h2>
      <div class="grid md:grid-cols-6">
        <section class="m-4 md:col-span-2">
          <div class="text-center">
            <h3>設計・デザイン</h3>
            <p>Web & Application Design</p>
          </div>
          <img src="/portfolio/skills/web_design.png" alt="Web Design" class="px-1/10 py-8">
          <p>
            内容やコンセプトがユーザーに伝わりやすく、使いやすいサイト設計をします。アニメーションや構成部品のデザインも工夫して、ユーザーに快適な環境と体験を提供することを第一に考えています。Webサイトだけでなくアプリ開発もしています。
          </p>
        </section>
        <section class="m-4 md:col-span-2">
          <div class="text-center">
            <h3>コーディング</h3>
            <p>Coding</p>
          </div>
          <img src="/portfolio/skills/coding.png" alt="Coding" class="px-1/10 py-8">
          <p>
            サイトのコンセプトやユーザーにとって使いやすいサイト・アプリを実現させます。レスポンシブ対応やアニメーションの使用など様々な状況に対応します。フレームワークやライブラリを活用して、効率的かつ最適な制作をしていきます。
          </p>
        </section>
        <section class="m-4 md:col-span-2">
          <div class="text-center">
            <h3>ロゴ制作</h3>
            <p>Logo Design</p>
          </div>
          <img src="/portfolio/skills/logo_design.png" alt="Logo Design" class="px-1/10 py-8">
          <p>
            イメージやコンセプトが伝わりやすく、印象に残りやすいロゴづくりを目指しています。常にロゴのもつ意図を意識して、それが効果的に伝わる配置・配色・文字を考えています。また、シンプルかつ斬新なデザインを常に追い求めています。
          </p>
        </section>
        <section class="md:col-start-2 m-4 text-center md:col-span-2">
          <h3>フロントエンド</h3>
          <p>Frontend</p>
          <p class="font-semibold">
            HTML/CSS, JavaScript, Gatsby,<br>
            VueJS, NuxtJS, Flutter,<br>
            WordPress, Photoshop, Illustrator
          </p>
        </section>
        <section class="m-4 text-center md:col-span-2">
          <h3>バックエンド</h3>
          <p>Backend</p>
          <p class="font-semibold">
            Python, PHP/Laravel, C/C++,<br>
            Linux, Git/GitHub,<br>
            Docker, MySQL/SQLite
          </p>
        </section>
      </div>
    </section>
    <section id="works" class="max-w-5xl mb-16 works">
      <h2 class="pb-4 text-center">Works</h2>
      <ul class="grid md:grid-cols-3">
        <li class="m-4">
          <a href="/portfolio/works/hokudai_cafe_project">
            <img src="/portfolio/works/hokudai_cafe_project/01.png" alt="Hokudai Café Project">
          </a>
        </li>
        <li class="m-4">
          <a href="/portfolio/works/portfolio">
            <img src="/portfolio/works/portfolio/01.png" alt="Portfolio">
          </a>
        </li>
        <li class="m-4">
          <a href="/portfolio/works/yozimaker">
            <img src="/portfolio/works/yozimaker/01.png" alt="Yozi Maker">
          </a>
        </li>
        <li class="m-4">
          <a href="/portfolio/works/todo_management_app">
            <img src="/portfolio/works/todo_management_app/01.png" alt="ToDo Application">
          </a>
        </li>
        <li class="m-4">
          <a href="/portfolio/works/bbs">
            <img src="/portfolio/works/bbs/01.png" alt="BBS">
          </a>
        </li>
      </ul>
    </section>
    <section id="about" class="max-w-5xl mb-16">
      <h2 class="pb-4 text-center">About</h2>
      <div class="flex flex-col mx-4">
        <div class="m-end">
          <h3 class="font-semibold">Kamichan_R</h3>
          <p>
            Webデザイン・プログラミング・ロゴデザインを勉強している大学生です。<br>
            2002年生まれ、趣味は温泉と読書とアニメ鑑賞です。
          </p>
        </div>
        <div id="contact" class="m-start text-right">
          <h3 class="font-semibold">Contact</h3>
          <p>
            kamichanr+info@gmail.com<br>
            Twitter(DM)
          </p>
        </div>
      </div>
    </section>
    <Footer />
  </div>
</template>

<script>
import Header from '@/components/Header.vue'
import Footer from '@/components/Footer.vue'
export default {
  components: {
    Header,
    Footer,
  },
  head() {
    return {
      titleTemplate: 'Kamichan_R - Design and App Development',
    }
  },
}
</script>

<style scoped>
.introduction,
.introduction > div {
  background-color: #eaeaea;
}

.px-1\/10 {
  padding-left: 10%;
  padding-right: 10%;
}

.works img {
  border: 0.5px solid #cacaca;
  width: 100%;
}

.m-start {
  margin-left: auto;
  margin-right: 0;
}

.m-end {
  margin-left: 0;
  margin-right: auto;
}
</style>
