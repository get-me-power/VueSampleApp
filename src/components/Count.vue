<template>
<div>
    <div>{{ count }}回クリック</div>
    <!-- Vueの中でクリックしたらincrementメソッドを呼び出す-->
    <button v-on:click="increment">カウントを増やす</button>
    <div class='counter'>Count</div>
</div>
</template>

<script>
export default {
    name: "Count",
    data() {
        return {
            //一番最初に初期化する
            count: 0
        };
    },
    methods: {
        increment: function() {
            this.count += 1;
        }
    }
};
</script>

<style scoped>
.counter {
    font-size: 26px;
    background-color: #dfd;
}
</style>

