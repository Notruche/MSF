<script setup>
</script>

<template>
<div class="gal">
  <Transition>
  <div :class="{ bulle1: disabled }"  v-if="disabled==true" class="bulle">
    <img src="../images/x.png" class="x" v-on:click="retour()"> <br>
    <img src="../images/bulle1.png" v-if="i==1">
    <img src="../images/bulle2.png" v-if="i==3">
    <img src="../images/bulle3.png" v-if="i==7">
    <img src="../images/bulle4.png" v-if="i==14">
    <img src="../images/bulle5.png" v-if="i==15">
    <img src="../images/bulle6.png" v-if="i==16">
    <img src="../images/bulle7.png" v-if="i==26">
  </div>
</Transition>
  <div class="perso" v-if="i==1">
    <img src="../images/portrait1.png" :class="{ animperso1: disabled }" v-if="disabled">  
    <img src="../images/portrait1.png" :class="{ animperso: abled }" v-on:click="warnDisabled()" v-if="abled">
    <img src="../images/portrait1cursor.png" :class="{ animpersostart: abled==false }" v-on:click="warnDisabled()" v-if="abled==false && disabled==false">
  </div>
  <div class="perso" v-if="i==3 || i == 14 || i == 16">
    <img src="../images/portrait2.png" :class="{ animperso1: disabled }" v-if="disabled">  
    <img src="../images/portrait2.png" :class="{ animperso: abled }" v-on:click="warnDisabled()" v-if="abled">
    <img src="../images/portrait2cursor.png" :class="{ animpersostart: abled==false }" v-on:click="warnDisabled()" v-if="abled==false && disabled==false">
  </div>
  <div class="perso" v-if="i==7 || i == 15">
    <img src="../images/portrait3.png" :class="{ animperso1: disabled }" v-if="disabled">  
    <img src="../images/portrait3.png" :class="{ animperso: abled }" v-on:click="warnDisabled()" v-if="abled">
    <img src="../images/portrait3cursor.png" :class="{ animpersostart: abled==false }" v-on:click="warnDisabled()" v-if="abled==false && disabled==false">
  </div>
  <div class="perso" v-if="i==26">
    <img src="../images/portrait4.png" :class="{ animperso1: disabled }" v-if="disabled">  
    <img src="../images/portrait4.png" :class="{ animperso: abled }" v-on:click="warnDisabled()" v-if="abled">
    <img src="../images/portrait4cursor.png" :class="{ animpersostart: abled==false }" v-on:click="warnDisabled()" v-if="abled==false && disabled==false">
  </div>
  <Transition>
  <div :class="{ black: disabled }"></div>
</Transition>
<div class="row container-fluid m-0 p-0">
  <div class="col-1 hasimage">
    <img src="../images/ui/home.png" alt="" class="home"
    v-on:click="homepage()">
    <img src="../images/ui/flecheg.png" class="fleche" alt="" v-on:click="prevpage()" v-if="i>1">
  </div>
  <div class="col-10 hasimage gal">
    <img v-if="i == 1" src="../images/Fummeti-Comic-ZC_1.jpg" alt="">
    <img v-if="i == 2" src="../images/Photos/Photo-P3.png" alt="">
    <img v-if="i == 3" src="../images/Fummeti-Comic-ZC_3.jpg" alt="">
    <img v-if="i == 4" src="../images/Fummeti-Comic-ZC_4.jpg" alt="">
    <img v-if="i == 5" src="../images/Fummeti-Comic-ZC_5.jpg" alt="">
    <div v-if="i == 6" class="hasimage gal">
    <img src="../images/quizz/titre1.png" class="quizz"> <br>
    <img src="../images/quizz/reponse1a.png" class="reponse" v-if="quizz" v-on:click="quizzrep()">
    <img src="../images/quizz/reponse1b.png" class="reponse" v-if="quizz" v-on:click="quizzrep()">
    <img src="../images/quizz/reponse1c.png" class="reponse" v-if="quizz" v-on:click="quizzrep()">
    <img src="../images/quizz/reponse1a2.png" class="quizz" v-if="reponse">
    <img src="../images/quizz/reponse1b2.png" class="quizz" v-if="reponse">
    <img src="../images/quizz/reponse1c2.png" class="quizz" v-if="reponse">
    </div>
    <img v-if="i == 7" src="../images/Fummeti-Comic-ZC_6.jpg" alt="">
    <img v-if="i == 8" src="../images/Photos/Photo-P7.png" alt="">
    <img v-if="i == 9" src="../images/Fummeti-Comic-ZC_7.jpg" alt="">
    <img v-if="i == 10" src="../images/Fummeti-Comic-ZC_8.jpg" alt="">
    <div v-if="i == 11" class="hasimage gal">
    <img src="../images/quizz/titre2.png" class="quizz"> <br>
    <img src="../images/quizz/reponse2a.png" class="reponse" v-if="quizz" v-on:click="quizzrep()">
    <img src="../images/quizz/reponse2b.png" class="reponse" v-if="quizz" v-on:click="quizzrep()">
    <img src="../images/quizz/reponse2c.png" class="reponse" v-if="quizz" v-on:click="quizzrep()">
    <img src="../images/quizz/reponse2a2.png" class="quizz" v-if="reponse">
    <img src="../images/quizz/reponse2b2.png" class="quizz" v-if="reponse">
    <img src="../images/quizz/reponse2c2.png" class="quizz" v-if="reponse">
    </div>
    <img v-if="i == 12" src="../images/Fummeti-Comic-ZC_9.jpg" alt="">
    <img v-if="i == 13" src="../images/Fummeti-Comic-ZC_10.jpg" alt="">
    <img v-if="i == 14" src="../images/Fummeti-Comic-ZC_11.jpg" alt="">
    <img v-if="i == 15" src="../images/Fummeti-Comic-ZC_12.jpg" alt="">
    <img v-if="i == 16" src="../images/Fummeti-Comic-ZC_13.jpg" alt="">
    <img v-if="i == 17" src="../images/Fummeti-Comic-ZC_14.jpg" alt="">
    <img v-if="i == 18" src="../images/Fummeti-Comic-ZC_15.jpg" alt="">
    <img v-if="i == 19" src="../images/Fummeti-Comic-ZC_16.jpg" alt="">
    <img v-if="i == 20" src="../images/Photos/Photo-P16.png" alt="">
    <img v-if="i == 21" src="../images/Fummeti-Comic-ZC_17.jpg" alt="">
    <img v-if="i == 22" src="../images/Fummeti-Comic-ZC_18.jpg" alt="">
    <img v-if="i == 23" src="../images/Fummeti-Comic-ZC_19.jpg" alt="">
    <img v-if="i == 24" src="../images/Fummeti-Comic-ZC_20.jpg" alt="">
    <img v-if="i == 25" src="../images/Fummeti-Comic-ZC_21.jpg" alt="">
    <img v-if="i == 26" src="../images/Fummeti-Comic-ZC_22.jpg" alt="">
  </div>
  <div class="col-1 hasimage">
  <img src="../images/ui/fleched.png" alt="" class="fleche" v-on:click="nextpage()" v-if="i<26">
  </div>
</div>
</div>
</template>
<script>
export default {
  data(){
        return {
          i: 1,
          disabled: false,
          abled:false,
          quizz:true,
          reponse:false,
        }
    },
  methods: {
    retour() {
      var that = this
      this.disabled = false
      this.abled = true
    },
    quizzrep() {
      var that = this
      this.quizz = false
      this.reponse = true
    },
    warnDisabled() {
      var that = this
      this.disabled = true
      this.abled = false
    },
    nextpage() {
      var that = this
      that.i += 1
      console.log(that.i)
      this.abled = false
      this.quizz = true
      this.reponse = false
    },
    prevpage() {
      var that = this
      if(that.i > 1){
      that.i -= 1
      console.log(that.i)
      this.abled = false
      this.quizz = true
      this.reponse = false
    }
    },
    homepage() {
      var that = this
      that.i = 1
      console.log(that.i)
      this.abled = false
      this.quizz = true
      this.reponse = false
    },
    },
  }
</script>
<style scoped>
</style>
