<template>
  <input
      type="text"
      :id="id"
      :placeholder="placeholder"
      :value="modelValue"
      @input="$emit('update:modelValue', $event.target.value)"
      class="shadow-xs border h-9 text-sm rounded-lg block w-full p-2.5 bg-gray-850 border-gray-700 placeholder-gray-400 text-white focus:ring-2 focus:ring-gray-600 focus:ring-offset-2 focus:ring-offset-gray-600 focus:outline-hidden shadow-xs-light"
      :class="{ 'border-red-500': error }"
      :name="name"
  />
</template>
<script>
export default {
  name: "InputText",
  props: {
    id: {
      type: String,
      required: true,
    },
    label: {
      type: String,
      default: "",
    },
    type: {
      type: String,
      default: "text", // Jenis input (text, email, password, dll.)
    },
    placeholder: {
      type: String,
      default: "",
    },
    name: {
      type: String,
      default: "",
    },
    modelValue: {
      type: [String, Number],
      default: "",
    },
    error: {
      type: String,
      default: "",
    },
  },
  emits: ["update:modelValue"],
};
</script>
