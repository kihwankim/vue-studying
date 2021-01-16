<template>
    <div>
        <label for="Name">Name</label>
        <input type="text" :value='name' style="pading: 30px;" @input="updateName"/>
    </div>
</template>

<script>
    export default {
        props: {
            value: {
                type: String,
                required: true
            }
        },
        methods: {
            updateName(e) {
               
                this.$emit('input', e.target.value) // 부모 컴포넌트로 데이터를 올리는 것
            }
            // 부모 컴포넌트에서 설정한 event이름 : update-name 그리고 인자 값 : e.target.value가 된다 <!--
            // @input="$emit('update-name', $event.target.value)" 도 가능
        }
    }
</script>