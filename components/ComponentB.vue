<template>
  <div style="border: 1px black solid; padding: 10px;">
    <h3>ComponentB</h3>
    <draggable :list="fruits" group="together" @start="drag=true" @end="drag=false" style="border: 1px black dashed; padding: 10px;">
      <transition-group name="scale" tag="p">
        <div
          v-for="fruit in fruits" 
          :key="fruit.name" 
          class="person-card-pink"
        >
          {{ fruit.name }}
        </div>
      </transition-group>
    </draggable>
  </div>
</template>

<script>
import draggable from 'vuedraggable'

export default {
  components: {
    draggable
  },

  data() {
    return {
      fruits: [
        { name: 'Apple', color: 'red' },
        { name: 'Banana', color: 'yellow' },
        { name: 'Melon', color: 'green' }
      ],

      drag: false
    }
  }
}
</script>
