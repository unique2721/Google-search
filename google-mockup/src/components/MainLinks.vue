<script setup>
import {defineProps} from 'vue'

const props = defineProps(['link','text','href'])

</script>

<template>
    <div class="mb-[20px]">
        <h1><a :href="href" target="_blank">{{link}}</a></h1>
        <p>{{text}}</p>
    </div>
</template>

<style scoped>
div {
    transform: translateX(180px);
}
div h1 a {
    color: #6114E0;
    font-size: 1.2rem;
}
div h1 a:hover {
    text-decoration: underline;
}

@media screen and (max-width: 1200px) {
    div {
        transform: translateX(40px)
    }
    
}
</style>