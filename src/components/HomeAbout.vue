<template>
    <v-container fluid fill-height max-height="100vh" class="align-start gradient">
        <v-container>
            <v-row no-gutters>
                <v-col cols=12>
                    <h1 class="ml-5 mt-5 text-h2 white--text font-weight-bold"
                        style="font-family: 'Montserrat', sans-serif !important;">PROJEKTY</h1>
                </v-col>
            </v-row>
            <v-row align="middle" justify="center" class="mt-5">
                <v-col v-for="card in cards" :key="card.title" :cols="card.grid[0]" :sm="card.grid[1]" :md="card.grid[2]" :lg="card.grid[3]">
                    <v-card class="">
                        <v-img class="white--text align-end" max-height="300px" width="auto" :src="card.src">
                        </v-img>
                        <v-divider></v-divider>
                        <v-card-title v-text="card.title" class=""></v-card-title>
                        <v-card-subtitle class="pb-0" v-text="card.subtitle"></v-card-subtitle>

                        <v-card-actions>
                            <v-spacer></v-spacer>
                            <v-btn color="orange" text>
                                Podgląd
                            </v-btn>
                        </v-card-actions>
                    </v-card>
                </v-col>
            </v-row>

        </v-container>
    </v-container>
</template>

<script>
    export default {
        name: 'HomeAbout',
        data: () => {
            return {
                cards: [{
                        title: 'cubeshop.pl',
                        subtitle: '',
                        src: 'cubeshop3.png',
                        grid: [11, 7, 6, 5]
                    },
                    {
                        title: 'podcesje.pl',
                        subtitle: '',
                        src: 'podcesje2.png',
                        grid: [11, 7, 6, 5]
                    }
                ]
            }
        }
    }
</script>

<style>
    .v-card__title {

    }
</style>