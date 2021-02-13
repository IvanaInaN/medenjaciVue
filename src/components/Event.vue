<template lang="html">

  <section class="event">
    <div class= 'card'>
      <div class= 'card-content'>
        <img src='../../public/propolis.jpg' weight=50px height=50px/>
        <router-link :to='/eventdetails/+ event.id'>
            <h2>{{event.naziv}}</h2>
        </router-link>
        <spam>{{event.datum}}</spam><br/>
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

<style scoped >
  .event {

  }
  .card{
    height: 200px;
  }
  .card-content{
    color: white;
    background: sandybrown;
    height: 200px;
  }
</style>
