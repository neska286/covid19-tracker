<template>
    <div class="dashboard">
      
        <BreadCrumb/>
        <Search/>
       <Footer/>
      

    </div>
</template>

<script>

import Footer from '@/components/Footer.vue'
import BreadCrumb from '@/components/BreadCrumb.vue'
import Search from '@/components/Search.vue'
    export default {
        name:'Dashboard',
         components: {
  
    BreadCrumb,
    Search,
    Footer
  }
    }
</script>

<style lang="scss" scoped>

</style>