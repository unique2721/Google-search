<script setup>
import {inject, ref} from 'vue'
import googlelogo from '../assets/images/googlelogo.png'
import setting from '../assets/images/setting.png'
import apps from '../assets/images/apps.png'
import record from '../assets/images/record.png'
import search from '../assets/images/search.png'
import searchByImage from '../assets/images/searchByImage.png'
let searchedWord = ref("");
const isSearch = inject('isSearch');


const searchHandler = () => {
    if(searchedWord.value.trim == "") {
        alert("please type some words to search");
        return
    }
    else if(searchedWord.value.trim() == "vue" || searchedWord.value.trim() =="vue js"|| searchedWord.value.trim() =="vue.js") {
        isSearch.value = true;
    }
    else {
        alert("only vue, vue.js, or vue js keywords are allowed to search");
        return
    }
}

const clearHandler = () => {
    searchedWord.value = ""
}
</script>

<template>
    <div class="navbar-container flex flex-wrap justify-between">
        <div class="logo">
            <img :src="googlelogo" alt="google logo" class="w-[92px] mt-[35px] mb-[35px] ml-[25px] mr-[25px]">
        </div>
        <div class="searchbar mt-[30px] mb-[30px]">
            <input type="text" placeholder="vue js" v-model="searchedWord" class="w-[705px] h-[45px] p-4 border-none rounded-[22px] outline-none"/>
        </div>

        <div class="input-icons flex absolute">
            <span class="x" @click="clearHandler">x</span>
            <img :src="record" alt="record" title="search by voice">
            <img :src="searchByImage" alt="searchByImage" title="search by image">
            <img :src="search" alt="search" title="search" id="search" @click="searchHandler">
        </div>
        <div class="rightside flex">
            <div class="right-icons flex">
                <img :src="setting" alt="setting" title="quick settings">
                <img :src="apps" alt="apps" class="apps w-[30px] h-[30px] mt-[37px]" title="google apps">
            </div>
            <button class="w-[80px] h-[35px] m-[20px] bg-blue-500 mr-[20px] p-2 text-white rounded-md mt-[35px]">Sign in</button>
        </div>
    </div>
</template>

<style scoped>
.navbar-container .searchbar {
    transform: translateX(-120px);
}
.navbar-container .searchbar input {
    box-shadow: 10px 10px 6px rgba(245, 245, 245, 0.925);
    outline: 3.25px solid  rgba(245, 245, 245, 0.685);
}
.navbar-container .searchbar input::placeholder {
    font-size: 1.2rem;
    font-weight: 400;
    color: rgba(0, 0, 0, 0.685);
}

.navbar-container .input-icons img,.navbar-container .input-icons span {
    width: 25px;
    height: 25px;
    margin-right: 15px;
    transform: translateX(680px);
    margin-top: 40px;
    cursor: pointer;
}
.navbar-container .input-icons span {
    font-size: 1.7rem;
    margin-top: 30px;
    color: rgba(0, 0, 0, 0.397);
}
.navbar-container .rightside .right-icons img {
    width: 25px;
    height: 25px;
    margin-top: 40px;
    margin-left: 20px;
}
@media screen and (max-width: 1200px) {
    .navbar-container .searchbar {
        transform: translateX(-60px);
    }
    .navbar-container .searchbar input {
        width: 600px;
    }
    .navbar-container .input-icons img,.navbar-container .input-icons span {
        transform: translateX(600px);
    }
}
</style>