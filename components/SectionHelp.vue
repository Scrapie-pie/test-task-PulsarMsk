<template>
  <section class="flex md:flex-row flex-col items-center gap-7 bg-secondary 2xl:px-16 2xl:py-16 xl:px-10 xl:py-12 md:px-5 md:py-8 px-2 py-7 rounded-2xl">
    <div class="md:text-left text-center max-w-[750px]">
      <h2 class="2xl:mb-7 xl:mb-6 md:mb-4 mb-4 text-primary 2xl:text-36 xl:text-28 md:text-18 text-16 md:font-medium font-bold">
        Нужна помощь? <br/>
        Мы поможем! Просто свяжитесь с нами.
      </h2>
      <p class="2xl:text-16 text-12 max-w-[550px]">
        Наши специалисты с радостью ответят на все ваши вопросы и дадут профессиональную консультацию по товарам.
      </p>
    </div>
    <div class="flex flex-col items-center w-full xl:max-w-[450px] max-w-[280px] xl:gap-6 gap-4 mx-auto leading-none">
      <a href="tel:+78008889028" class="text-primary font-medium 2xl:text-[50px] xl:text-[40px] md:text-24 text-26">
        8 (800) 888-90-28
      </a>
      <span class="uppercase 2xl:text-24 xl:text-18 text-12">
        или
      </span>
      <a href="mailto:info@example.ru" class="text-primary 2xl:text-34 xl:text-24 md:text-20 text-18">
        info@example.ru
      </a>
    </div>

  </section>
</template>

<script>
export default {
  name: "SectionHelp"
}
</script>