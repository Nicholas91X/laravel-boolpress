<template>
  <main>
    <router-view></router-view>
  </main>
</template>

<script>
export default {
    name: "Main",
    data() {
        return {
            posts: []
        }
    },
    created() {
        axios.get('/api/posts')
        .then ( (response) => {
            this.posts = response.data;
        })
    }
}
</script>

<style>

</style>