<template>
    <v-row class="portofolio" justify="center" align="center">
        
        <v-col cols="12" class="portofolio__title text-center mt-2 mt-lg-7 mb-lg-4">
            <h1 class="display-3 primary--text my-2 mb-6 mb-lg-13 d" style="font-weight: 700;" color="primary">My Portfolio</h1>
        </v-col>
        <v-col cols="12">
            <v-row>
                <v-col 
                    v-for="(portofolio, i) in portofolios"
                    :key="i"
                    cols="12"
                    sm="6"
                    md="6"
                    lg="4"
                    class="portofolio__item"
                >
                <a :href=portofolio.link target="_blank" style="text-decoration: none" rel="noopener noreferrer">
                    <v-card elevation="7" class="mx-5 my-5 p-2 primary rounded-lg">
                         <v-img
                        :src="require(`~/assets/img/${portofolio.asset}`)"
                        height="200px" cover class="portofolio__image"
                        ></v-img>

                        <v-card-title class="portofolio__title white--text font-weight-bold">
                        {{portofolio.title}}
                        </v-card-title>

                        <v-card-subtitle class="portofolio__content font-weight-bold">
                        {{portofolio.category}}
                        </v-card-subtitle>
                    </v-card>
                    </a>
                </v-col>
            </v-row>
        </v-col>
    </v-row>
</template>

<script>
export default {
    name: 'Portfolio',
    methods: {
        getUrl(pic) {
            return require(pic);
        }
    },
    data() {
        return {
            portofolios: [
                { 
                    title: 'PP Bahrul Ulum',
                    category: 'Education',
                    description: 'lorem',
                    link: 'https://bahrululumtajinan.sch.id/',
                    asset: 'p4.png'
                },
                {
                    title: 'BEM KBM IT PLN',
                    category: 'Education',
                    description: 'lorem',
                    link: '',
                    asset: 'p3.png'
                },
                {
                    title: 'Kriuk Hu Hah',
                    category: 'Company',
                    description: 'lorem',
                    link: 'https://amarizzal.github.io/proyek/kriukhuhah/index.html',
                    asset: "p1.jpg"
                },
                {
                    title: 'Film Ku',
                    category: 'Ensiklopedia',
                    description: 'lorem',
                    link: 'https://amarizzal.github.io/proyek/Submission%20;%20FilmKu/dist/index.html',
                    asset: 'p2.jpg'
                },
            ]
        }
    }
}

</script>