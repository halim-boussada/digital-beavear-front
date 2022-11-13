<template>
        <div class="card card__button is-primary">
            <div class="card-content">
                <div class="content has-text-centered">
                    <slot />
                </div>
            </div>
        </div>
</template>
  
<script>
export default {
    name: 'Project',
    props: {
        name: {
            type: String,
        },
    }
}
</script>
<style lang="scss" scoped>
@import "~/assets/css/main.scss";
.card__button {
    display: flex;
    flex-direction: column;
    justify-content: space-around;
    align-items: center;
    align-content: center;
    height: 100%;
    background-color: $primary;
}
</style>