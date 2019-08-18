<template>
  <div id="app">
    <!-- <div id="nav">
      <router-link to="/">Home</router-link>|
      <router-link to="/about">About</router-link>
    </div>
    <router-view />-->

    <div class="page page-1">
      <div class="top Z">Z</div>
      <div class="page page-2">
        <div class="top A">A</div>
        <div class="page page-3">
          <div class="top N">N</div>
          <div class="page page-4">
            <div class="top N">N</div>
            <div class="page page-5">
              <div class="top E">E</div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

.page {
  min-height: 100vh;
  width: 100vw;
  display: flex;
  flex-flow: row wrap;
  justify-content: center;
  align-items: flex-end;
  .page {
    min-height: 100vh;
    width: 100vw;
    display: flex;
    flex-flow: row wrap;
    align-items: flex-end;
  }
  .top {
    width: 100%;
    // height: 50px;
    // font-family: 'Courier New', Courier, monospace;
    // font-size: xx-large;
    // font-size: calc(100vh - 30px);
    line-height: 100vh;
    font-size: calc(100vh / 2);
    font-weight: 600;

    background-clip: text;
    color: transparent;
    background-color: rgba($color: #000000, $alpha: 0.4);
    // color: rgb(#000, 0.1);
    align-self: flex-start;
    // align-self: center;
    text-align: center;
    top: 0;
    position: sticky;
  }
}

.page-1 {
  height: 500vh;
  background-color: lightblue;
}
.page-2 {
  height: 400vh;
  background-color: darkgray;
  .top {
    text-indent: 3ch;
  }
}
.page-3 {
  height: 300vh;
  background-color: lightblue;
  .top {
    text-indent: 6ch;
  }
}
.page-4 {
  height: 200vh;
  background-color: darkgray;
  .top {
    text-indent: 9ch;
  }
}
.page-5 {
  height: 100vh;
  background-color: lightblue;
  .top {
    text-indent: 12ch;
  }
}
// #nav {
//   padding: 30px;
//   a {
//     font-weight: bold;
//     color: #2c3e50;
//     &.router-link-exact-active {
//       color: #42b983;
//     }
//   }
// }
</style>
<script lang="ts">
import Vue from 'vue';
export default class App extends Vue {

}
</script>

