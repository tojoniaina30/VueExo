<template>
  <div id="app">
    <WaitSpinner v-if="showLoading"/>
    <button @click="handleToggle">toggle</button>
    <AddForm @addUser="addUser" />
    <UserCard v-bind:allUsers="users" msg="form Done"/>
  </div>
</template>

<script>
import AddForm from './components/AddForm.vue';
import UserCard from './components/UserCard.vue';
import WaitSpinner from './components/WaitSpinner.vue';

export default {
  name: 'App',
  components: {
    AddForm,
    UserCard,
    WaitSpinner
},
  data(){
    return{
      users:[],
      showLoading:true,
    }
  },
  methods: {
    addUser: function (newUser) {
      this.users.push(newUser)
    },
    handleToggle:function(){
      console.log('clicked');
      this.showLoading = !this.showLoading
      /*  let oldValue = this.showLoading
          this.showLoading = !=oldValue */
    }
  },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
