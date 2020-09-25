<template>
  <div class="home">


      <div>

      </div>
      <div class="AboutMe_Holder">
        <strong>About Me</strong>
        <label>somebody who understands the Software Development Lifecycle and has the outright
          understanding of various automation tools for developing digital pipelines (CI/ CD pipelines).</label>
      </div>
      <div class="Knowledge_holder">
        <knowledge-item v-for="(item,index) in state.items" :name="item.name" :value="item.value"
                        :key="index"></knowledge-item>
      </div>

  </div>
</template>

<script>
// @ is an alias to /src

import KnowledgeItem from "@/components/KnowledgeItem";
import {reactive} from "@vue/reactivity";

export default {
  name: 'Home',
  components: {

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
          extras: []
        },
        {
          name: "JavaScript",
          logo: "",
          value: 15,
          extras: []
        },
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
          extras: []
        },
        {
          name: "JavaScript",
          logo: "",
          value: 15,
          extras: []
        },
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
          extras: []
        },
        {
          name: "JavaScript",
          logo: "",
          value: 15,
          extras: []
        },
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
          extras: []
        },
        {
          name: "JavaScript",
          logo: "",
          value: 15,
          extras: []
        },
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
          extras: []
        },
        {
          name: "JavaScript",
          logo: "",
          value: 15,
          extras: []
        },

      ]
    })
    return {
      state
    }
  }
}
</script>
<style scoped>
.AboutMe_Holder {
  display: flex;
  flex-direction: column;
  max-width: 500px;
  horiz-align: center;
  margin: 0;
}

.Knowledge_holder {
  display: flex;
  flex-direction: row;
}
</style>
