<script>
</script>

<div class="container">
    <slot />
</div>

<style lang="scss">
    @import "../scss/mixins.scss";

    .container {
        @include container-padding-x();
        @include container-max-width(1400px);
    }
</style>
