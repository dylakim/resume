<template>
    <section class="project">
        <img
            :src="require(`@/assets/projects/${imageFileName}`)"
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

<style lang="scss">
.project {
    border: 1px solid $colorPurpleDk;
    border-radius: calcRems(15px);
    @include boxShadow();
    box-sizing: border-box;
    margin: 0 calcRems(40px) calcRems(40px);
    padding: calcRems(40px);
    position: relative;
    
    @include bp(desktop) {
        align-items: center;
        display: flex;
        flex-direction: row-reverse;
        justify-content: space-between;
        margin: 0 0 calcRems(40px);
    }

    &__preview {
        @include boxShadow();
        border-radius: calcRems(10px);
        margin-bottom: calcRems(30px);
        width: 100%;

        @include bp(desktop) {
            flex-shrink: 1;
            margin: 0;
            width: 48%;
        }
        
    }

    &__details {
        width: 100%;
        
        @include bp(desktop) {
            align-self: stretch;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            text-align: left;
            width: 48%;
        }

        h2 {
            font-size: calcRems(22px);

            @include bp(desktop) {
                font-size: calcRems(24px);
                padding-bottom: calcRems(30px);
            }
        }
        
        p {
            font-size: calcRems(16px);
            font-weight: $lightWeight;

            @include bp(desktop) {
                font-size: calcRems(18px);
            }

            &:last-of-type {
                padding-bottom: calcRems(40px);
            }
        }
    }

}
</style>