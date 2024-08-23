<template>
    <div id="app">
        <h1>Mon titre</h1>
        <about-view></about-view>
    </div>
</template>

<script>
import AboutView from './components/aboutView.vue';

export default {
    name: 'App',
    components: {
        AboutView
    }
}
</script>

<style>
/* Vos styles CSS ici */
</style>