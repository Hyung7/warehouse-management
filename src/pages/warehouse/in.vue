<template>
  <div>
    <list-component :propsInfo="propsInfo"></list-component>
  </div>
</template>

<script>
import InApi from '../../api/warehouse/in.api.js'
import ListComponent from '../../components/list-component'

export default {
  name: 'in',
  components: {
    ListComponent
  },
  data () {
    return {
      propsInfo: {
        attr: '食品名称',
        page: 'in',
        title: '入库信息编辑',
        api: InApi,
        column: [
          { prop: 'foodName', label: '食品名称', width: '100px' },
          { prop: 'quantity', label: '数量', width: '70px' },
          { prop: 'brand', label: '厂家', width: '100px' },
          { prop: 'operatorName', label: '操作人', width: '70px' },
          { prop: 'time', label: '操作时间', width: '160px' }
        ]
      }
    }
  },
  mounted () { },
  methods: {}
};
</script>

<style scoped>
div {
  height: 100%;
}
</style>