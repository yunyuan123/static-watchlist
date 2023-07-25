<script setup>
import {ref} from 'vue'
import {userWatchList} from './js/watchList';
import SeriesCard from './components/SeriesCard.vue';
import TheNav from './components/TheNav.vue'

const localWatchList = ref(userWatchList)

</script>

<template>
  <div class='row'>
      <TheNav />
      <div class='col right'>

        <div class="courses-container">

        <SeriesCard v-for = "serie in localWatchList" :key="serie.series"
        
        :serie="serie" />
          
        </div>

      </div>
  </div>
</template>

<style scoped>

</style>
