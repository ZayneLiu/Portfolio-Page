<template>
  <nav class="navbar">
    <a href="#contact">
      <img alt="Zayne" src="src/assets/images/me.jpeg" />
    </a>

    <ul class="navbar_nav">
      <li class="home-link">
        <a href="#home">Home</a>
      </li>
      <li class="works-link">
        <a href="#works">Works</a>
      </li>
      <li class="contact-link">
        <a href="#contact">Contact</a>
      </li>
    </ul>
  </nav>

  <img alt="Vue logo" src="./assets/logo.png" />
  <HelloWorld @aa="log()" msg="Hello Vue 3.0 + Vite" />
  <button @click="hi='aaa'">aa</button>
  {{hi}}
</template>

<script lang="ts">
import HelloWorld from "./components/HelloWorld.vue";

export default {
  name: "App",
  components: {
    HelloWorld,
  },
  data() {
    return {
      hi: "sd",
    };
  },
  watch: {
    hi(newV, oldV) {
      console.log(newV);
    },
  },
  methods: {
    log() {
      console.log("asd");
    },
  },
};
</script>
