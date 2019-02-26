<template>
  <div class="d">
      

    <ul class="nav nav-tabs">
                        <li class="nav-item">
                            <a @click="tabIndex=0" :class="['nav-link',tabIndex==0&&'active']" href="javascript:;">
                                K线
                            </a>
                        </li>
                       
                        <li class="nav-item">
                            <a @click="tabIndex=2" :class="['nav-link',tabIndex==2&&'active']" href="javascript:;">
                                工具
                            </a>
                        </li>

                    
                    </ul>

    <Ekline v-if="tabIndex==0" />
    <Etools v-if="tabIndex==2"/>
  </div>
</template>

<script>

import Ekline from "@/components/Exchange_KLine";
import Etools from "@/components/Exchange_Tools";

export default {
  name: "Exchange_Content",
  components:{
      Ekline,Etools
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
  background-color: white;
}
</style>


