<template>
  <section>
    <form class="flex flex-col 2xl:gap-10 gap-5">
      <fieldset class="flex flex-col md:gap-8 gap-5">
        <VField v-model="fromCurrency" label="Валюта 1" placeholder="Введите название или код"/>
        <VField v-model="toCurrency" label="Валюта 2" placeholder="Введите название или код"/>
        <VField v-model="amount" label="Количество" placeholder="Введите число"/>
      </fieldset>

      <div class="flex xl:gap-10 gap-5 items-center bg-secondary xl:px-10 xl:py-12 md:px-7 md:py-9 px-6 py-5 rounded-2xl">
        <svgAttention class="text-red 2xl:w-[50px] 2xl:h-[50px] xl:w-[45px] xl:h-[45px] w-[42px] h-[42px]"/>
        <span class="font-bold 2xl:text-24 xl:text-20 md:text-16 text-14 text-primary">
          Итого: {{calculatedValue}}
        </span>
      </div>
    </form>
  </section>
</template>

<script>
import svgAttention from "@/assets/icons/attention.svg";
export default {
  name: "SectionCalculator",
  async fetch() {
    try {
      const response = await this.$axios.get('https://www.cbr-xml-daily.ru/daily_json.js');
      this.apiCurrencies = response.data["Valute"];
    } catch (e) {
      alert(e);
      throw e;
    } finally {}
  },
  data() {
    return {
      apiCurrencies: {},
      fromCurrency: "",
      toCurrency: "",
      amount: ""
    }
  },
  computed: {
    calculatedValue() {
      const a = this.findApiCurrency(this.fromCurrency)?.["Value"];
      const b = this.findApiCurrency(this.toCurrency)?.["Value"];
      const isAmountValid = /^[+-]?\d+(\.\d+)?$/.test(this.amount);

      if (a && b && isAmountValid) {
        return (parseFloat(a) / parseFloat(b) * this.amount).toFixed(4);
      } else {
        return "...";
      }
    }
  },
  methods: {
    findApiCurrency(currency) {
      const byKeys = ["CharCode", "Name"];
      return Object.values(this.apiCurrencies).find(
        apiCurrency => byKeys.filter(key => apiCurrency[key].toLowerCase() === currency.toLowerCase()).length
      )
    },
  },
  components: {
    svgAttention
  }
}
</script>
