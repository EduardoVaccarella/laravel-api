<template>
    <div>
        <div class="container grid grid-cols-2 d-flex flex-wrap">
            <div v-for="post in posts" :key="post.id" class="card">
                {{ post.title }}
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                posts: []
            }
        },
        methods: {
            fetchPosts() {
                axios.get('/api/posts')
                .then( res => {
                    const { posts } = res.data
                    this.posts = posts
                })
                .catch( err => {
                    console.warn( err )
                })
            }
        },
        mounted() {
            this.fetchPosts();
        }
    }
</script>

<style lang="scss" scoped>

</style>