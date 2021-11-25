<template>
  <footer id="footer1">
    <div class="containerauto">
      <div class="cont-footer cont-list">
        <ul class="list-footer-menu">
          <h1>DC COMICS</h1>
          <li v-for="(comic, i) in dcComic" :key="i">
            {{ comic.text }}
          </li>
        </ul>
        <ul class="list-footer-menu">
          <h1>DC</h1>
          <li v-for="term, i in DcTerm" :key="i">
              {{ term.text }}
          </li>
        </ul>
         <ul class="list-footer-menu">
          <h1>SITES</h1>
          <li v-for="site, i in Sites" :key="i">
              {{ site.text }}
          </li>
        </ul>
        <ul class="list-footer-menu shopnav">
          <h1>SHOP</h1>
          <li v-for="item, i in Shop" :key="i">
              {{ item.text }}
          </li>
        </ul>
      </div>
      <div class="cont-footer image-center">
          <img id="image-logo-bg" src="../assets/img/dc-logo-bg.png" alt="" />
      </div>
    </div>
  </footer>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'

export default {
  name: "Footer",
  data() {
    return {
      dcComic: [
        {
          text: "Characters",
        },
        {
          text: "Comics",
        },
        {
          text: "Movies",
        },
        {
          text: "TV",
        },
        {
          text: "Games",
        },
        {
          text: "Videos",
        },
        {
          text: "News",
        },
      ],
      DcTerm: [
        {
          text: "Terms Of Use",
        },
        {
          text: "Privacy policy(New)",
        },
        {
          text: "Ad Choices",
        },
        {
          text: "Advertising",
        },
        {
          text: "Jobs",
        },
        {
          text: "Subscriptions",
        },
        {
          text: "Talent Workshops",
        },
        {
          text: "CPSC Certificates",
        },
        {
          text: "Ratings",
        },
        {
          text: "Shop Help",
        },
        {
          text: "Contact Us",
        },
      ],
      Sites: [
        {
          text: "DC",
        },
        {
          text: "MAD Magazine",
        },
        {
          text: "DC Kids",
        },
        {
          text: "DC Universe",
        },
        {
          text: "DC Power Visa",
        },
      ],
      Shop: [
        {
          text: "Shop DC",
        },
        {
          text: "Shop DC Collectibles",
        },
      ],
    };
  },
};
</script>

<style lang="scss">
#footer1 {
  background-image: url("../assets/img/footer-bg.jpg");
  width: 100%;
  height: 400px;
}

#image-logo-bg {
  height: 140%;
}

.cont-footer {
    width: 50%;
    height: 100%;
    float: left;
    display: flex;
    overflow: hidden;
}

.cont-list {
  padding-top: 50px;
  padding-bottom: 50px;
}

.image-center {
    display: flex;
    align-items: center;
    overflow: hidden;
}

.list-footer-menu {
  padding: 30px;
  color: #fff;
  h1 {
    margin-bottom: 10px;
    margin-top: 10px;
    font-size: 30px;
  }
  li {
    font-size: 15px;
    font-weight: 700;
    cursor: pointer;
    color: grey;

  }
}

</style>
