<template>
    <div id="app" class="container">
        <div class="todo-wrapper">
            <todo-header></todo-header>
            <div class="todo-content">
                <todo-report></todo-report>
                <todo-list :collection = "ListState.items"></todo-list>
            </div>
        </div>
    </div>
</template>
<script>
    import ListStore from "../data/store.js";
    import TodoHeader from "./components/TodoHeader.vue";
    import TodoReport from "./components/TodoReport.vue";
    import TodoList from "./components/TodoList.vue";

    export default {
        data () {
            return {
                ListState: ListStore.state
            }
        },

        components: {
            // 组件注册后才能使用
            // "todo-header": TodoHeader,
            // "todo-report": TodoReport,
            // "todo-list": TodoList

            // vue 的简写方式  会自动解析  在驼峰式命名中间加上斜杠
            TodoHeader,
            TodoReport,
            TodoList
        }
    }
</script>
<style lang="stylus">
@import "../styl/style.styl"
</style>