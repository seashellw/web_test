<template>
<div id="app">
    <HelloWorld msg="Welcome to Your Vue.js App" />
</div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";

export default {
    name: "app",
    components: {
        HelloWorld,
    },
};
</script>

<style>
#app {
    color: #2c3e50;
}
</style>
