<template>
    <div id="news-events">
       <div v-for="n in news" :key="n.date">
           <event-head :detail="n"> </event-head>
       </div>
    </div>
</template>

<script>
import EventHead from './EventHead.vue'

export default {
    components: {
        EventHead
    },
    data() {
        return {
            news: [
                {
                    date: '2013/05/01',
                    title: 'Please feel free to send us any additional dummy texts.'
                },
                {
                    date: '2013/04/30',
                    title: 'Please feel free to send us any additional dummy texts.'
                },
                {
                    date: '2013/04/20',
                    title: 'Please feel free to send us any additional dummy texts.'
                },
                {
                    date: '2013/04/11',
                    title: 'Please feel free to send us any additional dummy texts.'
                },
                {
                    date: '2013/04/10',
                    title: 'Website OPEN.'
                },

            ]
        }
    }
}
</script>