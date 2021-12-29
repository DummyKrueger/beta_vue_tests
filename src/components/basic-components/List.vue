<template>
  <div>
    <li>
      <ListItem />
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
};
</script>

<style scoped></style>
