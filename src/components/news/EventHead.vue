<template>
    <div class="event-head">
        <span>{{ detail.date }}</span>
        <p>{{ detail.title }}</p>
    </div>
</template>

<script>
export default {
    props: {
        detail: {
            type: Object,
            required: true
        }
    }
}
</script>

<style>
    .event-head > span, .event-head > p {
        display: inline;
        color: var(--color-gray);
    }

    .event-head > span {
        margin-right: 12px;
    }

    .event-head {
        margin-top: 20px;
    }

    .event-head:nth-last-child() {
        margin-bottom: 12px;
    }
</style>