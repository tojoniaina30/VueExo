<template>
    <div>
        <form>
            <label for="">Name <br>
                <input type="text" placeholder="your Name here ..."  v-model="name"> <br>
            </label>
            <label for="">Age <br>
                <input type="text" placeholder="your Age here ..." v-model="age"> <br>
            </label>
            <label for="">Role <br>
                <input type="text" placeholder="your Role here ..." v-model="role"> <br>
            </label>

            <button  v-on:click.prevent ="handleSubmit()" >Add</button>
        </form>
    </div>
</template>
<script>

export default {
    name:'FormComponent',
    data() {  
       return {
        name: '',
        age: '',
        role: ''
       }
            
    },
    methods: {
        handleSubmit: () => {
            console.log(this);
        }
    },
}

        
</script>
<style scoped>
    
</style>