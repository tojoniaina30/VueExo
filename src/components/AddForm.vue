<template>
    <div>
        <!-- event modifier -->
        <form v-on:submit.prevent="handleAddUser">
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
    methods: {
        handleAddUser() {
            this.$emit('addUser', {name: this.name, age:this.age, role:this.role})
        }
    }
}
</script>

<style>

</style>