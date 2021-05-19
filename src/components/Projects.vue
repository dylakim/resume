<template>
    <section id="projects">
        <div class="description">
            <div>
                <h1>Projects</h1>
                <p>Most of the projects I work on are short-lived, due to the nature of promotional advertising. Below are working examples of projects that are currently live.</p>
            </div>
        </div>

        <Project
            project-url="test"
            image="test"
            imageAlt="test image"
        >
            <template v-slot:headline>Chobani Rewards</template>
            <template v-slot:body>
                <p>Project Description</p>
                <p>Multiple paragraphs describing the project. Long line testing. Multiple paragraphs describing the project. Long line testing.</p>
            </template>
        </Project>

        <Project
            project-url="test"
            image="test"
            imageAlt="test image"
        >
            <template v-slot:headline>Sony Rewards: The Perfect Pair</template>
            <template v-slot:body>
                <p>Project Description</p>
                <p>Multiple paragraphs describing the project</p>
            </template>
        </Project>
    </section>
</template>

<script>
    import Project from './Project';

    export default {
        components: {
            Project,
        },
    }
</script>