<template>
    <header>
        <div class="hd-left">
            <img src="../img/dc-logo.png" alt="Logo DC">
        </div>
        <div class="hd-right">
            <ul class="lnikstyle">
                <li v-for="link, i in navLink" :key="i">
                    <a href="">{{link.text}}</a>
                </li>
            </ul>
        </div>
    </header>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'Header',
  data () {
    return {
      navLink: [
        {
          text: "CHARACTERS",
          visible: "False",
        },
        {
          text: "COMIC",
          visible: "False",
        },
        {
          text: "MOVIES",
          visible: "False",
        },
        {
          text: "TV",
          visible: "False",
        },
        {
          text: "GAMES",
          visible: "False",
        },
        {
          text: "COLLECTIBLES",
          visible: "False",
        },
        {
          text: "VIDEOS",
          visible: "False",
        },
        {
          text: "FANS",
          visible: "False",
        },
        {
          text: "NEWS",
          visible: "False",
        },
        {
          text: "SHOP",
          visible: "False",
        },
      ]
    }
  },
}
</script>

<style lang="scss">

header {
    height: 150px;
    background-color: #fff;
    width: 80%;
    margin: auto;
} 
.hd-left {
        width: 40%;
        float: left;   
        height: 100%;
        display: flex;
        align-items: center;
}
.hd-right{
    width: 60%;
    float: right;
    height: 100%;
    display: flex;
    align-items: center;
}

.hd-left img {
    height: 50%;
}

.lnikstyle {
    font-size: 15px;
    width: 100%;
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
}

.lnikstyle li a {
    color: #000;
    padding: 7px;
    font-weight: 700;

}

.active {
    font-size: 500px;
}

</style>
