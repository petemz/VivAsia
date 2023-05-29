<template>
    <div class="pop-places">
        <div class="intro">
            <p>POPULAR</p>
            <h2>Places</h2>
            <p>take a glimpse of asia's <br /> popular places to visit</p>
        </div>

        <div class="place">
            <div class="place-main">
                <div class="location">
                    <p>EGYPT</p>
                    <h3>CAIRO</h3>
                </div>
                <img src="../assets/Places/fuji-main.jpg" alt="">
            </div>
            <div class="place-side">
                <img class="side-img" src="../assets/Places/fuji-side.jpg" alt="">
                <div>
                    <img class="place-pattern" src="../assets/place-pattern1.jpg" alt="">
                    <p></p>
                </div>
            </div>
        </div>
    </div>
</template>

<script> 
export default {
  name: 'HomeGrid'
}
</script>

<style scoped>
    .pop-places {
        height: 100%;
        padding-right: 120px;
        padding-left: 120px;
        width: max-content;
        display: flex;
    }

    .intro {
        height: 100%;
        display: flex;
        flex-direction: column;
        justify-content: center;
        margin-right: 135px;
    }

    .place {
        display: grid;
        grid-template-columns: 1fr 1fr;
        gap: 20px;
    }

    .place-main img {
        width: 310px;
    }

    .place-side {
    }

    .place-side .side-img {
       width: 200px;
    }

    .location {
        margin-bottom: 20px;
    }

    .location p {
        font-size: 12px;
        letter-spacing: 6px;
        margin: 5px;
    }

    .place-pattern {
        width: 70px;
        background-color: blue;
        border-radius: 0px;
    }
</style>