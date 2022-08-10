 <template>
  <button @click="myOnClick()" class="btn" :style="{ backgroundColor: color }">
    {{ text }}
  </button>
</template>

<script>
export default {
  name: "Button",
  props: {
    text: {
      type: String,
      default: "title-prop not passed to Button",
    },
    color: {
      type: String,
      default: "color-prop not passed to Button",
    },
  },
  methods: {
    myOnClick() {
      this.$emit('btn-click')
    }
  }
};
</script>