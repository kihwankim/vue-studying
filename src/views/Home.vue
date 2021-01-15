<template>
  <div>
    <h1>This is homepage</h1>
    <NewPage></NewPage>
  </div>
</template>

<script>
    import NewPage from '@/components/NewPage.vue';
    export default {
      components: {
        NewPage
      },
      data() {
        return {
          name: 'kihwan kim'
        }
      }
    }
</script>

<style scoped>
h1 {
  color: red;
}
</style>