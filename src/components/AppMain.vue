<template>
    <div>
        <h1>
            Ciaooo
        </h1>
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
            .then(function (response) {
                console.log(response);
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
    
</style>