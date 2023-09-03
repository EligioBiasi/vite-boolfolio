<template>
    <div class="main-center">
        <h1>
            Ciaooo
        </h1>
        <div class="project">
            <div class="single-project" v-for="project in projects">
                <h2 >
                    {{ project.title }}
                </h2>
            </div>
        </div>
    </div>
</template>

<script>
import axios from 'axios';

export default {
    name:'AppMain',

    data() {
        return {
            projects:[],
            apiUrl:'http://127.0.0.1:8000/api/projects',
        }
    },

    methods: {
        getProjects(){
            axios.get(this.apiUrl, {
                params: {}
            })
            .then((response)=>{
                console.log(response.data.results.data);
                this.projects= response.data.results.data
            })
            .catch(function (error) {
                console.log(error);
            })
        },
    },

    created() {
        this.getProjects();
    },
}
</script>

<style lang="scss">

    div.main-center{
        text-align: center;

        div.project{
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            align-items: center;

            div.single-project{
                width: calc((100%/3) - 2rem);
                border: 2px solid red;
                margin: 1rem;
            }
        }
    }
</style>