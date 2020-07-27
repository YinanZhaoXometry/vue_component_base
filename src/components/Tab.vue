<template>
  <div class="tab-wrapper">
    <div
      :class="['tab-item',activeTabItem === tabItem ? 'active':'']"
      v-for="(tabItem, index) in ['All','Course','Status','Item','Teacher']"
      @click="switchTab($event, tabItem, index)"
      :key="tabItem"
    >{{ tabItem }}</div>
    <div
      class="underline"
      :style="{ transform: `translateX(${underlineTranslateX}px) translateX(-50%)` }"
    ></div>
  </div>
</template>

<script>
export default {
  name: 'tab',
  components: {},
  props: {},
  data() {
    return {
      // underlineTranslateX: window.screen.availWidth / 10,
      underlineTranslateX: 60 / 6,
      activeTabItem: 'All',
      tabWidth: 0,
    }
  },
  computed: {},
  created() {},
  mounted() {
    this.tabWidth = 60
    this.underlineTranslateX = this.tabWidth / 2
  },
  methods: {
    switchTab(e, tabItem, index) {
      this.underlineTranslateX = this.tabWidth * (index + 0.5)
      if (this.activeTabItem === tabItem) {
        return false
      }
      this.activeTabItem = tabItem
    },
  },
}
</script>

<style scoped>
.tab-wrapper {
  background: #fff;
  top: 0;
  min-width: 100%;
  padding: 20px 0 10px;
  box-sizing: border-box;
  position: relative;
  overflow: auto;
  white-space: nowrap;
  text-align: left;
}
.tab-wrapper .tab-item {
  display: inline-block;
  width: 60px;
  border-bottom: 2px solid transparent;
  padding-bottom: 4px;
  color: #999;
  font-size: 17px;
  font-weight: 400;
  text-align: center;
  -webkit-tap-highlight-color: rgba(0, 0, 0, 0);
}
.tab-wrapper .active {
  color: color_primary;
  font-weight: 550;
}
.tab-wrapper .underline {
  height: 2px;
  width: 30px;
  background: #4fc08d;
  position: absolute;
  bottom: 10px;
  left: 0;
  transition: transform 0.3s;
}
</style>