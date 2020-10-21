<template>
<div class="hello">
    <h1>{{ msg }}</h1>
</div>
</template>

<script>
export default {
    name: "HelloWorld",
    props: {
        msg: String,
    },
    data() {
        return {
            name: "seashellw",
        };
    },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->

<style scoped>
a {
    color: #42b983;
}
</style>
