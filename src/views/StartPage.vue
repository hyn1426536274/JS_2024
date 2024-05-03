<template>
    <div class="page">
      <h1 data-aos="zoom-in">Singing Voice Conversion</h1>
      <h3 data-aos="zoom-in">方便的音色转换平台</h3>
    </div>
</template>

<script>
import AOS from 'aos';
import 'aos/dist/aos.css';

AOS.init();

export default {
  name: 'StartPage',
}
</script>

<style scoped>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
.page{
    width: 100%;
    height: 100vh;
    background-image: url('../assets/bg02.png');
    background-size: cover;
    h1{
      /* background-color: aliceblue; */
        font-size: 5rem;
        padding-top: 20%;
        color:rgb(134, 113, 255);
    }
    h3{
        font-size: 1.5rem;
        color:rgb(96, 75, 218);
    }
}
</style>