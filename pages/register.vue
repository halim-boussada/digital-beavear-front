<template>
    <div class="page">

        <div class=" card login">

        </div>
        <div class="illustration">

        </div>
    </div>

</template>
  
<script>
import Card from '~/components/Card'

export default {
    name: 'LoginPage',
    layout: '',
    components: {
        Card
    }

}
</script>
<style lang="scss">
@import "~/assets/css/main.scss";

.page {
    display: flex;
    flex-direction: row;
    width: 100%;
    height: 100vh;
}

.illustration,
.login {
    width: 50%;
}

.illustration {
    background-color: $primary;
}
</style>