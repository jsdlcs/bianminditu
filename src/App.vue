<template>
  <div id="app">
    <!-- <h2>vue+webpack+axios+百度地图实现父子组件的通信</h2>
    <h3>示例一：跳跃的图标(没有使用axios)</h3> -->
    <HeaderBtn></HeaderBtn>
    <MapView :m="giveData"></MapView>
  </div>
</template>

<script>
import MapView from './components/Map.vue'
import HeaderBtn from './components/HeaderBtn.vue'
export default {
  data () {
    return {
      giveData:{  //vue2.0将数据定位对象的形式，实现父子组件的通信
        height:1000,
        longitude:112.20518,
        latitude:31.022003
      },
    }
  },
  components:{
    MapView,
    HeaderBtn,
  }
}
</script>

<style>

</style>
