<template>
    <div class="projects">
        <h1 class="subheading grey--text">Projects</h1>

        <v-container class="my-5">

            <v-expansion-panel>
                <v-expansion-panel-content v-for="project in myProjects" :key="project.id">
                    <div slot="header">{{ project.title }}</div>
                    <v-card>
                        <v-card-text class="px-4 grey--text">
                            <div class="font-weight-bold">due by {{ project.due }}</div>
                            <div>{{ project.content }}</div>
                        </v-card-text>
                    </v-card>
                </v-expansion-panel-content>
            </v-expansion-panel>

        </v-container>
    </div>
</template>

<script>
export default {
    data() {
        return {
            projects: [
                { id: 0, title: "Design a new website", person: "kim", due: "2019-01-01", status: "ongoing", content: "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Fugit earum obcaecati, excepturi doloribus quas sunt asperiores corrupti accusantium totam, minus neque tenetur praesentium nisi saepe animi repellendus cupiditate autem molestias." },
                { id: 1, title: "Design a new dashboard", person: "hong", due: "2019-01-01", status: "complete", content: "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Dignissimos iste suscipit voluptas officiis quod excepturi est impedit obcaecati ex nihil neque quas corporis repudiandae consequatur illo in quam, asperiores assumenda!" },
                { id: 2, title: "Design a new thumnail", person: "dong", due: "2019-01-01", status: "complete", content: "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Adipisci error perspiciatis, perferendis sequi expedita omnis facilis. Asperiores amet, saepe eaque totam hic pariatur, dolorem harum nulla voluptates commodi, ratione quisquam." },
                { id: 3, title: "Design a new database", person: "choi", due: "2019-01-01", status: "overdue", content: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Consequuntur deleniti velit suscipit iste, laudantium minus amet ab aperiam. Quo sunt quaerat facilis officiis, ipsa quae est laudantium enim ab nihil?" },
            ]
        }
    },
    computed: {
        myProjects() {
            return this.projects.filter(project => {
                return project.person === "hong"
            })
        }
    }
}
</script>

<style>

</style>
