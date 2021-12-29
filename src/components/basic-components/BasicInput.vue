<template>
  <div class="container">
    <form>
      <label for="basic-input" class="label">Add item to the list:</label>
      <input
        name="basic-input"
        id="basic-input"
        class="input"
        v-bind:placeholder="initValue"
        v-model="newItem"
      />
      <button
        type="submit"
        class="button"
        v-on:click.prevent="sendItem(newItem)"
      >
        <strong>Add</strong>
      </button>
    </form>
  </div>
</template>

<script>
export default {
  name: "BasicInput",

  props: {
    initValue: { type: String },
  },

  data() {
    return {
      newItem: "",
    };
  },

  methods: {
    sendItem(item) {
      this.$emit("basic-input-content", item);
      this.newItem = "";
    },
  },
};
</script>

<style scoped>
.container {
  display: inline-block;
  margin-left: 20px;
}

.label {
  display: block;
  font-family: Arial, Helvetica, sans-serif;
  text-align: right;
  margin: 0 4px 5px 0;
}

.input {
  width: 262px;
  height: 30px;
  padding-left: 8px;
  border: solid 2px #505050;
  border-radius: 8px;
}

.button {
  font-family: Arial, Helvetica, sans-serif;
  font-size: 17px;
  background-color: #00ab46;
  color: #fff;
  border: solid 2px #000;
  border-radius: 8px;
  width: 45px;
  height: 35px;
  margin-left: 2px;
}
</style>
