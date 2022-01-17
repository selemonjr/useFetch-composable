<template>
    <div class="app">
       <p v-if="loading">Loading....</p>
      <div v-else>
            <div  class="flex" v-if="response && response.length > 0">
            <div v-for="item in response" :key="item.id">
            <p>{{item.title.substring(0,5)}}</p>
            <img :src="item.url" alt="">
        </div>
      </div>
        </div>
    </div>
</template>
<script setup>
 import { useFetch } from '@vueuse/core';
 const url = "https://jsonplaceholder.typicode.com/photos";
 const {isFetching: loading, data:response} = useFetch(url).json();
</script>
<style scoped>
.flex {
    display:flex;
    width:100%;
    flex-wrap:wrap;
}
p {
    text-align:center;
}
img {
    width:6rem;
    height:6rem;
    margin:1rem;
}
</style>