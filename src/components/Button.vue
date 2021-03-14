<template>
  <button>
    {{ label }}
  </button>
</template>

<script>
export default {
  name: 'Button',
  props: {
    label: String,
  },
};
</script>

<style lang="less" scoped>
button {
  display: flex;
  place-content: center;
  align-self: center;
  padding: 5px 55px;
  padding-bottom: 8px;
  border-radius: 30px;
  color: white;
  font-weight: bold;
  background-color: #ff9b23;
  border: none;
  font-size: 22px;
}
</style>
