<template>
  <div>
    <lian :lists="lianData" :curId="lianCurId"></lian>
  </div>
</template>

<script>
import Lian from './component/lian.vue'

let arrData = [
  {id: 1, parent_id: 0, name: '一级'},
  {id: 2, parent_id: 0, name: '一级2'},
  {id: 12, parent_id: 1, name: '二级1'},
  {id: 13, parent_id: 1, name: '二级2'},
  {id: 122, parent_id: 12, name: '三级1'},
  {id: 133, parent_id: 13, name: '三级2'},
  {id: 1335, parent_id: 133, name: '四级1'},
  {id: 1336, parent_id: 133, name: '四级2'}
]

export default {
  name: 'app',
  components:{
    Lian
  },
  data () {
    return {
      lianData: arrData,
      lianCurId: 1335
    }
  },
}
</script>

