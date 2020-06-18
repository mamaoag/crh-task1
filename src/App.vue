<template>
    <div>
        <navbar></navbar>
        <main-content></main-content>
        <foot />
    </div>
</template>

<script>
import Navbar from './components/Navbar.vue'
import Foot from './components/Foot.vue'
import MainContent from './components/MainContent.vue'
export default {
    name: 'App',
    components: {
        Navbar, Foot, MainContent
    }    
}
</script>
