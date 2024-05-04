<template>
    <div class="page">
        <h1 id="title" data-aos="fade-down">DownLoad</h1>
        <div class="description">
            You can download the platform and models
        </div>
        <div class="version" data-aos="fade-down">
            <h2>v1.0.0</h2>
        </div>
        <div class="download_block" data-aos="zoom-in">
            <div class="download_platform">
                <img src="../assets/windows.svg" alt="windows">
            </div>
            <button class="download_button" @click="download_platform">
                <p class="download_p1">Windows</p>
                <p class="download_p2">x86-64</p>
            </button>
        </div>

        <div class="download_models" data-aos="fade-up">
            <h1>
                Pretrained Models
            </h1>
            <button  v-for="model in models" :key="model.id" class="download_button" @click="download_model(model.url,model.name)">
                <p class="download_p1">{{ model.name }}</p>
                <p class="download_p2"></p>
            </button>
        </div>
    </div>
</template>

<script>
import AOS from 'aos';
import 'aos/dist/aos.css';
import axios from 'axios';


AOS.init();

export default {
    name: 'DownloadPage',
    data() {
        return {
            models: [
                { id: 1, name: 'models1', url: 'models/m1.txt' },
                { id: 2, name: 'models2', url: 'models/m1.txt' },
                { id: 3, name: 'models3', url: 'models/m1.txt' },
                { id: 4, name: 'models4', url: 'models/m1.txt' },
                { id: 5, name: 'models5', url: 'models/m1.txt' },
            ]
        };
    },
    methods: {
        download_platform() {
            axios.get('file/曲焕新声', {   //静态资源文件夹public            
                responseType: 'blob',
            }).then(response => {
                const url = window.URL.createObjectURL(new Blob([response.data]));
                const link = document.createElement('a');
                let fname = '曲焕新声';
                link.href = url;
                link.setAttribute('download', fname);
                document.body.appendChild(link);
                link.click();
            }).catch(error => {
                console.log('error:' + JSON.stringify(error))
            });
        },
        download_model(url, name) {
            axios.get(url, {   //静态资源文件夹public            
                responseType: 'blob',
            }).then(response => {
                const url = window.URL.createObjectURL(new Blob([response.data]));
                const link = document.createElement('a');
                let fname = name;
                link.href = url;
                link.setAttribute('download', fname);
                document.body.appendChild(link);
                link.click();
            }).catch(error => {
                console.log('error:' + JSON.stringify(error))
            });
        }
    }
}

</script>

<style scoped>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

.page {
    width: 100%;
    min-height: 100vh;
    height: 100%;
    background-color: #fffffd;
    overflow: hidden;
    display: flex;
    flex-direction: column;
    align-items: center;


    #title {
        padding: 12px;
        padding-top: 15%;
        min-width: 100px;
        font-size: 4rem;
        background-color: rgb(255, 215, 106);
        border-radius: 0px 0px 20px 20px;
        color: white;
    }
    .description {
            margin: 10px;
        }
    .version {
        background-color: rgb(252, 188, 50);
        width: 10%;
        min-width: 100px;
        border-radius: 10px;
        color: white;
    }

    .download_block {
        width: 100%;
        .download_platform {
            padding: 20px 0;
            img {
                height: 100px;
            }
        }

        .download_button {
            width: 16%;
            min-width: 120px;
            height: 60px;
            padding: 10px;
            background-color: rgb(252, 188, 50);
            border: none;
            border-radius: 10px;
            transition: all 0.3s;
            cursor: pointer;
            .download_p1 {
                font-size: 1.5rem;
            }
        }
        .download_button:hover {
            background-color: rgb(0, 0, 0);
            color: white;
        }
    }
    .download_models
    {
        width: 100%;
        display: flex;
        justify-content: center;
        align-items: center;
        flex-wrap: wrap;
        background-color: #58bfff;
        margin-top: 20px;
        h1{
            width: 100%;
            text-align: center;
            padding: 20px;
            color: white;
        }
        .download_button {
            width: 15%;
            min-width: 120px;
            height: 60px;
            margin: 20px 3%;
            font-size: 1.2rem;
            border-radius: 15px;
            border : none;
            background-color: rgb(0, 64, 154);
            color: white;
            transition: all 0.3s;
        }
        .download_button:hover {
            background-color: rgb(5, 29, 128);
            color: white;
            box-shadow: 0 0 8px 5px rgba(91, 91, 91, 0.2);
        }
    }
}
</style>