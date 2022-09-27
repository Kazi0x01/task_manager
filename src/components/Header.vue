<template>
  <header>
    <h1>{{ title }}</h1>
    <CustomButton :text="showAddTaskBtn ? 'Close' : 'Add Task'" 
	:color="showAddTaskBtn ? 'red' : 'green'" @btn-click="$emit('toggle-add-form')"/>
	
  </header>
</template>

<script>
import CustomButton from "./CustomButton.vue";


export default {
  name: "HeaderTab",
  props: {
    title: String,
	showAddTaskBtn: Boolean
  },
  components: {
    CustomButton,
  },
  emits: ['toggle-add-form']
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
