<template>
    <section class="project">
        <div>
            <div>
                <h2><slot name="headline" /></h2>
                
                <img
                    :src="image"
                    :alt="imageAlt"
                    class="project__preview"
                >

                <div><slot name="body" /></div>
            </div>

            <a
                v-if="projectUrl"
                :href="projectUrl"
                class="check-it-out"
                target="_blank"
            >
                Check it out <font-awesome-icon :icon="faAngleRight" />
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
            image: {
                required: true,
                type: String,
            },
            imageAlt: {
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