<template>
  <div>
    <vs-icon :icon="iconClass" v-if='iconClass.length > 0'></vs-icon>
    <span class='item-text'>{{text}}</span>
  </div>
</template>
<script>
export default {
  title: 'TopNavItem',
  data: () => ({
    iconClass: '',
    text: ''
  })
}
</script>
<style lang="sass"></style>
