<template>
  <div class="home">
  <nav class="navbar navbar-expand-lg navbar-light bg-light">
    <div class="container">
 
  <img src="../assets/logo.png" class="" alt="...">
  <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
    <span class="navbar-toggler-icon"></span>
  </button>

  <div class="collapse navbar-collapse" id="navbarSupportedContent">
    <ul class="navbar-nav ml-auto">
      <li class="nav-item active">
        <router-link class="nav-link" to="/admin">Admin <span class="sr-only">(current)</span></router-link>
      </li>
      <li class="nav-item">
        <a class="nav-link" href="#">LogOut</a>
      </li>  
    </ul>
   
  </div>
  </div>
</nav>
<div class="container">
  <img src="../assets/Drawkit-Vector-Illustration-Medical-19.svg" class="img-fluid" alt="...">
</div>

  </div>
</template>

<script>
// @ is an alias to /src



export default {
  name: 'Home',
}
</script>
