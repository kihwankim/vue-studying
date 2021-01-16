<template>
    <div>
        <h1>This is homepage</h1>
        <!-- <NewPage title="home title"/> -->
        <form>
            <InputFields v-model="name"/>
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
            return {name: ''}
        },
        beforeCreate() {
            console.log('beforecreate', this.name);
        }, // data에 접근 불가 -> instance전 -> this 가 없음
        created() {
            console.log('created data', this.name);
        },
        beforeMount() {
            // alert('before mount');  내부 dom이 생성 되기 전 상태
        },
        mounted() {
            // alert('mounted');  dom 이 형성 되었을 때 -> id 가 app인 부분에 내부에 이미 몯느 컴포넌트가 다 생성 될 때
        },
        beforeUpdate() {
            alert('before updated')
        },
        updated() {
            alert('updated');
        },
        beforeDestroy() {
            alert('before destoried');
        },
        destroyed() {
            alert('destoryed');
        }
    }
</script>

<style scoped="scoped">
    h1 {
        color: red;
    }
</style>