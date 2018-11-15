<template lang="pug">
  .incomes
    .card
      .card-header
        | Доходы
      ul.list-group.list-group-flush
        li.list-group-item(v-for="income in incomes" :key="income.title" :value="income")
          div.transaction-item
            div {{income.title}}
            div {{income.value}} {{income.currency === 'default' ? 'RUB' : income.currency}}
</template>

<script>
export default {
  name: 'Incomes',
  data: () => {
    return {
      incomes: [
        {
          title: "Зарплата",
          value: "3500",
          currency: "default",
        }
      ]
    }
  }
}
</script>

<style lang="scss">
</style>