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
            ],
            dc_comics_menu: [
                {
                    label: 'Characters',
                    url: '#'
                },
                {
                    label: 'Comics',
                    url: '#'
                },
                {
                    label: 'Movies',
                    url: '#'
                },
                {
                    label: 'TV',
                    url: '#'
                },
                {
                    label: 'Games',
                    url: '#'
                },
                {
                    label: 'Videos',
                    url: '#'
                },
                {
                    label: 'News',
                    url: '#'
                }
            ],
            shop_menu: [
                {
                    label: 'Shop DC',
                    url: '#'
                },
                {
                    label: 'Shop DC Collectibles',
                    url: '#'
                }
            ],
            dc_menu: [
                {
                    label: 'Terms of Use',
                    url: '#'
                },
                {
                    label: 'Privacy policy (New)',
                    url: '#'
                },
                {
                    label: 'Ad Choices',
                    url: '#'
                },
                {
                    label: 'Advertising',
                    url: '#'
                },
                {
                    label: 'Jobs',
                    url: '#'
                },
                {
                    label: 'Subscriptions',
                    url: '#'
                },
                {
                    label: 'Talent Workshops',
                    url: '#'
                },
                {
                    label: 'CPSC Certificates',
                    url: '#'
                },
                {
                    label: 'Ratings',
                    url: '#'
                },
                {
                    label: 'Shop Help',
                    url: '#'
                },
                {
                    label: 'Contact Us',
                    url: '#'
                }
            ],
            sites_menu: [
                {
                    label: 'DC',
                    url: '#'
                },
                {
                    label: 'MAD Magazine',
                    url: '#'
                },
                {
                    label: 'DC Kids',
                    url: '#'
                },
                {
                    label: 'DC Universe',
                    url: '#'
                },
                {
                    label: 'DC Power Visa',
                    url: '#'
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
        <!-- Top del footer  -->
        <div class="footerUp">
            <div class="contentFooterUp">
                <div class="footerLinks">
                    <!-- Menù con i link nel footer con sfondo -->
                    <div class="menu">
                        <h3>DC COMICS</h3>
                        <ul>
                            <li v-for="(link, index) in dc_comics_menu" :key="index">
                                <a :href="link.url">{{link.label}}</a>
                            </li>
                        </ul>
                        <h3 id="shop-label">SHOP</h3>
                        <ul>
                            <li v-for="(link, index) in shop_menu" :key="index">
                                <a :href="link.url">{{link.label}}</a>
                            </li>
                        </ul>
                    </div>
                    <div class="menu">
                        <h3>DC</h3>
                        <ul>
                            <li v-for="(link, index) in dc_menu" :key="index">
                                <a :href="link.url">{{link.label}}</a>
                            </li>
                        </ul>
                    </div>
                    <div class="menu">
                        <h3>SITES</h3>
                        <ul>
                            <li v-for="(link, index) in sites_menu" :key="index">
                                <a :href="link.url">{{link.label}}</a>
                            </li>
                        </ul>
                    </div>
                </div>
                <div class="footerLogo">
                    <img src="../assets/img/dc-logo-bg.png" alt="DC Comics">
                </div>
            </div>
        </div>
        <!-- Bottom del footer  -->
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

    .footerLinks {
        display: flex;

        h3 {
            color: white;
        }

        .menu {
            margin: 0px 20px;

            ul {
                display: block;

                li {
                    font-size: 12px;
                    margin: 6px 0;

                    a {
                        color: #b6b6b6;
                    }
                }
            }

            h3 {
                margin: 20px 0;
            }
        }
    }
}

.footerDown {
    background-color: $secondary_color;
    height: 110px;
    position: relative;
    z-index: 99999;

    button {
        border: 2px solid $brand_primary;
        background-color: transparent;
        color: #fff;
        padding: 0.8rem;
        font-weight: 500;
        font-size: 16px;
    }
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
    align-items: center;

    li {
        margin: 10px;
    }
}
</style>