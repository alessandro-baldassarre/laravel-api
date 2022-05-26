<template>
    <div class="container-fluid">
        <PostList/>
    </div>
</template>

<script>

import PostList from '../components/Post/PostList';
export default {
    name: "App",
    components: {
        PostList
    }
}
</script>

<style scoped>
</style>
