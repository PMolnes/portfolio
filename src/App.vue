<script setup lang="ts">
import SideMenu from './components/layout/SideMenu.vue';
import HomeView from './views/HomeView.vue';
import AboutView from './views/AboutView.vue';
import SkillsView from './views/TechnologyView.vue';
</script>

<template>
  <SideMenu />
  <main class="content">
    <div id="home" class="scroll-page">
      <HomeView />
    </div>
    <div id="about" class="scroll-page">
      <AboutView  />
    </div>
    <div class="scroll-page">
      <SkillsView />
    </div>
    <div class="scroll-page">
      <h1>hello world</h1>
    </div>
  </main>
</template>

<style lang="scss">
.page-title {
  font-size: 4rem;
  font-weight: bold;
  text-decoration: underline;
}

#app {
  font-family: 'Fira Code', monospace;
  color: white;
  height: 100vh;
  display: grid;
  grid-template-columns: 20rem 1fr;
  overflow: hidden;
}

.scroll-page {
  height: 100%;
  scroll-snap-align: center;
  background-color: #202020;
  padding: 0 4rem;
}

.content {
  min-height: fit-content;
  max-height: fit-content;
  overflow-y: scroll;
  scroll-snap-type: y mandatory;
  scroll-behavior: smooth;
}

a {
  color: white;
  text-decoration: none;
}

h1,
h2 {
  margin: 0;
}

body {
  margin: 0;
}
</style>
