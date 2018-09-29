<template>
<div id="app">
    <div id="wrapper">
        <div id="sidebar" class="bg-dark">
            <div id="logo_wrapper" class="px-4">
                <img class="img-fluid" src="./assets/logo.png">
            </div>
            <TransactionsList />
        </div>
        <div id="content">
            <div class="container-fluid">
                <div class="row">
                    <div class="col">
                    </div>
                </div>
            </div>
        </div>
    </div>
</div>
</template>

<script>
import TransactionsList from './components/TransactionsList.vue';

export default {
  name: 'app',
  components: {
    TransactionsList,
  },
};
</script>

<style lang="scss">
// importing the main theme.
@import './assets/theme/scss/toolkit-inverse.scss';

#app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
}

#wrapper {
  width: 100%;
  height: 100%;
  background-color: rgb(77,86,95);
  overflow: hidden;
}

#wrapper > #sidebar {
  height: 100%;
  width: 300px;
  top: 0;
  bottom: 0;
  position: fixed;
  z-index: 10;
  background-color: $gray-darkest;
}

#content {
  height: 100%;
  width: 100%;
  margin-left: 300px;
}

#logo_wrapper {
  display: inline-block;
  border-bottom: 1px solid rgb(77,86,95);
  height: 120px;
}

</style>
