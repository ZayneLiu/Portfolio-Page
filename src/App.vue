<template>
  <page :pageNo="0" class="first-page">
    <slot>
      <section class="section-a">a</section>
      <section class="section-b">b</section>
      <section class="section-c">c</section>
      <section class="section-d">d</section>
    </slot>
  </page>
  <page :pageNo="1" />
  <page />

  <img alt="Vue logo" src="./assets/logo.png" />
  <HelloWorld @aa="log()" msg="Hello Vue 3.0 + Vite" />
  <button @click="hi='aaa'">aa</button>
  {{hi}}
</template>

<style>
body {
  margin: 0;
}
#app {
  display: flex;
  flex-flow: column nowrap;
  align-items: center;
}
.navbar {
  display: flex;
  flex-flow: row nowrap;
}
.fullpage {
  width: 100vw;
  height: 100vh;
  background-color: #aaa;
  border-top: 1px solid grey;
  box-sizing: border-box;
}
.first-page {
  display: flex;
  flex-flow: row nowrap;
  overflow: hidden;
  justify-content: center;
}
.first-page img {
  width: 50vh;
  /* height: 50px; */
  border-radius: 25vh;
}
.first-page section {
  /* flex: 1; */
  width: 25%;
  clip-path: polygon(50px 0, 100% 0, calc(100% - 50px) 100%, 0 100%);
  box-sizing: content-box;
  margin-right: -50px;
}
.first-page .section-a {
  /* margin-left: -50px; */
  background-color: rebeccapurple;

  /* margin-right: -10%; */
}
.first-page .section-b {
  background-color: #fff;
  /* margin-left: -12.5%; */
}
.first-page .section-c {
  background-color: lime;
}
.first-page .section-d {
  background-color: teal;
}
</style>
<script lang="ts">
import HelloWorld from "./components/HelloWorld.vue";
import Page from "./components/Page.vue";

export default {
  name: "App",
  components: {
    HelloWorld,
    Page,
  },
  data() {
    return {
      hi: "sd",
    };
  },
  watch: {
    hi(newV: any, oldV: any) {
      console.log(newV);
    },
  },
  methods: {
    log() {
      // Axios({});
      // console.log(window.innerHeight);
      // console.log(window.pageYOffset);
      // console.log(window.pageYOffset / window.innerHeight);
      // document.getElementById("page-1").scrollIntoView();
    },
  },
  mounted() {
    // window.addEventListener("scroll", () => {
    //   this.log();
    // });
  },
};
</script>
