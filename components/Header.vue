<template>
  <header class="flex flex-col md:flex-row justify-between m-auto max-w-5xl">
    <div class="mx-4 my-4 md:my-auto">
      <h1>
        <a href="/">
          <img class="w-64" src="/portfolio/logo_wide.png" alt="Kamichan_R">
        </a>
      </h1>
    </div>
    <div class="menu mx-4 my-auto">
      <div class="socialButton">
        <ul>
          <li>
            <a href="https://twitter.com/Kamichan_R" target="_blank" rel="noopener noreferrer">
              <img src="/portfolio/social-icon/twitter.png" alt="Twitter">
            </a>
          </li>
          <li>
            <a href="https://qiita.com/Kamichan_R" target="_blank" rel="noopener noreferrer">
              <img src="/portfolio/social-icon/qiita.png" alt="Qiita">
            </a>
          </li>
          <li>
            <a href="https://github.com/KamichanR" target="_blank" rel="noopener noreferrer">
              <img src="/portfolio/social-icon/github.png" alt="GitHub">
            </a>
          </li>
        </ul>
      </div>
      <nav>
        <ul class="font-semibold text-xl md:text-2xl">
          <li>
            <a href="/portfolio/#skills">Skills</a>
          </li>
          <li>
            <a href="/portfolio/#works">Works</a>
          </li>
          <li>
            <a href="/portfolio/#about">About</a>
          </li>
          <li>
            <a href="/portfolio/#contact">Contact</a>
          </li>
        </ul>
      </nav>
    </div>
  </header>
</template>

<style scoped>
ul {
  display: flex;
  justify-content: flex-end;
}

.socialButton,
nav {
  height: 50px;
  margin: 10px 0;
}

.socialButton img {
  height: 32px;
  object-fit: contain;
}

li {
  margin: auto 8px;
}
</style>
