<template>
    <main>
        <div class="main_up-section_container">
            <div class="main_up-section">
                Placeholder
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

export default {
    name: 'MainComponent',
}

</script>

<style lang="scss" scoped>
    main {
        display: flex;
        flex-direction: column;
        width: 100%;
        color: white;
        flex-grow: 1;
    }

    .main_up-section_container {
        background-color: var(--main-color);
        flex-grow: 1;
    }

    .main_down-section_container {
        background-color: var(--primary-color);
    }

    .main_up-section, .main_down-section {
        margin: auto;
        max-width: var(--container-md);
        padding: var(--container-md-padding);
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