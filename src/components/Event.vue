<template lang="html">

  <section class="event">
    <div class= 'card'>
      <div class= 'card-content'>
        <router-link :to='/eventdetails/+ event.id'>
            <h2 class='linkStyle'>{{event.naziv}}  <img src='../../public/propolis.jpg' weight=50px height=50px/></h2> 
        </router-link>
        <spam>Cena: {{event.datum}} din</spam><br/>
        <spam>{{event.lokacija}}</spam> 
      </div>
    </div>
  </section>

</template>

<script lang="js">

  export default  {
    name: 'event',
    props: [
      'event'
    ],
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

<style  >
  .card{
    height: 130px;
  }
  .card-content{
    color: white;
    background: sandybrown;
    height: 1500px;
  }
  .linkStyle{
    color: white;
    background: sandybrown;
  }
</style>
