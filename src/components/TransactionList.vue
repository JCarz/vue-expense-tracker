<template>
  <h3>History</h3>

  <ul id="list" class="list">
    <!-- Using Vue.js v-for directive to loop through transactions array -->
    <li
      v-for="transaction in transactions"
      :key="transaction.id"
      :class="transaction.amount < 0 ? 'minus' : 'plus'"
    >
      <!-- Setting a unique key for each transaction and Applying dynamic class based on transaction amount 'minus' : 'plus' -->
      >
      {{ transaction.text }} <span>${{ transaction.amount }}</span
      ><button class="delete-btn">x</button>
    </li>
  </ul>
</template>
<script>
export default {
  data() {
    return {
      transactions: [
        { id: 1, text: "Flower", amount: -19.99 },
        { id: 2, text: "Wallpaper", amount: 1300.99 },
        { id: 3, text: "teesst", amount: -14.99 },
      ],
    }
  },
}
</script>
