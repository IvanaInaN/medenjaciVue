<template lang="html">

  <section class="navigation">
    <nav class='navbar container'>
      <div class='navbar-brand'>
        <b>Medenjaci</b>
      </div>
      <div class='navbar-menu'>
        <router-link to="/">Home</router-link> |
        <router-link to="/about">About</router-link>
      </div>
    </nav>
    <div id="nav">
     
    </div>
  </section>

</template>

<script lang="js">

  export default  {
    name: 'navigation',
    props: [],
    mounted () {

    },
    data () {
      return {

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
      background-color: coral;
      height: 50px;
  }
  a{
    font-weight: bold;
  }
</style>
