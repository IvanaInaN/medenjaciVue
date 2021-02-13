<template lang="html">

  <section class="eventdetails">
    <h1>{{myevent.naziv}}</h1>
    <div>{{myevent.lokacija}}</div>
  </section>

</template>

<script lang="js">
import events from '../data/events'

  export default  {
    name: 'eventdetails',
    props: [],
    mounted () {
      var id= Number(this.$route.params.id);
      var event = this.myevents.find(event => event.id== id )
      this.myevent = event;
      alert(event);
    },
    data () {
      return {
          myevents : events,
          myevent  : {}
      }
    },
    methods: {

    },
    computed: {

    }
}


</script>

<style>
  .eventdetails {

  }
</style>
