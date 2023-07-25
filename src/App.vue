<script setup>
import {ref} from 'vue'
import {userWatchList} from './js/watchList';
import SeriesCard from './components/SeriesCard.vue';

const localWatchList = ref(userWatchList)
const episodeEnCours = ref("")

const onContiueLecture = (data)=>{
  episodeEnCours.value = data
    console.log('👶',data)
}



</script>

<template>
  <div class='row'>
      <div class='col left'>
            <ul>
                <li>Ici c'est fixe</li>
                <li>Un lien de nav 1</li>
                <li>Un lien de nav 2</li>
            </ul>
            <span>▶ Lecture en cours: {{ episodeEnCours }} </span>
      </div>
      <div class='col right'>

        <div class="courses-container">

        <SeriesCard v-for = "serie in localWatchList" :key="serie.series"
        
        :serie="serie"
        @onContinue="onContiueLecture" />
          
        </div>

      </div>
  </div>
</template>

<style scoped>

</style>
