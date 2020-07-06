<template>
    <v-container fluid fill-height class="home-hero">
        <v-layout justify-center align-left column pa-5>
            <div class="heading display-4 font-weight-black white--text text-xs-center">HEALTHY MEALS</div>
            <div class="heading display-4 font-weight-black white--text text-xs-center mb-3">FOR YOUR TABLE</div>
            <div class="display-1 font-weight-bold white--text text-xs-center">Finally be a foodie at home with fresh, chef-prepared meals delivered daily to your door.</div>
            <v-btn fab class="mt-5 brown darken-4">
            <v-icon large color="white">mdi-heart</v-icon>
            </v-btn>
        </v-layout>
    </v-container>
</template>

<script>
export default {
    name: 'HomeHero'
};
</script>

<style scoped>
.home-hero {
    background: url('http://source.unsplash.com/0BhSKStVtdM');
    background-size: cover;

}

.heading {
  text-shadow: 2px 2px 3px rgba(33,33,33,0.5);
}
</style>