<script setup>
import { RouterLink, RouterView } from "vue-router";
import MainPage from "./components/MainPage.vue";
import { ref } from '@vue/reactivity'
const items = ref([
            {id:1, image:'',dsctiption:'Что то написано', amount:4},
            {id:2, image:'',dsctiption:'Что то написано', amount:2},
            {id:3, image:'',dsctiption:'Что то написано', amount:5},
            {id:4, image:'',dsctiption:'', amount:null},
            {id:5, image:'',dsctiption:'', amount:null},
            {id:6, image:'',dsctiption:'', amount:null},
            {id:7, image:'',dsctiption:'', amount:null},
            {id:8, image:'',dsctiption:'', amount:null},
            {id:9, image:'',dsctiption:'', amount:null},
            {id:10, image:'',dsctiption:'', amount:null},
            {id:11, image:'',dsctiption:'', amount:null},
            {id:12, image:'',dsctiption:'', amount:null},
            {id:13, image:'',dsctiption:'', amount:null},
            {id:14, image:'',dsctiption:'', amount:null},
            {id:15, image:'',dsctiption:'', amount:null},
            {id:16, image:'',dsctiption:'', amount:null},
            {id:17, image:'',dsctiption:'', amount:null},
            {id:18, image:'',dsctiption:'', amount:null},
            {id:19, image:'',dsctiption:'', amount:null},
            {id:20, image:'',dsctiption:'', amount:null},
            {id:21, image:'',dsctiption:'', amount:null},
            {id:22, image:'',dsctiption:'', amount:null},
            {id:23, image:'',dsctiption:'', amount:null},
            {id:24, image:'',dsctiption:'', amount:null},
            {id:25, image:'',dsctiption:'', amount:null},
        ])
</script>

<template>
  <div class="bg-page">
    <MainPage :items ='items'/>
  </div>

  <RouterView />
</template>

