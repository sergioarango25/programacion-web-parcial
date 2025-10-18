<template>
  <button 
    :class="{ 'nav-btn': true, 'active': isActive }"
    @click="$emit('navigate', sectionName)"
  >
    {{ displayLabel }}
  </button>
</template>

<script>
export default {
  name: 'NavButton',
  props: {
    sectionName: { 
      type: String,
      required: true
    },
    displayLabel: { 
      type: String,
      required: true
    },
    isActive: {
      type: Boolean,
      default: false
    }
  },
  emits: ['navigate']
}
</script>