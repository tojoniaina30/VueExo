<template>
    <div>
        <form>
            <label for="">Name <br>
                <input type="text" placeholder="your Name here ..." v-model="name"> <br>
            </label>
            <label for="">Age <br>
                <input type="text" placeholder="your Age here ..." v-model="age"><br>
            </label>
            <label for="">Role <br>
                <input type="text" placeholder="your Role here ..." v-model="role"> <br>
            </label>

            <button>Add</button>
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
    methodes: {
        handleAddUser:() => {
            console.log(this.name())
            console.log(this.age())
            console.log(this.role())
        }
    }
}
</script>

<style>

</style>