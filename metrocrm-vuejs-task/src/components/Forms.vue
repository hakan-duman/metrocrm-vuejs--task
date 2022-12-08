<template>
         <form @submit.prevent="">
          <div class="input">
            <h6>Input Type</h6>
        <select class="form-select form-select-sm mt-3" v-model="select">
          <option disabled value="">Please select one</option>
          <option>Seleck Box</option>
          <option>Text</option>
          <option>Yes or No</option>
        </select>
          </div>
          <div class="required mt-1">
          <h6>Is required</h6>
        <div class="d-flex" >
          <div class=" form-check check1" >
           <input v-model="picked" type="radio" class="form-check-input" id="radio1" name="optradio" value="Yes" checked>
            <label class="form-check-label " for="radio1">Yes</label>
          </div>
          <div class=" form-check">
           <input v-model="picked" type="radio" class=" form-check-input" id="radio2" name="optradio" value="No">
            <label class=" form-check-label" for="radio2">No</label>
          </div>
        </div>
          </div>        
          <div class="languages btn-group mt-1" >
              <button type="button" class="btn btn-outline-primary">TR</button>
              <button type="button" class="btn btn-outline-primary">EN</button>
              
          </div>
          <div class="descrip mt-2">
             <input type="text" v-model="question" class="form-control form-control-sm mt-1" placeholder="What is your gender?">
            <input type="text" v-model="descrip" class="form-control form-control-sm mt-2" placeholder="Description">
          </div>
          <h6>{{select}}</h6>
          <h6>{{picked}}</h6>
          <h6>{{question}}</h6>
          <h6>{{descrip}}</h6>
          
          
          <div class="option mt-2">
            
            <button class="btn btn-outline-primary" >Add another answer</button>
          </div>
          
          
        </form>
</template>
<script>

import Question from './Question.vue'


export default {
  
  data(){

    return{
      
      question : '',
      descrip: '',
      select: '',
      picked: '',
    }
  
  },
    
    components:{Question}
   
  }
 
  




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