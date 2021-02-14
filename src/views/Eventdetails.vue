<template lang="html">

  <section class="eventdetails">
    <br/>
     <img src='../assets/medodjija-box-1.jpg' weight=1000px height=200px>
    <br/>
    <h1>{{myevent.naziv}}</h1>
    <!-- <div class='prodDesc'>{{myevent.lokacija}}</div> -->
    <div class='prodDesc'>{{myevent.opis}}</div>
    <div class='prodDesc'>Naše veliko iskustvo koristimo da blagodeti naše zemlje putem pčelarstva u Vaše domove donesemo. Ukus, miris i svežinu naših beskrajno lepih i lekovitih livada, svežinu i i miris bagremovih šuma i nektar sa biljaka širom prelepih, netaknutih i nedostupnih planinskih vrhova.
    Kvalitet je prioritet, a on je prirodan. Poželite i dobićete.
    Čovek i pčele moraju da se vole, poštuju i samo iz tog poverenja, ljubavi i puno sunca dobićemo prirodan kvalitet meda.
    Pčele vole lepu reč, lep cvet, lepu muziku, sjajno sunce, zelenilo pašnjaka i neodoljive mirise koji nas okružuju.
    Ako im pomognemo da sve to im bude dostupno, rado će nas obradovati lepim, slatkim, mirisnim i nadasve zdravim medom.</div>
    <div class='prodDesc'>{{myevent.datum}} din</div>
    <div>
    <div>Unesite zeljenu kolicinu:</div>
    <div>
      <input type= text v-model="quantity"> Ukupna cena : {{this.quantity * myevent.datum }} din
      <button @click = 'dodajUKorpu' class="btn btn-primary" >Dodaj u korpu </button>
    </div>
    </div>
  </section>
</template>

<script lang="js">
import events from '../data/events'
import basketLines from '../data/basket'

  export default  {
    name: 'eventdetails',
    props: [],
    mounted () {
      var id= Number(this.$route.params.id);
      var event = this.myevents.find(event => event.id== id )
      this.myevent = event;
    },
    data () {
      return {
          myevents : events,
          myevent  : {},
          quantity : 1
      }
    },
    methods: {

      dodajUKorpu(){
        var id= Number(this.$route.params.id);
         var event = this.myevents.find(event => event.id== id )
        var line = {id :event.id, naziv : event.naziv,datum: event.datum, lokacija:event.lokacija, opis:event.opis, count: this.quantity}
        basketLines.push(line)
         alert("Uspesno ste dodali artikal u korpu!");
      }
    }
}


</script>

<style>
  .prodDesc{
    padding: 10px;
    margin-left: 100px;
    text-align: justify;
  }
</style>
