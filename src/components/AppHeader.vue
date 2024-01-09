<script>
export default {
    name: 'AppHeader',
    data() {
        return {
            // Array contenente i link del nav
            links: [
                {
                    label: 'CHARACTERS',
                    url: '#',
                    active: false
                },
                {
                    label: 'COMICS',
                    url: '#',
                    active: true
                },
                {
                    label: 'MOVIES',
                    url: '#',
                    active: false
                },
                {
                    label: 'TV',
                    url: '#',
                    active: false
                },
                {
                    label: 'GAMES',
                    url: '#',
                    active: false
                },
                {
                    label: 'COLLECTIBLES',
                    url: '#',
                    active: false
                },
                {
                    label: 'VIDEOS',
                    url: '#',
                    active: false
                },
                {
                    label: 'FANS',
                    url: '#',
                    active: false
                },
                {
                    label: 'NEWS',
                    url: '#',
                    active: false
                },
                {
                    label: 'SHOP',
                    url: '#',
                    active: false
                }
            ]
        }
    }
}
</script>
<template lang="">
    <header>
        <div class="containerHeader">
            <div class="navbar">
                <!-- Logo DC -->
                <a href="#" class="logo">
                    <img src="../assets/img/dc-logo.png" alt="DC Comics">
                </a>
                <!-- Nav  -->
                <nav>
                    <ul>
                        <!-- V-For per ciclare l'array dei link  -->
                        <li v-for="(link, index) in links" :key="index">
                            <a :class="link.active ? 'active' : ''" :href="link.url">
                                {{link.label}}
                            </a>
                        </li>
                    </ul>
                </nav>
            </div>
        </div>
    </header>
</template>
<style lang="scss" scoped>
@use '../styles/partials/variables' as *;


.containerHeader {
    max-width: 1200px;
    margin: 0 auto;

    .navbar {
        display: flex;
        justify-content: space-between;

    }

    ul {
        display: flex;
        list-style: none;
        height: 100%;
        align-items: center;
    }

    a {
        padding: 1rem;
        font-size: 12px;
        font-weight: 600;
        color: $secondary_color;
        position: relative;

        &.active,
        &:hover {
            color: $brand_primary;

            &::after {
                content: '';
                position: absolute;
                bottom: 0;
                left: 15px;
                width: calc(100% - 30px);
                height: 5px;
                background-color: $brand_primary;
            }
        }


        img {
            max-width: 80%;
        }
    }

}
</style>

