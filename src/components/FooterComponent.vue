<template>
    <footer>
        <div class="footer_up-section_container">
            <div class="footer_up-section">
                <nav>
                    <ul>DC COMICS
                        <li><a href="#">Characters</a></li>
                        <li><a href="#">Comics</a></li>
                        <li><a href="#">Movies</a></li>
                        <li><a href="#">TV</a></li>
                        <li><a href="#">Games</a></li>
                        <li><a href="#">Videos</a></li>
                        <li><a href="#">News</a></li>
                    </ul>
                    <ul>SHOP
                        <li><a href="#">Shop DC</a></li>
                        <li><a href="#">Shop DC collectibles</a></li>
                    </ul>
                    <ul>DC
                        <li><a href="#">Terms Of Use</a></li>
                        <li><a href="#">Privacy Policy (New)</a></li>
                        <li><a href="#">Ad Choices</a></li>
                        <li><a href="#">Advertising</a></li>
                        <li><a href="#">Jobs</a></li>
                        <li><a href="#">Subscriptions</a></li>
                        <li><a href="#">Talent Workshops</a></li>
                        <li><a href="#">CPSC Certificates</a></li>
                        <li><a href="#">Ratings</a></li>
                        <li><a href="#">Shop Help</a></li>
                        <li><a href="#">Contact Us</a></li>
                    </ul>
                    <ul>SITES
                        <li><a href="#">DC</a></li>
                        <li><a href="#">MAD Magazine</a></li>
                        <li><a href="#">DC Kids</a></li>
                        <li><a href="#">DC Universe</a></li>
                        <li><a href="#">DC Power Visa</a></li>
                    </ul>
                </nav>
                <img class="dc-logo-bg" src="../assets/img/dc-logo-bg.png" alt="dc-logo-bg.png">
            </div>
        </div>
        <div class="footer_down-section_container">
            <div class="footer_down-section">
                <a class="footer_button" href="#">SIGN-UP NOW!</a>
                <div class="social-box">
                    <a href="#">FOLLOW US</a>
                    <a href="#"><img src="../assets/img/footer-facebook.png" alt="footer-facebook.png"></a>
                    <a href="#"><img src="../assets/img/footer-twitter.png" alt="footer-twitter.png"></a>
                    <a href="#"><img src="../assets/img/footer-youtube.png" alt="footer-youtube.png"></a>
                    <a href="#"><img src="../assets/img/footer-pinterest.png" alt="footer-pinterest.png"></a>
                    <a href="#"><img src="../assets/img/footer-periscope.png" alt="footer-periscope.png"></a>
                </div>
            </div>
        </div>
    </footer>
</template>

<script>
export default {
    name: 'FooterComponent',
}
</script>

<style lang="scss" scoped>
    .footer_up-section_container {
        width: 100%;
        background-image: url(../assets/img/footer-bg.jpg);
        background-position: center;
        background-size: cover;
    }

    .footer_up-section{
        position: relative;
        overflow: hidden;
    }
    
    .dc-logo-bg {
        position: absolute;
        right: 0%;
        top: -50%;
        transform: translate(0 , 10%);
    }

    .footer_up-section, .footer_down-section {
        margin: auto;
        max-width: var(--container-md);
        padding: var(--container-md-padding);
    }

    .footer_up-section nav {
        display: flex;
        gap: 32px;
        ul {
            color: white;
            list-style-type: none;
            font-weight: 600;

            :first-child {
                margin-top: 10px;
            }

            li {
                margin-bottom: 4px;
            }

            a{
                text-decoration: none;
                color: grey;
                font-size: .75rem;
            }
        }
    }

    .footer_down-section_container {
        background-color: var(--footer-color);
    }

    .footer_down-section {
        display: flex;
        justify-content: space-between;
        .footer_button {
            color: white;
            border: 1px solid var(--primary-color);
            padding: 12px;
            text-decoration: none;
            &:hover {
                background-color: var(--primary-color);
            }
        }
        .social-box {
            display: flex;
            align-items: center;
            a {
                color: var(--primary-color);
                text-decoration: none;
                margin: 0 10px;
            }
        }
    }


</style>