<script>
export default {
    name: 'AppFooter',

    data() {
        return {
            links: [
                {
                    img: 'footer-facebook.png',
                    url: '#',
                },
                {
                    img: 'footer-twitter.png',
                    url: '#',
                },
                {
                    img: 'footer-youtube.png',
                    url: '#',
                },
                {
                    img: 'footer-pinterest.png',
                    url: '#',
                },
                {
                    img: 'footer-periscope.png',
                    url: '#',
                }
            ]
        }
    },
    methods: {
        getImagePath(imgPath) {
            return new URL(imgPath, import.meta.url).href;
        }
    }
}
</script>
<template lang="">
    <footer>
        <div class="footerUp">
            <div class="contentFooterUp">
                <div class="footerLinks">
                    QUI CI VANNO I LINK DA CREARE COL V-FOR
                        
                </div>
                <div class="footerLogo">
                    <img src="../assets/img/dc-logo-bg.png" alt="">
                </div>
            </div>
        </div>
        <div class="footerDown">
            <div class="contentFooterDown">
                <div>
                    <button>SIGN-UP NOW!</button>
                </div>
                <div class="followLinks">
                    <div class="followUs">FOLLOW US</div>
                    <ul>
                        <li v-for="(link, index) in links" :key="index">
                            <a :href="link.url">
                                <img :src="getImagePath(`../assets/img/${link.img}`)" alt="/">
                            </a>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </footer>
</template>
<style lang="scss" scoped>
@use '../styles/partials/variables' as *;

.footerUp {
    height: 350px;
    background-image: url('../assets/img/footer-bg.jpg');
    background-repeat: no-repeat;
    background-size: cover;
}

.footerDown {
    background-color: $secondary_color;
    height: 110px;
    position: relative;
    z-index: 99999;

}

.contentFooterUp,
.contentFooterDown {
    max-width: 1200px;
    display: flex;
    margin: 0 auto;
    justify-content: space-between;
    align-items: center;
    height: 100%;
}

img {
    position: relative;
    bottom: 20%;
}

button {
    border: 2px solid $brand_primary;
    background-color: transparent;
    color: #fff;
    padding: 0.8rem;
    font-weight: 500;
    font-size: 16px;
}

.followLinks {
    display: flex;
    align-items: center;
}

.followUs {
    color: $brand_primary;
    font-weight: bold;
    margin: 15px;
}

ul {
    display: flex;
    list-style: none;
    height: 100%;
    align-items: center;

    li {
        margin: 10px;
    }
}
</style>