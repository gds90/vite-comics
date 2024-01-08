<script>
export default {
    name: 'AppMain',
    data() {
        return {

        }
    }
}
</script>
<template lang="">
    <main>
        <div class="containerMain comics">
            <!-- tramite un v-for andremo ad inserire i fumetti con immagine e titolo  -->
            <div>--> Content goes here <--</div>
        </div>
    </main>
</template>
<style>
main {
    background-color: black;
}

.containerMain {
    max-width: 1200px;
    margin: 0 auto;
    height: 150px;
    color: white;
    font-weight: 800;
}
</style>