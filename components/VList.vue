<template>
  <ul class="flex flex-col">
    <li class="flex items-center gap-3 before:min-w-[10px] before:min-h-[10px] before:max-h-[10px] before:block before:border-2 before:rounded-full before:border-red"
        v-for="(item, i) of items" :key="i">
      {{ item }}
    </li>
  </ul>
</template>

<script>
export default {
  name: "VList",
  props: {
    items: {
      type: Array,
      required: true
    }
  }
}
</script>
