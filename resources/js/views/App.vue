<template>
    <div>
        <header>
            <nav>
                <ul>
                    <li>Home</li>
                    <li>Posts</li>
                    <li>Categories</li>
                </ul>
            </nav>
        </header>

        <PostsGrid/>

        <footer>
            &copy; Boolpress 2022
        </footer>
    </div>
</template>

<script>
    import PostsGrid from './Posts.index.vue'

    export default{
        components: {
            PostsGrid,
        }
    }
</script>

<style lang="scss" scoped>

</style>