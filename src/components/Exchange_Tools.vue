<template>
  <div class="d">
    <ul class="nav nav-tabs">
      <li class="nav-item">
        <a
          @click="tabIndex = 0"
          :class="['nav-link', tabIndex == 0 && 'active']"
          href="javascript:;"
        >
          出货
        </a>
      </li>

      <li class="nav-item">
        <a
          @click="tabIndex = 1"
          :class="['nav-link', tabIndex == 1 && 'active']"
          href="javascript:;"
        >
          吸货
        </a>
      </li>
    </ul>

    <Tchuhuo v-if="tabIndex==0"/>
    <Txihuo v-if="tabIndex==1"/>


  

  </div>
</template>

<script>

import Tchuhuo from "@/components/Tool_chuhuo";
import Txihuo from "@/components/Tool_xihuo";
export default {
  name: "Exchange_Tools",
  components:{
    Tchuhuo,Txihuo
  },
  data(){
      return {
          tabIndex:0
      }
  }
};
</script>

<style lang="less" scoped>
.d {
  height: 100%;

}
</style>


