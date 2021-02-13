<template>
  <div class="home">
    <br/>
    <h1>Dobrodšli u carstvo meda</h1>
    <button class='btn bg-primary'>Prijavite se </button>
    <br/>
    <br/>
    <eventList></eventList>
  </div>
</template>

<script>
// @ is an alias to /src
import eventList from '../components/EventList'

export default {
  name: 'Home',
  components: {
    eventList
  }
}
</script>
