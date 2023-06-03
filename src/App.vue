<template>
  <header>
    <p>VivAsiA</p>
  </header>

  <div class="content skew-element"  ref="content" @wheel="handleScroll">
    <Home />

    <PlacesComp />

    <Facts />
  </div>

  <footer>
    <div>
      <img class="footer-pattern" src="./assets/Home/pattern.jpg" alt="">
      <img class="footer-pattern" src="./assets/Home/pattern.jpg" alt="">
      <img class="footer-pattern" src="./assets/Home/pattern.jpg" alt="">
      <img class="footer-pattern" src="./assets/Home/pattern.jpg" alt="">
      <img class="footer-pattern" src="./assets/Home/pattern.jpg" alt="">
      <img class="footer-pattern" src="./assets/Home/pattern.jpg" alt="">
      <img class="footer-pattern" src="./assets/Home/pattern.jpg" alt="">
      <img class="footer-pattern" src="./assets/Home/pattern.jpg" alt="">
      <img class="footer-pattern" src="./assets/Home/pattern.jpg" alt="">
      <img class="footer-pattern" src="./assets/Home/pattern.jpg" alt="">
      <img class="footer-pattern" src="./assets/Home/pattern.jpg" alt="">
      <img class="footer-pattern" src="./assets/Home/pattern.jpg" alt="">
      <img class="footer-pattern" src="./assets/Home/pattern.jpg" alt="">
      <img class="footer-pattern" src="./assets/Home/pattern.jpg" alt="">
      <img class="footer-pattern" src="./assets/Home/pattern.jpg" alt="">
      <img class="footer-pattern" src="./assets/Home/pattern.jpg" alt="">
      <img class="footer-pattern" src="./assets/Home/pattern.jpg" alt="">
      <img class="footer-pattern" src="./assets/Home/pattern.jpg" alt="">
      <img class="footer-pattern" src="./assets/Home/pattern.jpg" alt="">
      <img class="footer-pattern" src="./assets/Home/pattern.jpg" alt="">
      <img class="footer-pattern" src="./assets/Home/pattern.jpg" alt="">
    </div>
  </footer>
</template>

<script>
import Home from './components/Home.vue'
import PlacesComp from './components/Places.vue'
import Facts from './components/Facts.vue'

export default {
  name: 'App',
  methods: {
    handleScroll(event) {
      this.isScrolling = true;
      clearTimeout(this.scrollTimeout);

      let scrollTop = event.deltaY;
      let contentElement = this.$refs.content;
      let maxScrollLeft = contentElement.scrollWidth - contentElement.clientWidth;
      let skewAngle = scrollTop * 0;

      if (!(contentElement.scrollLeft === 0 || Math.round(contentElement.scrollLeft) === maxScrollLeft)) {
        skewAngle = -scrollTop * 0.25; // Adjust the multiplier to control the skew intensity
      }

      let skewValue = 'skewX(' + skewAngle + 'deg)';
      document.querySelector('.skew-element').style.transform = skewValue;

      // Scroll horizontally to the right
      contentElement.scrollLeft += event.deltaY;
      event.preventDefault();

      this.scrollTimeout = setTimeout(() => {
        this.isScrolling = false;
        document.querySelector('.skew-element').style.transform = 'none';
      }, 200);
    },
  },
  components : {
    Home,
    PlacesComp,
    Facts,
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

img {
  border-radius: 20px;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 100%;
  height: 100%;
  color: #8b8b8b;
  background-color: rgb(0, 3, 17);
  display: flex;
  flex-direction: column;
  overflow-x: hidden;
  font-size: 13px;
}

header p {
  font-family: 'jelani', sans-serif;
  font-size: 30px;
  font-weight: 400;
  margin: 5px 25px;
  color: white;
}

footer {
  width: 100%;
  display: flex;
}
footer div {
  overflow: hidden;
  width: 100%;
  display: flex;
}
.footer-pattern {
  width: 50px;
  height: 50px;
  margin: 5px 15px;
}
@media (prefers-reduced-motion: no-preference) {
  .footer-pattern {
    animation: pattern-spin infinite 10s linear;
  }
}
@keyframes pattern-spin {
  from {
    transform: rotate(0deg);
  }
  to {
    transform: rotate(360deg);
  }
}

.content {
  display: inline-block;
  max-width: max-content;
  height: 100%;
  display: flex;
  align-items: center;
  overflow-x: scroll;
  padding-bottom: 50px;
}

.content::-webkit-scrollbar {
  display: none;
}

.skew-element {
  transition: transform 0.15s ease-out;
	will-change: transform;
}
</style>