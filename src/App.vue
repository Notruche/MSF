<script setup>
</script>

<template>
<div class="gal">
  <Transition name="fade">
  <div :class="{ bulle1: disabled }"  v-if="disabled==true" class="bulle">
    <img src="../public/images/x.png" class="x" v-on:click="retour()"> <br>
    <img src="../public/images/bulle1.png" v-if="i==1">
    <img src="../public/images/bulle2.png" v-if="i==4">
    <img src="../public/images/bulle3.png" v-if="i==8">
    <img src="../public/images/bulle4.png" v-if="i==14">
    <img src="../public/images/bulle5.png" v-if="i==15">
    <img src="../public/images/bulle6.png" v-if="i==16">
    <img src="../public/images/bulle7.png" v-if="i==29">
  </div>
</Transition>
  <div class="perso" v-if="i==1">
    <img src="../public/images/portrait1.png" :class="{ animperso1: disabled }" v-if="disabled">  
    <img src="../public/images/portrait1.png" :class="{ animperso: abled }" v-on:click="warnDisabled()" v-if="abled">
    <img src="../public/images/portrait1cursor.png" :class="{ animpersostart: abled==false }" v-on:click="warnDisabled()" v-if="abled==false && disabled==false">
  </div>
  <div class="perso" v-if="i==4 || i == 14 || i == 16">
    <img src="../public/images/portrait2.png" :class="{ animperso1: disabled }" v-if="disabled">  
    <img src="../public/images/portrait2.png" :class="{ animperso: abled }" v-on:click="warnDisabled()" v-if="abled">
    <img src="../public/images/portrait2cursor.png" :class="{ animpersostart: abled==false }" v-on:click="warnDisabled()" v-if="abled==false && disabled==false">
  </div>
  <div class="perso" v-if="i==8 || i == 15">
    <img src="../public/images/portrait3.png" :class="{ animperso1: disabled }" v-if="disabled">  
    <img src="../public/images/portrait3.png" :class="{ animperso: abled }" v-on:click="warnDisabled()" v-if="abled">
    <img src="../public/images/portrait3cursor.png" :class="{ animpersostart: abled==false }" v-on:click="warnDisabled()" v-if="abled==false && disabled==false">
  </div>
  <div class="perso" v-if="i==29">
    <img src="../public/images/portrait4.png" :class="{ animperso1: disabled }" v-if="disabled">  
    <img src="../public/images/portrait4.png" :class="{ animperso: abled }" v-on:click="warnDisabled()" v-if="abled">
    <img src="../public/images/portrait4cursor.png" :class="{ animpersostart: abled==false }" v-on:click="warnDisabled()" v-if="abled==false && disabled==false">
  </div>
  <Transition name="fade">
  <div :class="{ black: disabled }"></div>
</Transition>
<Transition name="fade">
<div :class="{ black2: warn }"></div>
</Transition>
<div class="row container-fluid m-0 p-0">
  <div class="col-1 hasimage">
    <img src="../public/images/ui/home.png" alt="" class="home"
    v-on:click="homepage()" v-if="i!=3 && i!=21 && i!=23">
    <img src="../public/images/ui/flecheg.png" class="fleche" alt="" v-on:click="prevpage()" v-if="i>1 && i!=3 && i!=21 && i!=23">
  </div>
  <div class="col-10 hasimage gal">
    <div class="warning" v-if="warn">
      <div class="box pt-3">
        <h3>Möchtest du wirklich zum Anfang des Comics zurück?</h3>
        <button class="btn btn-success exit mt-3" v-on:click="yes()">Ja</button>
        <button class="btn btn-danger exit mt-3" v-on:click="no()">Nein</button>
      </div>
    </div>
    <img v-if="i == 1" src="../public/images/Fummeti-Comic-ZC_1.jpg" alt="">
    <Transition name="test">
      <div class="fondu" v-if="i == 2">  </div>
  </Transition>
    <img v-if="i == 4" src="../public/images/Fummeti-Comic-ZC_3.jpg" alt="">
    <img v-if="i == 5" src="../public/images/Fummeti-Comic-ZC_4.jpg" alt="">
    <img v-if="i == 6" src="../public/images/Fummeti-Comic-ZC_5.jpg" alt="">
    <div v-if="i == 7" class="hasimage gal">
    <img src="../public/images/quizz/titre1.png" class="quizz"> <br>
    <img src="../public/images/quizz/reponse1a.png" class="reponse" v-if="quizz" v-on:click="quizzrep()">
    <img src="../public/images/quizz/reponse1b.png" class="reponse" v-if="quizz" v-on:click="quizzrep()">
    <img src="../public/images/quizz/reponse1c.png" class="reponse" v-if="quizz" v-on:click="quizzrep()">
    <img src="../public/images/quizz/reponse1a2.png" class="quizz" v-if="reponse">
    <img src="../public/images/quizz/reponse1b2.png" class="quizz" v-if="reponse">
    <img src="../public/images/quizz/reponse1c2.png" class="quizz" v-if="reponse">
    </div>
    <img v-if="i == 8" src="../public/images/Fummeti-Comic-ZC_6.jpg" alt="">
    <Transition name="carte">
    <div v-if="i == 9" class="carte" alt=""> </div>
    </Transition>
    <img v-if="i == 10" src="../public/images/Fummeti-Comic-ZC_8.jpg" alt="">
    <div v-if="i == 11" class="hasimage gal">
    <img src="../public/images/quizz/titre2.png" class="quizz"> <br>
    <img src="../public/images/quizz/reponse2a.png" class="reponse" v-if="quizz" v-on:click="quizzrep()">
    <img src="../public/images/quizz/reponse2b.png" class="reponse" v-if="quizz" v-on:click="quizzrep()">
    <img src="../public/images/quizz/reponse2c.png" class="reponse" v-if="quizz" v-on:click="quizzrep()">
    <img src="../public/images/quizz/reponse2a2.png" class="quizz" v-if="reponse">
    <img src="../public/images/quizz/reponse2b2.png" class="quizz" v-if="reponse">
    <img src="../public/images/quizz/reponse2c2.png" class="quizz" v-if="reponse">
    </div>
    <img v-if="i == 12" src="../public/images/Fummeti-Comic-ZC_9.jpg" alt="">
    <img v-if="i == 13" src="../public/images/Fummeti-Comic-ZC_10.jpg" alt="">
    <img v-if="i == 14" src="../public/images/Fummeti-Comic-ZC_11.jpg" alt="">
    <img v-if="i == 15" src="../public/images/Fummeti-Comic-ZC_12.jpg" alt="">
    <img v-if="i == 16" src="../public/images/Fummeti-Comic-ZC_13.jpg" alt="">
    <img v-if="i == 17" src="../public/images/Fummeti-Comic-ZC_14.jpg" alt="">
    <img v-if="i == 18" src="../public/images/Fummeti-Comic-ZC_15.jpg" alt="">
    <div v-if="i == 19" class="hasimage gal">
    <img src="../public/images/quizz/titre3.png" class="quizz"> <br>
    <img src="../public/images/quizz/reponse3a.png" class="reponse" v-if="quizz" v-on:click="quizzrep()">
    <img src="../public/images/quizz/reponse3b.png" class="reponse" v-if="quizz" v-on:click="quizzrep()">
    <img src="../public/images/quizz/reponse3c.png" class="reponse" v-if="quizz" v-on:click="quizzrep()">
    <img src="../public/images/quizz/reponse3a2.png" class="quizz" v-if="reponse">
    <img src="../public/images/quizz/reponse3b2.png" class="quizz" v-if="reponse">
    <img src="../public/images/quizz/reponse3c2.png" class="quizz" v-if="reponse">
    </div>
    <Transition name="test3">
    <div class="fondu3" v-if="i == 20">  </div>
  </Transition>
    <Transition name="test2">
      <div class="fondu2" v-if="i == 22">  </div>
  </Transition>
    <img v-if="i == 24" src="../public/images/Fummeti-Comic-ZC_17.jpg" alt="">
    <img v-if="i == 25" src="../public/images/Fummeti-Comic-ZC_18.jpg" alt="">
    <img v-if="i == 26" src="../public/images/Fummeti-Comic-ZC_19.jpg" alt="">
    <img v-if="i == 27" src="../public/images/Fummeti-Comic-ZC_20.jpg" alt="">
    <img v-if="i == 28" src="../public/images/Fummeti-Comic-ZC_21.jpg" alt="">
    <img v-if="i == 29" src="../public/images/Fummeti-Comic-ZC_22.jpg" alt="">
  </div>
  <div class="col-1 hasimage">
  <img src="../public/images/ui/fleched.png" alt="" class="fleche" v-on:click="nextpage()" v-if="i<29 && i!=3 && i!=21 && i!=23">
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
          warn: false
        }
    },
  methods: {
    retour() {
      this.disabled = false
      this.abled = true
    },
    quizzrep() {
      this.quizz = false
      this.reponse = true
    },
    warnDisabled() {
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
      if(that.i == 3){
        setTimeout(function(){
      that.i += 1
      console.log(that.i)
      this.abled = false
      this.quizz = true
      this.reponse = false
    }, 3000);
      }
      if(that.i == 21){
        setTimeout(function(){
      that.i += 1
      console.log(that.i)
      this.abled = false
      this.quizz = true
      this.reponse = false
    }, 3000);
      }
      if(that.i == 23){
        setTimeout(function(){
      that.i += 1
      console.log(that.i)
      this.abled = false
      this.quizz = true
      this.reponse = false
    }, 3000);
      }
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
    if(that.i == 3){
      that.i -= 1
      console.log(that.i)
      this.abled = false
      this.quizz = true
      this.reponse = false
    }
    if(that.i == 21){
      that.i -= 1
      console.log(that.i)
      this.abled = false
      this.quizz = true
      this.reponse = false
    }
    if(that.i == 23){
      that.i -= 1
      console.log(that.i)
      this.abled = false
      this.quizz = true
      this.reponse = false
    }
    },
    homepage() {
      this.warn = true
    },
    no() {
      this.warn = false
    },
    yes() {
      this.i = 1
      this.abled = false
      this.quizz = true
      this.reponse = false
      this.warn = false
    },
    },
  }
</script>
<style scoped>
</style>
