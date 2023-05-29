<template>
  <HeaderComp />

  <div class="content"  ref="content" @wheel="handleScroll">
    <!--<div class="one">
      <h1>
        Discover <br />
        Asia
      </h1>

      <p>
        take a glimpse of asia's <br />
        bewitching attractions
      </p>

      <button>EXPLORE</button>
    </div>

    <HomeGrid />-->

    <Places />

    <div class="four">
    </div>
  </div>
  
  <footer></footer>
</template>

<script>
import HeaderComp from './components/HeaderComp.vue'
//import HomeGrid from './components/HomeGrid.vue'
import Places from './components/Places.vue'

export default {
  name: 'App',
  methods: {
    handleScroll(event) {  
      // Scroll horizontally to the right
      this.$refs.content.scrollLeft += event.deltaY;
    
      event.preventDefault();
    }
  },
  components : {
    HeaderComp,
    //HomeGrid,
    Places
  }
}
</script>

<style>
@font-face {
  font-family: 'jelani';
  src: url('./assets/Jelani-Font/jelani.woff') format('woff');
}

html,
body {
  width: 100%;
  height: 100%;
  margin: 0;
  padding: 0;
}

img {
  border-radius: 20px;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 100%;
  height: 100%;
  white-space: nowrap;
  color: #8b8b8b;
  background-color: rgb(0, 3, 17);

  display: flex;
  flex-direction: column;
}

h1 {
  margin: 0;
  font-size: inherit;
  font-weight: inherit;
  line-height: inherit;
  color: inherit;
}

h1, h2, h3, h4 {
  color: white;
}

h2 {
  margin: 0;
  font-size: 3.8em;
  line-height: 1em;
}

h3 {
  margin: 0;
  font-size: 2em;
}

button {
  appearance: none;
  background-color: transparent;
  border: none;
  padding: 0;
  margin: 0;
  font: inherit;
  color: inherit;
  cursor: pointer;
}

footer {
  height: 40px;
}

.content {
  display: inline-block;
  max-width: max-content;
  height: 100%;
  display: flex;
  overflow-x: scroll;
}

.content::-webkit-scrollbar {
  display: none;
}

.one, .three, .four{
  flex-shrink: 0;

  height: 100%;
  padding-right: 120px;
  padding-left: 120px;
}

.one {
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.one h1 {
  font-family: 'jelani', sans-serif;
  font-size: 4em;
  font-weight: 200;
  line-height: 60px;
}

.one p {
  font-size: 0.8em;
}

.one button {
  border: 2px solid;
  padding: 10px;
  width: max-content;
}

.three {
  width: 600px;
  height: 100%;
  background-color: red;
}

.four {
  width: 600px;
  height: 100%;
  background-color: yellow;
}
</style>
