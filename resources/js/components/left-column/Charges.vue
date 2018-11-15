<template lang="pug">
  .charges
    .card
      .card-header
        | Доходы
      ul.list-group.list-group-flush
        li.list-group-item(v-for="charge in charges" :key="charge.title" :value="charge")
          div.transaction-item
            div {{charge.title}}
            div {{charge.value}} {{charge.currency === 'default' ? 'RUB' : charge.currency}}
</template>

<script>
export default {

  name: 'Charges',

  data () {
    return {
      charges: [
        {
          title: "Общие",
          value: "1500",
          currency: "default",
        },
        {
          title: "Кредит",
          value: "1000",
          currency: "default",
        }
      ]
    }
  }
}
</script>

<style lang="css" scoped>
</style>