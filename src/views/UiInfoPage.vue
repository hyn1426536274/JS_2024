<template>
    <hr>
    <div class="page">
      <h1 id="title" data-aos="fade-in">Interface</h1>
      <div class="contain">
        <div class="bottom_contain">
            <img id="bottom_mountain" src="../assets/mountain01.svg" data-aos="fade-up" data-aos-duration="800">
        </div>
        <div class="infos">
            <h2 data-aos="fade-left">界面设计</h2>
            <p data-aos="fade-left">提供用户友好的界面和交互方式：</p>
            <p data-aos="fade-left">一个直观、易于使用的用户界面</p>
            <p data-aos="fade-left">用户能够方便地上传、选择和转换音频文件。</p>
            <p data-aos="fade-left">及时的反馈和提示,获得优秀的使用体验。</p>
        </div>
        <div class="img_contain">
            <img class="imgs" id="img2" src="../assets/ui02.png" data-aos="fade-right" data-aos-duration="800">
            <img class="imgs" id="img3" src="../assets/ui03.png" data-aos="fade-right" data-aos-duration="800">
            <!-- on top -->
            <img class="imgs" id="img1" src="../assets/ui01.png" data-aos="fade-right" data-aos-duration="800">
        </div>

      </div>
    </div>
</template>

<script>
import AOS from 'aos';
import 'aos/dist/aos.css'; // You can also use <link> for styles
// ..
AOS.init();

export default {
  name: 'UiInfoPage',
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
    padding-bottom: 0;
    background-color: rgb(122, 60, 255);
    color: white;
    margin: 0;
    padding: 0;

    #title{
        font-size: 3rem;
        padding-top: 1%;
    }

    .contain{
        display: flex;
        justify-content: center;
        align-items: center;
        position: relative;
        height: 90%;

        .infos{
            position: relative;
            margin-bottom: 15%;
            text-align: left;
            width: 50%;
            margin-left: 10%;
            h2{
                font-size: 2rem;
                margin-bottom: 30px;
            }
            p{
                font-size: 1.1rem;
                margin-bottom: 8px;
            
            }
        }
        .img_contain{
            width: 40%;
            height: 100%;
            margin-right: 10%;
            padding-top: 10%;
            position: relative;
            /* background-color: blue; */
            .imgs{
                left: 0;
                width: 100%;
                position: absolute;
                padding: 10px;
                background-color: rgb(0, 0, 0);
                border: 2px solid rgb(255, 255, 255);
                border-radius: 10px;
                box-shadow: 0px 0px 5px 3px rgb(163, 163, 163);
            }
            #img1{
                width: 100%;
            }
            #img2{
                width: 100%;
                transform: translate3d(20%,150%,0);
                opacity: 70%;
            }
            #img3{
                width: 40%;
                transform: translate3d(-50%,-40%,0);
                opacity: 70%;
            }
        }
        .bottom_contain{
            position: absolute;
            width: 100%;
            height: 20%;
            bottom: -10%;
            background-color: rgb(122, 60, 255);
            margin: 0;
            padding: 0;
            #bottom_mountain{
                position: absolute;
                width: 100%;
                bottom: 0;
                left: 0;
            }
        }
    }
    
}
</style>