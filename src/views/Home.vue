<template>
  <div class="home">
    <h1>Inventory</h1>
    <InventoryTable />
  </div>
</template>

<script>
import InventoryTable from '../components/InventoryTable'

export default {
  name: 'Home',
  components: {
    InventoryTable
  }
}
</script>
