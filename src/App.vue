<template>
  <div id="app">
    <div class="container">
      <pp-header></pp-header>
    </div>
    <div class="container">
      <router-view></router-view>
    </div>
    <div class="container">
      <div class="row">
        <div class="col-sm-12 col-md-4">
          <router-view name="ordering"></router-view>
        </div>
        <div class="col-sm-12 col-md-4">
          <router-view name="delivery"></router-view>
        </div>
        <div class="col-sm-12 col-md-4">
          <router-view name="history"></router-view>
        </div>
      </div>
    </div>
    <div class="container">
      <pp-footer></pp-footer>
    </div>
  </div>
</template>

<script>
import Header from './components/Header.vue';
import Footer from './components/Footer.vue';

export default {
  components: {
    ppHeader: Header,
    ppFooter: Footer
  }
}
</script>

<style lang="scss">
#home {
  background: url('../src/assets/pizza.jpg');
  height: 800px;
  padding: 10%;
}

  h1, h2 {
    margin: 6%;
  }

  .background {
    background: #eee;
    opacity: 0.8;
    max-width: 60%;
    margin: 0 auto;
    padding: 20px 0;
  }
</style>
