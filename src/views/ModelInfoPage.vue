<template>
    <hr>
    <div class="page">
      <h1 id="title" data-aos="fade-in">Model Framework</h1>
      <div class="info_contain">
        <div class="infos">
            <h2 data-aos="fade-left" data-aos-offset="300">模型设计</h2>
            <p data-aos="fade-left" data-aos-offset="350">
                模型主要分成四大模块：
            </p>
            <p data-aos="fade-left" data-aos-offset="350">
                先验编码器模块、后验编码器模块、声码器模块、Flow模块
            </p>
            <p data-aos="fade-left" data-aos-offset="350">
                其中先验编码器模块包括特征提取模块、人声分类模块
            </p>
            <p data-aos="fade-left" data-aos-offset="350">
                声码器模块包括人声嵌入模块、上采样模块和激活模块
            </p>
        </div>
        <img class="imgs" src="../assets/m1.png" data-aos="zoom-in" data-aos-duration="800">
      </div>
      <div class="bottom_decoration_contain">
        <img id="bottom_plant" src="../assets/plant02.svg" data-aos="fade-up" data-aos-duration="800">
      </div>
    </div>
</template>

<script>
import AOS from 'aos';
import 'aos/dist/aos.css'; // You can also use <link> for styles
// ..
AOS.init();

export default {
  name: 'ModelInfoPage',
}
</script>

<style scoped>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
.page{
    color: white;
    width: 100%;
    height: 100vh;
    background-color: rgb(114, 136, 227);
    position: relative;

    #title{
        font-size: 3rem;
        padding-top: 1%;
    }

    .info_contain{
        display: flex;
        justify-content: center;
        align-items: center;
        padding-top: 8%;
        position: relative;

        .infos{
            text-align: left;
            width: 50%;
            margin-left: 10%;
            padding-bottom: 10%;
            h2{
                font-size: 2rem;
                margin-bottom: 30px;
            }
            p{
                font-size: 1.1rem;
                margin-bottom: 8px;
            }
        }
        .imgs{
            width: 40%;
            float: right;
            margin-right: 10%;
            padding: 20px;
            background-color: black;
            border-radius: 10px;
        }
    }
    .bottom_decoration_contain
    {
        width: 100%;
        position: absolute;
        bottom: 0;
        #bottom_plant{
            width: 20%;
            float: left;
        }
    }
    
}
</style>