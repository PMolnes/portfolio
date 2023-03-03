<template>
  <nav class="sidemenu">
    <div class="sidemenu-header">
      <a href="#home">molnes.dev</a>
    </div>
    <div class="sidemenu-items">
      <a class="links" href="#about">about me</a>
      <a class="links" href="">skills</a>
      <a class="links" href="">technologies</a>
      <a class="links" href="">projects</a>
      <a class="links" href="">contact me</a>
    </div>
  </nav>
</template>

<style lang="scss" scoped>
.sidemenu {
  max-height: 100vh;
  background-color: #222222;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 2rem;
}

.sidemenu-header {
  margin-bottom: auto;
  font-weight: bold;
  font-size: 1.5rem;
}

.sidemenu-items {
  display: flex;
  flex-direction: column;
  gap: 1rem;
  margin-bottom: auto;
  text-align: center;
}

.links {
  transition: ease-in-out 300ms;
  &:hover {
    transform: scale(1.2);
  }
}
</style>
