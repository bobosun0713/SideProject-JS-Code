<template>
  <div class="instance-footer">
    <div class="instance-control">
      <button type="button" class="instance-button">Enter</button>
      <button type="button" class="instance-button">Format</button>
      <button type="button" class="instance-button">Clear</button>
    </div>
    <div class="instance-output"></div>
  </div>
</template>

<script>
export default {
  name: 'InstanceFooter',
}
</script>

<style lang="scss" scoped>
.instance-footer {
  width: 100%;
  background-color: #333333;
  border-top: 1px solid #1a1a1a;
  border-radius: 0 0 8px 8px;
  padding: 16px;

  display: flex;
}

.instance {
  &-control {
    display: flex;
    flex-direction: column;
    flex-basis: 120px;
  }
  &-button {
    background-color: transparent;
    border: 1.5px solid white;
    color: white;
    margin: 0 auto;
    padding: 8px 0;
    width: 80px;
    display: block;
    cursor: pointer;
    &:not(:last-child) {
      margin-bottom: 10px;
    }
  }

  &-output {
    background-color: #2b2b2b;
    border: 1px solid #1a1a1a;
    flex-basis: 100%;
  }
}
</style>
