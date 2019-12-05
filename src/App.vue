<template>
  <div id="app">
    <div class="table">
      <div class="row">
        <div class="col">
        </div>
        <div class="col">
        </div>
        <div class="col">
        </div>
      </div>
      <div class="row">
        <div class="col">
        </div>
        <div class="col">
        </div>
        <div class="col">
        </div>
      </div>
      <div class="row">
        <div class="col">
        </div>
        <div class="col">
        </div>
        <div class="col">
        </div>
      </div>
    </div>
  </div>
</template>
<script>
  export default {
    name: 'app',
    data() {
      return {}
    }
  }
</script>

<style>

body {
  margin: 0;
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
