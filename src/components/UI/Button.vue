
<script setup>
defineProps({
  variant: {
    type: String,
    default: 'blue',
    validator: (value) => ['blue', 'white' ].includes(value)
  },
  size: {
    type: String,
    default: 'small',
    validator: (value) => ['small', 'medium', 'large'].includes(value)
  },
  disabled: Boolean
})

defineEmits(['click'])
</script>

<template>
  <button
    :class="['button', variant, size, { 'disabled': disabled }]"
    :disabled="disabled"
    @click="$emit('click', $event)"
  >
    <slot></slot>
  </button>
</template>

<style scoped>
.button {
  font-family: 'Montserrat-Bold';
  border-radius: 8px;
  cursor: pointer;
  transition: ease 0.3s;
}

/* .button:hover:not(.disabled) {
  background-color: var(--hover-bg);
  border-color: var(--hover-border);
} */

/* .button.disabled {
  opacity: 0.6;
  cursor: not-allowed;
} */

/* Варианты */
.button.blue {
  background-color: var(--bg-blue-color);
  color: var(--text-color);
}

.button.blue:hover {
  background-color: transparent;
  color: var(--text-grey--color);
  border: 1.5px solid var(--button-grey--color);
  transition: ease 0.3s;
}

.button.white {
  background-color: transparent;
  color: var(--text-grey--color);
  border: 1.5px solid var(--button-grey--color);
  color: var(--text-grey--color);
}

.button.white:hover {
  background-color: var(--bg-blue-color);
  color: var(--text-color);
  transition: ease 0.3s;
}

/* Размеры */
.button.small {
  width: 110px;
  height: 41px;
  font-size: 14px;
}

.button.medium {
  width: 150px;
  height: 41px;
  font-size: 14px;
}

/* .button.large {
  padding: 0.75rem 1.5rem;
  font-size: 1.125rem;
} */
</style>
