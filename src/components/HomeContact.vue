<template>
    <v-container fluid fill-height max-height="100vh" class="align-start gradient">

        <v-row no-gutters>
            <v-col cols=12>
                <h1 class="ml-5 mt-5 text-h2 white--text font-weight-bold"
                    style="font-family: 'Montserrat', sans-serif !important;">KONTAKT</h1>
            </v-col>
        </v-row>
        <v-row align="middle" justify="center" class="">
            <v-col cols="6">
                <v-form ref="form" v-model="valid" class="white pa-10 rounded">
                    <v-text-field v-model="name" :counter="10" :rules="nameRules" label="Imię" required></v-text-field>

                    <v-text-field v-model="email" :rules="emailRules" label="E-mail" required></v-text-field>

                    <v-textarea name="input-7-1" label="Wiadomość" value=""></v-textarea>

                    <v-btn color="success" class="mr-4" @click="validate">
                        Wyślij
                    </v-btn>
                </v-form>
            </v-col>
        </v-row>

    </v-container>
</template>

<script>
    export default {
        name: 'HomeContact',
    }
</script>

<style>

</style>