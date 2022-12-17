<script setup>
import { RouterLink, RouterView } from "vue-router";
import MainPage from "./components/MainPage.vue";
import { ref } from '@vue/reactivity'
const items = ref([
            {id:1, image:'',desctiption:'Что то написано', amount:4, isShow: false},
            {id:2, image:'',desctiption:'Что то написано', amount:2, isShow: false},
            {id:3, image:'',desctiption:'Что то написано', amount:5, isShow: false},
            {id:4, image:'',desctiption:'', amount:null, isShow: false},
            {id:5, image:'',desctiption:'', amount:null, isShow: false},
            {id:6, image:'',desctiption:'', amount:null, isShow: false},
            {id:7, image:'',desctiption:'', amount:null, isShow: false},
            {id:8, image:'',desctiption:'', amount:null, isShow: false},
            {id:9, image:'',desctiption:'', amount:null, isShow: false},
            {id:10, image:'',desctiption:'', amount:null, isShow: false},
            {id:11, image:'',desctiption:'', amount:null, isShow: false},
            {id:12, image:'',desctiption:'', amount:null, isShow: false},
            {id:13, image:'',desctiption:'', amount:null, isShow: false},
            {id:14, image:'',desctiption:'', amount:null, isShow: false},
            {id:15, image:'',desctiption:'', amount:null, isShow: false},
            {id:16, image:'',desctiption:'', amount:null, isShow: false},
            {id:17, image:'',desctiption:'', amount:null, isShow: false},
            {id:18, image:'',desctiption:'', amount:null, isShow: false},
            {id:19, image:'',desctiption:'', amount:null, isShow: false},
            {id:20, image:'',desctiption:'', amount:null, isShow: false},
            {id:21, image:'',desctiption:'', amount:null, isShow: false},
            {id:22, image:'',desctiption:'', amount:null, isShow: false},
            {id:23, image:'',desctiption:'', amount:null, isShow: false},
            {id:24, image:'',desctiption:'', amount:null, isShow: false},
            {id:25, image:'',desctiption:'', amount:null, isShow: false},
        ])
</script>

<template>
  <div class="bg-page">
    <MainPage :items ='items'/>
  </div>

  <RouterView />
</template>

