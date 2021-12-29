<template>
  <div>
    <li>
      <ListItem
        v-for="(item, index) in items"
        v-bind:key="index"
        :item="item"
      />
    </li>
  </div>
</template>

<script>
import ListItem from "./ListItem.vue";

export default {
  name: "List",

  components: {
    ListItem,
  },

  props: {
    items: { type: Array },
  },
};
</script>

<style scoped></style>
