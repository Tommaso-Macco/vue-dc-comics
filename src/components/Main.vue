<template>
    <main>
        <div class="jumbotron"></div>
        <section id="bgcolor-main">
            <div class="container-series containerauto">
                <div id="square-series">CURRENT SERIES</div>
                <div class="container-box">
                    <div class="serie" v-for="article, i in Articles" :key="i">
                        <img :src="article.thumb" :alt="article.series">
                        <h3> {{ article.series }} </h3>
                    </div>
                </div>
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
            ],
            Articles: [
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/AC1000_DLX_162-001_HD_5ba13723281ab0.37845353.jpg?itok=ZsI-C5eX",
                    "price": "$19.99",
                    "series": "Action Comics",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/AV1976_01_300-001_HD_5f738f6e39ddd7.18205602.jpg?itok=VgdYdJ01",
                    "price": "$3.99",
                    "series": "American Vampire 1976",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2018/08/AQMv4_UW_153-001_HD_5b7efa1745a9b8.08589135.jpg?itok=HPTtnrsb",
                    "price": "$16.99",
                    "series": "Aquaman",
                    "type": "graphic novel"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/06/batgirl_v5_1_5b23e1f1124941.50950783.jpg?itok=VnrJah76",
                    "price": "$2.99",
                    "series": "Batgirl",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
                    "price": "$3.99",
                    "series": "Batman",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
                    "price": "$2.99",
                    "series": "Batman Beyond",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2019/08/BMSM_5d4361b7116261.74371456.jpg?itok=kEDR2OL8",
                    "price": "$3.99",
                    "series": "Batman/Superman",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMSMANN_01_300-001_HD_5f5ff17fa1d665.74704970.jpg?itok=azz5sfGk",
                    "price": "$4.99",
                    "series": "Batman/Superman Annual",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMTJWZ_01_300-001_HD_5f5ff2307dcb37.34652945.jpg?itok=VswVjLR8",
                    "price": "$5.99",
                    "series": "Batman: The Joker War Zone",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/08/cover-v2_5f40314645a734.37285065.png?itok=ImNM2QBY",
                    "price": "$6.99",
                    "series": "Batman: Three Jokers",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/10/BMWK_HQ_01_300-001_HD_5f7cb4945e13f6.89501032.jpg?itok=sVwALbUX",
                    "price": "$4.99",
                    "series": "Batman: White Knight Presents: Harley Quinn",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2019/04/CTWv1_CC_144-001_HD_5ca5299a751963.53054221.jpg?itok=ooPaoLDq",
                    "price": "$16.99",
                    "series": "Catwoman",
                    "type": "graphic novel"
                },
                ]
        }
    },
}
</script>

<style lang="scss">
.jumbotron {
    width: 100%;
    height: 400px;
    background-image: url("../assets/img/jumbotron.jpg");
    background-repeat: no-repeat;
    background-size: cover;
    position: relative;
}

#bgcolor-main {
    background-color: #000;
    min-height: 500px;
}

.container-series {
    height: 100%;
    position: relative;
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

#square-series {
    position: absolute;
    left: 0;
    top: -20px;
    height: 40px;
    background-color: blue;
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 10px;
    color: #fff;
    font-weight: 1000;
    font-size: 15px;
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

.container-box {
    width: 100%;
    height: 100%;
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
}

.serie {
    width: calc(100% / 6);
    height: 200px;
    overflow: hidden;
    padding-left: 30px;
    padding-right: 30px;
    padding-bottom: 50px;
    padding-top: 30px;
    img {
        
    }
    h3 {
        color: #fff;
    }
}

</style>
