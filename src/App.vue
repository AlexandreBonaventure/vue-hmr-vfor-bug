<template>
  <ItemComponent
    v-for="(item, i) in items"
    :item="item"
    :key="item.id"
  />
</template>

<script>
import ItemComponent from './components/ItemComponent.vue'
import { ref } from 'vue'

export default {
  name: 'App',
  components: {
    ItemComponent
  },
  setup() {
    const items = ref(null);
    setTimeout(() => {
      items.value = [{ id: 0 }, { id: 1 }] 
    }, 100)
    setTimeout(() => {
      items.value = [{ id: 0 }, { id: 1 }]
    }, 200)
    return {
      items
    }
  }
}
</script>
