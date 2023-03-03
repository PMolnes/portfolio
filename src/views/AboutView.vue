<template>
  <div class="container">
    <AnimatedComponent animation-type="fade-slide">
      <h1 class="page-title">about me</h1>
    </AnimatedComponent>
    <AnimatedComponent>
      <div class="content">
        <div class="information">
          <p>
            I am 22 years old from Norway. I come from Norway, Aalesund, where I studied a Bachelor in
            Computer Engineering at NTNU.
          </p>
          <p>
            I chose to get into programming because I love creating stuff and because I love learning
            new stuff.
          </p>
          <p>Here's a list of what I use my freetime on:</p>
          <ul>
            <li>personal projects</li>
            <li>hanging with friends</li>
            <li>tv-shows</li>
            <li>chess</li>
            <li>video games</li>
          </ul>
        </div>
        <img src="@/assets/computer.png" alt="computer portrait illustration" />
      </div>
    </AnimatedComponent>
  </div>
</template>

<style scoped lang="scss">
.page-title {
  font-size: 4rem;
  font-weight: bold;
  text-decoration: underline;
}

.content {
  display: flex;
  justify-content: center;
  align-items: center;
}
.container {
  display: flex;
  flex-direction: column;
  justify-content: center;
  min-height: 100%;
  p {
    font-size: 2rem;
  }
}
</style>
