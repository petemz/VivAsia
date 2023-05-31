<template>
    <div class="pop-places">
        <div class="intro">
            <p>POPULAR</p>
            <h2>Places</h2>
            <p>take a glimpse of asia's <br /> popular places to visit</p>
        </div>

        
        <div class="places">
            <div class="place" v-for="place in places" v-bind:key="place.name">
                <div class="place-main">
                    <div class="location">
                        <p>{{ place.country }}</p>
                        <h3>{{ place.name }}</h3>
                    </div>
                    <img :src="require('../assets/Places/' + place.mainImg)" alt="">
                </div>
                <div class="place-side">
                    <img class="side-img" :src="require('../assets/Places/' + place.sideImg)" alt="">
                    <div class="place-desc">
                        <div >
                            <img class="mid-pattern" src="../assets/image.png" alt="">
                            <img class="mid-pattern" src="../assets/image.png" alt="">
                        </div>
                        <p>{{ place.description }}.</p>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script> 
export default {
    name: 'PlacesComp',
    data() {
        return {
            places: [
                {name: 'Fuji', country: 'Japan', description: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Atque ipsam quisquam commodi dicta expedita dolores id obcaecati consequuntur doloremque deserunt magnam repellat, quis quo adipisci perferendis ullam porro, vel ad. Lorem ipsum dolor sit amet consectetur adipisicing',
                mainImg: 'fuji-main.jpg', sideImg: 'fuji-side.jpg'
                },
                {name: 'Angkor Wat', country: 'Cambodia', description: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Atque ipsam quisquam commodi dicta expedita dolores id obcaecati consequuntur doloremque deserunt magnam repellat, quis quo adipisci perferendis ullam porro, vel ad. Lorem ipsum dolor sit amet consectetur adipisicing',
                mainImg: 'angkor-main.jpg', sideImg: 'angkor-side.jpg'
                },
                {name: 'Bali', country: 'Indonesia', description: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Atque ipsam quisquam commodi dicta expedita dolores id obcaecati consequuntur doloremque deserunt magnam repellat, quis quo adipisci perferendis ullam porro, vel ad. Lorem ipsum dolor sit amet consectetur adipisicing',
                mainImg: 'bali-main.jpg', sideImg: 'bali-side.jpg'
                },
                {name: 'Phuket', country: 'Thailand', description: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Atque ipsam quisquam commodi dicta expedita dolores id obcaecati consequuntur doloremque deserunt magnam repellat, quis quo adipisci perferendis ullam porro, vel ad. Lorem ipsum dolor sit amet consectetur adipisicing',
                mainImg: 'phuket-main.jpg', sideImg: 'phuket-side.jpg'
                },
                {name: 'Kuala Lumpur', country: 'Malaysia', description: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Atque ipsam quisquam commodi dicta expedita dolores id obcaecati consequuntur doloremque deserunt magnam repellat, quis quo adipisci perferendis ullam porro, vel ad. Lorem ipsum dolor sit amet consectetur adipisicing',
                mainImg: 'kuala-main.jpg', sideImg: 'kuala-side.jpg'
                }
            ]
        }
    }
}
</script>

<style scoped>
    .mid-pattern {
        width: 35px;
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
    .pop-places {
        height: 100%;
        padding-right: 120px;
        padding-left: 120px;
        width: max-content;
        display: flex;
        align-items: center;
    }

    .intro {
        height: 100%;
        display: flex;
        flex-direction: column;
        justify-content: center;
        margin-right: 65px;
    }

    .places {
        display: flex;
    }

    .place {
        display: grid;
        grid-template-columns: 310px 310px;
        gap: 20px;
        align-items: center;
        margin: auto 65px;
    }

    .place-main {
        display: flex;
        flex-direction: column;
        justify-content: center;
    }

    .place-main img {
        width: 310px;
    }

    .location {
        margin-bottom: 20px;
    }

    .location p {
        font-size: 12px;
        letter-spacing: 6px;
        margin: 5px;
    }

    .place-side {
        display: grid;
        align-items: center;
        gap: 10px;
        height: max-content;
        font-size: 13px;
        line-height: 20px;
    }

    .place-side .side-img {
       width: 200px;
       margin-bottom: 0px;
    }

    .place-desc {
        display: grid;
        grid-template-columns: 34px 1fr;
        gap: 20px;
        place-items: center;
    }

    .place-pattern {
        width: 40px;
        border-radius: 0px;
        height: max-content;
    }
</style>