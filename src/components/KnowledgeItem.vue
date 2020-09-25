<template>
  <div class="Item_Panel">
    <div>
      <img src="src/assets/python.png" alt="python logo">
    </div>


    <strong>{{ state.name }}</strong>
    <strong>{{ state.value }} %</strong>

  </div>
</template>

<script>
import {reactive} from "@vue/reactivity";

export default {
  name: "KnowledgeItem",
  props: {
    name: String,
    value: Number
  },
  setup(props) {
    const state = reactive({
      name: props.name,
      value: props.value,
      logo: ""
    })
    return {
      state
    }
  }
}
</script>

<style scoped>
.Item_Panel {
  display: flex;
  flex-direction: column;
  border: 1px solid dimgray;
  border-radius: 15px;
  background-color: #2c3e50;
  min-width: 50px;
  max-height: 300px;
  padding: 20px;
  margin: 5px;
  transition: all 0.50s ease;
}

.Item_Panel:hover {
  transform: scale(1.5, 1.5);
}

strong {
  color: white;
}
</style>
