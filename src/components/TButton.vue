<template>
  <button :class="classes">
    <slot></slot>
  </button>
</template>
<script>
export default {
  name: "TButton",
  props: {
    block: {
      type: Boolean,
      default: () => false,
    },
    disabled: {
      type: Boolean,
      default: () => false,
    },
    size: {
      type: String,
      default: () => "md",
    },
    variant: {
      type: String,
      default: () => "secondary",
      //primary, secondary, dark, danger, warning
    },
    type: {
      type: String,
      default: () => "button",
    },
    tag: {
      type: String,
      default: () => "button",
    },
    pill: {
      type: Boolean,
      default: () => false,
    },
    squared: {
      type: Boolean,
      default: () => false,
    },
    pressed: {
      type: Boolean,
      default: () => null,
    },
    href: {
      type: String,
    },
    rel: {
      type: String,
      default: () => null,
    },
    classes: {
      type: Array,
      default: () => [
        "active:bg-pink",
        "font-bold",
        "uppercase",
        "text-xs",
        "px-4",
        "py-2",
        "rounded",
        "shadow",
        "hover:shadow-md ",
        "outline-none",
        "focus:outline-none",
      ],
    },
  },
  mounted() {
    if (this.variant === "secondary") {
      this.classes.push("bg-grey");
    } else if (this.variant === "primary") {
      this.classes.push("bg-blue");
      this.classes.push("text-white");
    }
  },
};
</script>