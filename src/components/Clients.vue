<template>
    <section class="clients">
        <h1>Clients</h1>
        <p>I've had the pleasure of working with many different brands over the last 6 years. Here are just a few.</p>

        <div class="clients__logos">
            <Client
                imageFileName="samsung.svg"
                altText="Samsung"
            />

            <Client
                imageFileName="mondelez.png"
                altText="Mondelez International"
            />
            
            <Client
                imageFileName="sony.svg"
                altText="Sony"
            />
            
            <Client
                imageFileName="dunkin.jpg"
                altText="Dunkin'"
            />
            
            <Client
                imageFileName="chobani.svg"
                altText="Chobani"
            />

            <Client
                imageFileName="wyndham.png"
                altText="Wyndham Hotels and Resorts"
            />
        </div>

    </section>
</template>

<script>
    import Client from './Client';

    export default {
        components: {
            Client,
        },
    }
</script>