<template>
  <div class="modal">
    <div class="content">
      <slot></slot>
      <button @click="$emit('close')">Dismiss</button>
    </div>
  </div>
</template>
<script>
export default {
  emits: [ "close" ]
}
</script>
<style scoped>
  ::v-slotted(p) {
    font-style: italic;
  }
  .modal {
    width: 100%;
    height: 100%;
    position: fixed;
    top: 0;
    left: 0;
    background: rgba(0,0,0,0.8);
  }
  .content {
    background: #fff;
    left: 50%;
    padding: 40px;
    position: absolute;
    top: 50%;
    transform: translate(-50%,-50%);
    width: 60%;
  }
</style>