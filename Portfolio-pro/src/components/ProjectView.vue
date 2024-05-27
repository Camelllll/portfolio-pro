<template>
    <div id="app">
        <h1>Mon titre</h1>
        <project-view></project-view>
    </div>
</template>

<script>
import ProjectView from './components/ProjectView.vue';

export default {
    name: 'App',
    components: {
        ProjectView
    }
}
</script>

<style>
/* Vos styles CSS ici */
</style>