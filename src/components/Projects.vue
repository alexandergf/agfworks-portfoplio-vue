<template>
    <section class="project-section">
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
                        class="white--text align-end"
                        height="200px"
                        :src="project.image"
                        >
                            <v-card-title>{{ project.name }}</v-card-title>
                        </v-img>

                        <v-card-text class="text--primary">
                            {{ project.description }}
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
                    description: '',
                    image: ''
                },
                {
                    name: 'Hour Tracking App',
                    github: 'https://www.google.es',
                    description: '',
                    image: ''
                }
            ]
        }
    }
}
</script>


<style scoped>
.project-section{
    background-color: #FFD563;
}
</style>