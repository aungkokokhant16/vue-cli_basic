<template>
  <h1>hi there</h1>
  
  <div v-if="showModal"> 
      <Modal :theme="theme" @closeModal="showModal=false"> 

        <h1>Login success </h1>
        <p>Welcome Aung Ko Ko Khant</p>

        <!-- <template v-slot:links>
          <a href="">Sing Up</a>
          <a href="">Register</a>
        </template> -->

      </Modal>

      
  </div>

  <div v-if="showModal1"> 
      <Modal :theme1="theme1" @closeModal="showModal1=false"> 

        <h1>Login Failure </h1>
        <p>Pls try again</p>

        

      </Modal>

      
  </div>

 

  <button @click="showModal=true">open modal</button>
  <button @click="showModal1=true">close modal</button>
  
</template>

<script>
import Modal from "./components/Modal.vue"
export default {

  data(){

    return{
    header:"loggin success",
    content:"Welcom Aung Ko Ko Khant",
    theme:"success",
    theme1:"danger",
    showModal:false,
    showModal1:false,
   
    }

    
  },
  components:{
    Modal
    
  }
}
</script>

<style scoped>
  h1{
    color: blue;
  }
</style>