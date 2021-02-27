<template>
  <button
    class="square"
    :class="[value, { winner: winner }]"
    :disabled="disabled"
    @click="click"
  >
    {{ value }}
  </button>
</template>

<script lang="ts">
import { defineComponent } from "vue"

export default defineComponent({
  name: 'Square',
  props: {
    value: String,
    winner: Boolean,
    disabled: Boolean
  },
  methods: {
    click () {
      this.$emit('squareclick')
    }
  }
})
</script>

<style scoped>
.square {
  background: #03045E;
  background-blend-mode: exclusion;
  background-image: var(--noise-pattern);
  border: 1px solid #CAF0F8;
  font-size: 15vmin;
  font-weight: bold;
  line-height: 34px;
  padding: 0;
  text-align: center;
  box-shadow: inset 0 0 0 #CAF0F8;
  text-shadow: -1px -1px 1px #000b, -1px 1px 1px #000b, 1px -1px 1px #000b, 1px 1px 1px #000b;
  transition: all .25s ease;
  outline: none;
}
.square.winner {
  background: #90E0EF;
}
.square:not([disabled]):empty:hover,
.square:not([disabled]):empty:focus {
  box-shadow: inset 0 2px 25px #0006;
  cursor: pointer;
}
.square:not([disabled]):empty:active {
  box-shadow: inset 0 2px 50px #0008;
}
.square.X {
  color: #1FBBD6;
}
.square.O {
  color: #90E0EF;
}
</style>
