<template>
    <div class="social">
        <a
            href="https://www.instagram.com/kim.dyla/"
            title="Follow kim.dyla on Instagram"
            class="light"
            target="_blank"
        >
            <font-awesome-icon :icon="faInstagram" />
        </a>
        <a
            href="https://twitter.com/dyla_kim"
            title="Follow dyla_kim on Twitter"
            class="light"
            target="_blank"
        >
            <font-awesome-icon :icon="faTwitter" />
        </a>
        <a
            href="https://www.linkedin.com/in/dylakim"
            title="Connect with dylakim on LinkedIn"
            class="light"
            target="_blank"
        >
            <font-awesome-icon :icon="faLinkedinIn" />
        </a>
        <a
            href="https://github.com/dylakim"
            title="See dylakim's work on GitHub"
            class="light"
            target="_blank"
        >
            <font-awesome-icon :icon="faGithub" />
        </a>
    </div>
</template>

<script>
    import {
        faGithub,
        faInstagram,
        faLinkedinIn,
        faTwitter,
    } from '@fortawesome/free-brands-svg-icons';

    export default {
        data () {
            return {
                faGithub,
                faInstagram,
                faLinkedinIn,
                faTwitter,
            };
        },
    }
</script>