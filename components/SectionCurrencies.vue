<template>
  <section class="grid grid-flow-row auto-rows-max xl:grid-cols-3 md:grid-cols-2 gap-7 md:mb-8 mb-4">
    <div
      class="flex flex-col rounded-2xl bg-gray 2xl:px-9 2xl:py-14 md:px-6 md:py-10 px-6 py-6 hover:cursor-pointer hover:shadow-md"
      v-for="(currency) in apiCurrencies" :key="currency['CharCode']"
    >
      <svgCurrency class="text-primary md:mb-8 mb-6 2xl:w-[70px] 2xl:h-[70px] xl:w-[57px] xl:h-[57px] w-[50px] h-[50px]"/>
      <span class="font-bold xl:text-20 md:text-18 text-17 mb-5">
        {{currency["CharCode"]}}
      </span>
      <span class="2xl:text-16 xl:text-15 text-14 mb-10">
        {{currency["Name"]}}
      </span>
      <VList class="2xl:text-16 xl:text-15 text-14 font-medium md:mt-auto xl:gap-4 gap-2" :items='[
        `Номинал: ${currency["Nominal"]}`,
        `Курс: ${currency["Value"]}`
      ]'/>
    </div>
  </section>
</template>

<script>
import svgCurrency from "@/assets/icons/currency.svg"
export default {
  name: "SectionCurrencies",
  data() {
    return {
      apiCurrencies: {}
    }
  },
  async fetch() {
    try {
      let response = await this.$axios.get('https://www.cbr-xml-daily.ru/daily_json.js');
      this.apiCurrencies = response.data["Valute"];
    } catch (e) {
      alert(e);
      throw e;
    } finally {}
  },
  components: {
    svgCurrency
  }
}
</script>