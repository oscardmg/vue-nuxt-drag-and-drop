<template>
  <div
    :id="id"
    class="card"
    :draggable="draggable"
    @dragstart="dragStart"
    @dragover.stop
  >
    <slot />
  </div>
</template>

<script>
export default {
  name: 'Card',
  props: [
    'id', 'draggable'
  ],
  methods: {
    dragStart (e) {
      const target = e.target;
      console.log(e);
      console.log(target.id);
      e.dataTransfer.setData('card_id', target.id);
      setTimeout(() => {
        target.style.display = 'none';
      }, 0);
    }
  }
};
</script>

<style scoped>

</style>
