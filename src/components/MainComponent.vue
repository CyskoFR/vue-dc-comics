<template>
    <main>
        <div class="main-jumbo"></div>
        <div class="main_up-section_container">
            <div class="main_up-section">
                <h2 class="main-title">CURRENT SERIES</h2>
                <div class="card" v-for="(card, i) in cards" :key="i">
                    <div class="card-img" :style="{ backgroundImage: 'url(' + card.thumb + ')' }">
                    </div>
                    <p>{{card.series}}</p>
                </div>
                <a class="main-button" href="#">LOAD MORE</a>
            </div>
        </div>
        <div class="main_down-section_container">
            <div class="main_down-section">
                <a href="#"><img src="../assets/img/buy-comics-digital-comics.png" alt="">DIGITAL COMICS</a>
                <a href="#"><img src="../assets/img/buy-comics-merchandise.png" alt="">DC MERCHANDISE</a>
                <a href="#"><img src="../assets/img/buy-comics-subscriptions.png" alt="">SUBSCRIPTION</a>
                <a href="#"><img src="../assets/img/buy-comics-shop-locator.png" alt="">COMIC SHOP LOCATOR</a>
                <a href="#"><img src="../assets/img/buy-dc-power-visa.svg" alt="">DC POWER VISA</a>
            </div>
        </div>
    </main>
</template>

<script>

import json from '../assets/dc-comics.json';

export default {
    name: 'MainComponent',
    data() {
        return {
            cards: json,
        }
    }
}

</script>

<style lang="scss" scoped>
    main {
        display: flex;
        flex-direction: column;
        width: 100%;
        color: white;
    }

    .main-jumbo {
        background-image: url(../assets/img/jumbotron.jpg);
        background-size: cover;
        height: 400px;
    }

    .main_up-section_container {
        background-color: var(--main-color);
        flex-grow: 1;
    }

    .main_up-section, .main_down-section {
        margin: auto;
        max-width: var(--container-md);
        padding: var(--container-md-padding);
    }

    .main_up-section {
        position: relative;
        display: flex;
        flex-wrap: wrap;
        justify-content: center;
        padding: 40px 0;

        .main-title {
            position: absolute;
            top: -16px;
            left: 50px;
            display: inline-block;
            color: white;
            background-color: var(--primary-color);
            font-size: 1rem;
            padding: 8px 14px;
        }

        .card {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-items: baseline;
            width: 15%;

            img, p {
                width: 90%;
            }

            p {
                text-transform: uppercase;
                font-size: .875rem;
                margin: 10px 0;
            }

        }

        .card-img {
            height: 160px;
            width: 90%;
            background-size: cover;
        }

        .main-button {
            position: absolute;
            bottom: 20px;
            background-color: var(--primary-color);
            color: white;
            text-decoration: none;
            font-size: .75rem;
            padding: 6px 48px;
        }

    }

    .main_down-section_container {
        background-color: var(--primary-color);
    }

    .main_down-section {
        display: flex;

        a {
            display: flex;
            align-items: center;
            margin: 0 20px;
            text-decoration: none;
            color: white;
        }

        img {
            height: 40px;
            margin-right: 12px;
        }

    }
    
</style>