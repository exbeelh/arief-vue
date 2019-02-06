<template>

  <div id="app">

    <h1>{{ nama }}</h1>
    <h2>Nama: <input v-model="nama"><br></h2>
    <h2>Nilai Anda : {{ nilai }}</h2>
    <button @click="totalnilai">Click Me</button>  
    <h2>1. Salah satu nama kota di Jawa Barat</h2>
    <input type="radio" v-model="soal1" value="Bandung">Bandung 
    <input type="radio" v-model="soal1" value="Sabang">Sabang 
    <input type="radio" v-model="soal1" value="Denpasar">Denpasar 
    <input type="radio" v-model="soal1" value="Jambi">Jambi<br>
    <h2>2. Pada tanggal berapa Arief lahir</h2>
    <input type="radio" v-model="soal2" value="25">25
    <input type="radio" v-model="soal2" value="26">26
    <input type="radio" v-model="soal2" value="13">13
    <input type="radio" v-model="soal2" value="14">14<br>
    <h2>3. Game Ragnarok Mobile Eternal Love adalah game</h2>
    <input type="radio" v-model="soal3" value="RPG">RPG
    <input type="radio" v-model="soal3" value="MMORP">MMORPG
    <input type="radio" v-model="soal3" value="MOBA">MOBA
    <input type="radio" v-model="soal3" value="FPS">FPS<br>
  </div>
</template>

<script>
export default {
  name: 'app',
  data() {
    return{
      nama: '',
      nilai: 0,
      soal1: '',
      soal2: '',
      soal3: ''
      /*components: {
        HelloWorld
      }*/
    }
  },
methods: {
  totalnilai(){
    if (this.soal1 == 'Bandung' && this.soal2 == '25' && this.soal3 == 'RPG') {
      this.nilai=+3    
    }
    else if (this.soal1 == 'Bandung' && this.soal2 == '25') {
      this.nilai=+2 
    }
    else if (this.soal1 == 'Bandung' && this.soal3 == 'RPG') {
      this.nilai=+2 
    }
    else if (this.soal2 == '25' && this.soal3 == 'RPG') {
      this.nilai=+2 
    }
    else if (this.soal1 == 'Bandung') {
      this.nilai=+1 
    }
    else if (this.soal2 == '25') {
      this.nilai=+1 
    }
    else if (this.soal3 == 'RPG') {
      this.nilai=+1 
    }
    else {
      this.nilai = 0 
    }
  }
}
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
