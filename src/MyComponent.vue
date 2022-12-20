<template>
  <div>
    <div class="header">
      <slot name="header"></slot>
    </div>

    <div>
      <slot v-for="item in items"> {{ item.id }} {{ item.name }}<br /> </slot>
    </div>
  </div>
</template>

<script>
export default {
  name: "MyComponent",
  props: {
    items: {
      type: Array,
      default: () => [],
    },
  },
};
</script>

