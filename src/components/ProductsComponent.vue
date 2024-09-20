<template>
  <div>
    <item-component v-for="item in $store.state.products"
    v-bind:key="item.id"
    v-bind:item="item"
    ></item-component>
  </div>
</template>

<script>
import ItemComponent from './ItemComponent.vue';
export default {
  components: {ItemComponent}
}
</script>

<style>

</style>