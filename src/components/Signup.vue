<template v-if="$route.name !== 'Signup'">
    <section class="hero is-dark is-fullheight">
        <div class="hero-head">
            <header class="navbar">
                <div class="container">
                    <div class="navbar-brand">
                        <a class="navbar-item">
                            <router-link to="/">
                                <h1 class="is-size-6">eWork</h1>
                            </router-link>
                        </a>

                    </div>
                </div>
            </header>
        </div>
        <div class="hero-body">
            <div class="container">
                        <div class="columns">
                            <div class="column is-6 is-offset-3 has-text-centered" id="cover">
                                <h1 class="is-black is-size-4">Setup Account</h1>
                                <br/>
                                <p class="help is-danger" v-if="error.phone || error.password">Username/Password
                                    incorrect</p>

                                <div class="field has-addons">
                                    <p class="control"><a class="button is-static">
                                        +234
                                    </a></p>
                                    <p class="control is-expanded">
                                        <input id="phone" class="input" type="text" v-model="form.phone"
                                               placeholder="Phone"/>
                                    </p>
                                </div>
                                <div class="field">
                                    <div class="control has-icons-left has-icons-right">
                                        <input class="input" id="password" v-model="form.password" type="password"
                                               placeholder="Password"/>
                                    </div>
                                </div>
                                <button class="button is-centered is-success">Signup</button>
                            </div>
                        </div>
                    </div>
        </div>
        <div class="hero-foot">
            <p class="is-size-7">&copy;{{year}} powered by Evicon.io</p>
        </div>
    </section>
</template>

<script>
    export default {
        name: "Signup",
        data: function () {
            var date = new Date();
            return {
                year: date.getFullYear(),
                form: {
                    phone: "",
                    password: ""
                },
                error: {
                    phone: false,
                    password: false
                }
            };
        },
        methods: {
            tryLogin() {
                this.resetErrors();

                if (this.form.email !== "test@kini") {
                    return (this.error.email = true);
                }
                if (this.form.password !== "password") {
                    return (this.error.password = true);
                }

                this.resetErrors();
                this.$router.push("dashboard");
            },
            resetErrors() {
                this.error.email = false;
                this.error.password = false;
            }
        }
    };
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
