<template>
  <section class="flex flex-col border border-[#DFE1F0] rounded-2xl 2xl:gap-12 xl:gap-10 gap-6 bg-secondary 2xl:px-8 2xl:py-10 xl:px-6 xl:py-8 px-4 py-6">
    <h5 class="2xl:text-18 xl:text-15 text-13 text-primary uppercase font-medium">
      Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor:
    </h5>

    <div class="flex flex-col md:flex-row items-top justify-between md:gap-3 gap-7">
      <VList class="2xl:text-18 text-14 gap-4 max-w-[280px]" :items='[
        "incididunt ut labore et dolore magna aliqua",
        "incididunt ut labore et",
        "incididunt ut labore et dolore",
        "labore et dolore",
        "incididunt ut",
        "incididunt ut labore et dolore",
        "incididunt ut labore",
      ]'/>

      <figure class="xl:grid xl:grid-cols-2 flex md:flex-col 2xl:gap-x-[15px] 2xl:gap-y-[9px] xl:gap-x-[10px] xl:gap-y-[10px] gap-2 justify-center">
        <VImage file-name="img-1.jpg" :is-bg="true" class="2xl:w-[146px] 2xl:h-[146px] xl:w-[116px] xl:h-[116px] xl:rounded-none md:w-[86px] md:h-[58px] w-[68px] h-[45px] rounded-tr-[20%] rounded-bl-[20%]"/>
        <VImage file-name="img-2.jpg" :is-bg="true" class="2xl:w-[146px] 2xl:h-[146px] xl:w-[116px] xl:h-[116px] xl:rounded-none xl:rounded-tr-[40%] md:w-[86px] md:h-[58px] w-[68px] h-[45px] rounded-tl-[20%] rounded-br-[20%]"/>
        <VImage file-name="img-3.jpg" :is-bg="true" class="2xl:w-[146px] 2xl:h-[146px] xl:w-[116px] xl:h-[116px] xl:rounded-none xl:rounded-bl-[40%] md:w-[86px] md:h-[58px] md:rounded-tr-none md:rounded-bl-none md:rounded-tl-[20%] md:rounded-br-[20%] w-[68px] h-[45px] rounded-tr-[20%] rounded-bl-[20%]"/>
        <VImage file-name="img-4.png" :is-bg="true" class="2xl:w-[146px] 2xl:h-[146px] xl:w-[116px] xl:h-[116px] xl:rounded-none md:w-[86px] md:h-[58px] w-[68px] h-[45px] rounded-tl-[20%] rounded-br-[20%]"/>
      </figure>
    </div>
  </section>
</template>

<script>
export default {
  name: "SectionBuildings"
}
</script>
