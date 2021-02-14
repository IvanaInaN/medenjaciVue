<template lang="html">

  <section class="navigation">
    <nav class='navbar container'>
      <div class='navbar-brand'>
        <b>Medenjaci</b>
      </div>
      <div class='navbar-menu'>
        <router-link to="/login">Prijava</router-link> |
        <router-link to="/">O nama</router-link> |
        <router-link to="/user">O korisniku</router-link> |
        <router-link to="/basket" v-if = !user.isAdmin>Korpa</router-link> 
        <router-link to="/orders"  v-if = user.isAdmin>Orders</router-link> |
        <router-link to="/home"  v-if = !user.isAdmin >Products</router-link> 
        <router-link to="/seller" v-if = user.isAdmin>Products</router-link> 
      </div>
    </nav>
    <div id="nav">
     
    </div>
  </section>

</template>

<script lang="js">

import currentUser from '../data/currentUser'

  export default  {
    name: 'navigation',
    props: [],
    mounted () {

    },
    data () {
      return {
        user: currentUser
      }
    },
    methods: {

    },
    computed: {

    }
}


</script>

<style scoped >
  .navigation {
      background-color: #ff7f50;
      height: 50px;
  }
  a{
    font-weight: bold;
  }
</style>
