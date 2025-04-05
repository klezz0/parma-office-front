<template>
  <div v-if="isComplex" class="btn">
    <img :src="icon" :alt="label"/>
    <span v-html="formattedLabel"/>
    <div>
      <img :src="icon" :alt="label"/>
      {{ label }}
    </div>
  </div>
</template>
<script>
export default {
  props: ['icon', 'label', 'isComplex'],
  computed: {
    formattedLabel() {
      return this.label.replace('\n', '<br>');
    }
  }
}
</script>

<style scoped>

</style>