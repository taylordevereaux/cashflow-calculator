<template>
<div id="transactions">
  <ul>
    <li v-for="item in transactions" :key="item.id">
      <div class="list-item flex">
        <span class="date">{{ item.date }}</span>
        <span class="amount" v-bind:class="{ pos: item.amount>=0, neg: item.amount<0}">
            {{ item.amount }}
        </span>
      </div>
    </li>
  </ul>
</div>
</template>

<script>
export default {
  name: 'TransactionsList',
  // props: {
  //     msg: String,
  // },
  data() {
    return {
      transactions: [{
        id: 1,
        text: 'Paycheck',
        amount: 344.34,
        date: '2018-09-27',
        repeats: 'biweekly',
      }, {
        id: 2,
        text: 'Internet',
        amount: -96.54,
        date: '2018-09-13',
        repeats: 'monthly',
      }],
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->

<style lang="scss" scoped>
@import '../assets/theme/scss/variables-inverse.scss';

ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
}

ul .list-item {
  display: flex;
  flex-wrap: nowrap;
  justify-content: space-between;
  margin: 10px;
}

.list-item .date {
  font-weight: bold;
}

.list-item .amount.pos {
  color: $brand-success;
}

.list-item .amount.neg {
  color: $brand-danger;
}
</style>
