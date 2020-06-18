<template>
    <div id="section-content">
        <p>
            {{ content }}
        </p>
    </div>
</template>
<script>
export default {
    name: 'SectionBody',
    props: {
        content: {
            type: String,
            required: true
        }
    }
}
</script>

<style scope>
    #section-content p {
        color: var(--color-gray);
        font-size: 16px;
        line-height: 2;
    }
</style>