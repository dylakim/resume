<template>
    <section class="project">
        <img
            :src="`/images/projects/${imageFileName}`"
            :alt="imageAlt"
            class="project__preview"
        >

        <div class="project__details">
            <div>
                <h2><slot name="headline" /></h2>
                <div><slot name="body" /></div>
            </div>

            <a
                v-if="projectUrl"
                :href="projectUrl"
                class="check-it-out"
                target="_blank"
            >
                View {{ projectName }} <font-awesome-icon :icon="faAngleRight" />
            </a>
        </div>
    </section>
</template>

<script>
    import { faAngleRight } from '@fortawesome/free-solid-svg-icons';

    export default {
        props: {
            projectUrl: {
                default: null,
                required: false,
                type: String,
            },
            imageFileName: {
                required: true,
                type: String,
            },
            imageAlt: {
                default: '',
                required: false,
                type: String,
            },
            projectName: {
                default: '',
                required: false,
                type: String,
            },
        },

        data () {
            return {
                faAngleRight,
            };
        },
    }
</script>