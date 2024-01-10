<script>
export default {
    name: 'AppCardComic',
    props: {
        comic: Object
    }
}
</script>
<template lang="">
    <!-- tramite un v-for andremo ad inserire i fumetti con immagine e titolo  -->
    <div class="card" >
        <img :src="comic.thumb" alt="comic.series">
        <span class="comic-title">{{comic.series}}</span>
    </div>
</template>
<style lang="scss" scoped>
@use '../styles/partials/variables' as *;

.card {
    width: calc(100% / 6 - 20px);
    margin: 20px 10px;


    img {
        object-fit: cover;
        object-position: top;
        max-width: 180px;
        max-height: 180px;
        opacity: 0.7;
        cursor: pointer;
        transition: all 0.3s;
        margin-bottom: 5px;

        &:hover {
            opacity: 1;
            transform: scale(1.1);
        }
    }
}

.comic-title {
    text-transform: uppercase;
    font-size: 10px;
    font-weight: 200;
}
</style>