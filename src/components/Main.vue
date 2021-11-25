<template>
    <main>
        <section class="content">
            <div class="stylesection containerauto">
                <h1> --> Contet goes here </h1>
            </div>
        </section>
        <section class="digital-comics">
            <div class="stylesection containerauto">
                <div v-for="merch, i in mainMerch" :key="i" class="box-merch">
                    <img :src="merch.img" alt="">
                    <h3>{{merch.text}}</h3>
                </div>
            </div>
        </section>
    </main>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'Main',
    data () {
        return {
            mainMerch: [
                {
                    text: "DIGITAL COMICS",
                    img: "../assets/img/buy-comics-digital-comics.png",
                },
                {
                    text: "DC MERCHANDISE",
                    img: "../assets/img/buy-comics-merchandise.png",
                },
                {
                    text: "SUBSCRIPTION",
                    img: "../assets/img/buy-comics-subscriptions.png",
                },
                {
                    text: "COMIC SHOP LOCATOR",
                    img: "../assets/img/buy-comics-shop-locator.png",
                },
                {
                    text: "DC POWER VISA",
                    img: "../assets/img/buy-dc-power-visa.png",
                },
            ]
        }
    },
}
</script>

<style lang="scss">
.content {
    width: 100%;
    height: 150px;
    background-color: rgb(41, 41, 41);
}

.digital-comics {
    width: 100%;
    height: 200px;
    background-color: rgb(75, 129, 255);
}

.stylesection {
    display: flex;
    align-items: center;
    height: 100%;

}

.stylesection > h1{
    color: #fff;
    font-weight: 700;
}

.box-merch {
    width: calc(100% / 5);
    display: flex;
    align-items: center;
}



</style>
