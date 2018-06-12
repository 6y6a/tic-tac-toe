<template>
  <div id="app">
    <div id="details">
      <h1>Tic Tac Toe</h1>
    </div>

    <board />
  </div>
</template>

<script>
  import board from './components/Board.vue'

  export default {
    name: 'app',
    components: {
      board
    },
    data() {
      return {
        matches: 0,
        wins: {
          o: 0,
          x: 0
        }
      }
    }
  }
</script>

<style lang="scss">

  body {
    background-color: #FFEE58;
    color: #fff;
    font-family: 'Dosis', Helvetica, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    margin: 0;
  }

  #app {
    margin: 0 auto;
    max-width: 270px;
    color: #34495e;
  }

  h1 {
    text-transform: uppercase;
    font-weight: bold;
    font-size: 3em;
  }

  .restart {
    background-color: #e74c3c;
    color: #fff;
    border: 0;
    border-bottom-left-radius: 10px;
    border-bottom-right-radius: 10px;
    font-family: 'Dosis', Helvetica, sans-serif;
    font-size: 1.4em;
    font-weight: bold;
    margin: 0;
    padding: 15px;
    width: 100%;

    &:hover {
      background-color: #c0392b;
      cursor: pointer;
    }
  }

  .scoreBoard {
    display: flex;
    justify-content: space-around;
    align-items: center;
    width: 100%;
    height: 15px;
    background-color: #16a085;
    box-shadow: 10px solid #fff;
    padding: 20px;
    overflow-x: none;

    h2 {
      margin: 0;
    }

    span {
      float: right;
      font-size: 1.5em;
      font-weight: bold;
      margin-left: 20px;
    }
  }

</style>
