<template>
    <div class="container">
        <!-- event modifier -->
        <form v-on:submit.prevent="handleAddUser" class="form">
            <label for="">Name <br>
                <input type="text" placeholder="your Name here ..." v-model="name"> <br>
            </label>
            <label for="">Age <br>
                <input type="text" placeholder="your Age here ..." v-model="age"><br>
            </label>
            <label for="">Role <br>
                <input type="text" placeholder="your Role here ..." v-model="role"> <br>
            </label>

            <button type="submit">Add</button>
            <button @click="openModal">Open Modal</button>
            <button @click="changeTestValue"> Change </button>
        </form>
    </div>
</template>

<script>
export default {
    name: 'AddForm',
    data: function () {
        return {
            name: '',
            age: '',
            role: '',
        }
    },
    props: ['test'],
    methods: {
        handleAddUser() {
            this.$emit('addUser', {name: this.name, age:this.age, role:this.role})
        },
        openModal () {
            this.$emit('showModal')
        },
        changeTestValue () {
            /* = :affeectation de valeur */
        }
    },


}
</script>

<style scoped>
    .container{
        display: flex;
        align-items: center;
        justify-content: center;
        width: 100vw;
        height: 100vh;
    }
    .form{
        display:flex;
        flex-direction: column;
        justify-content: center;
        align-items: start;
        gap: 10px;
        padding: 50px 150px;
        background-color: rgb(232, 56, 147);
        border-radius: 25px;
        width: 500px;
    }
</style>