<template>
  <div>
    <slot></slot>
    <button @click="close">Close Modal</button>
  </div>
</template>

<script>
export default{
  methods:{
    close(){
      this.$emit('close');
    }
  }
}
</script>

<style scoped>

</style>

