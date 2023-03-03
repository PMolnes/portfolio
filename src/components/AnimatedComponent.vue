<template>
  <div ref="target">
    <Transition :name="animationType">
      <div v-if="animate" class="animated-component">
        <slot />
      </div>
    </Transition>
  </div>
</template>

<script setup lang="ts">
import { onMounted, ref } from 'vue';

const props = withDefaults(
  defineProps<{
    animationType?: string;
  }>(),
  {
    animationType: 'fade'
  }
);

const target = ref();
const animate = ref(false);

const observer = new IntersectionObserver(
  ([entry]) => {
    if (entry.isIntersecting) {
      animate.value = entry.isIntersecting;
      observer.unobserve(target.value);
    }
  },
  { threshold: 0.5 }
);

onMounted(() => {
  observer.observe(target.value);
});
</script>

<style scoped>
.animated-component.fade-enter-from,
.animated-component.zoom-enter-from {
  transition: none;
} 

/* Fade animation */
.fade-enter-active,
.fade-leave-active {
  transition: opacity 500ms ease-in-out;
}
.fade-enter-from,
.fade-leave-to {
  opacity: 0;
} 

/* Zoom animation */
.zoom-enter-active,
.zoom-leave-active {
  transition: transform 500ms ease;
}
.zoom-enter-from,
.zoom-leave-to {
  transform: scale(0.9);
}

/* Fade slide animation */
.fade-slide-enter-active,
.fade-slide-leave-active {
  transition: transform 500ms ease, opacity 500ms ease;
}
.fade-slide-enter-from,
.fade-slide-leave-to {
  opacity: 0;
  transform: translateX(100rem);
}
.fade-slide-enter-to,
.fade-slide-leave-from {
  opacity: 1;
  transform: translateY(0);
}
</style>
