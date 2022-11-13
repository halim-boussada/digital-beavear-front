<template>
    <div class="page">
        <div class="illustration">

        </div>
        <div class="card login">
            <div class=" form">
                <section>
                    <b-field label="Name">
                        <b-input value="Kevin Garvey"></b-input>
                    </b-field>

                    <b-field label="Email" type="is-danger" message="This email is invalid">
                        <b-input type="email" value="john@" maxlength="30">
                        </b-input>
                    </b-field>

                    <b-field label="Username" type="is-success" message="This username is available">
                        <b-input value="johnsilver" maxlength="30"></b-input>
                    </b-field>

                    <b-field label="Password" type="is-warning"
                        :message="['Password is too short', 'Password must have at least 8 characters']">
                        <b-input value="123" type="password" maxlength="30"></b-input>
                    </b-field>

                    <b-field label="Subject">
                        <b-select placeholder="Select a subject">
                            <option value="1">Option 1</option>
                            <option value="2">Option 2</option>
                        </b-select>
                    </b-field>
                    <b-button type="is-primary">Primary</b-button>
                </section>
            </div>
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

.login {
    display: flex;
    flex-direction: column;
    justify-content: space-around;
}

.illustration {
    background-color: $primary;
}

.form {
    display: flex;
    flex-direction: row;
    justify-content: space-around;
}
</style>