<template>
    <div>
        <p>header</p>
        <slot name="header" :inputData="testData"></slot>
        <p>Body</p>
        <slot></slot>
        <p>footer</p>
        <button @click="updateName">Change Name</button>
    </div>
</template>

<script>
    export default {
        props: {
            'title': {
                type: String, // type설정 한다
                required: false // 무조건 받아야한는 것을 명시
            },
            'name': {
                type: String,
                required: false
            }
        },
        data() {
            return {
                testData: 'child component data'
                // name: 'kihwan kim'
            } // props 에서 사용하는 변수는 data에서 사용할 수 없음
        },
        methods: {
            updateName() {
                // this.name = "new Name Kihwan kim";  부모 컴포넌트에서 바꿔줘야 한다.
            }
        }
    }
    // <NewPage></NewPage> 사이에 작성된 html tag는 자동으로 slot 안으로 들어가게 된다.
    // name을 설정하면 template에서 v-slot: 으로 설정된 테그를 가지고 온다
    // default : name 이 없는 경우 default로 들 어간다.
</script>

<style scoped="scoped"></style>