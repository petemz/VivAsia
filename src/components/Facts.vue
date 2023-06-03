<template >
    <div class="facts">
        <div class="facts-intro">
            <h2>Travel Facts <br/> About <span>Asia</span></h2>
        </div>

        <div class="facts-container">
            <div class="fact fact-1">
                <p>Asia is the largest continent on Earth, covering about 30% of the land area.</p>
            </div>
            <div class="fact fact-2">
                <p>Asia is home to over 4.6 billion people, representing about 60% of the global population.</p>
            </div>
            <div class="fact fact-3">
                <p>Asia is home to some of the world's most beautiful and diverse landscapes, including mountains, deserts, forests, and beaches.</p>
            </div>
            <div class="fact fact-4">
                <p>Asia is a major tourist destination, with millions of visitors each year.</p>
            </div>
            <div class="fact fact-5">
                <p>Asia is a major tourist destination, with millions of visitors each year.</p>
            </div>
            <div class="fact fact-6">
                <p>Asia is a continent of great contrast, from the bustling cities of Tokyo and Shanghai to the tranquil villages of rural Laos.</p>
            </div>
            <div class="fact fact-7">
                <p>Asia is home to some of the world's oldest civilizations, including China, India, and Japan.</p>
            </div>
            <img class="pattern pt-1" src="../assets/Home/pattern.jpg" alt="">
            <img class="pattern pt-2" src="../assets/Home/pattern.jpg" alt="">
            <img class="pattern pt-3" src="../assets/Home/pattern.jpg" alt="">
            <img class="pattern pt-4" src="../assets/Home/pattern.jpg" alt="">
            <img class="pattern pt-5" src="../assets/Home/pattern.jpg" alt="">
            <img class="pattern pt-6" src="../assets/Home/pattern.jpg" alt="">
            <img class="pattern pt-7" src="../assets/Home/pattern.jpg" alt="">
            <img class="pattern pt-8" src="../assets/Home/pattern.jpg" alt="">
            <img class="pattern pt-9" src="../assets/Home/pattern.jpg" alt="">
        </div>
        
        <div class="facts-outro">
            <p id="outro">you've reached <br/> the end of this <br/>
                <span id="exp">experi- <br/> ence</span>
            </p>

            <p id="greetings">MADE WITH LOVE <br/> IN LAGOS, NIGERIA</p>
            <p id="adeola">Inspired by Adeola Adeoti</p>
        </div>
    </div>
</template>

<style scoped>
.facts {
    flex-shrink: 0;
    display: flex;
}

.facts-intro {
    display: flex;
    flex-direction: column;
    justify-content: center;
    margin-right: 20px;
    padding-bottom: 140px;
}
.facts-intro h2 {  
    color: #8b8b8b;
    font-size: 65px;
    letter-spacing: -3px;
}
.facts-intro span {
    color: white;
}
.facts-container {
    width: 1350px;
    height: 470px;
    position: relative;
    color: black;
    padding: 0 110px;
    margin: auto 110px;
}

.fact {
    background-image: url(../assets/steps.png);
    width: 330px;
    height: 110px;
    background-size: contain;
    display: flex;
    align-items: center;
    position: absolute;
    overflow: hidden;
}

.fact p {
    font-weight: 600;
    margin-left: 15px;
    margin-right: 85px;
}

.fact-1 {
    top: 100px;
    left: 10px;
}
.fact-2 {
    top: 10px;
    left: 460px;
}
.fact-3 {
    top: 60px;
    right: 150px;
}
.fact-5 {
    bottom: 50px;
    left: 230px;
}
.fact-7 {
    bottom: 100px;
    right: 0;
}
.fact-4 {
    bottom: 190px;
    left: 630px;
}
.fact-6 {
    bottom: 10px;
    right: 390px;
}

.pattern {
    width: 50px;
    height: 50px;
    position: absolute;
    margin: 5px 15px;
}
@media (prefers-reduced-motion: no-preference) {
  .pattern {
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

.pt-1 {
    top: 30px;
    left: 30px;
}
.pt-2 {
    top: 60px;
    right: 700px;
}
.pt-3 {
    right: 340px;
}
.pt-4 {
    left: 400px;
    top: 200px;
}
.pt-5 {
    top: 240px;
    right: 510px;
}
.pt-6 {
    right: 100px;
    top: 185px;
}
.pt-7 {
    bottom:  20px;
    left: 120px;
}
.pt-8 {
    left: 670px;
    bottom: 50px;
}
.pt-9 {
    right: 300px;
    top: 390px;
}

.facts-outro {   
    display: flex;
    flex-direction: column;
    justify-content: center;
    margin-right: 20px;
    font-size: 14px;
    line-height: 17px;
    margin-left: 90px;
    margin-right: 1100px;
    padding-top: 170px;
}

.facts-outro span {
    color: white;
    line-height: 50px;
    letter-spacing: -3px;
}

#outro {
    margin-bottom: 40px;
}

#exp {
    font-size: 60px;
    font-weight: bolder;
    color: white;
    margin-bottom: 50px;
}

#greetings {
    color: green;
    letter-spacing: 5px;
    font-size: 10px;
    font-weight: bold;
}

#adeola {
    font-style: italic;
    font-size: 13px;
}
</style>