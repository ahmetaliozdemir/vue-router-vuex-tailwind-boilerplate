<template>
  <component :is="tag" :class="[this.class, weight, type]"> <slot></slot></component>
</template>

<script>
export default {
  name: "Text",
  props: ["tag", "type", "weight", "class"],
};
</script>


<style scoped>
.body {
  @apply font-roboto text-sm  leading-normal;
}
.big-header {
  @apply font-roboto text-6xl leading-normal;
}
.header {
  @apply font-roboto text-xl  leading-normal;
}
.subheader {
  @apply font-roboto text-lg  leading-normal;
}
.bold {
  @apply font-bold;
}
.semibold {
  @apply font-semibold;
}
.light {
  @apply font-light;
}
.normal {
  @apply font-normal;
}
</style>