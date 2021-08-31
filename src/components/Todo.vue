<template>
  <div> 
      <div>
        {{ todo.title }}       {{ todo.project }}
      </div>

      <div>
          <span >
             <div v-on:click="showForm">Edit</div> 
             <div  v-on:click="deleteTodo(todo)">Delete</div> 
          </span>

          <span >
             
         </span>
      </div>
      

         <div v-show="isEditing">
      <div>
        <div >
          <label>Title</label>
          <input type='text' v-model="todo.title" >
        </div>
        <div >
          <label>Project</label>
          <input type='text' v-model="todo.project" >
        </div>
        <div >
          <button  v-on:click="hideForm">
            Close X
          </button>
        </div>
      </div>
    </div>

      <div v-show="todo.done">Completed</div>
      <div v-show="!todo.done">Complete</div>
  </div>
</template>

<script type = "text/javascript" >
export default {
  props: ["todo"],
   data() {
    return {
      isEditing: false,
    };
  },
  methods: {
    showForm() {
      this.isEditing = true;
    },
    hideForm() {
    //  this.isEditing = false;
    },

    deleteTodo(todo) {
      console.log(todo)
      this.$emit('delete-todo', todo);
    },
  },
};
</script>
<style>
</style>