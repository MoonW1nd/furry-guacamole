<template>
  <button class="ButtonClose" v-on="$listeners" v-bind="$attrs"></button>
</template>

<script>
/**
 * @class ButtonClose
 * @description кнопка зарытия (красный крест)
 */
export default {
  name: 'ButtonClose',
  inheritAttrs: false
}
</script>

<style lang="scss" scoped>
.ButtonClose {
  position: absolute;
  top: 10px;
  right: 10px;
  bottom: 0;
  width: 40px;
  height: 40px;
  font-size: 30px;
  color: #cc9a9a;
  display: none;
  transition: color 0.2s ease-out;
  margin: 0;
  padding: 0;
  border: 0;
  outline: none;
  background: none;
  vertical-align: baseline;
  font-family: inherit;
  -webkit-appearance: none;
  appearance: none;
  -webkit-font-smoothing: antialiased;
  cursor: pointer;

  &:after {
    content: '×';
  }

  &:focus,
  &:hover {
    color: #e06c75;
  }
}
</style>
