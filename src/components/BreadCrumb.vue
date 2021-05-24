<template>
    <div class="breadcrumb">
<nav aria-label="breadcrumb ">
  <ol class="breadcrumb">
    <li class="breadcrumb-item">Dashboard</li>
    <li class="breadcrumb-item active" aria-current="page"></li>
  </ol>
</nav>
    </div>
</template>

<script>
    export default {
        name: 'BreadCrumb'
        
    }
</script>

<style lang="scss" scoped>
.breadcrumb {
    display: -ms-flexbox;
    display: flex;
    -ms-flex-wrap: wrap;
    flex-wrap: wrap;
    padding: .75rem 1rem;
    margin-bottom: 1rem;
    list-style: none;
    background-color:#fffefe;
    border-radius: .25rem;
}
</style>