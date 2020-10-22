<template>
<el-backtop target=".page-component__scroll .el-scrollbar__wrap"></el-backtop>
<div>
    <el-container>
        <el-header>
            <el-menu :default-active="activeIndex" class="el-menu-demo" mode="horizontal" @select="handleSelect">
                <el-menu-item><i class="el-icon-eleme" @click="icon_on_click"></i></el-menu-item>
                <el-menu-item :style="el_menu_item_right_style">
                    <el-button type="primary" class="button_top_style" icon="el-icon-search" plain>搜索</el-button>
                </el-menu-item>
                <el-menu-item index="1" :style="el_menu_item_right_style">处理中心</el-menu-item>
                <el-submenu index="2" :style="el_menu_item_right_style">
                    <template slot="title">我的工作台</template>
                    <el-menu-item index="2-1">选项1</el-menu-item>
                    <el-menu-item index="2-2">选项2</el-menu-item>
                    <el-menu-item index="2-3">选项3</el-menu-item>
                    <el-submenu index="2-4">
                        <template slot="title">选项4</template>
                        <el-menu-item index="2-4-1">选项1</el-menu-item>
                        <el-menu-item index="2-4-2">选项2</el-menu-item>
                        <el-menu-item index="2-4-3">选项3</el-menu-item>
                    </el-submenu>
                </el-submenu>
            </el-menu>
        </el-header>
        <el-main>main </el-main>
        <el-footer height="120px">
            <div class="el_footer_style">
                <el-divider><i class="el-icon-user-solid"></i></el-divider>
                {{ footer_text }}
                <el-divider><i class="el-icon-user-solid"></i></el-divider>
            </div>
        </el-footer>
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
            activeIndex: "1",
            footer_text: "this is a footer text",
            main_page: "https://element.eleme.cn/#/zh-CN/component/installation",
            el_menu_item_right_style: {
                float: "right",
            },
        };
    },
    methods: {
        icon_on_click() {
            window.open(this.main_page);
        },
        handleSelect(key, keyPath) {
            console.log(key, keyPath);
        },
    },
    computed: {},
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->

<style scoped>
.el_footer_style {
    text-align: center;
    height: 120px;
}
</style>
