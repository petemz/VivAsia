<template>
    <div class="two">  
        <div class="home-left">
            <img class="home-main" src="../assets/leon-buter-i0YR9Hn7vQI-unsplash.jpg" alt="Wildlife Elephant"/>
        </div>
      
      
        <div class="home-right">
            <div class="home-right-top">
                <div class="home-right-sub">
                    
                    <img class="home-two" src="../assets/vitor-monthay-z4LFpUS37k8-unsplash.jpg" alt="">
                    
                        
                    <div class="mid-pattern">
                        <img src="../assets/image.png" alt="">
                    </div>
                </div>

                <img class="home-three" src="../assets/home-three.jpg" alt="">
            </div>

            <img class="home-four" src="../assets/home-four.jpg" alt="Vue logo"/>
                
        </div>
    </div>
</template>

<script> 
export default {
  name: 'HomeGrid'
}
</script>

<style scoped>
    .two {
        height: 100%;
        padding-right: 120px;
        padding-left: 120px;

        width: max-content;
        display: grid;
        grid-template-columns: 310px 350px;
        align-items: center;
        column-gap: 25px;
    }

    .two img{
        border-radius: 20px;
    }

    .two .home-left {
        width: 310px;
        height: 420px;
        border-radius: 20px;
    }
    
    .two .home-main {
        width: 100%;
        height: 100%;
        object-fit: cover;
    }

    .two .home-right {
        display: grid;
        row-gap: 25px;
    }

    .two .home-right-top {
        width: max-content;
        display: grid;
        grid-template-columns: 110px 210px;
        gap: 25px;
        align-items: end;
    }
    
    .home-right-sub {
        display: grid;
        gap: 20px;
        align-items: end;
    }

    .two .home-two {
        width: 110px;
        height: 125px;
        border-radius: 20px;
        overflow: hidden;
    }

    .mid-pattern {
    }
    
    .mid-pattern img {
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

    .home-three {
        width: 200px;
    }

    .two .home-four {
        height: 195px;
    }

</style>