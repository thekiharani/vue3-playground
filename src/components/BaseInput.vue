<template>
    <input
      type="text"
      v-bind="$attrs"
      class="rounded-md w-full"
      :value="modelValue"
      @input="$emit('update:modelValue', $event.target.value)"
      :placeholder="label"
    />
</template>

<script>
export default {
  name: "BaseInput",
  props: {
    label: {
      type: String,
      default: "",
    },
    modelValue: {
      type: [String, Number],
      default: "",
    },
  },
};
</script>

<style>
</style>