<script>
export default {
    name: 'AppHeader',
    data() {
        return {
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
            <a href="#" class="logo">
                <img src="../assets/img/dc-logo.png">
            </a>
            <nav>
                <ul>
                    <li v-for="(link, index) in links" :key="index">
                        <a :class="link.active ? 'active' : ''" :href="link.url">
                            {{link.label}}
                        </a>
                    </li>
                </ul>
            </nav>
        </div>
    </header>
</template>
<style>
ul {
    display: flex;
    list-style: none;
}

a {
    padding: 1rem;
    text-decoration: none;
    font-size: 14px;
    align-items: center;
    color: black;
    display: flex;
}

.containerHeader {
    display: flex;
    max-width: 1200px;
    margin: 0 auto;
    justify-content: space-between;
}

img {
    max-width: 80%;
}
</style>