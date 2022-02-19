<template>
  <div class="sidebar">
    <div class="sidebar-panels">
      <div class="sidebar-panels__panel" @click="handleClickList">C</div>
    </div>
    <div :class="{ active: isShowList }" class="sidebar-content"></div>
  </div>
</template>

<script>
import { ref } from '@vue/reactivity'
export default {
  name: 'Sidebar',
  setup() {
    const isShowList = ref(false)
    const handleClickList = () => (isShowList.value = !isShowList.value)

    return {
      isShowList,
      handleClickList,
    }
  },
}
</script>

<style lang="scss" scoped>
.sidebar {
  background-color: #333333;
  border-right: 1px solid #1a1a1a;
  display: flex;

  &-panels {
    padding: 6px 12px;

    &__panel {
      cursor: pointer;
    }
  }

  &-content {
    background-color: #1a1a1a;
    width: 0;
    padding: 0;
    transition: all 0.5s;

    &.active {
      width: 150px;
      padding: 8px 16px;
    }
  }
}
</style>
