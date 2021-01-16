<template>
    <div>
        <h1>{{ title }}</h1>
        <p>{{ name }}</p>
        <button @click="updateName">Change Name</button>
    </div>
</template>

<script>
    export default {
        props: {
            'title' : {
                type: String, // type설정 한다
                required: true // 무조건 받아야한는 것을 명시
            }
        },
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