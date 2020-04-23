<template>
    <button
      :class="[
          'ui-button',
          `ui-button_variant-${variant}`,
          {'ui-button_flat': flat}
      ]"
      @click="onButtonClick"
    >
        <slot/>
    </button>
</template>

<script>
const BUTTON_VARIANTS = [
    'primary',
    'danger',
    'minor'
]
export default {
  name: "ui-button",
  props: {
    variant: {
        type: String,
        default: 'primary',
        validator: (value) => BUTTON_VARIANTS.includes(value)
    },
    flat: {
      type: Boolean,
      default: false
    }
  },
  methods: {
    onButtonClick () {
      this.$emit('click')
    }
  }
}
</script>

<style>
  .ui-button {
      padding: 14px;
      display: inline-block;
      outline: none;
      border: none;
      border-radius: 5px;
      transition: background-color var(--transition-bg-duration) ease;
  }
  .ui-button:hover:not(:disabled) {
      cursor: pointer;
  }

  .ui-button_variant-primary {
      background-color: var(--button-primary-bg-color);
      color: var(--button-primary-font-color);
  }
  .ui-button_variant-primary:hover {
      background-color: var(--button-primary-bg-color_hover);
  }
  .ui-button_variant-primary:active {
      background-color: var(--button-primary-bg-color_active);
  }

  .ui-button_variant-danger {
      background-color: var(--button-danger-bg-color);
      color: var(--button-danger-font-color);
  }
  .ui-button_variant-danger:hover {
      background-color: var(--button-danger-bg-color_hover);
  }
  .ui-button_variant-danger:active {
      background-color: var(--button-danger-bg-color_active);
  }

  .ui-button_variant-minor {
      background-color: var(--button-minor-bg-color);
      color: var(--button-minor-font-color);
  }
  .ui-button_variant-minor:hover {
      background-color: var(--button-minor-bg-color_hover);
  }
  .ui-button_variant-minor:active {
      background-color: var(--button-minor-bg-color_active);
  }

  .ui-button_flat {
      background-color: var(--button-flat-bg-color);
      border: 1px solid;
      transition: color var(--transition-bg-duration) ease, border var(--transition-bg-duration) ease;
  }
  .ui-button_flat:hover {
      background-color: var(--button-flat-bg-color);
  }
  .ui-button_flat:active {
      background-color: var(--button-flat-bg-color);
  }
  .ui-button_variant-primary.ui-button_flat {
      border-color: var(--button-primary-bg-color);
      color: var(--button-primary-bg-color);
  }
  .ui-button_variant-primary.ui-button_flat:hover {
      border-color: var(--button-primary-bg-color_hover);
      color: var(--button-primary-bg-color_hover);
  }
  .ui-button_variant-primary.ui-button_flat:active {
      border-color: var(--button-primary-bg-color_active);
      color: var(--button-primary-bg-color_active);
  }

  .ui-button_variant-danger.ui-button_flat {
      border-color: var(--button-danger-bg-color);
      color: var(--button-danger-bg-color);
  }
  .ui-button_variant-danger.ui-button_flat:hover {
      border-color: var(--button-danger-bg-color_hover);
      color: var(--button-danger-bg-color_hover);
  }
  .ui-button_variant-danger.ui-button_flat:active {
      border-color: var(--button-danger-bg-color_active);
      color: var(--button-danger-bg-color_active);
  }

  .ui-button_variant-minor.ui-button_flat {
      border-color: var(--button-minor-bg-color);
      color: var(--button-minor-font-color);
  }
  .ui-button_variant-minor.ui-button_flat:hover {
      border-color: var(--button-minor-bg-color_hover);
      color: var(--button-minor-bg-color_hover);
  }
  .ui-button_variant-minor.ui-button_flat:active {
      border-color: var(--button-minor-bg-color_active);
      color: var(--button-minor-bg-color_active);
  }
</style>
