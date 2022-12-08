<template>
  <div class="container m-5">
    <div class="container mt-5 ">
      <div class="container path1">
        <div class="row ">
          <h4 class="col-sm-11 mb-5">Edit Form</h4>
        
      </div>

        <div class="container">
            <div class="btn-group mb-3">
              <button type="button" class="btn btn-outline-primary">TR</button>
              <button type="button" class="btn btn-outline-primary">EN</button>
            </div>
            <div class="container">
              <h5 class="">Title EN</h5>
              
              <input type="text"  class="input-sm mb-3 form-control" placeholder="...">

            </div>
            <div class="d-flex justify-content-center">
              
              <button @click="showModal = true" class="btn btn-outline-primary">+ Add Question</button> <QuestionsView/>
      <teleport to="#modal-root">
        <Modal v-show="showModal" @close="showModal = false"/>
          
      </teleport>
             
            </div>
            
        </div>
          <button class="btn btn-primary">save</button>    
       </div>
       
</div>

  </div>

</template>

<script>
import Modal from "./components/Modal.vue";
import { createI18n } from 'vue-i18n'

const i18n = createI18n({
  // something vue-i18n options here ...
})

export default {
  name: "App",
  components: {
    Modal,
    
  },
  data() {
    return {
      showModal: false,
    };
  },

};



</script>

<style>

.path1{
box-shadow: 0px 0px 10px #00000040;

}



</style>
