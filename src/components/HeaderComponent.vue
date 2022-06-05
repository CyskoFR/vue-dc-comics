<template>
    <header>
        <div class="header_container">
            <div class="header_logo">
                <img src="../assets/img/dc-logo.png" alt="dc-logo.png">
            </div>
            <nav class="header_nav">
                <ul>
                    <li v-for="(link, i) in links" :key="i" :class="{active : link.current}"><a :href="link.url">{{link.text}}</a></li>
                </ul>
            </nav>
        </div>
    </header>
</template>

<script>

export default {
    name: 'HeaderComponent',
    data() {
        return {
            links: [
                {
                    text: "CHARACTERS",
                    url: "#",
                    current: false,
                },
                {
                    text: "COMICS",
                    url: "#",
                    current: true,
                },
                {
                    text: "MOVIES",
                    url: "#",
                    current: false,
                },
                {
                    text: "TV",
                    url: "#",
                    current: false,
                },
                {
                    text: "GAMES",
                    url: "#",
                    current: false,
                },
                {
                    text: "COLLECTIBLES",
                    url: "#",
                    current: false,
                },
                {
                    text: "VIDEOS",
                    url: "#",
                    current: false,
                },
                {
                    text: "FANS",
                    url: "#",
                    current: false,
                },
                {
                    text: "NEWS",
                    url: "#",
                    current: false,
                },
                {
                    text: "SHOP",
                    url: "#",
                    current: false,
                }
            ]
        }
    }
}

</script>

<style lang="scss" scoped>
    .header_container {
        display: flex;
        justify-content: space-between;
        padding: 8px 0;
        margin: auto;
        max-width: var(--container-md);

        .header_logo {
            display: flex;
            margin-left: 16px;
            height: 70px;
        }

        .header_nav {
            display: flex;
            ul {
                display: flex;
                list-style-type: none;
                li {
                    display: flex;
                    margin: 0.5rem;
                    a {
                        display: flex;
                        align-self: center;
                        text-decoration: none;
                        color: black;
                        font-weight: 600;
                    }
                }
            }
        }
        
        .active a {
            color: var(--primary-color);
        }
    }

</style>