<template>
  <div class="header_container">
    <header class="header">
      <div class="flex_between_center w100">
        <div class="logo">
          MONG's <br>
          Portfolio
        </div>
        <nav class="header_nav">
          <a href="#" v-for="(nav,idx) in navList" :key="idx">{{idx+1}}.{{nav}}</a>
        </nav>
      </div>
    </header>
  </div>
  
</template>

<script>
export default {
  data() {
    return {
      navList:['My information','About Me','Skill','Publishing','Contact']
    }
  },
}
</script>

<style scoped>
.header_container {
  background: var(--main_black);
  color: var(--main_white);
}
.header {
  width: 1200px;
  height: 50px;
  display: flex;
  margin: 0 auto;
}
.header_nav a {
  padding: 0 16px;
}
</style>
