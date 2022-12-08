<template>
  <div class="modal-overlay">
    <div  class="modal-content">   
      <div class="languages btn-group mt-5" >
              <button type="button" class="btn btn-outline-primary">TR</button>
              <button type="button" class="btn btn-outline-primary">EN</button>
              
          </div>
           <div class="card mt-5">
            
             <div class="card-header">
               <h4>What is your gender?</h4>
              </div>
              
                <div class="card-body">
                  <select class="form-select form-select-sm mt-3" v-model="select">
                  <option>Female</option>
                  <option>Male</option>
                  <option>Other</option>
        </select>
                </div>
                </div>
                <slot></slot>
    </div>

  </div>
   
</template>

<script>
export default {
 
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
  min-height: 200px;
  margin: 1rem;
  position: relative;
  min-width: 100px;
  box-shadow: 0 5px 6px rgba(95, 94, 94, 0.884), 0 3px 6px rgb(255, 255, 255);
  justify-self: center;
}


</style>