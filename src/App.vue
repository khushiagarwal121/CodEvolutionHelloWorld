<template>
  <div>{{ greet }} {{ name }}</div>
  <div v-text="channel"></div>
  <div v-html="channel"></div>
  <h2 v-bind:id="headingId">hwllo</h2>
  <button v-bind:disabled="isDisabled">bind</button>

  <h2 v-bind:class="underline">d</h2>
  <!-- isPromoted is true → Since it's true, the second operand 'promoted' is returned as the result of the expression. -->
  <h2 v-bind:class="'promoted' && isPromoted">Promoted movie</h2>
  <!-- <div v-text='name'>Hello</div> -->
  <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  <!-- CLASS EXPECTS DATA PROPERTY SO BELOW WORKS -->
  <h2 v-bind:class="isSoldOut ? 'soldOut' : 'new'">Soldout?Movie</h2>

  <h2 v-bind:class="soldOut">Newly Promoted movie</h2>
  <h2 v-bind:class="['soldOut', isPromoted && 'promoted', 'hj']">new</h2>

  <h1
    v-bind:class="{
      promoted: isPromoted,
      new: !isSoldOut,
      soldOut: isSoldOut,
      h: '19',
      k: '',
      l: 0,
      m: 1,
    }"
  >
    object conditional movie
  </h1>

  <h1
    v-bind:style="{
      color: highlightColor,
      'font-size': headerSize + 'px',
    }"
  >
    inline styles
  </h1>

  <!-- <h2 v-bind:class="new">Soldout?Movie</h2> -->
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
      isSoldOut: true,
      highlightColor: "orange",
      headerSize: 50,
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
.soldOut {
  color: red;
}
/* .highlightColor {
  color: "green";
} */
</style>
