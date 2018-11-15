<template lang="pug">
  .assets
    .card
      .card-header
        | Активы
      ul.list-group.list-group-flush
        li.list-group-item(v-for="asset in assets" :key="asset.title" :value="asset")
          div.transaction-item
            div {{asset.title}}
            div {{asset.value}} {{asset.currency === 'default' ? 'RUB' : asset.currency}}
</template>

<script>
export default {

  name: 'Assets',

  data () {
    return {
      assets: [
      ]
    }
  }
}
</script>

<style lang="css" scoped>
</style>