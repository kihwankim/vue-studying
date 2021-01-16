<template>
  <div>
    <h1>This is homepage</h1>
    <!-- <NewPage title="home title"/> -->
    <form action="">
      <InputFields v-model="name" />
      <button>Submit</button>
    </form>
    {{ name }}
  </div>
</template>

<script>
    import InputFields from '@/components/InputFields';
    // import NewPage from '@/components/NewPage.vue';
    export default {
      components: {
        InputFields
      },
      data() {
        return {
          name: ''
        }
      },
      methods: {
        updateName(name) { // event 이름 설정
          this.name = name;
        }
      }
    }
</script>

<style scoped>
h1 {
  color: red;
}
</style>