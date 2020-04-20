<template>
  <div style="border: 1px black solid; padding: 10px;">
    <h3>ComponentA</h3>
    <draggable :list="people" group="together" @start="drag=true" @end="drag=false" style="border: 1px black dashed; padding: 10px;">
      <transition-group name="slide" tag="p">
        <div
          v-for="person in people"
          :key="person.name"
          class="person-card-aqua"
        >
          {{ person.name }}
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
      people: [
        { name: 'John', age: 28 },
        { name: 'Tina', age: 30 },
        { name: 'Estela', age: 26 }
      ],

      drag: false
    }
  }
}
</script>
