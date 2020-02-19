<template>
  <div class="dashboard-container">
    <div class="dashboard-text">我的笔记页面</div>
  </div>
</template>

<script>
import { mapGetters } from 'vuex'

export default {
  name: 'Note',
  computed: {
    ...mapGetters([
      'name'
    ])
  }
}
</script>

<style lang="scss" scoped>
.dashboard {
  &-container {
    margin: 30px;
  }
  &-text {
    font-size: 30px;
    line-height: 46px;
  }
}
</style>
