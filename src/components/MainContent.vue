<template>
    <div class="row">
        <div class="col _20"></div>
        <div class="col _60 main-content">
            <cover-photo></cover-photo>
            <featured head="Sample1">
                <section-body :content="text"></section-body>
            </featured>
            <featured head="News" style="margin-top: 42px">
                <events> </events>
                <div class="link">
                    <span class="icon-btn">⯈</span>
                    <a href="#">More Information</a>
                </div>
            </featured>
        </div>
        <div class="col _20"></div>
    </div>
</template>

<script>
import CoverPhoto from './content/CoverPhoto.vue'
import Featured from './content/Featured.vue'
import SectionBody from './article/SectionBody.vue'
import Events from './news/Events.vue'

export default {
    components: {
        CoverPhoto, Featured, SectionBody, Events
    },
    data() {
        return {
            text: 'But I must explain to you how all this mistaken idea of denouncing pleasure and praising pain was born and I will give you a complete account of the system, and expound the actual teachings of the great explorer of the truth, the master-builder of human happiness. No one  rejects, dislikes, or avoids pleasure itself, because it is pleasure, but because those who do not know how to pursue pleasure rationally encounter consequences that are extremely painful. Nor again is there anyone who loves or pursues or desires to obtain pain of itself, because it is pain, but because occasionally circumstances occur in which toil and pain can procure him some great pleasure. To take a trivial example, which of us ever undertakes laborious physical exercise, except to obtain some advantage from it? But who has any right to find fault with a man who chooses to enjoy a pleasure that has no annoying consequences, or one who avoids a pain that produces no resultant pleasure? On the other hand, we denounce with righteous indignation and dislike men who are so beguiled and demoralized by the charms of pleasure of the moment, so blinded by desire, that they cannot foresee'
        }
    }
}
</script>

<style>
    .main-content {
        height: calc(100% - 60px);
    }

    .link {
        margin-top: 12px;
        margin-bottom: 46px;
        float: right;
    }

    .link > a {
        color: var(--color-secondary);
        text-decoration: underline;
    }

    .icon-btn {
        color: #fff;
        background: var(--color-secondary);
        font-size: 8px;
        padding: 2px;
    }

    .icon-btn, .link > a {
        vertical-align: middle;
    }
</style>