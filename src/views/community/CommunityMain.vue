<template>
    <div class="in-background">
        <br><br>
        <Swiper></Swiper>
        <br><br>
        <CommunitySearch></CommunitySearch>
    </div>
</template>

<script setup>
//import Swiper from './Swiper.vue';
import Swiper from '@/views/community/Swiper.vue';
import CommunitySearch from '@/views/community/CommunitySearch.vue';
</script>

<style scoped>

.in-background {
    background-color: #E6E6FA;
}

.con-paging {
    width:100%; height:100px; display:flex; justify-content: center; align-items: end;
}
</style> 