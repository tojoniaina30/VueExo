<template>
  <div id="app">
    <WaitSpinner v-if="showLoading"/>  
    <button v-if="showLoading" @click="handleToggle">toggle</button>
    <AddForm v-if="!showLoading" @showModal ="handleOpenModal" v-bind:test="test"/>
    <UserCard v-bind:allUsers="users" msg="form Done"/>
    <AddModal v-if="showModal" @showModal = "!handleOpenModal"/>
  </div>
</template>

<script>
import AddForm from './components/AddForm.vue';
import UserCard from './components/UserCard.vue';
import WaitSpinner from './components/WaitSpinner.vue';
import AddModal from './components/AddModal.vue'

export default {
  name: 'App',
  components: {
    AddForm,
    UserCard,
    WaitSpinner,
    AddModal,
},
  data(){
    return{
      users:[],
      showLoading:true,
      showModal:false,
      test:""
    }
  },
  methods: {
    addUser: function (newUser) {
      this.users.push(newUser)
    },
    handleToggle:function() {
        this.showLoading = !this.showLoading
      /*  let oldValue = this.showLoading
          this.showLoading = !=oldValue */
    },
    handleOpenModal(){
    console.log('handelOpenModal');
    this.showModal = !this.showModal
  }
  },
  mounted() {
    setTimeout(() => {
      console.log('after 7 seconds');
      this.showLoading = !this.showLoading;
    }, 7000);
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
}
</style>
