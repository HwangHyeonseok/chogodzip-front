<template>
    <div>
        <SearchHouse />
        <div class="container">
            <LikeRegionState />
        </div>
        <LikeRegionLatest />
        <div class="container">
            <LottosInfo />
        </div>
        <TodayLecture />
    </div>
</template>

<script setup>
import LikeRegionLatest from '@/modules/components/home/home03/LikeRegionLatest.vue';
import LikeRegionState from '@/modules/components/home/home02/LikeRegionState.vue';
import LottosInfo from '@/modules/components/home/home04/LottosInfo.vue';
import SearchHouse from '@/modules/components/home/home01/SearchHouse.vue';
import TodayLecture from '@/modules/components/home/home05/TodayLecture.vue';
</script>

<style scoped> 
</style>