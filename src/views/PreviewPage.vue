<template>
    <div class="page">
        <div class="bg_img"> 
            <h1 id="title" data-aos="fade-in">Samples</h1>
            <img  src="../assets/bg01.svg" alt="bg"  data-aos="zoom-in"/>
        </div>
        <div class="vedio_contain">
            <div class="vedio_block">
                <h2 class="vedio_name">Taylor</h2>
                <video class="vedio_media" controls=""  name="media">
                <source src="../assets/music/taylor.mp3" type="audio/mpeg">
                </video>
            </div>
            <div class="vedio_block">
                <h2 class="vedio_name">Trump</h2>
                <video class="vedio_media" controls=""  name="media">
                <source src="../assets/music/trump.mp3" type="audio/mpeg">
                </video>
            </div>
            <div class="vedio_block">
                <h2 class="vedio_name">Adele</h2>
                <video class="vedio_media" controls=""  name="media">
                <source src="../assets/music/adele.mp3" type="audio/mpeg">
                </video>
            </div>
            <div class="vedio_block">
                <h2 class="vedio_name">Justin</h2>
                <video class="vedio_media" controls=""  name="media">
                <source src="../assets/music/justin.mp3" type="audio/mpeg">
                </video>
            </div>
            <div class="vedio_block">
                <h2 class="vedio_name">Ours</h2>
                <video class="vedio_media" controls=""  name="media">
                <source src="../assets/music/other.mp3" type="audio/mpeg">
                </video>
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
    name: 'PreviewPage',
}
</script>

<style scoped>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    z-index: 1;
}

.page {
    width: 100%;
    min-height: 100vh;
    background-color:#ED322E;
    position: relative;
    overflow: hidden;

    .bg_img{
        width: 100%;
        height: 100%;
        position: absolute;
        top: 0;
        left: 0;
        #title{
            font-size: 3rem;
            padding-top: 1%;
            color: white;
            text-align: center;
        }
        img{
            opacity: 0.3;
        }
    }
    .vedio_contain {
        display: flex;
        justify-content: center;
        align-items: center;
        width: 100%;
        height: 100%;
        margin-top: 10%;
        flex-wrap: wrap;

        .vedio_block {
            width: 25%;
            min-width: 250px;
            margin: 5% 2%;
            background-color: aliceblue;
            border-radius: 10px;
            overflow: hidden;
            opacity: 0.9;
            transition: all 0.5s;
            .vedio_name {
                text-align: center;
                font-size: 1.5rem;
                padding: 10px;
                background-color: rgb(255, 255, 255);
                color: rgb(0, 0, 0);
                border-bottom: 1px solid rgb(0, 0, 0);
            }
            .vedio_media {
                width: 100%;
                margin-top: 5%;
                height: 50px;
            }
        }
        .vedio_block:hover {
            opacity: 1;
            transform: scale(1.02);
            box-shadow: 0 0 8px 5px rgba(91, 91, 91, 0.2);
        }
    }

}
</style>