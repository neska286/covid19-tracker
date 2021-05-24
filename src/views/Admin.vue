<template>
    <div class="admin">
 <div class="page-wrapper default-theme sidebar-bg bg1 toggled">
        <nav id="sidebar" class="sidebar-wrapper">
            <div class="sidebar-content">
                <!-- sidebar-brand  -->
                <div class="sidebar-item sidebar-brand">
                    <img src="../assets/whiteLogo.svg" alt="..."  class="shadow-sm">
                </div>
                <!-- sidebar-header  -->     
                <!-- sidebar-menu  -->
                <div class=" sidebar-item sidebar-menu">
                    <ul>
                             <li class="sidebar-dropdown">
                            <a href="#">
                                <i class="fa fa-shopping-cart"></i>
                                 <router-link to="/">Home</router-link>
                               
                            </a>
                        </li>  
        
                        <li class="sidebar-dropdown">
                            <a href="#">
                                <i class="fa fa-tachometer-alt"></i>
                               <router-link to="/admin/dashboard">Dashboard</router-link>
                            </a>
 
                        </li>
                                        
                    </ul>
                </div>
                <!-- sidebar-menu  -->
            </div>
            <!-- sidebar-footer  -->
       
        </nav>
        <!-- page-content  -->
        <main class="page-content pt-2">
           <Header/>
     <router-view/>
        </main>
        <!-- page-content" -->
    </div>
    <!-- page-wrapper -->

    </div>
</template>

<script>
import Header from '@/components/Header.vue'
    export default {
        name: 'Admin',
         components: {
           Header
         }
        
    }
</script>

<style lang="scss" scoped>


.sidebar-wrapper {
  width: 280px;
  height: 100%;
  max-height: 100%;
  position: fixed;
  top: 0;
  left: -280px;
  z-index: 999;
  -webkit-transition: left .3s ease, width .3s ease;
  transition: left .3s ease, width .3s ease; 
  }
  .sidebar-wrapper ul {
    list-style-type: none;
    padding: 0;
    margin: 0; 
    }
  .sidebar-wrapper a {
    text-decoration: none;
    -webkit-transition: color .3s ease;
    transition: color .3s ease; 
    }
  .sidebar-wrapper .sidebar-item {
    -webkit-transition: all .3s linear;
    transition: all .3s linear; 
    }
  .sidebar-wrapper .sidebar-content {
    max-height: calc(100% -35px);
    height: calc(100% - 35px);
    overflow-y: scroll;
    position: relative; 
    }
    .sidebar-wrapper .sidebar-content.desktop {
      overflow-y: hidden; 
      }
 

.sidebar-bg .sidebar-wrapper {
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat; }
  .sidebar-bg .sidebar-wrapper:before {
    content: '';
    position: absolute;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0; 
    }

.sidebar-wrapper .sidebar-brand {
  padding: 1rem 1.2rem;
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  -webkit-box-align: center;
  -ms-flex-align: center;
  align-items: center;
  height: 55px; 
  }
  .sidebar-wrapper .sidebar-brand > a {
    text-transform: uppercase;
    font-weight: bold;
    -webkit-box-flex: 1;
    -ms-flex-positive: 1;
    flex-grow: 1;
    overflow: hidden;
    white-space: nowrap;
    text-overflow: ellipsis; 
    }

.sidebar-wrapper .sidebar-menu {
  padding-bottom: 10px; 
  }
  .sidebar-wrapper .sidebar-menu .header-menu span {
    font-weight: bold;
    font-size: 14px;
    padding: 15px 20px 5px 20px;
    display: inline-block; 
    }
  .sidebar-wrapper .sidebar-menu ul li a {
    display: -webkit-box;
    display: -ms-flexbox;
    display: flex;
    -ms-flex-wrap: nowrap;
    flex-wrap: nowrap;
    -webkit-box-align: center;
    -ms-flex-align: center;
    align-items: center;
    text-decoration: none;
    position: relative;
    padding: 8px 30px 8px 20px;
    width: 100%; 
    }

body {
  font-size: .9rem; 
  }

/*----------------page-wrapper----------------*/
.page-wrapper {
  height: 100vh; 
  }
  .page-wrapper .theme {
    width: 40px;
    height: 40px;
    display: inline-block;
    margin: 2px;
    background-size: cover; 
    }
  .page-wrapper .theme.light-theme {
    background: #ececec;
     }
  .page-wrapper .page-content {
    display: inline-block;
    width: 100%;
    -webkit-transition: padding-left .3s ease;
    transition: padding-left .3s ease;
    overflow-x: hidden; 
    }
    .page-wrapper .page-content .overlay {
      position: fixed;
      top: 0;
      right: 0;
      bottom: 0;
      left: 0;
      z-index: 998;
      background: #000;
      opacity: .5;
      display: none; 
      }
  .page-wrapper.toggled .sidebar-wrapper {
    left: 0px; 
    }
  @media screen and (min-width: 768px) {
    .page-wrapper.toggled .page-content {
      padding-left: 280px; 
      } 
      }
 
 


    /*---- sidebar ----*/@at-root.default-theme .sidebar-wrapper {
  background-color: #1d1d1d; 
  }
  .default-theme .sidebar-wrapper .sidebar-item {
    border-top: 1px solid #2b2b2b; 
    }
    .default-theme .sidebar-wrapper .sidebar-item:first-child {
      border-top: none; 
      }
 
  .default-theme .sidebar-wrapper .sidebar-menu a:hover i,
  .default-theme .sidebar-wrapper .sidebar-menu a:hover:before,
  .default-theme .sidebar-wrapper .sidebar-menu li.active a i {
    color: #BDD357; }
 

.default-theme .mCSB_scrollTools .mCSB_draggerRail {
  background-color: transparent; 
  }

.default-theme.sidebar-bg .sidebar-wrapper:before {
  background-color:#082C49;
  }

.default-theme.sidebar-bg .sidebar-wrapper a:not(.dropdown-item),
.default-theme.sidebar-bg .sidebar-wrapper .sidebar-header,
.default-theme.sidebar-bg .sidebar-wrapper .sidebar-search input,
.default-theme.sidebar-bg .sidebar-wrapper .sidebar-search i {
  color: #c7c7c7; 
  }

</style>