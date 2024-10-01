<script>
import { store } from '@/store/store';
import axios from 'axios';

export default {
    data(){
        return{
            progetti = []
        }
    }
};

methods: {
    getApi(){
        axios.get(store.apiUrl+'progetti')
        .then(Response=>{ this.progetto = Response.data.posts})
    }
}

mounted() {
    this.apiUrl()
}



</script>

<template>

<h1>Questa è la pagina dei Progetti</h1>

</template>

<style>

</style>