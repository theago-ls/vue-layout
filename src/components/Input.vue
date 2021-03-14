<template>
  <div class="inputContainer">
    <label v-bind:for="id">{{ label }}</label>
    <input v-bind:id="id" />
  </div>
</template>

<script>
export default {
  name: 'Input',
  props: {
    id: String,
    label: String,
  },
};
</script>

<style lang="less" scoped>
.inputContainer {
  display: flex;
  flex-direction: column;
}

label {
  color: white;
  margin-top: 4px;
}
input {
  height: 30px;
  background: rgba(255,255,255,0.4);
  border: none;
  color: white;
}

input:focus {
    border: 1px solid white;
}
</style>
