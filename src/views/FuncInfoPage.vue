<template>
    <hr>
    <div class="page">
      <h1 id="title" data-aos="fade-in">Advantages</h1>
      <div class="up_contain">
        <img id="bird_01" class="birds" src="../assets/bird01.svg" alt="bird01" data-aos="zoom-in">
        <img id="bird_02" class="birds" src="../assets/bird02.svg" alt="bird02" data-aos="zoom-in">
      </div>
      <div class="info_contain" data-aos="zoom-in">
        <FuncCard title="Fast" content="快速的分解和推理，4min音频的推理时间仅需60s左右"/>
        <FuncCard title="Small" content="简化和轻量的推理模型，压缩后的大小可以从600MB缩小到60MB"/>
        <FuncCard title="Personalized" content="个性化的定制和使用，不仅提供模型，还支持用户自定义训练，将数据预处理集成到平台中，无需用户自行实现"/>
        <FuncCard title="Preview" content="支持预览，对于打开的音频和中间结果分别设计了预览模块，直接试听效果"/>
      </div>
    </div>
</template>

<script>
import AOS from 'aos';
import 'aos/dist/aos.css'; 

import FuncCard from '../components/FuncCard.vue';

AOS.init();

export default {
  name: 'FuncInfoPage',
  components: {
    FuncCard
  }
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
    min-height: 100vh;
    background-color: #fff0f0;
    position: relative;
    overflow: hidden;

    #title{
        font-size: 3rem;
        padding-top: 1%;
    }
.up_contain{
        width: 100%;
        height: 30%;
        position: absolute;
        top: 0;
        .birds{
            height: 100%;
            top: 0;
            transition: all 0.8s;
        }
        #bird_01{
            float: left;
            margin-left: 5%;
        }
        #bird_02{
            float: right;
            margin-right: 5%;
        }
    }
    .info_contain{
        width: 100%;
        display: flex;
        justify-content: center;
        align-items: center;
        position: relative;
        flex-wrap: wrap;
        margin-top: 12%;
        transition: all 0.8s;
    }
    
}
</style>