<template>
   <div class="navigation text-right">
      <b-navbar-toggle target="nav_collapse"></b-navbar-toggle>
      <b-navbar toggleable="md" class=" pl-0">
         <b-collapse is-nav id="nav_collapse">
            <b-navbar-nav>
               <router-link v-for="(navLink, index) in navLinks" :key="index" :to="navLink.link">{{ navLink.name }}</router-link>
            </b-navbar-nav>
         </b-collapse>
      </b-navbar>
   </div>
</template>

<script>
export default {
   name: 'MainNavigation',
   data() {
      return {
         navLinks: [
            {name: 'Home', link: '/'},
            {name: 'About', link: '/about'},
            {name: 'Work', link: '/work'},
            {name: 'Contact', link: '/contact'}
         ]
      }
   }
}
</script>

<style>
.navigation  a {
   font-size: 1.125rem;
   letter-spacing: 0.02;
   text-decoration: none;
   color: #737373;
   margin-right: 30px;
   display: inline;
   padding: 0px;
}
.navigation  a:hover {
color: #3fa369;
}
.navigation {
   border-top: #dadada 1px solid;
   margin-top: 30px;
   padding-top: 14px;
}
.navigation .router-link-exact-active {
   color: #2ecc71;
}
.navigation button {
   display: none;
}
@media (max-width: 576px) {
   .navigation .b-nav-item {
      display: list-item;
      list-style: none;
   }
   .navigation {
      float: right;
      border-top: none;
      margin-top: 0px;
      padding-top: 0px;
   }
   .navigation button {
   display: inline;
}
}
</style>
