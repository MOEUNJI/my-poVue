<template>
<div class="background_black">
    <Header></Header>
    <div>
        <Home></Home>
        <Info></Info>
    </div>
  </div>
</template>

<script>
import Header from './components/HeaderView.vue'
import Home from './views/HomeView.vue'
import Info from './views/InfoView.vue'
export default {
  name: 'app',
  components: {
    Header,
    Home,
    Info,
  }
}
</script>

<style>
.background_black {
    background: #121212;
}
</style>
