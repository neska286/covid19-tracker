<template>
    <div class="footer bg-light shadow-sm">
  <div class="card-header">
   <div class="row">
     <div class="col-md-6">
       <ul>
         <li>
   Version 1.1.0
         </li>
         <li>
 <span> support@mitygate.com</span>
         </li>
         <li>
   Techincal Documentation
         </li>
       </ul>
    
      
    
     </div>
     <div class="col-md-6">
      <ul>
        <li> &#169; Copyright 2019-2021</li>
        <li> <span>MITYGATE GmbH</span></li>
        <li>All rights reserved</li>
      </ul>
     </div>
   </div>
  </div>
    </div>
   
</template>

<script>
    export default {
        name:'Footer'
        
    }
</script>

<style lang="scss" scoped>
.footer {
   position: fixed;
   left: 0;
   bottom: 0;
   width: 100%;
   color: #9E9D9D;
   text-align: center;
}
ul{
   list-style-type: none;
}
span{
  color:#3B7F91;
}

</style>