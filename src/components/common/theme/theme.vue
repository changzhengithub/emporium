<template>
  <!-- s 公共头部  -->
  <header class="theme">
    <div class="theme-title">{{theme.title}}</div>
    <div id="back-btn" class="theme-left" @click="goback">
      <i class="iconfont icon-arrow-left"></i>
    </div>
    <!-- <div class="theme-right" v-show="theme.themeRight">
      <i class="iconfont icon-fenxiang"></i>
    </div> -->
  </header>
  <!-- e 公共头部 -->
</template>

<script>
export default {
  name: 'Theme',
  props: ['theme'],
  methods: {
    goback () {
      if (this.theme.goal) {
        this.$router.push({
          name: this.theme.goal,
          params: this.theme.params
        })
      } else {
        this.$router.back(-1)
      }
    }
  }
}
</script>

<style lang="sass" scoped>
@import "./theme.scss";
</style>
