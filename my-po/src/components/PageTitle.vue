<template>
    <div class="main_title">
        <p class="page_num">{{ page_numOfChild }}</p>
        <h2 class="page_name">{{ page_nameOfChild }}</h2>
    </div>
</template>

<script>
export default {
  name: 'PageTitle',
  props: ['page_numOfChild','page_nameOfChild'],
    data() {
      return {
        }
    },
}
</script>

<style>

</style>