<template>
  <div class="about">
    <h1>This is an about page</h1>
    <NewPage>
      <template #header="props">
        <p>header data {{ props.inputData }}</p>
      </template>
      <template #default>
        <p>default place</p>
      </template>
      <div>
        <h1>Hello</h1>
        <p>Hi</p>
      </div>
    </NewPage>
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