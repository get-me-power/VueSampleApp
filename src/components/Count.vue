<template>
<div>
    <div class="text-red">{{ count }}回クリック</div>
    <!-- Vueの中でクリックしたらincrementメソッドを呼び出す-->
    <button v-on:click="increment">カウントを増やす</button>
    <button v-on:click="decrement">カウントを減らす</button>
    <div class='counter'>Count</div>
    <div class="text-blue">{{ ClickCount }}</div>
</div>
</template>

<script>
// new Vueの変わり 
export default {
    name: "Count",
    data() {
        return {
            //一番最初に初期化する
            count: 0,
            ClickCount: 0
        };
    },
    methods: {
        //メソッド名の簡略化
        increment (){
            this.count += 1;
            this.ClickCount += 1
        },
        decrement () {
            this.count -= 1;
            this.ClickCount += 1
        }
    }
};
</script>

<style scoped>
.counter {
    font-size: 26px;
    background-color: #dfd;
}
.text-red {
    color: #f22;
}
.text-blue {
    color: #22f
}
</style>

