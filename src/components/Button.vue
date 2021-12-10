<template>
  <button disabled :class="[type, size, this.class]" class="default rounded">
    <Text tag="p" type="body" weight="semibold" class="text-white">
      <slot></slot
    ></Text>
  </button>
</template>

<script>
import Text from "@/components/Text";
export default {
  name: "Button",
  components: {
    Text,
  },
  props: {
    type: {
      type: String,
      default: "primary",
    },
    size: {
      type: String,
      default: "medium",
    },
    radius: {
      type: String,
      default: "medium",
    },
    textclass: {
      type: String,
      default: "text-white",
    },
    class: {
      type: String,
      default: "",
    },
  },
};
</script>

<style scoped>
.primary {
  @apply bg-blue-600 hover:bg-blue-800 active:bg-blue-900 transition-all duration-150;
}
.secure {
  @apply bg-green-600 hover:bg-green-800 active:bg-green-900 transition-all duration-150;
}
.alert {
  @apply bg-red-600 hover:bg-red-800 active:bg-red-900 transition-all duration-150;
}
.default {
  @apply px-2 py-1;
}
.medium {
  @apply px-4 py-2;
}
.big {
  @apply px-8 py-2 disabled:opacity-20;
}
</style>
