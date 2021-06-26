<template>
    <section id="projects">
        <div class="description">
            <div>
                <h1>Projects</h1>
                <p>Most of the projects I work on are short-lived, due to the nature of promotional advertising. Below are working examples of projects that are currently live.</p>
            </div>
        </div>

        <Project
            v-for="project in projects"
            :key="project.name"
            :project-url="project.url"
            :imageFileName="project.image"
            :imageAlt="project.altText"
            :projectName="project.name"
        >
            <template v-slot:headline>{{ project.headline }}</template>
            <template v-slot:body>
                <div v-html="project.body" />
            </template>
        </Project>
    </section>
</template>

<script>
    import projects from '../data/projects.json';
    import Project from './Project';

    export default {
        components: {
            Project,
        },

        data () {
            return {
                projects,
            };
        },
    };
</script>

<style lang="scss">
#projects {
    margin: 0 0 calcRems(75px);
    
    @include bp(desktop) {
        margin: 0 auto calcRems(85px);
        width: calcRems(920px);
    }

    .description {
        background: $colorPurpleDk;
        margin: 0 auto calcRems(40px);
        padding: calcRems(45px) calcRems(80px);

        @include bp(desktop) {
            padding: calcRems(50px) calcRems(200px);
        }

        h1, p {
            color: $colorWhite;
        }
    }
}
</style>