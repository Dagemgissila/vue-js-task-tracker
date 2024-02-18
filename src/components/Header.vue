<template>
    <header>
        <h1>{{ title  }}</h1>
        <AppButton :text="showAddTask ? 'close' : 'add' " @add-show-task="$emit('add-show-task')"  :color="showAddTask ? 'red' : 'green'" />
    </header>
  </template>
  
  <script>
  import AppButton from "./Button"
  export default {
    name: "AppHeader",
    props :{
      title:String,
      showAddTask:Boolean
    },
    components : {
          AppButton
    }
  };
  </script>
  
  <style scoped>
  header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 20px;
  }
  </style>
  