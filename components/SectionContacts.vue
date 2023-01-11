<template>
  <section class="flex md:flex-row md:items-center flex-col xl:gap-10 md:gap-6 gap-7 bg-gray xl:px-10 xl:py-12 px-6 py-7 rounded-2xl">
    <svgAttention class="text-primary 2xl:w-[50px] 2xl:h-[50px] xl:w-[45px] xl:h-[45px] w-[42px] h-[42px]"/>
    <span class="font-bold xl:text-20 md:text-18 text-16 text-primary">
      <a href="tel:+78008889028" class="whitespace-nowrap">Телефон: 8 (800) 888-90-28</a>,
      <a href="mailto:info@example.ru" class="whitespace-nowrap">email: info@example.ru</a>.
    </span>
  </section>
</template>

<script>
import svgAttention from "@/assets/icons/attention.svg";
export default {
  name: "SectionContacts",
  components: {
    svgAttention
  }
}
</script>