<script>
export default {
    name: 'AppBuyProduct',
    data() {
        return {
            sections: [
                {
                    label: 'DIGITAL COMICS',
                    img: 'buy-comics-digital-comics.png'
                },
                {
                    label: 'DC MERCHANANDISE',
                    img: 'buy-comics-merchandise.png'
                },
                {
                    label: 'SUBSCRIPTION',
                    img: 'buy-comics-subscriptions.png'
                },
                {
                    label: 'COMIC SHOP LOCATOR',
                    img: 'buy-comics-shop-locator.png'
                },
                {
                    label: 'DC POWER VISA',
                    img: 'buy-dc-power-visa.svg'
                },
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
    <section class="buyProduct">
        <div class="contentBuyProduct">
            <ul>
                <li v-for="(section, index) in sections" :key="index">
                    <a>
                        <img :src="getImagePath(`../assets/img/${section.img}`)" alt="/">
                        <span class="label">{{section.label}}</span>
                    </a>
                </li>
            </ul>
        </div>
    </section>
</template>
<style lang="scss">
@use '../styles/partials/variables' as *;

.buyProduct {
    background: $brand_primary;
    height: 150px;
    position: relative;
    z-index: 1;


    ul {
        display: flex;
        list-style: none;
        height: 100%;
        justify-content: space-around;
        align-items: center;

        li a {
            display: flex;
            align-items: center;
        }
    }

    img {
        max-width: 50px;
    }
}

.contentBuyProduct {
    max-width: 1200px;
    margin: 0 auto;
    height: 100%;
}

.label {
    color: white;
    font-size: 13px;
    margin: 15px;
    font-weight: 400;
}
</style>