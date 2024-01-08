<script>
export default {

}
</script>
<template lang="">
    <footer>
        <div class="footerUp">
            <div class="contentFooterUp">

            </div>
        </div>
        <div class="footerDown">
            <div class="contentFooterDown">

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
    height: 100px;
}

.contentFooterUp,
.contentFooterDown {
    max-width: 1200px;
}
</style>