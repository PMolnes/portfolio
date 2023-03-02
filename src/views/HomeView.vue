<template>
  <div class="container">
    <div class="greeting">
      <h1 class="name">Hello! My name is Petter Molnes.</h1>
      <h2 class="description">I am a Fullstack Developer.</h2>
    </div>
    <img class="waving-portrait" src="@/assets/wave.png" alt="portrait waving illustration" />
  </div>
</template>

<style lang="scss" scoped>
.name {
  font-weight: bold;
  font-size: 4rem;
}

.description {
  font-weight: lighter;
  font-size: 2rem;
}
.container {
  min-height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
