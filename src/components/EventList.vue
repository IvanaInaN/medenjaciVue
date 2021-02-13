<template lang="html">

  <section class="event-list">
    <div class='row'>
      <div class='col-sm-5' v-for='event in events'>
          <event :event= 'event'/>
      </div>
    </div>
  </section>

</template>

<script lang="js">

  import event from './Event'

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
        events:[
          {
            id: 1,
            naziv: "med",
            datum: "2022-02-01",
            lokacija: "Beograd"
          },
          {
            id: 2,
            naziv: "med2",
            datum: "2022-02-01",
            lokacija: "Beograd"
          },
          {
            id: 3,
            naziv: "med2",
            datum: "2022-02-01",
            lokacija: "Beograd"
          }, 
          {
            id: 4,
            naziv: "med2",
            datum: "2022-02-01",
            lokacija: "Beograd"
          }
        ]
      }
    },
    methods: {

    },
    computed: {

    }
}


</script>

<style scoped >
  .event-list {

  }
  .row{
    justify-content: center ! important;
    margin: 0px !important;
  }
</style>
