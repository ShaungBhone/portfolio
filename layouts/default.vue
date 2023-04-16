<template>
  <div>
    <Header />
    <slot />
    <Footer />
  </div>
</template>

<script setup lang="ts">
useHead({
  title: "Portfolio",
  meta: [{ name: "description", content: "My amazing site." }],
  bodyAttrs: {
    class: "bg-gray-100",
  },
});
</script>
