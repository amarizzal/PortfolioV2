<template>
    <v-row justify="center" align="center">
        
        <v-col cols="12" class="text-center mt-7 mb-4">
            <h1 class="display-3 primary--text my-2 mb-13 d" style="font-weight: 700;" color="primary">My Portfolio</h1>
        </v-col>
        <v-col cols="12">
            <v-row>
                <v-col 
                    v-for="(portofolio, i) in portofolios"
                    :key="i"
                    cols="4"
                >
                    <v-card elevation="0" class="mx-5 primary rounded-lg">
                         <v-img
                        src="https://cdn.vuetifyjs.com/images/cards/sunshine.jpg"
                        height="200px"
                        ></v-img>

                        <v-card-title class="white--text font-weight-bold">
                        {{portofolio.title}}
                        </v-card-title>

                        <v-card-subtitle>
                        {{portofolio.category}}
                        </v-card-subtitle>
                    </v-card>
                </v-col>
            </v-row>
        </v-col>
    </v-row>
</template>

<script>
export default {
    name: 'Portfolio',
    data() {
        return {
            portofolios: [
                {
                    title: 'PP Bahrul Ulum',
                    category: 'Education',
                    description: 'lorem',
                    link: ''
                },
                {
                    title: 'BEM KBM IT PLN',
                    category: 'Education',
                    description: 'lorem',
                    link: ''
                },
                {
                    title: 'Kriuk Hu Hah',
                    category: 'Company',
                    description: 'lorem',
                    link: ''
                },
                {
                    title: 'Film Ku',
                    category: 'Non-Profit',
                    description: 'lorem',
                    link: 'https://amarizzal.github.io/proyek/Submission%20;%20FilmKu/dist/index.html'
                },
            ]
        }
    }
}

</script>