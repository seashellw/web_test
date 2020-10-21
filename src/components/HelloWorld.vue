<template>
<div>
    <el-container>
        <el-header>
            <el-row :gutter="20">
                <el-col :span="10">
                    <div class="header_col_1_style"></div>
                </el-col>
                <el-col :span="12">
                    <div class="header_col_2_style">
                        <el-menu :default-active="activeIndex" class="el-menu-demo" mode="horizontal" @select="handleSelect">
                            <el-menu-item index="1">处理中心</el-menu-item>
                            <el-submenu index="2">
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
                    </div>
                </el-col>
                <el-col :span="2">
                    <el-button type="success" class="button_top_style" icon="el-icon-search">前进</el-button>
                </el-col>
            </el-row>
        </el-header>
        <el-main>main </el-main>
        <el-footer>{{ footer_text }}</el-footer>
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
        };
    },
    methods: {
        handleSelect(key, keyPath) {
            console.log(key, keyPath);
        },
    },
    computed: {},
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->

<style>
.header_col_1_style {
    height: 60px;
}

.header_col_2_style {
    height: 60px;
}

.button_top_style {
    margin-top: 10px;
    float: right;
}

.el-footer {
    background-color: #909399;
    text-align: center;
    padding-top: 10px;
}
</style>
