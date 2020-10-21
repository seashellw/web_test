<template>
<div>
    <el-container>
        <el-header class="el_header_style">{{ header }}</el-header>
        <el-main>main </el-main>
        <el-footer class="el_footer_style">footer</el-footer>
    </el-container>
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
            header: "hhhhhhhhh",
        };
    },
    computed: {},
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->

<style>
.el_header_style {
    background-color: aquamarine;
}

.el_footer_style {
    background-color: aquamarine;
}
</style>
