<script setup>
import vue from '../assets/images/vue.png'
import dots from '../assets/images/dots.jpg'
</script>
<template>
    <div class="flex justify-between mb-[45px]">
        <ul class="flex ml-[180px]">
            <li><a href="https://www.google.com/search?sca_esv=33fda89bc4ea5a26&sca_upv=1&rlz=1C1CHBF_enET1103ET1103&biw=1366&bih=641&q=vue+js&source=lnms&uds=ADvngMjLOPeXMMrRVcrWOWypsVoiLZkBAoKvHdsnC1C4gs2yCN4qhyOg0kDa6MABh_XPb-5RnD_GIDLdnFr4x1YjJydH3vJpuCBjvVmqUwhKwTuHSxpggfldohCVXk_rUjegD43d9wHqscEfDmO-JCL8uvpsQht8Uj67lEykHb4Ev7e9i-NW3opz9qnT2rSbSXOPoNgYJAEHkv0P3Kj7HGYLizBvKJIhyqr45vdh6K6-78x6LbtaB-szgMNiTvRZHVoxxaCcVT-wMPKQJHby0GkZaObXpCyrTg&sa=X&ved=2ahUKEwjuwNXxxoKGAxWPiP0HHbbaBAUQ0pQJegQIERAB&cshid=1715326039465806">All</a></li>
            <li><a href="https://www.google.com/search?sca_esv=33fda89bc4ea5a26&sca_upv=1&rlz=1C1CHBF_enET1103ET1103&q=vue+js&uds=ADvngMjTNPKEE-q7I44lun7GC2_xLW1fqApxSV5ERMfRC9on6Xdtme_o1M6R-g6sMpZBtcOjsAUMtnZv1cidk8I4JbJDXbopkNdSeXAqx4BhtDhl_d5rTAMfEs6ICLbpgE8zhQzpXlXTyBTN_z00hpaGnltFtTd1WizgkFB3vIZd2Rttu1FIAvPGYjGAnAdwr5DrlWfPvQqCvjzZFohZpThH76InJEZ5LIBEAuP5KUnY8qkNNHgI2kq66vZ5Ot-TY095rvfN-_MtTgWEcx0YJkWEUPNzJvgaOw&udm=2&prmd=ivsnmbz&sa=X&ved=2ahUKEwjR3OLxooGGAxXQ_7sIHePJAB0QtKgLegQIFBAB">Images</a></li>
            <li><a href="https://www.google.com/search?sca_esv=33fda89bc4ea5a26&sca_upv=1&rlz=1C1CHBF_enET1103ET1103&q=vue+js&tbm=vid&source=lnms&prmd=ivsnmbz&sa=X&ved=2ahUKEwjR3OLxooGGAxXQ_7sIHePJAB0Q0pQJegQIExAB">Videos</a></li>
            <li><a href="https://www.google.com/search?sca_esv=33fda89bc4ea5a26&sca_upv=1&rlz=1C1CHBF_enET1103ET1103&q=vue+js&tbm=shop&source=lnms&prmd=ivsnmbz&ved=1t:200715&ictx=111">Shopping</a></li>
            <li><a href="https://www.google.com/search?sca_esv=33fda89bc4ea5a26&sca_upv=1&rlz=1C1CHBF_enET1103ET1103&q=vue+js&tbm=nws&source=lnms&prmd=ivsnmbz&sa=X&ved=2ahUKEwjR3OLxooGGAxXQ_7sIHePJAB0Q0pQJegQIFRAB">News</a></li>
            <li><a href="">More</a></li>
        </ul>
        <div>
            <a href="" class="mr-[20px] text-black-700 ml-[-100px]">Tools</a>
        </div>
        <div class="safesearch">
            <a href="" class="mr-[43px]">SafeSearch</a>
        </div>
    </div>
    <div class="dots-container flex">
        <img :src="vue" alt="vue logo" class="vue w-[35px] h-[35px] mr-[10px] p-2 rounded-full mb-7">
        <div>
            <p>Vue.js</p>
            <a href="https://vuejs.org">https://vuejs.org</a>
        </div>
        <img :src="dots" alt="dots" class="dots w-[20px] h-[20px]">
    </div>  
</template>
<style scoped>
div ul li a {
    margin-right: 20px;
    color: rgba(0, 0, 0, 0.685);
}
.dots-container {
    transform: translateX(180px);
}
.dots-container .vue {
    transform: translateY(10px);
    outline: 1px solid rgba(0, 0, 0, 0.212);
}
.dots-container .dots {
    transform: translateY(27px);
}
@media screen and (max-width: 1200px) {
    div ul {
        margin-left: 30px;
    }
    .dots-container {
        transform: translateX(30px);
    }
    .tools a {
        margin-left: 30px;
    }  
.safesearch a {
    margin-right: 3px;
}
}
</style>