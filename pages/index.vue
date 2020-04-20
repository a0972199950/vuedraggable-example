<template>
  <div>
    <div class="page-container">
      <h1 class="page-container__title">Page</h1>
      <ComponentA />
      <ComponentB />
    </div>

    <ul>
      <li>使用套件：vuedraggable</li>
      <li>OK: 同Component, 同Array托拽</li>
      <li>OK: 同Component, 跨Array托拽</li>
      <li>OK: 跨Component托拽</li>
      <li>OK: 托拽動畫</li>

      <li>Notice: 移動的只有資料，DOM本身不移動，因此style也不會跟著移動(例如當把itemA從listA移動到listB時，itemA會套用listB的style)</li>
    </ul>
  </div>
</template>

<script>
import ComponentA from '../components/ComponentA'
import ComponentB from '../components/ComponentB'

export default {
  components: { ComponentA, ComponentB }
}
</script>

