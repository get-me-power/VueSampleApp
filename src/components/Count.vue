<template>
<div>
    <!-- :classはv-bindしているよ -->
    <div :class="[isRed ? 'text-red': 'text-blue']">{{ count }}回クリック</div>
    <!-- Vueの中でクリックしたらincrementメソッドを呼び出す-->
    <button v-on:click="increment">カウントを増やす</button>
    <button v-on:click="decrement">カウントを減らす</button>
    <div class='counter'>Count</div>
    <div class="text-blue">{{ ClickCount }}</div>
    <img v-bind="imageItem">
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
            ClickCount: 0,
            isRed: true,
            imageItem: {
                id: 1,
                src: "https://cdn-ssl-devio-img.classmethod.jp/wp-content/uploads/2018/09/vim-e1537247611733.png",
                alt: "Vim使ってますか？使ってない？使いましょう",
                width: 200,
                height: 200

            }
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

