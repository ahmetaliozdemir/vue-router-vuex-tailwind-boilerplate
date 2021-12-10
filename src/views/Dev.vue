<template>
  <div class="container max-w-5xl mx-auto px-2 md:px-12">
    <Text tag="h1" weight="bold" type="big-header">Merhaba Dünya</Text>

    <Text
      class="text-red-600 bg-red-100 p-4 rounded"
      tag="p"
      type="header"
      weight="light"
    >
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Praesentium,
      laborum beatae animi quisquam ex sed, soluta obcaecati mollitia doloremque
      ipsa laudantium impedit, facere dolor consectetur sequi minus in
      voluptates! Deleniti?</Text
    >

    <div class="space-x-4 py-2">
      <Button type="primary" size="big" textclass="text-white"
        >Lorem, ipsum.</Button
      >
      <Button type="alert" size="medium" textclass="text-white"
        >Not click me</Button
      >
      <Button type="secure" size="default" textclass="text-white"
        >Click me</Button
      >
    </div>

    <div class="test relative">
      <img src="https://picsum.photos/1024/400" class="object-cover" alt="" />
      <div class="test2">
        <Text class="shadow-xl" tag="h1" weight="bold" type="big-header"
          >Merhaba Dünya</Text
        >
      </div>
    </div>
  </div>
</template>

<script>
import Text from "@/components/Text.vue";
import Button from "@/components/Button.vue";
export default {
  components: {
    Text,
    Button,
  },
};
</script>

<style scoped lang="scss">
.test {
  @apply bg-transparent w-full h-96 shadow-xl relative;
  clip-path: polygon(0 0, 100% 0, 100% 76%, 0 95%);
}
.test2 {
  @apply absolute left-0 top-5 text-center w-full;
}
</style>