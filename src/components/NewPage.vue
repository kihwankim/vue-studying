<template>
    <div>
        <h1>{{ title }}</h1>
        <p>{{ name }}</p>
        <button @click="updateName">Change Name</button>
    </div>
</template>

<script>
    export default {
        props: ['title'],
        data() {
            return {name: 'kihwan kim'}
        },
        methods: {
            updateName() {
                this.name = "new Name Kihwan kim";
            }
        }
    }
</script>

<style scoped="scoped"></style>