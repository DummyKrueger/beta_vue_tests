<template>
  <ul>
    {{
      item
    }}
  </ul>
</template>

<script>
export default {
  name: "ListItem",

  props: {
    item: { type: String },
  },
};
</script>

<style scoped></style>
