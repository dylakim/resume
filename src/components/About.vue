<template>
    <section id="about">
        <div class="description">
            <div>
                <h1>Front End Web Developer</h1>
                <p><font-awesome-icon :icon="faMapMarkerAlt" /> Troy, MI or Remote</p>
                <p>I am a Senior Interface Developer at Merkle. I use technologies like HTML, SCSS, JavaScript, and Vue.js to build fully responsive and accessible websites.</p>

                <Social />
            </div>
        </div>

        <div id="skills">
            <section>
                <font-awesome-icon :icon="faCode" />
                <h2>Languages</h2>
                <ul>
                    <li>Javascript</li>
                    <li>HTML</li>
                    <li>CSS/SCSS</li>
                    <li>Vue.js</li>
                </ul>
            </section>

            <section>
                <font-awesome-icon :icon="faTools" />
                <h2>Tools</h2>
                <ul>
                    <li>Git</li>
                    <li>Bitbucket</li>
                    <li>JIRA</li>
                    <li>VSCode</li>
                    <li>Photoshop</li>
                </ul>
            </section>

            <section>
                <font-awesome-icon :icon="faHeart" />
                <h2>Interests</h2>
                <ul>
                    <li>Travel</li>
                    <li>Mountain Biking</li>
                    <li>Snowboarding</li>
                    <li>Cocktails</li>
                    <li>Netflix and Chill</li>
                </ul>
            </section>
        </div>

        <p class="learn-more">Learn more on <a href="https://www.linkedin.com/in/dylakim" target="_blank">LinkedIn</a></p>
    </section>
</template>

<script>
    import {
        faCode,
        faHeart,
        faMapMarkerAlt,
        faTools,
    } from '@fortawesome/free-solid-svg-icons';

    import Social from './Social';

    export default {
        components: {
            Social,
        },

        data (){
            return {
                faCode,
                faHeart,
                faMapMarkerAlt,
                faTools,
            };
        },
    }
</script>