<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    <div class="Knowledge_holder">
      <knowledge-item v-for="(item,index) in state.items" :name="item.name" :value="item.value" :key="index"></knowledge-item>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'
import KnowledgeItem from "@/components/KnowledgeItem";
import {reactive} from "@vue/reactivity";

export default {
  name: 'Home',
  components: {
    HelloWorld,
    KnowledgeItem
  },
  setup() {
    const state = reactive({
      items: [
        {
          name: "python",
          logo: "",
          value: 95,
          extras: []
        },
        {
          name: "c#",
          logo: "",
          value: 75,
          extras:[]
        },
        {
          name:"JavaScript",
          logo:"",
          value:15,
          extras:[]
        }
      ]
    })
    return {
      state
    }
  }
}
</script>
<style scoped>
.Knowledge_holder{
  display: flex;
  flex-direction: row;
}
</style>
