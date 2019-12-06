<template>
  <div id="app">
    <div class="table">
      <!--:key="ri" signifie passer une variable en attribut -->
      <div
       v-for="(row, ri) in values"
       :key="ri"
        class="row">
        <div
         v-for="(value, ci) in row"
         :key="ci"
         v-on:click="addSymbol ('ri', 'ci')"
         class="col">
          {{ri}} {{ci}}
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import Vue from 'vue'

  export default {
    name: 'app',
    data() {
      return {
        isPlayer: true,
        nbCol:3,
        values: [],
      }
    },
    methods: {
      addSymbol (row, col) {  //on passe l'index de row + col dans l'addSymbol
        Vue.set(this.values[row], col, this.turn === 1 ? 'X' : '0')
        this.isPlayer = !this.isPlayer
      },
      isPlayable
    },
    methods: {},
    created () {
      for (let i=0; i<3; i++) {
        const row = []
        this.values.push(row)
        for(let j=0; j<3; j++)
          row.push(null)
      }
    }
  }
</script>


<style>

body {
  margin: 0;
  color: white;
  background-color: #D8ABEA
}



#app {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100vw;
  height: 100vh;
}

.table {
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  width: 700px;
  height: 700px;
  background-color: #273746
}

.row {
  width: 100%;
  flex: 0 33.33%;
  display: flex;
  justify-content: center;
  align-items: center;

}

.col {
  height: 100%;
  flex: 0 33.33%;
  display: flex;
  align-items: center;
  justify-content: center;
  border: 1px solid red;
  border: thick double #EAECEE
}


</style>
