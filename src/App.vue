<template>
    <div id="app">
        <router-view></router-view>
    </div>
</template>

<script>
    export default {
        name: "App",
        data : function(){
            var date =  new Date();
            return {
                year : date.getFullYear(),
            }
        },
    };
</script>

<style>
    #app {
        font-family: "Avenir", Helvetica, Arial, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        text-align: center;
        color: #2c3e50;
    }
    button {
        background-color: #c4702e !important;
        width: 50%;
        border: none;
    }
    #cover {
        background-color: whitesmoke;
        border-radius: 5px;
    }
    #cover h1 {
        color: #4a4a4a;
    }
</style>