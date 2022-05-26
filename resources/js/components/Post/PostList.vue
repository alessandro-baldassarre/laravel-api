<template>
    <div>
        <Post/>
    </div>
</template>

<script>

import Post from './Post';
export default {
    name: "App",
    components: {
        Post
    },
    data: function() {
        return{
            posts: [],
        }
    },
    methods:{
        getPosts(){
            const apiUrl = 'http://localhost:8000/api/posts';
            axios.get(apiUrl).then((results)=>{
                // this.posts = results.data;
                console.log(results.data.data);
            })
        }
    },
    created(){
        this.getPosts();
    }
}
</script>

<style scoped>
</style>
