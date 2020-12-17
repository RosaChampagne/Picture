<template>
  <div class="tab-wrapper">
    <div class="tab-box">
      <div :class="['tab-item', active == index ? 'active-tab-item' : '']" v-for="(item, index) in tabs" :key="index" @click="changeTab(item, index)">
        {{item.text}}
      </div>
      <div :class="['risk-active-line', active == 0 ? 'risk-active-line-f' : 'risk-active-line-r']"></div>
    </div>
  </div>
</template>

<script>
export default {
  name: '',
  props: {
    current: {
      type: Number | String,
      default: () => {
        return 0
      }
    },
    tabs: {
      type: Array,
      default: () => {
        return []
      }
    }
  },
  data() {
    return {
      active: 0
    }
  },
  created () {
    this.active = this.current
  },
  methods: {
    changeTab (item, index) {
      this.active = index
      this.$emit('changeTab', item, index);
    }
  }
}
</script>

<style scoped>
.tab-wrapper {
  width: 100%;
}
.tab-box {
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: space-between;
  background: #FFFFFF;
}
.tab-box::after {
  transform: scaleY(.5);
  height: 1px;
  content: '';
  border-bottom: 1px solid #ccc;
  display: block;
}

.tab-item {
  width: 100%;
  height: 2rem /* 150/75 */;
  line-height: 2rem /* 150/75 */;
  display: flex;
  align-items: center;
  justify-content: center;
}
.active-tab-item {
  border-bottom: 2px solid #1BB5F1;
  margin-bottom: -1px;
  color: #1BB5F1;
}
.risk-active-line {
  width: 71px;
  height: 2px;
  background: rgba(0, 255, 255, 1);
  position: absolute;
  top: 28px;
  left: 166px;
  transition: all 0.3s ease;
}
.risk-active-line-f {
  transform: translate3d(0, 0, 0);
}
.risk-active-line-r {
  transform: translate3d(120px, 0, 0);
}
</style>