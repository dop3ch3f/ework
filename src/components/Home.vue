<template v-if="$route.name !== 'Home'">
    <section class="hero is-dark is-fullheight ">
        <!-- Hero head: will stick at the top -->
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

                    <div class="navbar-end"></div>
                </div>
            </header>
        </div>

        <!-- Hero content: will be in the middle -->
        <div class="hero-body">
            <div class="container has-text-centered">
                <h1 class="is-size-2">
                    Welcome to eWork.Ng
                </h1>
                <br/>
                <div class="card" id="cover">
                    <div class="card-content">
                        <h1 class="is-dark is-size-4">
                            Your Uber for Brown-Collar Jobs
                        </h1>
                        <h2 class="is-text">Lorem ipsum dolor sit amet,
                            consectetur adipisicing elit. At autem blanditiis debitis eligendi
                            eos est, et, ex expedita facere iure minima molestiae nemo neque perferendis
                            quia, quis sequi tempora totam?</h2>
                        <br/>
                        <div class="columns">
                            <div class="column">
                                <router-link to="/login">
                                    <button class="button is-success">Login</button>
                                </router-link>
                            </div>
                            <div class="column">
                                <router-link to="/signup">
                                    <button class="button is-success">Signup</button>
                                </router-link>
                            </div>
                        </div>
                    </div>
                </div>

            </div>
        </div>

        <!-- Hero footer: will stick at the bottom -->
        <div class="hero-foot">
            <p class="is-size-7">&copy;{{year}} powered by Evicon.io</p>
        </div>
    </section>
</template>
<script>
    export default {
        name: 'Home',
        data: function () {
            var date = new Date();
            return {
                year: date.getFullYear(),
            }
        }
    }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    section {

    }
</style>
