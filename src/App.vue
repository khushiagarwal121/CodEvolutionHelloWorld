<template>
  <!-- Hello Vishwas -->
  <!-- text interpolation -->
  <!-- moustache syntax -->
  <div>{{ greet }} {{ name }}</div>
  <div v-text="channel"></div>
  <div v-html="channel"></div>
  <h2 v-bind:id="headingId">hwllo</h2>
  <button v-bind:disabled="isDisabled">bind</button>
  <!-- satic class -->
  <!-- <h2 class="underline" v-bind:class="status">d</h2> -->
  <h2 v-bind:class="underline">d</h2>
  <h2 v-bind:class="'promoted' && isPromoted">Promoted movie</h2>
  <!-- <div v-text='name'>Hello</div> -->
  <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'

export default {
  name: "App",
  // components: {
  //   HelloWorld
  // }
  data() {
    return {
      greet: "Hello",
      name: "Vishwas",
      channel: "<b>code evolution<b>",
      headingid: "heading",
      isDisabled: false,
      status: "danger",
      isPromoted: true,
      underline: "underline",
      // isSoldOut
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.underline {
  text-decoration: underline;
}
.promoted {
  font-style: italic;
}
.new {
  color: olivedrab;
}
.sold-out {
  color: red;
}
</style>
