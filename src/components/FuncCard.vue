<template>
        <div class="card">
            <div class="card_title">
                <h2>{{title}}</h2>
            </div>
            <div class="card_content">
                <p>{{content}}</p>
            </div>
        </div>
</template>

<script>
import AOS from 'aos';
import 'aos/dist/aos.css'; // You can also use <link> for styles
// ..
AOS.init();

export default {
    props: {
        title: String,
        content: String
    },
  name: 'FuncCard',
}
</script>

<style scoped>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
.card{
    width: 15%;
    min-width: 200px;
    height: 300px;
    background-color: rgb(255, 255, 255);
    margin: 0 50px;
    padding-bottom: 10%;
    border-radius: 10px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
    overflow: hidden;
    transition: all 0.5s;
    .card_title{
        padding: 10px;
        background-color: rgb(255, 255, 255);
        transition: all 0.5s;
        border-bottom: 2px solid rgb(121, 0, 0);
    }

    .card_content{
        padding: 20px;
        font-size: 16px;
        line-height: 30px;
    }
}
.card:hover{
    transform: scale(1.1);
    box-shadow: 0 0 8px 5px rgba(165, 165, 165, 0.2);
}
.card:hover .card_title{
    background-color: rgb(188, 83, 83);
    color: white;
    border-bottom: none;
}
</style>