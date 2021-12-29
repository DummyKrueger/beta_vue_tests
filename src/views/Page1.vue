<template>
  <div>
    <div>
      <Bar />
      <Clock :time="time" @new-time="updateTime" />
      <RedLine :time="time" />
    </div>
    <div>
      <InputWall @user-input="writeOutput" />
      <OutputWall :text="outputText" />
    </div>
    <div>
      <BasicInput
        v-bind:initValue="pHolder"
        v-on:basic-input-content="items.push($event)"
      />
      <List />
    </div>
  </div>
</template>

<script>
import Bar from "../components/Bar.vue";
import Clock from "../components/Clock.vue";
import RedLine from "../components/RedLine.vue";
import InputWall from "../components/InputWall.vue";
import OutputWall from "../components/OutputWall.vue";
import BasicInput from "../components/basic-components/BasicInput.vue";
import List from "../components/basic-components/List.vue";

export default {
  name: "Page1",

  components: {
    Bar,
    Clock,
    RedLine,
    InputWall,
    OutputWall,
    BasicInput,
    List,
  },

  data() {
    return {
      time: "waiting...",
      outputText: "",
      pHolder: "es. Apple",
      items: [],
    };
  },

  methods: {
    updateTime(newTime) {
      this.time = newTime;
    },

    writeOutput(input) {
      this.outputText = input;
    },
  },
};
</script>
