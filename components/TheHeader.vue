<template>
  <header class="bg-gray py-4 xl:mb-9 mb-5">
    <nav class="container flex gap-11 text-12 font-medium">
      <NuxtLink to="/" exact-active-class="font-bold">Калькулятор</NuxtLink>
      <NuxtLink to="/rubleExchangeRate" exact-active-class="font-bold">Курс рубля</NuxtLink>
    </nav>
  </header>
</template>

<script>
export default {
  name: "VHeader"
}
</script>