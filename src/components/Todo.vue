<template>
  <div> 
      <div>
        {{ todo.title }}       {{ todo.project }}
      </div>
     
      <div v-show="todo.done">Completed</div>
      <div v-show="!todo.done">Complete</div>
  </div>
</template>

<script type = "text/javascript" >
export default {
  props: ["todo"],
};
</script>
<style>
</style>