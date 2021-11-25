<template>
    <footer id="footer1">
        <div>
            <div></div>
            <div></div>
            <div></div>
        </div>
        <div>
            <img id="image-logo-bg" src="../assets/img/dc-logo-bg.png" alt="">
        </div>
    </footer>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'Footer',
 
}
</script>

<style lang="scss">

#footer1 {
  background-image: url("../assets/img/footer-bg.jpg");
  width: 100%;
  height: 400px;
    div {
      width: 50%;
      height: 100%;
      float: left;
      display: flex;
      align-items: center;
      overflow: hidden;
  }
}

#image-logo-bg {
  height: 140%;
}

</style>
