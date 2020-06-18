<template>
    <div>
        <section-head>
            {{ head }}
        </section-head>
        <slot />
    </div>
</template>

<script>
import SectionHead from '../article/SectionHead.vue'

export default {
    name: 'Featured',
    components: {
        SectionHead
    },
    props: {
        head: {
            type: String,
            required: true
        }
    }
}
</script>