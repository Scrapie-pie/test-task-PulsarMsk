<template>
  <label class="flex flex-col gap-3">
    <span class="2xl:text-16 text-14 font-medium color-dark">
      {{ label }}
    </span>
    <input
      class="border rounded-[5px] border-[#DFDFDF] px-6 py-4 outline-none placeholder-gray-300 2xl:text-14 text-12"
      @input="$emit('input', $event.target.value)"
      v-bind="$attrs"
    >
  </label>
</template>

<script>
export default {
  name: "VInput",
  inheritAttrs: false,
  props: {
    label: String,
  },
}
</script>
