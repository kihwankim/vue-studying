<template>
  <div class="about">
    <h1>This is an about page</h1>
    <NewPage title="about page"/>
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