<template>
    <div id="places" class="places">
        <div class="places-intro">
            <p>POPULAR</p>
            <h2>Places</h2>
            <p>take a glimpse of asia's <br /> popular places to visit</p>
        </div>

        <div class="places-container">
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
                        <div>
                            <img class="mid-pattern" src="../assets/Home/pattern.jpg" alt="">
                            <img class="mid-pattern" src="../assets/Home/pattern.jpg" alt="">
                        </div>
                        <p>{{ place.description }}</p>
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
                {name: 'Fuji', country: 'Japan', description: 'Fuji, Japan\'s highest mountain, is a captivating tourist attraction known for its symmetrical beauty. Climbing its majestic peak offers breathtaking views, while the surrounding Fuji Five Lakes region provides cultural immersion and scenic exploration.',
                mainImg: 'fuji-main.jpg', sideImg: 'fuji-side.jpg'
                },
                {name: 'Angkor Wat', country: 'Cambodia', description: 'Angkor Wat is a temple complex in Cambodia. It is the largest religious monument in the world and is a UNESCO World Heritage Site. The temple was built in the 12th century by King Suryavarman II and is dedicated to the Hindu god Vishnu.',
                mainImg: 'angkor-main.jpg', sideImg: 'angkor-side.jpg'
                },
                {name: 'Bali', country: 'Indonesia', description: 'Bali, an Indonesian paradise, enchants visitors with its breathtaking beaches, vibrant culture, and lush landscapes. From ancient temples to vibrant markets and world-class surfing spots, Bali offers a blend of relaxation and adventure that leaves a lasting impression on all who visit.',
                mainImg: 'bali-main.jpg', sideImg: 'bali-side.jpg'
                },
                {name: 'Phuket', country: 'Thailand', description: 'Phuket, Thailand\'s tropical gem, beckons with its stunning beaches, crystal-clear waters, and vibrant nightlife. Whether you seek relaxation on the palm-fringed shores or adventure in the lush rainforests, Phuket offers an unforgettable escape into paradise.',
                mainImg: 'phuket-main.jpg', sideImg: 'phuket-side.jpg'
                },
                {name: 'Kuala Lumpur', country: 'Malaysia', description: 'Kuala Lumpur, Malaysia\'s bustling capital, captivates with its impressive skyline, vibrant street life, and rich cultural heritage. From towering skyscrapers to mouthwatering cuisine and lively markets, Kuala Lumpur offers an unforgettable fusion of modernity and tradition.',
                mainImg: 'kuala-main.jpg', sideImg: 'kuala-side.jpg'
                }
            ]
        }
    }
}
</script>

<style scoped>
    .places {
        height: 100%;
        padding: 0 110px;
        width: max-content;
        display: flex;
    }

    .places-intro {
        height: 100%;
        display: flex;
        flex-direction: column;
        justify-content: center;
        margin-right: 60px;
    }

    .places-container {
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
    }

    .location {
        margin-bottom: 20px;
    }
    .location p {
        letter-spacing: 6px;
        margin: 5px auto;
    }

    .place-side {
        display: grid;
        gap: 10px;
        line-height: 20px;
        margin-top: 20px;
    }

    .side-img {
       width: 200px;
    }

    .place-desc {
        display: grid;
        grid-template-columns: 34px 1fr;
        gap: 20px;
        place-items: center;
    }

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
</style>