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
                <a :href=portofolio.link target="_blank" style="text-decoration: none" rel="noopener noreferrer">
                    <v-card elevation="7" class="mx-5 my-5 pt-2 primary rounded-lg">
                         <v-img
                        :src="require(`~/assets/img/${portofolio.asset}`)"
                        height="200px" contain class="m-2"
                        ></v-img>

                        <v-card-title class="white--text font-weight-bold">
                        {{portofolio.title}}
                        </v-card-title>

                        <v-card-subtitle class="font-weight-bold">
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
                    asset: 'p1.jpg'
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