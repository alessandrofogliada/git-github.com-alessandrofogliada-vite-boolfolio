<script>
import { store } from '../store/store';
import axios from 'axios';

export default {
        data(){
            return{
                progetti : [],
            }
        },

        methods: {
            getApi(){
                axios.get(store.apiUrl + 'progetti').then(response=>{
                    this.progetti = response.data.result
                    console.log(this.progetti);
                    
                })
            }
        },

        mounted() {
            this.getApi()
        }
}




</script>

<template>

<div class="container">
    <div class="menu">
        <h1>Questa è la pagina dei Progetti</h1>    
        <ul>
            <li v-for="progetto in progetti" :key="progetto.id"> {{ progetto.title }}</li>
        </ul>
    </div>
</div>

</template>

<style>

</style>