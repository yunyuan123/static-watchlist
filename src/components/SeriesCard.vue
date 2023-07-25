<script setup>

const props = defineProps({
    serie:Object,
})



</script>

<template>
<div class="course">
              <div class="course-preview" :style="{'background-color': serie.color}">
                  <h6>Season {{ serie.season }}</h6>
                  <h2>{{serie.series}}</h2>
              </div>
              <div class="course-info">
                  <h6>ep: S{{serie.season < 10 ? '0'+ serie.season:serie.season }}E{{ serie.episode < 10 ?'0'+serie.episode:serie.episode }}</h6>
                  <h2>{{ serie.title }} </h2>
                  <button class="btn" :style="{'background-color': serie.color}">Continue</button>
              </div>
          </div>
</template>
