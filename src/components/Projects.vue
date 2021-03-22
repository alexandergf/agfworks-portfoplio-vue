<template>
    <section id="projects" class="project-section">
        <v-container>
            <v-row>
                <v-col>
                    <h1>Projects</h1>
                </v-col>
            </v-row>
            <v-row class="justify-space-around mb-8 mt-4">
                    <v-card
                        v-for="project in projects"
                        :key="project.name"
                        class=""
                        max-width="300"
                    >
                        <v-img
                        class="align-end"
                        height="200px"
                        :src="project.image"
                        />
                        <v-card-title>{{ project.name }}</v-card-title>
                        <v-card-text class="text--primary">
                            {{ truncate(project.description) }}
                        </v-card-text>

                        <v-card-actions>
                            <v-btn
                                color="orange"
                                text
                                :href="project.github"
                                target="_blank"
                            >
                                GitHub repo
                            </v-btn>
                        </v-card-actions>
                    </v-card>
            </v-row>
        </v-container>
    </section>
</template>

<script>
export default {
    data() {
        return{
            projects: [
                {
                    name: 'Curriculum',
                    github: 'https://www.google.es',
                    description: 'Lorem fistrum te va a hasé pupitaa ese hombree por la gloria de mi madre. Caballo blanco caballo negroorl está la cosa muy malar me cago en tus muelas hasta luego Lucas se calle ustée ese pedazo de te voy a borrar el cerito qué dise usteer caballo blanco caballo negroorl. Se calle ustée va usté muy cargadoo va usté muy cargadoo a gramenawer mamaar caballo blanco caballo negroorl ese hombree quietooor a peich. Qué dise usteer caballo blanco caballo negroorl no te digo trigo por no llamarte Rodrigor pupita pecador ese que llega. Te va a hasé pupitaa ese pedazo de ese que llega ese pedazo de pecador me cago en tus muelas está la cosa muy malar amatomaa me cago en tus muelas a peich hasta luego Lucas. Caballo blanco caballo negroorl ese hombree al ataquerl mamaar me cago en tus muelas no te digo trigo por no llamarte Rodrigor por la gloria de mi madre caballo blanco caballo negroorl fistro.',
                    image: 'https://media.istockphoto.com/photos/watercolor-textured-background-picture-id887755698?k=6&m=887755698&s=612x612&w=0&h=_yEUF8gLpWjZv5IgwuWkecNVt4X4P7vpuFBKCWIuR44='
                },
                {
                    name: 'Hour Tracking App',
                    github: 'https://www.google.es',
                    description: 'Description Hour Tracking App',
                    image: 'https://img.freepik.com/foto-gratis/habitacion-piso-concreto-fondo-humo_9083-2991.jpg?size=626&ext=jpg&ga=GA1.2.1562385141.1605398400'
                }
            ]
        }
    },
    methods: {
        truncate(str){
            if(str.length > 50){
                return str.slice(0, 79) + '...';
            }
            return str;
        }
    }
}
</script>


<style scoped>
.project-section{
    background-color: #FFD563;
}
.v-image{
    border-bottom: 1px solid; 
}
</style>