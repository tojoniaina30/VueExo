<template>
    <div>
        <div class="card" v-for="(user, index) in allUsers" :key="index">
            <p>{{ user.name }}</p>
            <p>{{ user.age }}</p>
            <p>{{ user.role }}</p>
            <p>{{ msg }}</p> 
        </div>
    </div>
</template>

<script>
export default {
    name:'UserCard',
    props:['allUsers', 'msg']
}
</script>

<style scoped>
    .card {
        border-bottom: 2px solid black;
    }
</style>