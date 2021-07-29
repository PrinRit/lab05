<template>
  <p>{{ event.time }} on {{ event.date }} @ {{ event.location }}</p>
  <p>{{ event.description }}</p>
  <div id="flash_edit" v-if="GStore.flash_edit">
    {{GStore.flash_edit}}
  </div>
</template>

<script>
export default {
  props: ['event'],
  inject: ['GStore']
}
</script>

<style>
@keyframes yellowfade{
  from {
    background: yellow;
  }
  to {
    background: transparent;
  }
}

#flash_edit {
  animation-name: yellowfade;
  animation-duration: 3s;
}
</style>
