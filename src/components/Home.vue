<template>
    <div class="home">
        <div class="home-intro">
            <h1>Discover <br /> Asia</h1>

            <p>take a glimpse of asia's <br /> bewitching attractions</p>

            <a href="#places">
                <button>EXPLORE</button>
            </a>
        </div>

        <div class="home-grid">
            <img class="home-main" src="../assets/Home/home-main.jpg" alt="Wildlife Elephant"/>
        
            <div class="home-side">
                <div class="home-side-top">
                    <div class="home-side-sub">    
                        <img class="home-two" src="../assets/Home/home-two.jpg" alt="photo of sushi in a wooden bowl">             
                        <img class="mid-pattern" src="../assets/Home/pattern.jpg" alt="">
                    </div>

                    <img class="home-three" src="../assets/Home/home-three.jpg" alt="">
                </div>

                <img class="home-four" src="../assets/Home/home-four.jpg" alt="Vue logo"/>               
            </div>
        </div>
    </div>
    
</template>

<script> 
export default {
  name: 'Home'
}
</script>

<style scoped>
.home {
    display: flex;
    padding: 0px 110px;
}
.home-intro {
  display: flex;
  flex-direction: column;
  justify-content: center;
  margin-right: 240px;
}

.home-intro h1 {
  font-family: 'jelani', sans-serif;
  font-size: 4.4em;
  font-weight: 500;
  line-height: 60px;
}

.home-intro button {
    color: white;
    border: 2px solid;
    margin-top: 20px;
    padding: 15px 35px;
    width: max-content;
    font-size: 10px;
    letter-spacing: 3px;
    -webkit-transition: background 1s; /* For Safari 3.0 to 6.0 */
    transition: background 1s
}

.home-intro button:hover {
    background-color: white;
    color: black;
    border: red 2px dotted;
}

.home-grid {
    height: 100%;
    width: max-content;
    display: grid;
    grid-template-columns: 310px 335px;
    align-items: center;
    column-gap: 25px;
}

.home-main {
    width: 100%;
}

.home-side {
    display: grid;
    row-gap: 25px;
}

.home-side-top {
    width: max-content;
    display: grid;
    grid-template-columns: 110px 210px;
    gap: 25px;
    align-items: end;
}

.home-side-sub {
    display: grid;
    gap: 20px;
}
    
.mid-pattern {
    width: 110px;
}
@media (prefers-reduced-motion: no-preference) {
    .mid-pattern {
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

.home-two {
    width: 110px;
}

.home-three {
    width: 200px;
}

.home-four {
    width: 256px;
}
</style>