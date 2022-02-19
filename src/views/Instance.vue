<template>
  <div class="instance">
    <InstanceHeader />
    <div class="instance-main">
      <Sidebar />
      <VueCodemirror />
    </div>
    <InstanceFooter />
  </div>
</template>

<script>
import InstanceHeader from '@/components/InstanceHeader.vue'
import Sidebar from '@/components/Sidebar.vue'
import VueCodemirror from '@/components/VueCodemirror.vue'

import InstanceFooter from '@/components/InstanceFooter.vue'

export default {
  name: 'Instance',
  components: {
    InstanceHeader,
    Sidebar,
    VueCodemirror,
    InstanceFooter,
  },
}
</script>

<style lang="scss" scoped>
.instance {
  position: absolute;
  left: 50%;
  transform: translate(-50%, 20%);
  width: 800px;
  height: 400px;

  &-main {
    display: flex;
  }
}
</style>
