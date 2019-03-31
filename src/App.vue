<template>
  <div id="app">
    <Head/>
    <router-view/>
    <Foot/>
  </div>
</template>
<script>
  import Foot from './common/tabbar/index'
  import Head from './common/head/index'
  export default {
      components:{
          Foot,
          Head
      }
  }
</script>
