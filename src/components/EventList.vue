<template lang="html">

  <section class="event-list">
    <div class='row'>
      <div class='col-sm-5' v-bind:key=event v-for='event in events' >
          <event :event= 'event'/>
      </div>
    </div>
  </section>

</template>

<script lang="js">

  import event from './Event'
  import myevents from '../data/events'

  export default  {
    name: 'event-list',
    components:{
      event
    },
    props: [],
    mounted () {

    },
    data () {
      return {
        events: myevents
      }
    },
    methods: {

    },
    computed: {

    }
}


</script>

<style >
  .row{
    justify-content: left ! important;
    margin-left: 200px !important;
  }
</style>
