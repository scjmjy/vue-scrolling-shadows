<template>
  <div id="app" class="container">
    <h2>No scroll shadow</h2>
    <div class="no-shadows">
      <p>Scroll me!</p>
      <ul>
        <li v-for="n in 30" :key="n">List item {{ n }}</li>
      </ul>
    </div>

    <h2>With scroll shadow (vertical)</h2>
    <ScrollShadow class="shadows">
      <p>Scroll me!</p>
      <ul>
        <li v-for="n in 30" :key="n">List item {{ n }}</li>
      </ul>
    </ScrollShadow>

    <h2>With scroll shadow (horizontal)</h2>
    <ScrollShadow class="shadows-horizontal">
      <p>Scroll me!</p>
      <ul class="horizontal-list">
        <li v-for="n in 30" :key="n">
          <h5>List item {{ n }}</h5>
          <p>Lorem Ipsum dolor ist amet.</p>
        </li>
      </ul>
    </ScrollShadow>
  </div>
</template>

<script>
import ScrollShadow from "./components/ScrollShadow.vue";

export default {
  name: "App",
  components: {
    ScrollShadow
  }
};
</script>

<style>
body {
  margin: 0;
  padding: 0;
}

img {
  max-width: 100%;
  max-height: 100%;
}

*,
*::before,
*::after {
  box-sizing: border-box;
}

#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}

.no-shadows {
  overflow: auto;
  max-height: 200px;
}

.shadows {
  max-height: 200px;
}

.horizontal-list {
  display: flex;
}

.horizontal-list li {
  min-width: 100px;
}

.container {
  max-width: 42em;
  margin-right: auto;
  margin-left: auto;
  padding-right: 1em;
  padding-left: 1em;
}
</style>
