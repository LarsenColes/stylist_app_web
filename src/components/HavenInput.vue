<template>
  <div>
    <p>
      <slot></slot>
    </p>
    <input
      v-if="setType == 'text'"
      :type="type"
      class="basicInput"
      :value="value"
      @input="$emit('input', $event.target.value)"
    />
    <textarea
      v-else-if="setType == 'textarea'"
      class="basicInput"
      :value="value"
    />
  </div>
</template>
<script>
export default {
  name: 'HavenInput',
  props: ['type', 'value'],
  computed: {
    setType() {
      if (
        this.type == 'text' ||
        this.type == 'date' ||
        this.type == 'password'
      ) {
        return 'text'
      } else if (this.type == 'textarea') {
        return 'textarea'
      } else {
        return ''
      }
    },
  },
}
</script>
<style scoped>
.basicInput {
  @apply border;
  @apply border-black;
  @apply text-lg;
  @apply font-thin;
  @apply appearance-none;
  @apply bg-blue-400;
  @apply outline-none;
  @apply block;
  @apply rounded;
}
</style>
