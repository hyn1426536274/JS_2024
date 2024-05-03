<template>
    <StartPage/>
    <ModelInfoPage/>
    <UiInfoPage/>
    <FuncInfoPage/>
    <PreviewPage/>
    <DownloadPage/>
</template>

<script>
import StartPage from './StartPage.vue';
import ModelInfoPage from './ModelInfoPage.vue';
import UiInfoPage from './UiInfoPage.vue';
import FuncInfoPage from './FuncInfoPage.vue';
import PreviewPage from './PreviewPage.vue';
import DownloadPage from './DownloadPage.vue';

export default {
  name: 'HomePage',
  components: {
    StartPage,
    ModelInfoPage,
    UiInfoPage,
    FuncInfoPage,
    PreviewPage,
    DownloadPage
  }
}
</script>

<style scoped>

</style>