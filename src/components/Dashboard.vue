<template v-if="$route.name !== 'Dashboard'">
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
                </div>
            </header>
        </div>

        <!-- Hero content: will be in the middle -->
        <div class="hero-body">
            <div class="container has-text-centered">
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
  name: "Dashboard",
  data() {
    return {

    }
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
