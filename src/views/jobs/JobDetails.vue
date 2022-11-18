<template>
    <h1>Job Details Page</h1>
    <p>The job id is {{ id }}</p>
</template>

<script>
export default {
    props: ['id'],
    mounted() {
        fetch('http://localhost:3000/jobs/' + this.id)
        .then(res => res.json())
        .then(data => this.jovs = data)
        .catch(err => console.log(err.message))
    }
}
</script>

<style>

</style>