<template>
    <v-container fluid fill-height class="justify-center gradient" max-height="100vh">
        <v-row no-gutters>
            <v-col cols=12>
                <h1 class="text-h2 text-center white--text font-weight-bold" style="font-family: 'Montserrat', sans-serif !important;">FILIP<br>HALEWSKI</h1>
                <p class="text-center mt-2 white--text">Freelance Web Developer</p>
            </v-col>
        </v-row>
    </v-container>
</template>

<script>
    export default {
        name: 'HomeHero'
    };
</script>

<style>
    .gradient {

    }

    .arrow-down {
        transition: all 0.5s ease-in-out;
    }

    .arrow-down:hover {
        color: rgba(0, 0, 0, 0.75) !important;
    }
</style>