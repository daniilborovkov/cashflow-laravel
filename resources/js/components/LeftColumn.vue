<template lang="pug">
  div
    incomes
    charges
</template>

<script>
import Incomes from './left-column/Incomes.vue';
import Charges from './left-column/Charges.vue';

export default {
  components: {
    Incomes,
    Charges,
  }
}
</script>

