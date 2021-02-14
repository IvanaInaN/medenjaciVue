<template>
  <div class="home">
    <br/>
    <h1>Dobrodšli u carstvo meda</h1>
    <br/>
    <br/>
    <eventList></eventList>
  </div>

</template>

<script>
// @ is an alias to /src
import eventList from '../components/EventList'
import users from '../data/users'

export default {
  name: 'Home',
  components: {
    eventList
  },
  methods:{
    clickShow(){
      this.$modal.show('loginModal')
    },
    closeModal(){
      this.$modal.hide('loginModal')
    },
    login(){
      var user = this.myuser.find(user => user.username == this.username && user.password == this.password)
      if(user==null){
          this.message= 'Ne postoji taj user'
      }else{
          this.message = 'sve ok'
          this.$router.push('About')
      }
    }
  },
  data(){
    return{
      username: '',
      password: '',
      myuser : users,
      message : ''
    }
  }
}
</script>

<style>
  
</style>
