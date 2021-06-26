<template>
  <div id="app">
    <header>
      <div class="logo">Kim Dyla</div>
      <a
        href="https://github.com/dylakim/portfolio"
        class="github-banner"
        title="View on GitHub"
        target="_blank"
      >
        <GitHubBanner />
      </a>
    </header>

    <main>
      <About />
      <Projects />
      <Clients />
    </main>
  </div>
</template>

<script>
import About from './components/About';
import Clients from './components/Clients';
import GitHubBanner from './components/svg/GitHubBanner';
import Projects from './components/Projects';

export default {
  name: 'App',

  components: {
    About,
    Clients,
    GitHubBanner,
    Projects,
  }
}
</script>
