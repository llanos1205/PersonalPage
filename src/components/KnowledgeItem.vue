<template>
  <div class="Item_Panel">
    <div>
      <img src="src/assets/python.png" alt="python logo">
    </div>

    <div>
      <strong>{{ state.name }}</strong>
    </div>
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
      value: 0,
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
  border: 1px solid dimgray;
  border-radius: 15px;
  background-color: #2c3e50;
  max-width: 200px;
  max-height: 300px;
  padding: 100px;
  margin: 5px;
  transition: all 0.50s ease;
}

.Item_Panel:hover {
  transform: scale(1.05, 1.05);
}

strong {
  color: white;
}
</style>
