<template>
    <div class="modal-overlay" >
      <div class="modal-content">
      
        <slot></slot>
        
        <div class="row ">
              <h4 class="col-sm-11">Add Form Input</h4>
              <button @click="$emit('close')" class="col-sm-1 btn btn-outline-primary">x</button>
        </div>
        <Forms/>
        <div class="save clearfix mt-5 ">
            <button type="button" @click="$emit('close')" class="btn btn-danger float-start">Close</button>
            <button type="submit" @click="(showModal1 = true)" class="btn btn-success float-end">Save</button>
            </div>
            <teleport to="#modal-root">
              <Question v-show="showModal1" @close="(showModal1= false)" >
                <button type="submit" @click="(showModal1 = false)" class="btn btn-danger float-end">Close</button>
                <div>{{question}}</div>
                
              </Question>
            </teleport>
          
      </div>
    </div>
  </template>
  
  <script>
  import Forms from './Forms.vue';
  import Question from './Question.vue'
    export default {
    name: "Modal",
    emits: ["close"],
    components:{Forms,Question},
    data() {
    return {
      showModal1: false,
     
    };
  },

  };
  </script>
  
  <style>
  .modal-overlay {
    position: absolute;
    top: 0;
    bottom: 0;
    left: 0;
    right: 0;
    display: grid;
    justify-content: center;
    align-items: center;
    background-color: rgba(255, 255, 255, 0.8);
   
  }
  
  .modal-content {
    
    padding: 20px;
    background-color: #fff;
    border-radius: 2px;
    display: inline-block;
    min-height: 500px;
    margin: 1rem;
    position: relative;
    min-width: 400px;
    box-shadow: 0 5px 6px rgba(95, 94, 94, 0.884), 0 3px 6px rgb(255, 255, 255);
    justify-self: center;
  }

  .check1{
    margin-right: 15px;
  }
  </style>