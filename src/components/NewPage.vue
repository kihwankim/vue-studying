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
            'title': {
                type: String, // type설정 한다
                required: true // 무조건 받아야한는 것을 명시
            },
            'name': {
                type: String,
                required: false
            }
        },
        data() {
            return {
                // name: 'kihwan kim'
            } // props 에서 사용하는 변수는 data에서 사용할 수 없음
        },
        methods: {
            updateName() {
                // this.name = "new Name Kihwan kim"; // 부모 컴포넌트에서 바꿔줘야 한다.
            }
        }
    }
</script>

<style scoped="scoped"></style>