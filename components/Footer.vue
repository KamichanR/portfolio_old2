<template>
  <footer class="flex md:flex-row flex-col justify-between max-w-5xl mx-auto my-4">
    <nav class="m-end">
      <ul class="font-semibold">
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
    <div class="ml-4 mr-auto md:ml-auto md:mr-4">
      <p>&copy; 2021 Kamichan_R</p>
    </div>
  </footer>
</template>

<style scoped>
ul {
  display: flex;
}

li {
  margin: auto 8px auto auto;
}

.m-start {
  margin-left: auto;
  margin-right: 1rem;
}

.m-end {
  margin-left: 1rem;
  margin-right: auto;
}
</style>
