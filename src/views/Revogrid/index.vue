<template>
  <div class="revogrid">
    <v-grid style="height: 800px" theme="compact" :source="rows" :columns="columns" />
  </div>
</template>

<script>
// https://revolist.github.io/revogrid/
import VGrid from '@revolist/vue-datagrid'
export default {
  name: 'Revogrid',
  components: {
    VGrid,
  },
  data() {
    return {
      columns: [{ prop: 'name',name: "First", }, { prop: 'details',name: "Second", }],
      rows: [
        {
          name: '1',
          details: 'Item 1',
        },
        {
          name: '2',
          details: 'Item 2',
        },
        {
          name: '3',
          details: 'Item 3',
        },
      ],
    }
  },
}
</script>

<style scoped>
.revogrid {
  min-height: 800px;
  width: 100%;
}

</style>
