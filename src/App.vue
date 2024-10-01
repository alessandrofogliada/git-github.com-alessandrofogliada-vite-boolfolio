<script>
import Home from '../src/pages/Home.vue'

import Progetti from '../src/pages/Progetti.vue'

</script>

<template>
  <div>
    <nav>
      <ul>
        <li>
          <router-link :to="{name:'home'}"> Homepage</router-link>
        </li>

        <li>
          <router-link :to="{name:'progetti'}"> Progetti</router-link>
        </li>
      </ul>
    </nav>
  </div>


  <router-view></router-view>

</template>

<style>

</style>

