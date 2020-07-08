<template>
    <span>
        <home-hero></home-hero>
        <home-about></home-about>
        <home-contact></home-contact> 
    </span>
</template>

<script>
    import HomeHero from '@/components/HomeHero';
    import HomeAbout from '@/components/HomeAbout';
    import HomeContact from '@/components/HomeContact';

    export default {
        name: 'Home',
        components: {
            HomeHero,
            HomeAbout,
            HomeContact
        }
    };
</script>

<style>
    .arrow-down {
        transition: all 0.5s ease-in-out;
    }

    .arrow-down:hover {
        color: rgba(0, 0, 0, 0.75) !important;
    }
</style>