<template>
  <input @change="$emit('input', checked)" v-model="checked" class="weui-switch" type="checkbox">
</template>

<script>
export default {
  name: "",
  components: {},
  props: {
    value: {
      Boolean,
      default: null
    }
  },
  data() {
    return {
      checked: false
    };
  },
  computed: {},
  watch: {
    value: {
      immediate: true,
      handler(newVal) {
        if (newVal !== null) {
          this.checked = newVal;
        }
      }
    }
  },
  created() {},
  mounted() {},
  methods: {}
};
</script>

<style scoped>
.weui-switch {
  -webkit-appearance: none;
  appearance: none;
}
.weui-switch {
  position: relative;
  width: 52px;
  height: 32px;
  border: 1px solid #DFDFDF;
  outline: 0;
  border-radius: 16px;
  box-sizing: border-box;
  background-color: #DFDFDF;
  -webkit-transition: background-color 0.1s, border 0.1s;
  transition: background-color 0.1s, border 0.1s;
}
.weui-switch:before {
  content: " ";
  position: absolute;
  top: 0;
  left: 0;
  width: 50px;
  height: 30px;
  border-radius: 15px;
  background-color: #FDFDFD;
  -webkit-transition: -webkit-transform 0.35s cubic-bezier(0.45, 1, 0.4, 1);
  transition: -webkit-transform 0.35s cubic-bezier(0.45, 1, 0.4, 1);
  transition: transform 0.35s cubic-bezier(0.45, 1, 0.4, 1);
  transition: transform 0.35s cubic-bezier(0.45, 1, 0.4, 1),
    -webkit-transform 0.35s cubic-bezier(0.45, 1, 0.4, 1);
}
.weui-switch:after {
  content: " ";
  position: absolute;
  top: 0;
  left: 0;
  width: 30px;
  height: 30px;
  border-radius: 15px;
  background-color: #FFFFFF;
  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.4);
  -webkit-transition: -webkit-transform 0.35s cubic-bezier(0.4, 0.4, 0.25, 1.35);
  transition: -webkit-transform 0.35s cubic-bezier(0.4, 0.4, 0.25, 1.35);
  transition: transform 0.35s cubic-bezier(0.4, 0.4, 0.25, 1.35);
  transition: transform 0.35s cubic-bezier(0.4, 0.4, 0.25, 1.35),
    -webkit-transform 0.35s cubic-bezier(0.4, 0.4, 0.25, 1.35);
}
.weui-switch:checked,
.weui-switch-cp__input:checked,
.weui-switch-cp__box {
  border-color: #04BE02;
  background-color: #04BE02;
}
.weui-switch:checked:before {
  -webkit-transform: scale(0);
  transform: scale(0);
}
.weui-switch:checked:after {
  -webkit-transform: translateX(20px);
  transform: translateX(20px);
}
</style>